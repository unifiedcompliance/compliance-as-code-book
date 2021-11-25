# Wireframes



This dictionary wireframe model assumes that it is being built _on top of_ the **Standardized Account with Federated Contributors** as users of this tool should be able to contribute content _back_ to the federated dictionary.

The Balsamiq wireframes for this project are located [HERE](https://balsamiq.cloud/srj76i4/pweqj5f) and public comments are open and looked forward to.

## Basic Navigation

Basic navigation is covered in two wireframes, with the first being the _closed_ navigation.

![Basic Navigation](https://www.complianceascode.net/wp-content/uploads/2021/11/Basic-Dictionary-Navigation.png)

1. The left-hand navigation is the main navigation for this MVP. The top icon expands and contracts the navigation pane. The _Home_ icon always takes the user to the landing page. For this project, the _Book_ icon represents the dictionary, and the _file cabinet_ below it represents the corpora.
2. Subnavigation is shown across the top of the window, with the current section highlighted with a colored bar below it (as shown with _Search_).
3. The bottom left of the main navigation always has the _gear_ icon to reach the settings and the _question_ icon for the relevant help features.

### Expanded Basic Navigation

When the left-hand navigation pane is expanded, the sub navigation items will be shown below the main navigation.

![Expanded Basic Navigation](https://www.complianceascode.net/wp-content/uploads/2021/11/Expanded-Basic-Dictionary-Navigation.png)

1. The main navigation item will display a disclosure triangle if there are multiple sub navigation items below it.
2. Once expanded, each item in the subnavigation list will be shown.

## Landing Page

The landing page for the MVP will show a basic “about” page, explaining the purpose of the MVP.

![Landing Page](https://www.complianceascode.net/wp-content/uploads/2021/11/Dictionary-Landing-Page.png)

## Search Dictionaries

Search allows users to search _multiple_ dictionaries, find terms, and then add them to localized dictionaries or term lists.

![Search Page](https://www.complianceascode.net/wp-content/uploads/2021/11/Search-Page.png)

1. The **Clear button** button is disabled until a term has been searched for.
2. The **Advanced Search** checkbox with associated help icon denotes whether the user has chosen to perform a _string_ search (meaning search for whatever text was entered) or use advanced search features for more complex searches.
3. The **Search By** combo box allows the user to set _which field_ the search is performed. This can either be set to search by the _term, acronym, or definition_ fields. This is a standard list with no additional list items.
4. The **Dictionary** combo box sets which dictionary to use when searching. This is a dynamic list and is set by the various API calls enabled by the AGPM gateway.

### Found Terms

Once a search has been performed, the list of found terms is returned.

![Found Terms](https://www.complianceascode.net/wp-content/uploads/2021/11/Found-Terms-List-Page.png)

1. Because a search has been performed, the **Clear** button is now enabled. Clicking this button removes all found items and empties the search field.
2. A list of found terms is presented and a **View** button allows the user to view _that_ term’s information.
3. Because of the constraints on screen size, lists are returned in a paginated fashion. Pagination navigation is found on the bottom left of the main window and the number of results per page (along with the total number of results found) is shown on the bottom right.

### Term Basics

The Term Basics window allows adding/subtracting a term from local custom dictionaries as well as local terms lists.

![Term Basics](https://www.complianceascode.net/wp-content/uploads/2021/11/Term-Basics-Page.png)

1. This is the Term itself.
2. The **Add to Dictionary** combo box allows the user to add or remove the term from an existing organizational dictionary. Adding or removing the dictionaries themselves is done through the **Dictionary & Lists** section.
3. The **Add to List** combo box allows the user to add or remove the term from an existing organizational dictionary. Adding or removing the lists themselves is done through the **Dictionary & Lists** section.
4. A list of all acronyms is listed here. This list is _not_ hyperlink-enabled.
5. Some dictionaries, such as the UCF’s Compliance Dictionary, allow for the preference of one term over any of it’s synonyms. This is a hyperlink-enabled list of those terms.
6. **Non-standard Terms** is a hyperlink-enabled list of all terms that are considered non-standard (such as common mis-spellings, etc.) of this term.
7. **Other Forms** presents the various forms verbs and nouns can take (past, present, etc. for verbs, plural, possessive for nouns). These are vary useful in natural language processing.

#### Non-standard Terms

The non-standard terms page is a very limited version of the basic page.

![Non-standard Term Basics](https://www.complianceascode.net/wp-content/uploads/2021/11/Non-Standard-Term-Page.png)

1. The **Term** is presented in italic to show that it is not a normal term.
2. The list of acronyms is handled the same way as in the Term Basics page.
3. There is a single **Standard Term** listed as a hyperlink to that term.
4. The **Other Forms** is presented the same as with the Term Basics page.
5. The only tabs available for a non-standard term are **Basics, Examples,** and **Change History**.

### Term Definitions

Term Definitions are presented as a paged list. Remember that terms are polysemous; they have the capacity for multiple related meanings.

![Term Definitions](https://www.complianceascode.net/wp-content/uploads/2021/11/Term-Definitions-Page.png)

1. Definition **Type** is shown in the first column with the **Definition** itself shown in the next column.
2. The **Sources** for the definition are shown in that column. If the source of the definition is a JSON-LD source or URL source, the source is a hyperlink-enabled source.
3. A clipboard **Copy** icon is shown to the right of each definition. Clicking that icon copies the following to the clipboard: **Term | Type | Definition | Source** as comma separated values.
4. Because of the constraints on screen size, lists are returned in a paginated fashion. Pagination navigation is found on the bottom left of the main window and the number of results per page (along with the total number of results found) is shown on the bottom right.

### Relationship Graph

The relationship graph shows the UCF’s patented _Advanced Semantic Relationship_ graph.

![Relationship Graph](https://www.complianceascode.net/wp-content/uploads/2021/11/Term-Relationships-Page.png)

1. This graph is a hyperlink-enabled graph that takes the user from one term to the other. **Which means that it is performing a search** each time a term is clicked on. It should be displayed in a dual horizontal-vertical window.
2. A clipboard **Copy** icon is shown to the top right of the window and should create a PNG image on the clipboard, or, allow the user to save the image as a PNG to their device.

### Term Examples

Term examples are a paginated response drawn from the various corpora the user has loaded into the system. _If there are no corpora loaded, there are no examples shown_.

![Examples List](https://www.complianceascode.net/wp-content/uploads/2021/11/Term-Examples-Page.png)

1. The **Corpus** combo box allows the user to filter _which_ of the various corpora to show examples from. If nothing is selected - _and there are multiple corpora_ - the examples are shown from _all_ corpora.
2. The **Corpus** for each example is shown in the first column.
3. The second column shows the example text in which the term was found. The term is **bolded** in each instance it was found in these examples.
4. The **Corpus Record ID** is displayed to the right of the example as hyperlink enabled text and takes the user to _that_ particular record in _that_ corpus.
5. A clipboard **Copy** icon is shown to the right of each definition. Clicking that icon copies the following to the clipboard: **Term | Corpus | Example | Record ID** as comma separated values.
6. Because of the constraints on screen size, lists are returned in a paginated fashion. Pagination navigation is found on the bottom left of the main window and the number of results per page (along with the total number of results found) is shown on the bottom right.

### Term Change History

Terms that are in the local dictionary, or the federated dictionary, can be added or edited. This shows the change history for those terms.

![Term Change History](https://www.complianceascode.net/wp-content/uploads/2021/11/Term-Change-History.png)

1. The history itself starts with a date/time list that is default sorted as newest to oldest. However, that sort should be reversible by the user.
2. This shows the public persona name for the person or organization that created or modified the term.
3. This is a hyperlink to the contributor’s profile. If the contributor is a local user, and the edits are in the local dictionary, this should take the user to _that_ person’s profile.
4. Because of the constraints on screen size, lists are returned in a paginated fashion. Pagination navigation is found on the bottom left of the main window and the number of results per page (along with the total number of results found) is shown on the bottom right.

## Term Frequencies

Term Frequencies are corpus dependent and the searches performed here are performed on the corpus’ content.

![Term Frequencies](https://www.complianceascode.net/wp-content/uploads/2021/11/Frequencies-Page-No-selection.png)

1. If a corpus is _not_ selected, the **Search** button must be grayed out. The first showing of this window should bring up a dialog like the one shown on the screen, which should be dismissed when a corpus has been selected.
2. This is the list of existing corpora. One _has_ to be selected in order for this to work.

### Found Terms in Frequencies

Once a search has been performed, the list of found terms with frequencies is returned.

![Found Terms with Frequencies](https://www.complianceascode.net/wp-content/uploads/2021/11/Frequencies-Search-List.png)

1. A list of found terms is presented with the _count of how many times the term has been found in the selected corpus_.
2. A **View** button allows the user to view _that_ term’s information _within the Frequencies version_ of the term window, shown below.
3. Because of the constraints on screen size, lists are returned in a paginated fashion. Pagination navigation is found on the bottom left of the main window and the number of results per page (along with the total number of results found) is shown on the bottom right.

### Frequencies Examples (as well as basic, etc.)

When the user views a term within the **Frequencies** subnavigation, the **Examples** window is displayed different than the same window when performing a basic search.

![Frequencies Example Window](https://www.complianceascode.net/wp-content/uploads/2021/11/Frequencies-Examples-Page.png)

1. First, the sub-navigation that is selected is the **Term Frequencies** subnavigation for these particular panes.
2. All of the tabs perform the same within the **Freqencies** subnavigation as they would in the **Search** subnavigation.
3. The Examples portion _doesn’t have the Corpora combo box_ as that has already been set when searching for the term within this subnavigation.

## List Management

Having specific lists is great for focusing your team on terms _that matter to them_. In this portion of the MVP you can delete terms or distribute the list.

![List Management](https://www.complianceascode.net/wp-content/uploads/2021/11/List-Management.png)

1. Unless a List is selected, the **Delete** button is deactivated.
2. Creating a new List is done through the selection combo box by selecting the \*_New List_ entry. Once a new List has been selected, a dialog should appear asking the user to name it and give it a description.

### Found List Terms

Once a list has been selected the found terms are returned.

![List Found Terms](https://www.complianceascode.net/wp-content/uploads/2021/11/List-Terms.png)

1. The list of terms can be shared through several means; email, or exporting a Word, Excel, or PDF file.
2. The entire list can be deleted.
3. Each entry can be deleted.
4. Because of the constraints on screen size, lists are returned in a paginated fashion. Pagination navigation is found on the bottom left of the main window and the number of results per page (along with the total number of results found) is shown on the bottom right.

## Dictionary Management

Some organizations like to create dictionaries - list collections that are pretty large. Unlike lists, whole dictionaries aren’t appropriate for export and distribution. But they _are_ great for research and selecting terms’s definitions that fit the organization!

![Dictionary Management](https://www.complianceascode.net/wp-content/uploads/2021/11/Dictionary-Management.png)

1. Unless a Dictionary is selected, the **Delete** button is deactivated.
2. Creating a new Dictionary is done through the selection combo box by selecting the \*_New Dictionary_ entry. Once a new Dictionary has been selected, a dialog should appear asking the user to name it and give it a description.

### Found Dictionary Terms

Once a dictionary has been selected the found terms are returned.

![Dictonary Found Terms](https://www.complianceascode.net/wp-content/uploads/2021/11/Dictionary-Terms.png)

1. The entire list can be deleted.
2. Each entry can be deleted.
3. Because of the constraints on screen size, lists are returned in a paginated fashion. Pagination navigation is found on the bottom left of the main window and the number of results per page (along with the total number of results found) is shown on the bottom right.

## Concordance

The Concordance is corpus dependent and the searches performed here are performed on the corpus’ content. The search results are displayed as a **K**ey**W**ord **I**n **C**ontext (KWIC) result, meaning that the search term is displayed in the middle column of a three column result.

![KWIC Concordance](https://www.complianceascode.net/wp-content/uploads/2021/11/Concordance.png)

1. After searching for a _string_ within the selected corpus, a list is returned that allow for filtering of _strings_ in both the left and right hand columns. Any text in either of these filters reduces what is displayed in the list of returned values.
2. The _sentence_ or _citation_ that the text was found in is displayed in the list, split between everything found to the left or right of the term in the appropriate column.
3. A clipboard **Copy** icon is shown to the right of each column. Clicking that icon copies the following to the clipboard: \*\*Term | Corpus | Example \*\* as comma separated values.
4. Because of the constraints on screen size, lists are returned in a paginated fashion. Pagination navigation is found on the bottom left of the main window and the number of results per page (along with the total number of results found) is shown on the bottom right.

## Corpus Management

In linguistics, a corpus or text corpus is a language resource consisting of a large and structured set of texts. In corpus linguistics, they are used to do statistical analysis and hypothesis testing, checking occurrences or validating linguistic rules within a specific language territory. This section of the MVP allows you to manage your corpora and the text within each corpus.

![Corpus Management](https://www.complianceascode.net/wp-content/uploads/2021/11/Corpus-Management.png)

1. Unless a Corpus is selected, the **Delete** button is deactivated.
2. Creating a new Corpus is done through the selection combo box by selecting the **New Manual Input** entry. _Automatic creation of corpora through APIs is done through the settings section and not a part of these dialogs_. Once a new corpus has been selected, a dialog should appear asking the user to name it and give it a description.

### Corpus Entry List

Once a corpus has been selected, a paginated list of entries is returned.

![Corpus List of Entries](https://www.complianceascode.net/wp-content/uploads/2021/11/Corpus-Content-List.png)

1. Each entry has its ID and content displayed.
2. A **View** button is shown to the right. Clicking it takes the user to the entry edit page for that entry.
3. At the bottom of the list a **New** button exists to allow the user to create a new entry.
4. Because of the constraints on screen size, lists are returned in a paginated fashion. Pagination navigation is found on the bottom left of the main window and the number of results per page (along with the total number of results found) is shown on the bottom right.

### Corpus Edit Entry

This page allows the user to edit the content of the corpus entry, or delete it entirely.

![Corpus Edit Entry](https://www.complianceascode.net/wp-content/uploads/2021/11/Corpus-Edit-Page.png)

1. The Edit tab is selected.
2. The corpus entry’s ID is displayed along with the entry itself (in a scrollable field).
3. The **Delete** button allows the user to delete the entry.
4. The **Cancel** and **Save** buttons are only activated once a change has been made. Canceling or saving returns the user to the list view.

### Corpus Entry Change History

Corpus entries that are in the local system, or the federated system, can be added to or edited. This shows the change history for those entries.

![Corpus Entry Change History](https://www.complianceascode.net/wp-content/uploads/2021/11/Corpus-Change-History.png)

1. The history itself starts with a date/time list that is default sorted as newest to oldest. However, that sort should be reversible by the user.
2. This shows the public persona name for the person or organization that created or modified the entry.
3. This is a hyperlink to the contributor’s profile. If the contributor is a local user, and the edits are in the local dictionary, this should take the user to _that_ person’s profile.
4. Because of the constraints on screen size, lists are returned in a paginated fashion. Pagination navigation is found on the bottom left of the main window and the number of results per page (along with the total number of results found) is shown on the bottom right.
