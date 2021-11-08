# Dataflow for converting an Account to a known Organization



The Compliance as Code federated system uses a couple of API calls to convert an Account to a known Organization so that the organization as a whole can contribute content.

![Abbreviated Flow](https://www.complianceascode.net/wp-content/uploads/2021/11/NoCode-User-or-Organization-to-Contributor.png)

Let’s walk through the process.

The process to convert an Account to a known Organization can only by done by the account’s administrator. It begins on the **Our Organization** page within the application.

![Our Organization](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Our-Organization-Not-Public.png)

If an account has not set up a public organization (or any other account belonging to the same domain hasn’t yet done it), the screen should be grayed out and a dialog should appear asking if the administrator would like to convert the account to an organization.

Before we convert the account to an Organization, the administrator must first accept what we call the _TLP_ (Terms of Service, License, and Privacy Policy).

## Accepting the Terms of Service, License, and Privacy Policy

It all begins with walking the administrator through the **Terms of Service**, **License Agreement**, and **Privacy Policy**.

![No-Code TLP process](https://www.complianceascode.net/wp-content/uploads/2021/11/NoCode-TLP-Acknowledgement2.png)

### Terms of Service

The No-Code application must make the call to get the current Terms of Service.

> **API Call**: GET /ToS;

To which the gateway will return those terms.

> **API Return**: ToS;

Once the data is returned, the application must notify the administrator that he or she _must_ accept the Terms of Service prior to moving forward.

> **Prompt administrator**: "You must accept the terms of service.”

A window is then displayed with the current Terms of Service in it, as shown below.

![TLP Acknowledgement](https://www.complianceascode.net/wp-content/uploads/2021/11/TLP-Window.png)

1. If the text is longer than fits within the window, the window must display a scrolling field.
2. Both the **Decline** and **Accept** buttons are initially disabled _if_ the scroll bar is activated. _Scrolling to the end_ of the text is what activates both buttons.

_If_ the administrator accepts the Terms of Service, they can continue.

_If_ the administrator _does not_ accept the Terms of Service, the application must display a prompt that the process will be canceled.

> **Prompt administrator**: "You cannot continue without acknowledging the Terms of Service."

### Privacy Policy

The No-Code application makes an API call to get the Privacy Policy.

> **API Call**: GET /PrivacyPolicy;

To which the gateway will return the current version of the Privacy Policy.

> **API Return**: PrivacyPolicy;

Once the data is returned, the application must notify the administrator that he or she _must_ accept the Privacy Policy prior to moving forward.

> **Prompt administrator**: "You must accept the Privacy Policy.”

A window is then displayed with the current Privacy Policy in it that acts the same as the one for the Terms of Service above.

_If_ the administrator accepts the Privacy Policy, they can continue.

_If_ the administrator _does not_ accept the Privacy Policy, the application must display a prompt that the process will be canceled.

> **Prompt administrator**: "You cannot continue without acknowledging the Privacy Policy.”

### License Agreement

The No-Code application makes an API call to get the License Agreement.

> **API Call**: GET /License;

To which the gateway will return the current version of the License Agreement.

> **API Return**: License;

Once the data is returned, the application must notify the administrator that he or she _must_ accept the License Agreement prior to moving forward.

> **Prompt administrator**: "You must accept the License Agreement.”

A window is then displayed with the current License Agreement in it that acts the same as the one for the Terms of Service above.

_If_ the administrator accepts the License Agreement, they can continue.

_If_ the administrator _does not_ accept the License Agreement, the application must display a prompt that the process will be canceled.

> **Prompt administrator**: "You cannot continue without acknowledging the License Agreement.”

## Begin validate Organization

The dataflow diagram for this process is shown below:

![Organization Validation flow](https://www.complianceascode.net/wp-content/uploads/2021/11/NoCode-Organization-Validation-1.png)

Once the user has accepted the three agreements, the Person Validation process begins.

### Initial API Call

The No-Code application sends an API call to get Organization information using its domain name.

> **API Call**: GET /OrganizationbyDomain

#### On the server side

On the server side, one of three things is going to happen. Either

1. the request is going to be queued (meaning it is taking a bit of time to gather the information),
2. it is going to return whatever it found, or
3. it won’t find anything about the Organization.

#### Request queued

> **API Return**: Error = Request Queued

If the request is queued you’ll need to present the user with some form of dialog, informing them that they’ll need to retry the request again _at least after 5 minutes_.

> **Prompt User**: "Your request is queued. Please wait 5 min and click Validate Public Organization again."

#### Invalid response

An invalid response can be returned if no information was found for any organization using that domain address.

> **API Return**: Error = Unknown Organization

There are a lot of reasons that the API might not find an organization, too many to go into here. At this point what is required by the administrator is to provide the minimum information the industry has agreed on to disambiguate _this_ organization from _that_ organization. For now, that means that the user has to add an office address and at least two social addresses (LinkedIn, Twitter, Facebook) and an office address.

> **Prompt User**: "There is not enough information to disambiguate this organization. You must submit two Social Addresses and an Office Address.”

Once the user has contributed at least that much information, they can continue.

#### Valid Response

> **API Response**: Organization Information

If an Organization has been found that matches the domain address given, the API will return a valid response with some or all of the data fields specified in the Organization schema.

There is also something to note about this response that has to be dealt with at the No-Code application. An account could submit a domain such as _unifiedcompliance.com_, and the response back from the API will have that domain _in the domain list, but not the primary domain_. The reason for this is that many organizations will have multiple domains (our organization owns 30 of them). The **Organization’s primary domain** will be returned by the API, but that might not be the domain that was submitted.

If the primary domain doesn’t match the submitted domain, then the No-Code application has to ask the user whether the domain submitted was just one in the list of acceptable ones, or, if that organization is a _subsidiary_ of the returned organization.

**The primary domain and submitted domain don’t match**

If they don’t match, the No-Code application must ask the administrator what to do.

> **Prompt User**: "Your mail domain is not <>. Are you a subsidiary or is this just one domain among many?"

**If the organization is **_**not**_** a subsidiary**

If the administrator states that the organization is not a subsidiary then write the available data to the Organization table.

> **Write**: available data to Organization tables, updating Organization Profile visually

If the administrator states that the organization _is_ a subsidiary, then you can’t use the returned information.

> **Prompt User**: "This is a subsidiary, only the domain information will be written, all else will be drawn from Account info."

In that case, write what you found in the account info to the Organization table and go from there.

> **Write**: Account data to Organization tables, updating Organization Profile visually

**The primary domain matches the submitted domain**

In this instance, the domain that was submitted is the same as the primary domain that we returned. This is much easier. At that point, the No-Code application needs to write the contents of the response into the local system, and it also needs to set the validated field’s boolean value to true.

> **Write**: "validated" boolean value of "true" in Organization Profile

> **Write**: available data to Organization tables, updating Organization Profile visually

### Continuing with the validation process

After that’s been done, the user will have to still validate all of the data that’s been returned by the API. **The administrator should be given some form of visual notification that each profile segment has to be validated individually prior to submission.**

> Mark **Basic Info**, **Classification**,**Social Addresses**, **Postal Addresses** for editing

And then the application will need to prompt the administrator to validate the profile.

> **Prompt User**: "Validate your organization's profile"

### Trapping for section saves

Each conversion from Account to Organization requires several sections of data (basic info, addresses, etc.). Before the administrator can submit the conversion each and every one of these sections has to be reviewed. Therefore, the No-Code application will need to trap for the administrator saving each of those.

### Submitting the Organization

Once each of the sections has been checked the No-Code application needs to submit the data via the API call when the administrator clicks the Submit Organization button via whatever dialog is to be displayed.

> **Prompt User**: Select Submit Organization

When the button is clicked, the No-Code application sends off the following API call:

> **API Call**: Patch /Organization

### Receiving the data and checking it

On the server side, we will be writing that organization’s data to our table and will then add some CoreMetaData you’ll need to write back into the No-Code system; the Organization’s ID, date created & modified, etc.

> **Write**: Organization Data

> **API Response**: Organization Data

After you submit the Patch for the Organization, the system will return the same information with the additional CoreMetadata. This will need to be written into that record’s Organization table.

> **Write**: Organization Information
