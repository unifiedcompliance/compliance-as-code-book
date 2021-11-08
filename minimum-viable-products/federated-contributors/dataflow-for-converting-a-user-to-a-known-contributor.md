# Dataflow for converting a User to a known Contributor



The Compliance as Code federated system uses a couple of API calls to convert an Account’s User to a known Person so that the person can contribute content.

![Abbreviated Flow](https://www.complianceascode.net/wp-content/uploads/2021/11/NoCode-User-or-Organization-to-Contributor.png)

Let’s walk through the process.

The process to convert a user to a known Person begins within the User’s Profile when the user clicks the **Contributor** checkbox (1) in the screen below:

![Contributor button](https://www.complianceascode.net/wp-content/uploads/2021/11/User-Profile-Convert-to-Contributor-1.png)

Before we convert the User to a Person, the user must first accept what we call the _TLP_ (Terms of Service, License, and Privacy Policy).

## Accepting the Terms of Service, License, and Privacy Policy

It all begins with walking the user through the **Terms of Service**, **License Agreement**, and **Privacy Policy**.

![No-Code TLP process](https://www.complianceascode.net/wp-content/uploads/2021/11/NoCode-TLP-Acknowledgement2.png)

### Terms of Service

The No-Code application must make the call to get the current Terms of Service.

> **API Call**: GET /ToS;

To which the gateway will return those terms.

> **API Return**: ToS;

Once the data is returned, the application must notify the user that he or she _must_ accept the Terms of Service prior to moving forward.

> **Prompt User**: "You must accept the terms of service.”

A window is then displayed with the current Terms of Service in it, as shown below.

![TLP Acknowledgement](https://www.complianceascode.net/wp-content/uploads/2021/11/TLP-Window.png)

1. If the text is longer than fits within the window, the window must display a scrolling field.
2. Both the **Decline** and **Accept** buttons are initially disabled _if_ the scroll bar is activated. _Scrolling to the end_ of the text is what activates both buttons.

_If_ the user accepts the Terms of Service, they can continue.

_If_ the user _does not_ accept the Terms of Service, the application must display a prompt that the process will be canceled.

> **Prompt User**: "You cannot continue without acknowledging the Terms of Service."

### Privacy Policy

The No-Code application makes an API call to get the Privacy Policy.

> **API Call**: GET /PrivacyPolicy;

To which the gateway will return the current version of the Privacy Policy.

> **API Return**: PrivacyPolicy;

Once the data is returned, the application must notify the user that he or she _must_ accept the Privacy Policy prior to moving forward.

> **Prompt User**: "You must accept the Privacy Policy.”

A window is then displayed with the current Privacy Policy in it that acts the same as the one for the Terms of Service above.

_If_ the user accepts the Privacy Policy, they can continue.

_If_ the user _does not_ accept the Privacy Policy, the application must display a prompt that the process will be canceled.

> **Prompt User**: "You cannot continue without acknowledging the Privacy Policy.”

### License Agreement

The No-Code application makes an API call to get the License Agreement.

> **API Call**: GET /License;

To which the gateway will return the current version of the License Agreement.

> **API Return**: License;

Once the data is returned, the application must notify the user that he or she _must_ accept the License Agreement prior to moving forward.

> **Prompt User**: "You must accept the License Agreement.”

A window is then displayed with the current License Agreement in it that acts the same as the one for the Terms of Service above.

_If_ the user accepts the License Agreement, they can continue.

_If_ the user _does not_ accept the License Agreement, the application must display a prompt that the process will be canceled.

> **Prompt User**: "You cannot continue without acknowledging the License Agreement.”

## Begin Validate Person

The dataflow diagram for this process is shown below:

![Person Validation flow](https://www.complianceascode.net/wp-content/uploads/2021/11/NoCode-Person-Validation-1.png)

Once the user has accepted the three agreements, the Person Validation process begins.

### Initial API Call

This kicks off with the API call to find out what we know about this user based on his or her email address.

> **API Call**: GET /PersonByEmail;

#### On the server side

On the server side, one of three things is going to happen. Either

1. the request is going to be queued (meaning it is taking a bit of time to gather the information),
2. it is going to return whatever it found, or
3. it won’t find anything about the user.

**Request queued**

> **API Response**: Error = Request Queued;

If the request is queued you’ll need to present the user with some form of dialog, informing them that they’ll need to retry the request again _at least after 5 minutes_.

> **Prompt**: Your request is queued. Please wait 5 min and click Validate Public Person again."

#### **Invalid response**

An invalid response can be returned if no information was found for any person using that email address.

> **API Response**: Error = Unknown person

There are a lot of reasons that the API might not find a user, too many to go into here. At this point what is required by the user is that the user provides _the minimum_ information the industry has agreed on to disambiguate _this_ person from _that_ person. For now, that means that the user has to add at least two social addresses (LinkedIn, Twitter, Facebook) and an office address.

> **Prompt User**: "There is not enough social information to disambiguate you. You must submit two Social Addresses and an Office Address."

Once the user has contributed at least that much information, they can continue.

**Valid response**

If a person has been found that matches the email address given, the API will return a valid response with _some_ or _all_ of the data fields specified in the [Person schema](https://grcschema.org/Person).

> **API Response**: Person Information

At that point, the No-Code application needs to write the contents of the response into the local system, **and** it also needs to set the _validated_ field’s boolean value to true.

> **Write**: "validated" boolean value of "true" in User Profile;

_If_ the No-Code application is storing User information in the same structure as Person information, the information returned from the API can be stored in that table. If not, the User’s information must be linked to a new record in the Person table.

> **Write**: available data to user/person table, updating User Profile visually;

### Continuing with the validation process

After that’s been done, the user will have to still validate all of the data that’s been returned by the API. **The user should be given some form of visual notification that each profile segment has to be validated individually prior to submission.**

> **Prompt User**: "Validate each section of your profile"

### Trapping for section saves

Each conversion from User to Person requires several sections of data (basic info, addresses, etc.). Before the user can submit the conversion _each and every_ one of these sections has to be reviewed by the user. Therefore, the No-Code application will need to trap for the user saving each of those.

### Submitting the Person

Once each of the sections has been checked the No-Code application needs to submit the data via the API call when the user clicks the **Submit Public Person** button via whatever dialog is to be displayed.

> **Prompt User**: Select Submit Public Person

When the button is clicked, the No-Code application sends off the following API call:

> **API Call**: Patch /Person

### Receiving the data and checking it

On the server side, we will be writing that person’s data to our table and will then add some CoreMetaData you’ll need to write back into the No-Code system; the Person’s ID, date created & modified, etc.

> **API Response**: Person Data

After you submit the Patch for the Person, the system will return the same information with the additional CoreMetadata. This will need to be written into that record’s Person table.

> **Write**: Person Information
