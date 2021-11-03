# Account Management Wireframes

All wireframes for this portion of the Compliance as Code project are available at:

[https://balsamiq.cloud/srj76i4/ple67oc](https://balsamiq.cloud/srj76i4/ple67oc)

The scope of this portion of the project is to allow _the administrator_ of a known account and to fill out additional information about the account assigned to the Organization.

The layouts expressed in this documentation are for _communication purposes only_. They are not meant to provide branding guidance or even an official look-and-feel. They exist merely to convey the technical aspects of the project. _Real_ designers will create something much more effective.

### Schema

The schema for an account is found in multiple locations:

* [http://grcschema.org/Account](http://grcschema.org/Account), which provides the core schema for an account; and
* [http://grcschema.org/Organization](http://grcschema.org/Organization), which provides the schema for the domain to organization match.

The ERD for working with an account looks like the diagram that follows:

![Account ERD](https://www.complianceascode.net/wp-content/uploads/2021/11/AccountERD.png)

#### What needs to be understood about this structure

Organizations exist outside of Accounts. When you think of an organization, think of, say, IBM. It exists whether IBM has an account within this system or not.

Then, when someone that has _ibm.com_ in their email address wishes to establish an Account in the system, they can do so, and it is tied to the IBM Organization. And then another person with _ibm.com_ in their email address might want to establish a _different_ account – they can do so – and _that account, too_, will be linked to the IBM Organization. Both accounts are tied to the IBM Organization through the domain in their email addresses.

Each Account can have its own, private, Groups and Initiatives. As well as its own addresses and phone numbers, not directly associated with the formal addresses associated with the Organization.

### Navigation

Navigation to the Account is accessed through the **Account Settings** icon at the bottom of the navigation pane. When the pane is open, it is named **Account Settings** as shown below.

![Account Settings](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Open-Navigation.png)

Within the Account section of the shell, sub-navigation must include capabilities to switch between _this_ account, _the account’s organization_, other subnavigation items associated with the account.

![Account subnavigation](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Sub-Navigation.png)

### Basic Info

Basic information for the account isn’t much. Just the account name (which should already exist), the meta data (which also should exist), and the optional description and telephone numbers.

![Account Basic Info](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Basic-Info2.png)

1. **Account Name** should be pulled directly from the content entered during the signup phase.
2. **Telephone numbers** can be entered or deleted as well.
3. **Description** is completely optional.
4. **Organizational Character Index** is manually added when the user clicks the **Click for Survey** button. The button should take the user [HERE](https://theucf.info/MyersBriggsIndex) to this URL: https://theucf.info/MyersBriggsIndex.

#### Adding and deleting telephone numbers

Adding a new telephone number brings up a modal dialog prompting the user to enter the telephone number.

![New telephone number](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-New-Telephone-Number.png)

Deleting a telephone number brings up a dialog to ensure that the deletion request wasn’t a mistake.

![Delete telephone number](https://www.complianceascode.net/wp-content/uploads/2021/11/Delete-Telephone-Number.png)

### Postal Addresses

There are three addresses (with at least the primary being required); primary billing, and shipping.

![Postal addresses](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Postal-Addresses.png)

When filled out, they must be filled out in the order of _country_, _state_, _city_, and then the rest of the information. This is because _country_, _state_, and _city_ are all pop-ups, one deriving its list from the other.

1. **Country** **API** – Country List API will be linked here.
2. **State API** - State List API will be linked here.
3. **City API** - City List API will be linked here.

### Users

This is a listing of Users. Users are added/managed through the Account Users layout. Users can be navigated to by clicking on arrow by their name.

![Users](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Members.png)

For information about the Users' fields, see the section on [User Profile Wireframes](user-profile-wireframes.md#basic-info).

The main difference between the User Profile Management look and feel and the Account Management for _Users_ look and feel is that the Account Management version has a vertical left navigation for all of the users that allows linking to that User's account, as shown below:

![Account view of User Basic Info](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Users-Basic-Info.png)

### Account Groups

Each account can have multiple groups within the account, for various purposes. There are three screens that can be accessed for each group.

#### Account Group Basic Info

![Account Group – Basic Info](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Group-Basic-Info.png)

1. Groups can be navigated to by their name in the Groups navigation pane.
2. This is the group’s name, and is mandatory.
3. An optional description of the group can be added here.
4. A parent group can be selected _from existing account-related groups_. Any child of _this_ _group_ will be listed in the sub groups list.
5. This is optional. However, when filled out, the address must be filled out in the order of _country_, _state_, _city_, and then the rest of the information. This is because _country_, _state_, and _city_ are all pop-ups, one deriving its list from the other.
6. An optional telephone number for the group can be added.

#### Account Group Character

An account group’s character helps determine how to interact with the group when trying to achieve a goal. This can be very useful.

![Account Groups Character](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Group-Character.png)

1. **Group Character settings** – these are options settings wherein the user selects a number from 1 to 10 for each of the four characterizations. Selections from 1-5 will create a _formal_ setting and 6-10 will create an _informal_ setting. There are images associated with each of the formal and informal settings for each of the four characterizations.
2. **Organizational Character Index** – this is an optional field to be filled out for the _the account_. If it was filled out at the account level, that information will show up here. The button for the survey should link to: [https://theucf.info/MyersBriggsIndex](https://theucf.info/MyersBriggsIndex).

#### Account Group Members

This is a listing of members. Members are added/managed through the Account Users layout. Members can be navigated to by clicking on arrow by their name.

![Account Group Members](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Group-Members.png)

#### Account Initiative Basic Info

![Account Initiative – Basic Info](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Initiatives-Basics.png)

1. Initiatives can be navigated to by their name in the Initiatives navigation pane.
2. This is the Initiative’s name, and is mandatory.
3. An optional description of the Initiative can be added here.
4. A parent group can be selected _from existing account-related groups_. Unlike Account Groups, Account Initiatives cannot have children.
5. Duration is unique to Initiatives. Initiatives often have a begin and end date.
6. This is optional. However, when filled out, the address must be filled out in the order of _country_, _state_, _city_, and then the rest of the information. This is because _country_, _state_, and _city_ are all pop-ups, one deriving its list from the other.
7. An optional telephone number for the group can be added.

#### Account Initiative Character

An account group’s character helps determine how to interact with the group when trying to achieve a goal. This can be very useful.

![Account Initiative – Character](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Initiative-Character.png)

1. **Group Character settings** – these are options settings wherein the user selects a number from 1 to 10 for each of the four characterizations. Selections from 1-5 will create a _formal_ setting and 6-10 will create an _informal_ setting. There are images associated with each of the formal and informal settings for each of the four characterizations.
2. **Organizational Character Index** – this is an optional field to be filled out for the _the account_. If it was filled out at the account level, that information will show up here. The button for the survey should link to [https://theucf.info/MyersBriggsIndex](https://theucf.info/MyersBriggsIndex).

#### Account Initiative Members

This is a listing of members. Members are added/managed through the Account Users layout. Members can be navigated to by clicking on arrow by their name.

![Account Initiative Members](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Initiative-Members.png)

### Account Teams

Teams is a very simplistic screen. A team doesn’t need much information, other than the team lead’s designation and the team members.

![Account – Teams](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Teams.png)

1. Teams can be navigated to by their name in the Initiatives navigation pane.
2. The name of the team is entered here.
3. The team lead appears in this field. It is _not_ modifiable here, as this is a selection that can be made in the user’s table.
4. The description for the team is optional.
5. The members of the team are listed and can be navigated to via clicking the arrow by their names.

### Account Other Settings

There also should be a “catch all” area for additional settings that will be necessary, such as a place to put the AGPM API key, etc.

![Account Other Settings](https://www.complianceascode.net/wp-content/uploads/2021/11/Account-Basic-Settings.png)
