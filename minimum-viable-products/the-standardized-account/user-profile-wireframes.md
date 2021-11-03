# User Profile Wireframes

3This document identifies the core wireframe features for managing a User Profile within the Compliance as Code environment. The left-hand navigation in this diagram is limited to only those items that pertain to _this diagram_ and _do not contain_ any normative navigation items found within the rest of the application.

### The difference between a User and a known Person

There is a huge difference between an account user and a disambiguated (known) Person. A User of an account can request information fro the federated database and can change _local_ information within their own application. In order to contribute content _to_ the federated database, the user must be vetted and disambiguated and be registered as a known Person. The content in these wireframes shows _all_ of the content that pertains to a Person, and the User’s content is a subset of that. Throughout this document we will distinguish between a User’s information and a Person’s information.

#### JSON Schema for User and Person

The JSON Schema for a User is as follows:

![User JSON](https://www.complianceascode.net/wp-content/uploads/2021/11/UserJSON.png)

The JSON Schema for a Person is as follows:

![Person JSON](https://www.complianceascode.net/wp-content/uploads/2021/11/PersonJSON.png)

The two can be connected through a one-to-one relationship from the User to the Person:

![User to Person](https://www.complianceascode.net/wp-content/uploads/2021/11/User-to-Person.png)

### Navigating to the User Profile

Navigation to the User profile can be achieved from two locations as exhibited in items 2 & 3.

![User Profile Navigation](https://www.complianceascode.net/wp-content/uploads/2021/11/Navigation-to-User-Profile.png)

1. The User’s name is always shown on the top right of each window. When the user clicks their name, a pop-up opens up with at least two items in it:
2. **Managing User Profile** which links to the _User Profile Basic Info_ page, and **Log Out** which logs the user out of the system.
3. The bottom left of the window always has the **Settings** cog. _Only the administrator_ of the system can open up the settings for the system. All other users are directed to the _User Profile Basic Info_ page.

### Basic Info

Basic information for each User comprises their primary name & email address (mandatory), and optional social addresses. The suggested layout for basic information follows:

![Basic Info](https://www.complianceascode.net/wp-content/uploads/2021/11/User-Profile-Basic-Info2.png)

1 The **Save** and **Delete** buttons should be activated and the **Cancel** button should only be activated _if_ changes to the record were made by the User.

2\. Each person’s name has two mandatory fields: first name and last name. This sets the person’s primary name content in the Names layout.

2a. The Prefix for a person’s name is created from a pop-up selector. The results of the selection should show both the abbreviated prefix and the full prefix. (see Name prefixes and suffixes below)

2b. The Suffix for a person’s name is created from a pop-up selector. The results of the selection should show both the abbreviated suffix and the full suffix. (see Name prefixes and suffixes below)

3\. It is **mandatory** that the domain for the staff member’s email address be derived from the domain of the organization. Therefore, this field can either be manually filled out (but tested against the domain) or it can be automatically filled out from the _disambiguated system name_ (10) plus the domain name.

4-6. Social media addresses are optional.

7\. This is automated data and comes from the records. Having this in the Staff layout _is optional_.

8\. This is automated. (see Calculating the full name below).

9 & 10. These are both automatically calculated. (see Calculating disambiguated names below).

11\. These are optional checkboxes that denote whether the staff member is the **admin**, the **billing contact**, or a **contributor** to content added to the federated mapping system. Only the **Administrator** of the Account can promote a user to **Admin** or **Billing Contact**. Clicking the **Contributor** button sets off a process to convert the user to a Contributor and is not covered at this time.

12\. This is the API Key from the AGPM gateway.

### Name prefixes and suffixes

For standardization purposes all name prefixes and suffixes are added via a predefined list, using the ID of the prefix and suffix to tie the text to the ID. The application _must_ maintain tables of these references and _must_ update those tables on a regular basis to ensure parity with the federated system.

* **Name Prefix** **schema** – [http://grcschema.org/NamePrefixes](http://grcschema.org/NamePrefixes)
* **Name Prefix API** – This will be accomplished via a future API call.
* **Name Suffix schema** – [http://grcschema.org/NameSuffixes](http://grcschema.org/NameSuffixes)
* **Name Suffix API** – This will be accomplished via a future API call.

#### Calculating the full name

The full name is calculated as

if(prefix≠null;prefix & “ “) & first name & “ “ & if(middle initial≠null;middle initial & “ “) & last name & if(suffix≠null;” “ & suffix)

#### Calculating disambiguated names

The larger the organization, the greater the chances that duplicate names might exist when combining first and last names. Two people named James and John Smith would create a duplicate if the organization’s naming standard were first initial followed by last name. Joseph L. Smith and Joe T Smith would create duplicates if the organization’s naming standard were first name followed by last name.

Therefore, two things must happen.

a. The organization should establish a standard name configuration system for creating system names. The basic system can be as simple as the “name configurator” shown below:

![Sample name configurator](https://www.complianceascode.net/wp-content/uploads/2021/11/Name-Configurator.png)

This has settings for first, middle, last names, whether to uses spaces or periods between names, how to set the case, and even whether to convert the text to ASCII characters.

b. The name configuration standard _could_ produce duplicate results. Therefore, a methodology for disambiguation needs to be put into place. Whether this method is configurable (such as the name configurator) or automatic doesn’t matter. One algorithm is to simply add a numeric value behind the system name so that the second joseph.smith would become joseph.smith2, the third joseph.smith3, and so on. It can be more complicated than that, or as simple as that.

### User Names

User names is an array of names. The person’s primary name can be set from here or on the Basic Info layout.

For all names, the First Name and the Last Name must be filled out.

![Staff Names](https://www.complianceascode.net/wp-content/uploads/2021/11/User-Profile-Names.png)

There is a bit of a trick to this layout – a person’s name can either be in the format of a name or an alias. If an alias, the only thing filled out is the freeform\_name field, not shown here. Therefore, this layout should not include any record wherein the freeform\_name is the only entry.

### Aliases

There is a bit of a trick to this layout, as mentioned in Staff Names above. This layout is _only_ for names records that _only_ have the freeform\_name field filled out.

![Aliases](https://www.complianceascode.net/wp-content/uploads/2021/11/User-Profile-Aliases.png)

1. This is the freeform name. The **Disambiguated System Name** is _always_ entered as a record for this user.
2. This is the _alias type ID_ and is derived from _something other than_ “1”, from the Primary field.

2 = disambiguated system name

3 = previous system name

### Emails and Phone Numbers

These are both arrays assigned to a staff member. Other than the primary email address, they are optional.

![Email & Phone Numbers](https://www.complianceascode.net/wp-content/uploads/2021/11/User-Profile-Email.png)

The _calling codes_ for phone numbers can be automatically created using the callingcodes schema and API calls.

* **Calling Codes Schema** - http://grcschema.org/CallingCode
* **Calling Codes API** – not finished yet

### Postal Addresses

Postal Addresses for each staff member are optional. When filled out, they must be filled out in the order of _country_, _state_, _city_, and then the rest of the information. This is because _country_, _state_, and _city_ are all pop-ups, one deriving its list from the other.

![Postal Address](https://www.complianceascode.net/wp-content/uploads/2021/11/User-Profile-Addresses.png)

1. **Country** **API** – This will be accomplished via a future API call.
2. **State API** - This will be accomplished via a future API call.
3. **City API** - This will be accomplished via a future API call.

### Teams and Roles

These are completely optional for being filled out. Both teams and roles should be pop-ups selectable from _existing_ teams and roles _found in this account or Organization_.

![Teams & Roles](https://www.complianceascode.net/wp-content/uploads/2021/11/User-Profile-Teams-and-Roles.png)

###
