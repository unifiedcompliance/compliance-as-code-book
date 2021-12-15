# Introduction to the Federated Authority Document Library



Everyone who has gone to high school and college has written at least _one_ paper where they’ve had to cite where the information was drawn from. These are called _citations_ and you’ll see at the bottom of the page how this citation (a citation about what a citation is) is formed1. If you are going to create policies, standards, procedures, audit questions, etc., _based on external rules and regulations_, you are going to need to cite where you’ve drawn your information from. In other words, “this policy for XYZ is based on these portions of these rules we have to follow”.

The list of documents, or sources, you’ve used is called a _bibliography2_ when you add it to the documents where you’ve created your citations (this document has a _huge_ bibliography). That’s great on a _per document_ basis – it gives you one place to look for all of your references. But it doesn’t help much when you have _many_ documents with _different_ sources in them. That’s when you need to create a catalog of all of the sources for all of your bibliographies. This single catalog will ensure that your list has been deduplicated. It’s called by various names:

* library catalog
* resource catalog
* authority document catalog

We’ll just refer to all of these as the **catalog**. Each record in the catalog is officially called a **bibliographic record** or **work** as it is officially called.

We say _officially called_ because there are standards upon which modern library catalogs (including the federated catalog described here) are built and maintained.

## The standards surrounding library cataloging

From 1992-1995 the International Federation of Library Associations and Institutions (IFLA) Study Group on Functional Requirements for Bibliographic Records (FRBR) developed an entity-relationship model as a generalized view of the bibliographic universe, intended to be independent of any cataloging code or implementation3. In 2008 the Resource Description and Access (RDA) standard was released, based upon FRBR. RDA is a suite of data elements, guidelines, and instructions for creating library metadata that are well-formed according to international models for user-focused linked data applications4. It is this standard we are applying to Authority Document cataloging.

## The Groups and Entities of cataloging information

Cataloging a bibliographic record, according to FRBR and RDA, is broken down into 3 Groups of data Entities (as they call them).

1. Products of intellectual endeavor.
2. Those responsible for the intellectual content, the physical production, the dissemination, and the custodianship of the Group 1 Entities.
3. The subjects of intellectual endeavor.

### Group 1 Entities

As stated above, Group 1 Entities describe the _what_, the products. Within this group, the FRBR and RDA break down the _what_ into four different entities, from most abstract to most concrete.

| **Term**       | **Definition**                                                                                                                                                                  | **Example**                                                                                                                                                                                                                                                                                                                                                                            |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Works          | Works are the distinct intellectual creation of something. A law; a standard; an Audit Guide; a Secure Technical Implementation Guide _in general._                             | _NIST 800-53 Rev 5 (as something the folks that wrote/edited it worked on)_                                                                                                                                                                                                                                                                                                            |
| Expressions    | The intellectual or artistic realization of a work in the form of alpha-numeric (written in letters and numbers), sound, image, object, etc., or any combination of such forms. | <p><em>NIST 800-53 Rev 5 NIST OLIR mapping</em><br><em>NIST 800-53 Rev 5 UCF mapping</em></p><p><em>NIST 800-53 Rev 5 OSCAL format</em></p>                                                                                                                                                                                                                                            |
| Manifestations | The physical or electronic embodiment of an expression of a work.                                                                                                               | <p><em>NIST 800-53 Rev 5 PDF format</em></p><p><em>NIST 800-53 Rev 5 Excel format</em><br><em>NIST 800-53 Rev 5 OSCAL JSON format</em></p><p><em>NIST 800-53 Rev 5 OSCAL xml format</em></p><p><em>NIST 800-53 Rev 5 OSCAL yaml format</em></p><p><em>NIST 800-53 Rev 5 UCF AD In-depth Report</em></p><p><em>NIST 800-53 Rev 5 to CIS Benchmark Derived Relationship Mapping</em></p> |
| Item           | A single exemplar of a manifestation of a work.                                                                                                                                 | The copy of the above that _you_ _can download_ on _your_ computer.                                                                                                                                                                                                                                                                                                                    |

Think of it this way – _works_ are realized through _expressions_ that are embodied in _manifestations_. When you write something, you might have multiple copies of your _work_. When you finalize it, you have a copy as an _expression_. You then post that for sale or free download, **in a certain format**, as a _manifestation._ The individual files that get copied to everyone’s computers are _items_.

The difference here between _works_ and _expressions_ can come in what gets _added to_ a work, or _how it is interpreted_. In our instance, the NIST 800-53 Rev 5 document has two mapping _expressions_ with one done by NIST itself through the OLIR process, the other by the UCF team in their way. Expressions can almost be thought of as interpretations.

The difference between _expression_ and _manifestation_ is the output format. If you were to peruse the NIST OSCAL website, you can see that there are several manifestations of the OSCAL version as shown below.

![OSCAL GitBook Repository](https://www.complianceascode.net/wp-content/uploads/2021/12/NISTOSCAL.png)

The download URLs then become individual _items_. This is important, because the _same manifestation_ of a document could easily be posted to multiple websites, ebook publishers, etc.

### **Group 1 Work and Expression entities as JSON objects**

There are very few entities we need to track at the _work_ level.

| **Property**       | **Expected Type** | **Description**                                           |
| ------------------ | ----------------- | --------------------------------------------------------- |
| title              | String            | The title for the item.                                   |
| subtitle           | String            | The subtitle of the document.                             |
| CommonNames        | Thing             | A collection of variant names for the title and subtitle. |
| published\_version | String            | The published version of the document.                    |
| effective\_date    | Date              | The effective date of the document.                       |
| epub\_type         | String            | The type of electronic publication this was found in.     |

### Group 1 Manifestation and Item entities as JSON objects

When recording a _manifestation_ and _Item_, we need to add to the above, the following information, specifying specific information about the intellectual property and where it can be obtained:

| **Property**        | **Expected Type** | **Description**                                                                         |
| ------------------- | ----------------- | --------------------------------------------------------------------------------------- |
| chapter             | String            | The chapter of the item.                                                                |
| citation\_format    | String            | The Authority Document citation format.                                                 |
| pages               | Integer           | The total number of pages in the document.                                              |
| section             | String            | The section of the item.                                                                |
| series              | String            | Series information for the item.                                                        |
| subchapter          | String            | The sub-chapter of the item.                                                            |
| availability        | String            | The Authority Document availability.                                                    |
| blog\_title         | String            | The title of the blog the document was found on.                                        |
| database            | String            | The database that houses the record.                                                    |
| date\_accessed      | String            | The date the record was last accessed.                                                  |
| doi                 | String            | The Digital Object Identifier record locator.                                           |
| epub\_type          | String            | The type of electronic publication this was found in.                                   |
| id                  | Integer           | A unique and persistent identifier for the record.                                      |
| isbn                | String            | The ISBN number for the record.                                                         |
| periodical\_title   | String            | The title of the periodical that the document was found in.                             |
| publication\_place  | String            | Where the document was published if that is known.                                      |
| published\_date     | Date              | The date the document was published or promulgated.                                     |
| search\_information | String            | This is database search information for finding the record.                             |
| url                 | URL               | The Uniform Resource Locator of an internet address.                                    |
| uuid                | String            | The Unique ID of the record in a database system.                                       |
| volume\_issue       | String            | The volume or issue identifier of the periodical that the document was found in.        |
| website\_title      | String            | The title of the website itself and not to be confused with the title of the publisher. |

### Group 2 Entities

Group 2 entities describe the _who_ surrounding the intellectual content. Who:

* are the authors
* are the editors
* are the publishers/promulgators
* are subsequential hosting websites where the documents can be found

Notice in the above, that the _who_ can be a person or an organization.

#### Group 2 Entities as JSON objects

Following information about the _work_ through _item_, we need to add the _who_ surrounding the intellectual content:

| **Property**                                  | **Expected Type** | **Description**                                                                          |
| --------------------------------------------- | ----------------- | ---------------------------------------------------------------------------------------- |
| Authors                                       | Thing             | A collection of Authors.                                                                 |
| Editors                                       | Thing             | A collection of Editor.                                                                  |
| publisher\_promulgator\_organizations\_id\_fk | Integer           | The publisher id of the document or in the case of laws the promulgator of the document. |
| website\_publisher                            | String            | The website publisher's name the document was found on.                                  |

### Group 3 Entities

Group 3 entities give us the subjects of the intellectual content, such as the concepts, hierarchical information, etc.

| **Property**         | **Expected Type** | **Description**                                                                                                          |
| -------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------ |
| HierarchicalMetaData | Thing             | MetaData about a JSON Type's hierarchical information. If the record is in a non-hierarchical array this will be nulled. |
| SubjectMattersStubs  | Thing             | A collection of Stub for Subject Matters.                                                                                |

## References

***

1.  “What Is Citation? - Plagiarism.Org.” n.d. Accessed December 3, 2020. [http://www.plagiarism.org/article/what-is-citation](http://www.plagiarism.org/article/what-is-citation).

    “What’s a Bibliography? - Plagiarism.Org.” n.d. Accessed December 3, 2020. [http://www.plagiarism.org/article/whats-a-bibliography](http://www.plagiarism.org/article/whats-a-bibliography). ↩︎
2.  “IFLA -- Functional Requirements for Bibliographic Records.” n.d. Accessed December 3, 2020. [https://www.ifla.org/publications/functional-requirements-for-bibliographic-records](https://www.ifla.org/publications/functional-requirements-for-bibliographic-records).

    “IFLA -- Multilingual Dictionary of Cataloguing Terms and Concepts (MulDiCat).” n.d. Accessed December 3, 2020. [https://www.ifla.org/publications/multilingual-dictionary-of-cataloguing-terms-and-concepts-muldicat](https://www.ifla.org/publications/multilingual-dictionary-of-cataloguing-terms-and-concepts-muldicat). ↩︎
3.  “IFLA -- Functional Requirements for Bibliographic Records.” n.d. Accessed December 3, 2020. [https://www.ifla.org/publications/functional-requirements-for-bibliographic-records](https://www.ifla.org/publications/functional-requirements-for-bibliographic-records).

    “IFLA -- Multilingual Dictionary of Cataloguing Terms and Concepts (MulDiCat).” n.d. Accessed December 3, 2020. [https://www.ifla.org/publications/multilingual-dictionary-of-cataloguing-terms-and-concepts-muldicat](https://www.ifla.org/publications/multilingual-dictionary-of-cataloguing-terms-and-concepts-muldicat). ↩︎
4.  “Resource Description and Access (RDA).” n.d. Accessed December 3, 2020. [https://www.librarianshipstudies.com/2017/07/resource-description-and-access-rda.html](https://www.librarianshipstudies.com/2017/07/resource-description-and-access-rda.html).

    “Resource Description and Access (RDA): Information and Resources in Preparation for RDA (Aquisitions and Bibliographic Control, Library of Congress).” n.d. Accessed November 16, 2020. [https://www.loc.gov/aba/rda/index.html](https://www.loc.gov/aba/rda/index.html). ↩︎
