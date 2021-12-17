# Source

### Searching the federated Authority Document Library <a href="#_toc58312069" id="_toc58312069"></a>

Below is a mockup of the Federated Authority Document library. We provide this mockup instead of actual in-use products because each product can be designed slightly different as, again, this is a collaborative effort based on _suggested_ layouts.

There are online repositories of layouts (and the code to build them) in both React and VUE.js. Those libraries are listed here:

**React Demo**: [https://developer.unifiedcompliance.com/demo/react/](https://developer.unifiedcompliance.com/demo/react/)

**React Code:** [https://github.com/unifiedcompliance/demo-react-authdoc-list](https://github.com/unifiedcompliance/demo-react-authdoc-list)

**Vue.js Demo:** [https://developer.unifiedcompliance.com/demo/vue/](https://developer.unifiedcompliance.com/demo/vue/)

**Vue.js Code:** [https://github.com/unifiedcompliance/demo-vue-authdoc-list](https://github.com/unifiedcompliance/demo-vue-authdoc-list)

![Graphical user interface, text, application

Description automatically generated](../../.gitbook/assets/14)

Sample Federated Authority Document Library search window

1. Probably the easiest way to find an Authority Document is to type the name and version number into the search field – even a partial name or version number brings up results. You don’t have to worry about getting the name absolutely correct either. Searching for NIST CSF will bring up the correct document, even though that’s not it’s official name. Current search capabilities in the demo include
   1. Official Name (title, subtitle, etc.)
   2. Common Name
   3. Subject Matter
   4. Author or Editor
2. Or, you can get a list of Authority Documents by their Geography by clicking the Geography button or Subject Matter by clicking _that_ button.

A more advanced method to search would be to click Subject Matter and then click a checkbox for a Subject Matter area of compliance. The Impact Zones and related Common Controls populate on the right side of the page. Then click Geography, and you will be able to see the coverage the UCF has in those displayed countries. Additionally, you can unselect any countries that aren’t relevant to your organization.

Alternatively, you could reverse that process and start by clicking Geography and click the checkboxes of the countries your organization must comply with. The Impact Zones with Common Controls will populate on the right side of the page. Then click Subject Matter, and you can disable or uncheck categories or areas of compliance that aren’t relevant to your company.

1. Disclosure triangles are used to the point wherein an Authority Document is shown. The Authority Document will have a document icon in front of the name, and the name that will be displayed is the Official Name.
2. An (i) button will be immediately to the right of the Authority Document name. Clicking this button will display the Authority Document’s Title report (shown later).
3. A checkbox will be placed to the right of the (i) button. Checking this box will add the Authority Document to the Selected List in the right pane.
4. Clicking Remove will bring up a dialog asking the end user if they wish to remove the Authority Document from the selected list. Clicking Yes will remove it from the list.
5. The Save List button allows the user to save the list of found Authority Documents to their device as a JSON file, or if they are using one of the Mapping tools, the Common Controls Hub, etc., save it to their workspace.

### Adding an Authority Document to the library <a href="#_toc58312070" id="_toc58312070"></a>

The Federated Authority Document Library is designed to be an open platform where anyone with interest in the matter having the capability of contributing. To that end, users from around the world have already suggested documents for addition to the library through various means – email requests, forums, support tickets through participating vendors (OnSpring, MetricStream, the UCF team, etc.). Herein we lay out sample layouts (with associated code) and sample steps to show how anyone can request new documents be added to the library.

#### Existing Request systems <a href="#_toc58312071" id="_toc58312071"></a>

Here is a listing of URLs wherein these organizations have already implemented an _open_ Authority Document request format:

UCF Team: [https://forms.monday.com/forms/0187181278d27e2d5ae8f217f12e82ec](https://forms.monday.com/forms/0187181278d27e2d5ae8f217f12e82ec)

#### Step 1 – searching the library <a href="#_toc58312072" id="_toc58312072"></a>

The first step in adding an Authority Document to the Federated Authority Document Library is to ensure that it _isn’t already in there._ While one might think that having a layout for searching the library would suffice as a lead in, real life has proven otherwise. So we begin the multi-step process of adding an Authority Document to the library through searching. We’ve found that really only two fields are **required** in the process (URL and e-mail address).

![](../../.gitbook/assets/15)

Searching for existing Ads

* **Authority Document Title** – this asks the end user for (as close as they are going to get) the official title of the document they want to add to the library.
* **Common Name** ­– **** this gives them the ability to add the name of the document as they might know it colloquially.
* **URL** – this is _the_ mandatory search field. If they get the other two names wrong when the document is officially added later, a process will be put in place to examine the official title found on the document at _that_ URL and compare it to something that might already be in the library (remember that the same document can be published at different locations, and hence, different URLs). All that matters for _this_ point is to include a valid URL.

#### Step 2 – search results <a href="#_toc58312073" id="_toc58312073"></a>

Once the URL and accompanying information are added to the form, a couple of things could happen, and what is returned will dictate the next steps.

![](../../.gitbook/assets/16)

The Search Results page

**An exact URL match found**

If an _exact_ URL match was found, that will be the only document returned in the list. The layout should include an **Exists** option (like that shown above) to indicate that the document does indeed exist in the library, or is being queued to be mapped into the library.

**An approximation was found**

If there is no _exact_ URL match, but the elastic search has found a couple of _suggestions_, the layout should return that list of suggestions along with a method to select the best fit to continue. Or, if the end user so chooses, they can forego selecting one of the suggestions and continue on with their search criteria.

**Nothing was found**

If the elastic search found _nothing_, that too should be indicated in the layout and the user should continue on with their search criteria.

#### Step 3a – An exact match was found in the library <a href="#_toc58312074" id="_toc58312074"></a>

If an exact match was found, and the document has already been mapped into the library, that information should be returned to the user. We also suggest that the user be shown what _they_ entered as the title and what the actual title is.

![](../../.gitbook/assets/17)

An existing document was found in the library

Giving the user the ability to display the reference card for the Authority Document is a bonus, and that is what is shown here with the **Display** button.

#### Step 3b – A queued document has been selected <a href="#_toc58312075" id="_toc58312075"></a>

This step assumes that the user has found an Authority Document in the mapping queue that was a near approximation of what they searched for, and selected it from the previous screen.

![](../../.gitbook/assets/18)

An existing document was selected in the queue

The only addition here is that the user must add their email address if they want to be notified when the document has been added to the library.

#### Step 3c – This is a new document <a href="#_toc58312076" id="_toc58312076"></a>

If the elastic search found _nothing_, and the URL match found _nothing_, that means that the document doesn’t exist within the library _or_ the queue. It should be added.

![](../../.gitbook/assets/19)

Accepting the document to add to mapping

The only addition here is that the user must add their email address if they want to be notified when the document has been added to the library.

### Further research <a href="#_toc58312077" id="_toc58312077"></a>

For a full list of research sites and documents, consult our Zotero library catalog here:

[https://theucf.info/research/cataloging](https://theucf.info/research/cataloging)

#### Bibliography <a href="#_toc58312078" id="_toc58312078"></a>

“GRCschema.Org Authority Document.” n.d. Accessed December 8, 2020. https://grcschema.org/AuthorityDocument.

“IFLA -- Functional Requirements for Bibliographic Records.” n.d. Accessed December 3, 2020. https://www.ifla.org/publications/functional-requirements-for-bibliographic-records.

“RDA Toolkit.” n.d. Accessed December 8, 2020. https://www.rdatoolkit.org/.

“Resource Description and Access (RDA).” n.d. Accessed December 3, 2020. https://www.librarianshipstudies.com/2017/07/resource-description-and-access-rda.html.

“What’s a Bibliography? - Plagiarism.Org.” n.d. Accessed December 3, 2020. http://www.plagiarism.org/article/whats-a-bibliography.

#### End Notes <a href="#_toc58312079" id="_toc58312079"></a>

1. (“IFLA -- Functional Requirements for Bibliographic Records” n.d.) ↑
2. (“RDA Toolkit” n.d.) ↑
3. (“GRCschema.Org Authority Document” n.d.) ↑
4. “What Is Citation? - Plagiarism.Org.” n.d. Accessed December 3, 2020. http://www.plagiarism.org/article/what-is-citation. ↑
5. (“What’s a Bibliography? - Plagiarism.Org” n.d.) ↑
6. (“IFLA -- Functional Requirements for Bibliographic Records” n.d.) ↑
7. (“Resource Description and Access (RDA)” n.d.) ↑
