# Dataflow for converting a User to a known Contributor

The Compliance as Code federated system uses a couple of API calls to convert an Account’s User to a known Person so that the person can contribute content. The dataflow diagram for this process is shown below:

![Person Validation flow](https://www.complianceascode.net/wp-content/uploads/2021/11/NoCode-Person-Validation.png)

Let’s walk through the process.

### Begin Validate Person

The process to convert a user to a known Person begins within the User’s Profile when the user clicks the **Contributor** checkbox (1) in the screen below:

![Contributor button](https://www.complianceascode.net/wp-content/uploads/2021/11/User-Profile-Convert-to-Contributor-1.png)

### Choosing to Convert

Clicking the **Contributor** checkbox should bring up a dialog that asks the end user to convert to a known person.

> Action: Select Validate Public Person

### Initial API Call

This, in turn, kicks off the API call to find out what we know about this user based on his or her email address.

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

**Valid response**

If a person has been found that matches the email address given, the API will return a valid response with the _some_ or _all_ of the data fields specified in the [Person schema](https://grcschema.org/Person).

> **API Response**: Person Information

At that point, the No-Code application needs to write the contents of the response into the local system, **and** it also needs to set the _validated_ field’s boolean value to true.

> **Write**: "validated" boolean value of "true" in User Profile;

_If_ the No-Code application is storing User information in the same structure as Person information, the information returned from the API can be stored in that table. If not, the User’s information must be linked to a new record in the Person table.

> **Write**: available data to user/person table, updating User Profile visually;

After that’s been done, the user will have to still validate all of the data that’s been returned by the API. **The user should be given some form of visual notification that each profile segment has to be validated individually prior to submission.**

> **Prompt User**: "Validate each section of your profile"

**Invalid response**

An invalid response can be returned if no information was found for any person using that email address.

> **API Response**: Error = Unknown person

There are a lot of reasons that the API might not find a user, too many to go into here. At this point what is required by the user is that the user provides _the minimum_ information the industry has agreed on to disambiguate _this_ person from _that_ person. For now, that means that the user has to add at least two social addresses (LinkedIn, Twitter, Facebook) and an office address.

> **Prompt User**: "There is not enough social information to disambiguate you. You must submit two Social Addresses and an Office Address."

Once the user has contributed at least that much information, they can continue.

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
