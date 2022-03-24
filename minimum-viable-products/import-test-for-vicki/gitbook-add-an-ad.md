# Gitbook Add an AD

![https://www.unifiedcompliance.com/wp-content/themes/ucf/1.0/images/mast-logo.png](<../../.gitbook/assets/0 (1)>)

**Mapper 2. 0: Request an Authority Document**

**Contents**

User Stories 4

I'm a policy/procedure writer 4

I manage or work with the compliance team 4

I’m a company librarian 4

Wireframes 5

Left-Hand Navigation 5

Search Catalog - Geography 6

Search Catalog – Subject Matter 7

Add an Authority Document 8

New Record Saved 9

Pending Changes 10

### User Stories <a href="#_toc99020260" id="_toc99020260"></a>

The following are the user stories supporting the building of a custom Authority Document catalog.

#### I'm a policy/procedure writer <a href="#_toc99020261" id="_toc99020261"></a>

I need to add to, and then reference, documents in the Authority Document catalog that I am citing in our internal policies and procedures. Where do I search for all of the Authority Documents our various groups and initiatives are using? How do I use that list to reference as a bibliography? What if I want to suggest new documents, not found in the list, to the various people in our organization?   

#### I manage or work with the compliance team <a href="#_toc99020262" id="_toc99020262"></a>

I need a catalog of the Authority Documents we use as sources for our compliance mandates.

 Where do I search for all of the Authority Documents our various groups and initiatives are using? What if I want to suggest new documents, not found in the list, to the various people in our organization? I need to create several Authority Document lists, bespoke for various groups within our organization, of the Authority Documents they have to follow. I also need to route that list of Authority Documents around to various groups for their edification.   

#### I’m a company librarian <a href="#_toc99020263" id="_toc99020263"></a>

I maintain the “card catalog”, if you will, of all regulations and standards we must follow. I need to manage the list of documents we must follow for compliance purposes, adding new ones, subtracting others. I need to add metadata to each of the Authority Documents during the cataloging process so that we have a way to search them based on content and other items. I need to provide a way for our company to search our catalog and create subset lists for various purposes. Our staff will also need a way to update those lists, adding and subtracting documents they care about. Our staff needs an easy way to cite, in a standard citation format, any of the Authority Documents in their list when referencing them for various reasons.

### Wireframes <a href="#_toc99020264" id="_toc99020264"></a>

These are the wireframes for adding an Authority Document are listed here.

The assumption is that this MVP is built upon the Core Account MVP that already has the flows and structures for establishing an account and connecting the account to the Compliance as Code API gateway.

All wireframes in Balsamiq format can be found at [https://balsamiq.cloud/srj76i4/p26mwgs](https://balsamiq.cloud/srj76i4/p26mwgs)

All wireframes in Figma format can be found at

#### Left-Hand Navigation <a href="#_toc99020265" id="_toc99020265"></a>

![](<../../.gitbook/assets/1 (1)>)The left-hand navigation pane is collapsible.

Left-Hand Navigation

1. Search/Edit Catalog, is the name of the app section. This should direct users to the Search Catalog tab.
2. Account information can be accessed by clicking the cog in the bottom left of the main navigation pane.
3. Basic information for the landing page will be presented, along with a link to the documentation for the MVP.

#### Search Catalog - Geography <a href="#_toc99020266" id="_toc99020266"></a>

The Search Catalog - Geography view is the default layout for the Search/Edit Catalog Section.

![](<../../.gitbook/assets/2 (1)>)Search Catalog – Geography

1. Authority Documents can be searched in the hierarchy by name, and/or filtered by geography and subject matter.\
   \*Values for dropdown filters and functionality TBD.
2. The default layout is Geography. These buttons allow the user to flip between the Geography view and the Subject Matter view.
3. This button opens the Add an Authority Document request modal.
4. This icon opens the Authority Document Details modal. Layout TBD.
5. This displays the AD status: Queued, Cataloged, or Mapped.
6. This +ADD link opens the Add an Authority Document request modal, with the Geography info prefilled based on where in the hierarchy the +ADD is selected from.

#### Search Catalog – Subject Matter <a href="#_toc99020267" id="_toc99020267"></a>

The Search Catalog – Subject Matter view is an alternate layout Search Catalog tab.

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/3 (2)>)Search Catalog – Subject Matter

1. Authority Documents can be searched in the hierarchy by name, and/or filtered by geography and subject matter.\
   \*Values for dropdown filters and functionality TBD.
2. The default layout is Geography. These buttons allow the user to flip between the Geography view and the Subject Matter view.
3. This button opens the Add an Authority Document request modal.
4. This icon opens the Authority Document Details modal. Layout TBD.
5. This displays the AD status: Queued, Cataloged, or Mapped.
6. This +ADD link opens the Add an Authority Document request modal, with the Subject Matter info prefilled based on where in the hierarchy the +ADD is selected from.

#### Add an Authority Document <a href="#_toc99020268" id="_toc99020268"></a>

![](<../../.gitbook/assets/4 (1)>)The Add an Authority Document modal provides the information fields required to add an Authority Document.

Add an Authority Document

1. Text field for the name of the Authority Document.
2. Text field for the URL the Authority Document is located at.
3. Single select for the availability/accessibility of the Authority Document at the provided URL.
4. Single select for the language the Authority Document is available in at the provided URL.
5. Multi-select list of subject matters applicable to the Authority Document.
6. Single select widget for location of Authority Document in the Authority Document Geography Hierarchy.\
   \*Implementation of widget TBD.
7. User Direction for Geography Widget.
8. These buttons allow the user to **SAVE** the Authority Document record or **CANCEL** the Authority Document addition.
9. This cancels the Authority Document addition.

#### New Record Saved <a href="#_toc99020269" id="_toc99020269"></a>

The New Record Saved modal confirms the Authority Document has been added.

![Graphical user interface, text, application

Description automatically generated](<../../.gitbook/assets/5 (2)>)Record Saved

1. Text informing the user a new record has been created.
2. Closes out the modal.

#### Pending Changes <a href="#_toc99020270" id="_toc99020270"></a>

![Graphical user interface, text, application

Description automatically generated](<../../.gitbook/assets/6 (2)>)The pending changes tab shows all the changes and additions a user has added to their local environment and allows them to publish content to the federated DB.

Pending Changes Tab

1. This button opens the Add an Authority Document request modal.
2. This column displays the Authority Document name.
3. This column displays the types of changes. Data TBD.
4. This column displays the date changes were made.
5. This selection indicates the changes that will be published to the federated DB. All are selected by default.
6. This button publishes the changes to the federated DB.
