# Wireframes



These are the wireframes for adding an Authority Document are listed here.

The assumption is that this MVP is built upon the Core Account MVP that already has the flows and structures for establishing an account and connecting the account to the Compliance as Code API gateway.

All wireframes in Balsamiq format can be found at [https://balsamiq.cloud/srj76i4/p26mwgs](https://balsamiq.cloud/srj76i4/p26mwgs)

All wireframes in Figma format can be found at

## Landing Page <a href="#_toc99020265" id="_toc99020265"></a>

![Landing Page](<../../.gitbook/assets/1 (1)>)

1. Search/Edit Catalog, is the name of the app section. This should direct users to the Search Catalog tab.
2. Account information can be accessed by clicking the cog in the bottom left of the main navigation pane.
3. Basic information for the landing page will be presented, along with a link to the documentation for the MVP.

## Search Catalog - Geography <a href="#_toc99020266" id="_toc99020266"></a>

The Search Catalog - Geography view is the default layout for the Search/Edit Catalog Section.

![Search Catalog – Geography](<../../.gitbook/assets/2 (1)>)

1. Authority Documents can be searched in the hierarchy by name, and/or filtered by geography and subject matter.\
   \*Values for dropdown filters and functionality TBD.
2. The default layout is Geography. These buttons allow the user to flip between the Geography view and the Subject Matter view.
3. This button opens the Add an Authority Document request modal.
4. This icon opens the Authority Document Details modal. Layout TBD.
5. This displays the AD status: Queued, Cataloged, or Mapped.
6. This +ADD link opens the Add an Authority Document request modal, with the Geography info prefilled based on where in the hierarchy the +ADD is selected from.

## Search Catalog – Subject Matter <a href="#_toc99020267" id="_toc99020267"></a>

The Search Catalog – Subject Matter view is an alternate layout Search Catalog tab.

![Search Catalog – Subject Matter](<../../.gitbook/assets/3 (2)>)

1. Authority Documents can be searched in the hierarchy by name, and/or filtered by geography and subject matter.\
   \*Values for dropdown filters and functionality TBD.
2. The default layout is Geography. These buttons allow the user to flip between the Geography view and the Subject Matter view.
3. This button opens the Add an Authority Document request modal.
4. This icon opens the Authority Document Details modal. Layout TBD.
5. This displays the AD status: Queued, Cataloged, or Mapped.
6. This +ADD link opens the Add an Authority Document request modal, with the Subject Matter info prefilled based on where in the hierarchy the +ADD is selected from.

## Add an Authority Document <a href="#_toc99020268" id="_toc99020268"></a>

The Add an Authority Document modal provides the information fields required to add an Authority Document.

![Add an Authority Document](<../../.gitbook/assets/4 (1)>)

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

## New Record Saved <a href="#_toc99020269" id="_toc99020269"></a>

The New Record Saved modal confirms the Authority Document has been added.

![Record Saved](<../../.gitbook/assets/5 (2)>)

1. Text informing the user a new record has been created.
2. Closes out the modal.

## Pending Changes <a href="#_toc99020270" id="_toc99020270"></a>

The pending changes tab shows all the changes and additions a user has added to their local environment and allows them to publish content to the federated DB.

![Pending Changes Tab](<../../.gitbook/assets/6 (2)>)

1. This button opens the Add an Authority Document request modal.
2. This column displays the Authority Document name.
3. This column displays the types of changes. Data TBD.
4. This column displays the date changes were made.
5. This selection indicates the changes that will be published to the federated DB. All are selected by default.
6. This button publishes the changes to the federated DB.
