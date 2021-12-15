# Schema

The full schema for an Authority Document comprises 8 core tables as shown in the ERD diagram below. While the schema is _more or less_ locked, the RDA standard is still evolving and the schema with it. Therefore, the full schema’s documentation will only be maintained online at GRCschema.org [HERE](https://grcschema.org/AuthorityDocument).

![ERD Diagram for an Authority Document record](<../../.gitbook/assets/8 (1)>)

For the purposes of this document, we will describe each of the tables presented above as those will not change.

| **JSON-LD Thing**  | **Description**                                                                                                                                                                           | **Reference**                                     |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| AuthorityDocument  | This is the primary table and includes all Group 1 entities. Each Authority Document is a single record.                                                                                  | [Link](https://grcschema.org/AuthorityDocument)   |
| CommonNames        | This is an array of all name variants for the Authority Document.                                                                                                                         | [Link](https://grcschema.org/CommonNames)         |
| Authors            | This is the list of authors or single author, presented as an array.                                                                                                                      | [Link](https://grcschema.org/Authors)             |
| Editors            | This is the list of editors or single editor, presented as an array.                                                                                                                      | [Link](https://grcschema.org/Editors)             |
| ADIdentifiers      | This is the array of Group 2 Entities for publishing locations.                                                                                                                           | [Link](https://grcschema.org/ADIdentifiers)       |
| SubjectMatterStubs | This is the array of Group 3 Entities for the Authority Document                                                                                                                          | [Link](https://grcschema.org/SubjectMattersStubs) |
| ADMappings         | This is a derivation of FRBR and RDA and describes the access point for a tagged version of the Authority Document’s Citations and/or a mapping those Citations to a reference framework. | [Link](https://grcschema.org/ADMappings)          |
| Members            | This describes the individuals and organizations responsible for the tagging and mapping described above.                                                                                 | [Link](https://grcschema.org/Members)             |

## Groups and Entities as a Bibliographic Record display <a href="#_toc58312068" id="_toc58312068"></a>

It is one thing to discuss a bibliographic record in the abstract, and something different to _see it_ as a record being displayed. We will cover where the data originates from for each of the four areas shown below.

![Bibliographic Record display](../../.gitbook/assets/9)

### **1 – Work and Expression entities**

These objects are drawn from the **work** and **expression** entities in Group 1. Notice that Common Name (variant name in RDA) is displayed as an array. That’s because documents can have multiple Common Names. In the data structure, this is a linked sub table. As such, there only needs to be one entry per document, except for Common Names.

The example below shows how this information is filled out for a single document, _Protecting Controlled Unclassified Information in Nonfederal Information Systems and Organizations, NIST Special Publication 800-171, Revision 2_, written by a team at the National Institute of Standards and Technology.

![NIST SP 800-171 Work and Expression entities](../../.gitbook/assets/10)

Notice that the Common Names entity is displayed as an array.

### **2 – Agents entities**

These objects are drawn from the **agent** entities in Group 2. Because both authors and editors can be lists, these are maintained as linked sub tables and displayed as arrays.

![NIST SP 800-171 Agents entities](../../.gitbook/assets/11)

### **3 – Item and manifestation entities**

These objects are drawn from the **item** and **manifestation** entities in Group 1. The _entire collection_ of this information is displayed as an array and structured as a linked sub table because, as we already know, there can be multiple manifestations and items (especially published locations for the same document) tracked for each work. In the example below we have expanded this to show both published locations for this document (NIST and at DOI.org).

![NIST SP 800-171 Item and Manifestation entities](../../.gitbook/assets/12)

### **4 – Mapped Version entities**

These objects are drawn from the **manifestation** entities in Group 1. Mapped Version information is specific to the federated mapping schema and details which organizations have created a manifestation of a work by mapping the contents of that work. We have not expanded this example because the database doesn’t currently have multiple mapped versions.

![NIST SP 800-171 Mapped Version entities](../../.gitbook/assets/13)

