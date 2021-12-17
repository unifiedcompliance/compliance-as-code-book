# Wireframes

The wireframes for Authority Documents are listed here. The assumption is that this MVP is built upon the Core Account MVP that already has the flows and structures for establishing an account and connecting the account to the Compliance as Code API gateway.

## Landing Page

![Landing Page](https://www.complianceascode.net/wp-content/uploads/2021/12/Basic-AD-Navigation.png)

1. Account information can be accessed by clicking the cog in the bottom left of the main navigation pane.
2. The icon for the main navigation will be the design icon.
3. Basic information for the landing page will be presented, along with a link to the documentation for the MVP.

![Landing Page with navigation open](https://www.complianceascode.net/wp-content/uploads/2021/12/Expanded-AD-Navigation.png)

1. When opened, the main navigation will show two sub pages - the Library and the Workspace.

## Searching the federated Authority Document Library

Below is a mockup of the Federated Authority Document library. We provide this mockup instead of actual in-use products because each product can be designed slightly different as, again, this is a collaborative effort based on _suggested_ layouts.

There are online repositories of layouts (and the code to build them) in both React and VUE.js. Those libraries are listed here:

**React Demo**: [https://developer.unifiedcompliance.com/demo/react/](https://developer.unifiedcompliance.com/demo/react/)

**React Code:** [https://github.com/unifiedcompliance/demo-react-authdoc-list](https://github.com/unifiedcompliance/demo-react-authdoc-list)

**Vue.js Demo:** [https://developer.unifiedcompliance.com/demo/vue/](https://developer.unifiedcompliance.com/demo/vue/)

**Vue.js Code:** [https://github.com/unifiedcompliance/demo-vue-authdoc-list](https://github.com/unifiedcompliance/demo-vue-authdoc-list)

![Federated Authority Document Library search window](https://www.complianceascode.net/wp-content/uploads/2021/12/Authority-Document-Search-Window.png)

1. Probably the easiest way to find an Authority Document is to type the name and version number into the search field – even a partial name or version number brings up results. You don’t have to worry about getting the name absolutely correct either. Searching for NIST CSF will bring up the correct document, even though that’s not its official name. Current search and filter capabilities in the demo include
   * Official Name (title, subtitle, etc.)
   * Common Name
   * Subject Matter
   * Author or Editor
2. Or, you can get a list of Authority Documents by their Geography by clicking the Geography button or Subject Matter by clicking _that_ button.
3. The found Authority Documents will show up in the left pane in a hierarchical manner. Disclosure triangles are used to the point wherein an Authority Document is shown. The Authority Document will have a document icon in front of the name, and the name that will be displayed is the Official Name.
4. Each Authority Document in the list will have an (i) **information** button. Clicking that button will bring up the Authority Document’s card as a dialog.
5. Each Authority Documenting the list will have a checkbox next to it to include (or remove) it from the current list selection. Once checked, the Authority Document will appear in the **Selected List** pane.
6. An Authority Document can be removed from that list by checking the **Remove** button in the Selected List pane.
7. The Save List button allows the user to save the list of found Authority Documents to their device as a JSON file, or if they are using one of the Mapping tools, the Common Controls Hub, etc., save it to their workspace.

### Traversing by Geography or Subject Matter

![Authority Document Geography traversal](https://www.complianceascode.net/wp-content/uploads/2021/12/Authority-Document-Geography-View.png)

A more advanced method to search would be to click Subject Matter and then click a checkbox for a Subject Matter area of compliance. The Impact Zones and related Common Controls populate on the right side of the page. Then click Geography, and you will be able to see the coverage the UCF has in those displayed countries. Additionally, you can unselect any countries that aren’t relevant to your organization.

![Authority Document Subject Matter traversal](https://www.complianceascode.net/wp-content/uploads/2021/12/Authority-Document-Subject-View.png)

Alternatively, you could reverse that process and start by clicking Geography and click the checkboxes of the countries your organization must comply with. The Impact Zones with Common Controls will populate on the right side of the page. Then click Subject Matter, and you can disable or uncheck categories or areas of compliance that aren’t relevant to your company.
