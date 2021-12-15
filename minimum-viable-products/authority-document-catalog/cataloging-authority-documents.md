# Cataloging Authority Documents

### Cataloging Authority Documents <a href="#_toc457485760" id="_toc457485760"></a>

What is presented herein is the standard and methodology for a Federated Authority Document Library that is open to all organizations or individuals wishing to

search the library for known Authority Documents;

create and export JSON-LD based lists of Authority Documents found in the library; and

add or maintain records in the library.

A single, vast, Authority Document library is needed for any practitioner within the Governance, Risk, and Compliance space because the number of documents organizations must follow to maintain compliance is growing at a fast pace. Until the establishment of this library, organizations wishing to create a list of documents they had to follow were forced into one of three situations:

1. searching the web’s myriad locations for laws, rules, regulations, etc.;
2. employing a law firm or utilizing multiple legal research tools (which are still inadequate); or
3. looking for documents in the UCF’s Common Controls Hub (which only hosts the documents _that_ team uses).

The Federated Authority Document Library allows content contributions or use from any person or organization. It was created, and is maintained by GRCschema.org, a 501(c)(3) organization with a mission to create, maintain, and promote schemas for structured data within the Governance, Risk, and Compliance universe. The library is not a single URL location. It is a dynamic API driven library that is already located in _many_ locations and can be integrated into organizational websites, GRC tools, databases, and mobile browsers.

Contents

Research and foundation for the structure 3

What is an Authority Document? 4

Statutes (aka Bills or Acts) 5

Regulations 5

Regulatory Directives or Regulatory Guidance 5

Contractual Obligations 5

International and national standards 6

Audit Guidelines 7

Safe Harbors 7

Best practice guidelines 8

Vendor Documentation 8

Organizationally-documented controls 8

Creating a list of Authority Documents _prior to_ the Federated Authority Document Library 10

Searching for Authority Documents and managing lists manually 10

Using paid systems like LexisNexis 11

Introduction to the Federated Authority Document Library 13

The standards surrounding library cataloging 13

The Groups and Entities of cataloging information 13

The full schema for an Authority Document 17

Groups and Entities as a Bibliographic Record display 17

Searching the federated Authority Document Library 20

Adding an Authority Document to the library 22

Existing Request systems 22

Step 1 – searching the library 22

Step 2 – search results 23

Step 3a – An exact match was found in the library 23

Step 3b – A queued document has been selected 24

Step 3c – This is a new document 24

Further research 26

Bibliography 26

End Notes 26

### Research and foundation for the structure <a href="#_toc58312049" id="_toc58312049"></a>

An _immense_ amount of research went into the publication of this content. The research documents for this content can be found at our research library [HERE](https://theucf.info/research/cataloging). The JSON-LD structure for the Federated Authority Document Library is founded upon the Functional Requirements for Bibliographic Records (FRBR)\[1], the Resource Description and Access (RDA) standard\[2], and additional work done by GRCSChema.org in defining the schema for AuthorityDocument\[3]. Additional assistance was provided by three core library and cataloging groups; the ALA, IFLA, and GODORT.

| **ALA**                                                                                                                                                                                                                                                                                                                                                                                                                     | **IFLA**                                                                                                                                                                                                                                                         | **GODORT**                                                                                                                                                                                                                                                 |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![A picture containing text, gauge&#xA;&#xA;Description automatically generated](../../.gitbook/assets/0)                                                                                                                                                                                                                                                                                                                   | ![A picture containing icon&#xA;&#xA;Description automatically generated](<../../.gitbook/assets/1 (1)>)                                                                                                                                                         | ![Logo&#xA;&#xA;Description automatically generated](<../../.gitbook/assets/2 (1)>)                                                                                                                                                                        |
| The American Library Association (ALA) is the oldest and largest library association in the world. Founded on October 6, 1876 during the Centennial Exposition in Philadelphia, the mission of ALA is “to provide leadership for the development, promotion and improvement of library and information services and the profession of librarianship in order to enhance learning and ensure access to information for all.” | The International Federation of Library Associations and Institutions (IFLA) is the leading international body representing the interests of library and information services and their users. It is the global voice of the library and information profession. | The Government Documents Round Table (GODORT) is a dynamic forum where information professionals learn, discuss, advocate, and create scholarship on and about government information at all levels of government (local, state, national, international). |

What we present herein is an open, federated methodology, of cataloging Authority Documents for all members of the Governance, Risk, and Compliance communities. The schemas and methodologies have been adapted from the standards which these organizations have published and abide by.

### What is an Authority Document? <a href="#_toc58312050" id="_toc58312050"></a>

![A picture containing letter

Description automatically generated](<../../.gitbook/assets/3 (1)>)

Our graphic for an Authority Document

When we say that we are “complying”, we are saying that we are complying with authoritative rules that are not of our own creation. These authoritative rules can come in the form of regulations, principles, standards, guidelines, best practices, policies, and procedures. Which is which, and what makes one authoritative body a regulator and another a best practice author? Let’s start with regulations and move on from there.

Statutes, regulations, and directives are rules of law that, if not followed, can result in penalties. Regulations state that something must be done. Regulations are promulgated by governmental agencies to interpret or expand the reach of statutes.

Contractual obligations are just that — contracts that, if not followed, can result in penalties.

Standards are levels of quality or attainment created by organized groups or that are generally accepted within the industry. Standards determine what must be done.

Guidelines are detailed outlines and plans for determining a course of action. Guidelines prioritize and direct the course of action.

Best practices are programs, initiatives, or activities that are considered leading edge, or exceptional models for others to follow. Best practices set the example of how to do something the best way.

So yes, there is a legal hierarchy to the documents that the UCF tracks. We have identified 10 Authority Document types which are listed in their legal hierarchical status below.

1. Statutes (Bills or Acts)
2. Regulations
3. Regulatory Directive or Guidance
4. Contractual Obligation
5. International or National Standard
6. Self-regulatory Body Requirements
7. Audit Guideline
8. Safe Harbor
9. Best Practice Guideline
10. Vendor Documentation
11. Organizational Governance Documents

#### Statutes (aka Bills or Acts) <a href="#_toc457485763" id="_toc457485763"></a>

A statute is an act of federal, state, Parliament, or provincial legislation that declares the law pertaining to a certain subject (e.g., the Income Tax Act, The Canada Corporations Act, the Sarbanes-Oxley Act of 2002). Statutory law is legislatively created law. Administrative agencies adopt statutes as regulations, and lesser bodies adopt them as ordinances.

_Failure to follow laws will get you put in jail or result in penalties._

#### Regulations <a href="#_toc457485764" id="_toc457485764"></a>

To regulate is to bring under _the force of law_ or a _governing authority_. People and businesses are subject to national, regional, and local laws. Traditional regulators are those agencies within the aforementioned levels of government. When governmental agencies create their acts, they are codifying legal documents that resulted from deliberations of their legislative bodies. Often, however, the acts passed by those legislative bodies establish broad principles rather than detailed prescriptions for the behavior of people and companies and delegate to the regulators responsibility for filling in the details and gaps. The regulators are empowered to interpret how the laws are to be implemented and to establish rules for following those laws. Those rules are then documented as **regulations**, such as the “Code of Federal Regulations” that we have in the United States. _Regulations are enforceable by law_.&#x20;

_Failure to follow regulations will result in penalties._

#### Regulatory Directives or Regulatory Guidance <a href="#_toc457485765" id="_toc457485765"></a>

Directives can be legislative acts, such as those of the European Union, or organizational directives, such as those issued by the U.S. White House’s Office of Management and Budget (OMB), which requires those organizations under the issuer’s purview to achieve a particular result without dictating the means of achieving the result. Directives normally leave those entities that follow them with a certain amount of leeway as to the exact rules to be adopted. Some regulators like FDa are empowered to make regulations that impose criminal penalties for non-compliance.

_Directives are only enforceable against and binding for the group they address._

#### Contractual Obligations <a href="#_toc457485766" id="_toc457485766"></a>

There is much confusion between “regulations” promulgated by government regulators as discussed above and the rules, standards, and, yes, “regulations” promulgated by other so-called regulatory bodies and other organizations that can and do emerge to reign in our actions. Variously known as “self-regulatory bodies”, “standards bodies”, or by similar names, these organizations are not part of the government and do not have the force of law behind their requirements, but failure to comply with those requirements may well disqualify an entity from participating in certain businesses. The promulgators of these rules may be industry-based organizations that band together to address a concern that is common to industry members. For example, the credit card companies (Visa, MasterCard, American Express, etc.) have banded together to create the Payment Card Industry Security Standard. The promulgators may be self-appointed watchdog organizations that have gained sufficient acceptance, prominence, and/or moral authority over time and to which people turn to as authorities in the field. For example, the ability to display the BBBOnline and TRUSTe seals in online commerce has achieved this type of prominence, so it makes it worthwhile for businesses to comply with their standards. Certain membership-based organizations promote similar types of rules as a condition of membership. The unifying principle is that they all have something you want and you’re willing to contractually commit to playing by their rules to get it.

We’ll get to the definition of a standard in a moment, but just because something is called a **standard** (it can’t be called a law, act, or regulation, because it does not come from the government), it doesn’t mean that it can be ignored without consequences. Yes, compliance with these types of contractual standards are, legally speaking, optional. If a company is not interested in accepting credit cards as a form of payment, it is not obligated to comply with the PCI standards. However, anyone wanting to accept credit cards is required to contractually agree to comply with the PCI standards. Similarly, anyone wanting to display the BBBOnline seal must contractually agree to follow certain guidelines and processes. Failure to comply with these obligations creates a breach of contract and, depending on the contract terms, may result in a variety of fines and, potentially, the loss of valuable contractual rights — losing the ability to accept credit cards in the case of the PCI standards could have grave consequences for just about any merchant. Losing the right to use the BBBOnline or TRUSTe seals may not have as severe an effect on a merchant as being unable to accept credit cards, but it could drive customers away to competitor sites — particularly if the contractual breach is widely publicized. The payment card industry has already fined a great many organizations and affected the closure of at least one organization that we know of for not properly following its standard. Because the payment card industry can exercise authority over its user body, and that user body is so large, in this instance, they can be compared to regulators, even though they haven’t been given the statutory mandate of a regulator. However, there is one (1) big difference between the payment card industry and true regulators — while the payment card industry may be able to put you out of business, they can’t put you in jail.

_Contractual structures promulgated by self-regulatory bodies are enforceable under contract. Failure to comply carries with it the remedies established by the contract, which may include fines and/or loss of valuable contract rights. Such consequences are enforceable under contract law._

#### International and national standards <a href="#_toc457485767" id="_toc457485767"></a>

We love the origination of the term “standard”. Originally, a standard was a conspicuous object (a tall pole with a banner, flag, or symbol on top) that was used to mark a rallying point in battle. Today, a standard is a criterion or criteria established by an authority (government or industry) that apply to a given situation in order to reach a certain level of quality or attainment. Control models are much the same thing but tend to focus more specifically on certain aspects of implementation. In contrast to the original definition, a standard today comes into existence _because_ people rally around it, rather than the other way around. International standards and control models are consensus models that are generally accepted by the user community (or at least by the community creating the standard), such as the “Control Objectives for Information Technology” created by Information Systems Audit and Control Association (a control model) or the International Organization for Standardization’s (ISO) various standards, such as its “ISO 27001-2005 Information Security Management Standard”.

Formal international standards begin as draft documents, which are then published as a Request for Comments (RFC) document. As these RFCs mature through the editing process, they become proposed standards, draft standards, and, ultimately, the final published standard.

Is your organization _required_  to follow any given standard? Not if the standard’s author isn’t a regulator or a body with contractual authority over it — meaning that the standard’s authors can’t _force_ your organization to use their standard under threat of legal action or penalty. Some might think de facto standards must be followed, but that isn’t true.

_Standards are not enforceable by law_. _However, failure to follow standards may result in actions contrary to regulations, which **are** enforceable by law_.

#### Audit Guidelines <a href="#_toc457485768" id="_toc457485768"></a>

In the world of regulatory compliance for information services, the CobiT audit standard comes pretty close to being _the_ de facto standard. We’ve seen presentations in which the speaker mistakenly told the audience that this or that regulation _called for_ the use of CobiT as the measuring stick against which they must judge whether they were following the regulation. That just isn’t so. There isn’t a single regulation that mandates the use of CobiT. However, the Sarbanes-Oxley Act did create the Public Company Accounting Oversight Board, which created and mandates the use of its own auditing standards. The Payment Card Industry Association also mandates the use of its PCI-DSS standard as the audit standard that must be followed when proving that you’ve met their guidelines.

Other Audit Guidelines, like those published by the Payment Card Industry Data Security Standards Council derive their authority from the Contractual Obligations that call for the organization to follow not only the guidelines set forth by the council, but their audit guides as well.

Finally, there are other audit guidelines that are inherent and are also safe harbors (more on that below), such as the Secure Technical Implementation Guides that define configuration standards for systems _and_ can be used as Audit Guidelines.

_Failure to pass an audit brings with it “audit items” and other modes of enforcement that are only as strong as the standard, contractual obligation, regulatory guidance, or regulation that calls for the audit._

#### Safe Harbors <a href="#_toc457485769" id="_toc457485769"></a>

Nothing muddies the waters more than a good “safe harbor”. While a safe harbor is intended to make laws and regulations easier to follow, oftentimes the safe harbor is used by consultants, speakers, and other well-meaning (or not so well-meaning) folks to support their position that a particular standard, guideline, procedure, or control is required under the law and that failure to adopt that particular standard, guideline, procedure, or control will subject the organization to legal action. Nothing could be further from the truth.

Now, what’s its real purpose? A safe harbor in a law or regulation is a shortcut used by the regulators to ensure that the majority of people are in compliance with the law without requiring an in-depth analysis of each particular case. Thus, the safe harbor provides that _if_ you take the steps required to be within the safe harbor, _then_ you will (more or less) automatically be in compliance with that particular aspect of the law or regulation. However, the converse is not true – if you do _not_ fall within the safe harbor, that does not necessarily mean that you are not in compliance with the law. What it does mean is that you will have to show that the steps you chose to take are also in compliance with the law.

Let’s use our previously mentioned CobiT standard as an illustration. Suppose that some regulator enacted a regulation requiring that certain types of organizations conduct annual audits of their information services systems that adhere to auditing standards that are reasonable and customary in the industry. Suppose further that our helpful regulators add a statement along the lines of “The CobiT audit standards are reasonable and customary standards in the industry.” This safe harbor offers organizations the opportunity to reduce compliance risk by adopting the CobiT audit standards. However, there are many reasons why the CobiT standards are inappropriate for the particular organization — cost, complexity, etc., so its use may simply not be warranted. Is the organization bound to use CobiT anyway? (If you’ve read this far, you probably already know the answer.) The answer, of course, is no — the organization is free to use whatever auditing standard it chooses, provided that it meets the two-prong test of “reasonable” and “customary in the industry”. However, if the organization chooses to use a standard other than CobiT, and the regulator doesn’t like it, the organization will have an uphill battle to convince the regulator (and, perhaps ultimately, the court) that the chosen standard is reasonable and customary. Safe harbors tend to be very conservative and avoid gray areas.

_If a safe harbor is available, it’s always good to know. However, the needs of the organization may dictate that it leave the safe harbor and enter riskier waters._

#### Best practice guidelines <a href="#_toc457485770" id="_toc457485770"></a>

Best practices are leading edge models of methods or actions for others to follow. These are combinations of activities, processes, policies, or procedures that document the _best_ _possible_ way of doing something.

_Are they enforceable? Nope_. As a matter of fact, many times they aren’t even _desirable_ — in their fullest sense, the “best” way to do something is often also the costliest. Too many times we’ve seen people spending $1,000 to fix a $100 problem by using an industry “best practice”. Best practices must always be viewed in context and adapted to the particular situation.

#### Vendor Documentation <a href="#_toc457485771" id="_toc457485771"></a>

More and more, vendors are being called on to “bake in” security measures when building out their systems. For example, it is the foundation of the US’ FDA’s Postmarket Management of Cybersecurity in Medical Devices regulatory guidance. Because of that, vendors following the FDA’s guidance and posting vendor documentation on how to secure their systems can elevate the standing of their security documentation to one level higher as a safe harbor. Vendors have a great deal to say about configuration guidance in the form of Secure Technical Implementation Guides, and the UCF team tracks these for you at STIGViewer.com.

_In and of themselves, vendor documentation is usually treated as a form of a best practice, or minimum standard of due care. Vendor documentation following regulatory guidance is treated with the same accord as a safe harbor._

#### Organizationally-documented controls <a href="#_toc457485772" id="_toc457485772"></a>

Organizationally-documented controls (especially compliance controls) are the activities that are created from and are carried out by policies, standards, procedures, and practices designed to provide reasonable assurance that certain business objectives will be achieved, and undesired events will be prevented or detected. These control activities help to ensure that management directives are carried out by providing a description of what physical-, software-, procedural-, or people-related conditions must be met or be in existence in order to satisfy a core requirement.

_Following properly structured and validated organizational controls that align with mandates that have to be followed is **the** essential prerequisite to compliance, and failure to follow controls will directly lead to whatever fines or penalties the regulatory body can impose._

### Creating a list of Authority Documents _prior to_ the Federated Authority Document Library <a href="#_toc52638586" id="_toc52638586"></a>

Now that we know what we must comply with, we have to turn our attention to creating that _list_ of Authority Documents that we are complying with. We must both create the list and _share_ the list within the organization so that everyone knows which documents are on the _must_ comply with, and which documents are on the _we should_ comply with.

Your list of Authority Documents should have the following capabilities:

*
  * It should be updateable by everyone in the team that needs to contribute;
  * It should have the capability to be displayed on your intranet or distributed within your organization; and
  * Ultimately each Authority Document should be linked directly to that document’s Citations so that you can examine the text.

There are three ways you can establish and maintain your lists of Authority Documents you need to comply with:

1\. Search for them yourself and create a way to publish that list internally (even if it’s a simple Word document);

2\. Use paid systems like LexisNexis, Thomson Reuters, Westlaw, Loislaw, etc.,; or

3\. Use the Federated Authority Document library.

#### Searching for Authority Documents and managing lists manually <a href="#_toc58312062" id="_toc58312062"></a>

So what happens when you try to search for something like the General Data Protection Regulation, known to most people within the compliance world as GDPR? You get over _400 million results_.

![A screenshot of a cell phone

Description automatically generated](../../.gitbook/assets/4)

Google response list is **huge**

**IF** you knew that GDPR stands for _General Data Protection Regulation_, that narrows the results down to around _20 million_. And if you look at the 1st through 10th pages of Google and try linking to the **official** text, you’ll get companies like Intersoft Consulting listing the text.

![A screenshot of a social media post

Description automatically generated](../../.gitbook/assets/5)

And a Google research list contains crap, like this

This is, by far, the _worst_ way of doing this. It isn’t even the cheapest (as the Federated Authority Document library is free), but some folks are stubborn, and they want to re-invent the wheel. If this is what you want to do, you should first test your search skills. The UCF team have created an insanely short quiz and posted it online for free for anyone who wants to try their hand at searching for Authority Documents. The quiz is free and can be found online [HERE](https://edu.unifiedcompliance.com/courses/).

![Text

Description automatically generated](<../../.gitbook/assets/6 (1)>)

Authority Document Search capabilities quiz

Most people find that they fail miserably at the searching part and don’t even get to the managing and distributing the list part.

#### Using paid systems like LexisNexis <a href="#_toc58312063" id="_toc58312063"></a>

If you are a legal firm, undoubtedly you have access to such online legal research sites as Westlaw, LexisNexis, Casetext, RossIntelligence, and others. Those are pricey. **Westlaw** suggests that the average cost is around $99 per **search**, which **price** includes all the documents _clicked on_ during the search. Even then, those specialized libraries only have statutes and regulations or court cases. And some of them, such as the Ross Intelligence library, only has US Federal and State statutes and regulations. LexisNexis is able to do this for you and so much more because it is a powerhouse of public information. Over 37 billion records are contained in the database and it just continues to grow! However, it _is_ expensive. There are some other less expensive alternatives you can turn to.

**FactSet**

If you want even more specificity in your niche for your research and you have financial needs, then FactSet is a great service to consider. FactSect can be found [HERE](https://www.factset.com).

**Thomson Reuters**

Thomson Reuters is very much like LexisNexis, with focuses on healthcare, finance, and science sectors. They can be found [HERE](https://thomsonreuters.com).

**Westlaw**

It’s primarily for lawyers and covers 40k databases, but anyone who needs legal advice or help can benefit from this system. They can be found [HERE](https://web2.westlaw.com).

**Loislaw**

Covering the law libraries of all US state and federal jurisdictions, this legal database also offers a citation service that summarizes all sources in the database that cite documents and provides hyperlinks to those sources. They can be found [HERE](https://loislaw.com).

\-----------------------------------------------------------------------------------------------------------------------------------------------

The problem with the five of these choices is that they don’t also include international standards, Secure Technical Implementation Guides, etc. Therefore, each organization needs to create and maintain _its own_ catalog of Authority Documents they need to comply with.

### Introduction to the Federated Authority Document Library <a href="#_toc58312064" id="_toc58312064"></a>

Everyone who has gone to high school and college has written at least _one_ paper where they’ve had to cite where the information was drawn from. These are called _citations_ and you’ll see at the bottom of the page how this citation (a citation about what a citation is) is formed\[4]. If you are going to create policies, standards, procedures, audit questions, etc., _based on external rules and regulations_, you are going to need to cite where you’ve drawn your information from. In other words, “this policy for XYZ is based on these portions of these rules we have to follow”.

The list of documents, or sources, you’ve used is called a _bibliography\[5]_ when you add it to the documents where you’ve created your citations (this document has a _huge_ bibliography). That’s great on a _per document_ basis – it gives you one place to look for all of your references. But it doesn’t help much when you have _many_ documents with _different_ sources in them. That’s when you need to create a catalog of all of the sources for all of your bibliographies. This single catalog will ensure that your list has been deduplicated. It’s called by various names:

* library catalog
* resource catalog
* authority document catalog

We’ll just refer to all of these as the **catalog**. Each record in the catalog is officially called a **bibliographic record** or **work** as it is officially called.

We say _officially called_ because there are standards upon which modern library catalogs (including the federated catalog described here) are built and maintained.

#### The standards surrounding library cataloging <a href="#_toc58312065" id="_toc58312065"></a>

From 1992-1995 the International Federation of Library Associations and Institutions (IFLA) Study Group on Functional Requirements for Bibliographic Records (FRBR) developed an entity-relationship model as a generalized view of the bibliographic universe, intended to be independent of any cataloging code or implementation\[6]. In 2008 the Resource Description and Access (RDA) standard was released, based upon FRBR. RDA is a suite of data elements, guidelines, and instructions for creating library metadata that are well-formed according to international models for user-focused linked data applications\[7]. It is this standard we are applying to Authority Document cataloging.

#### The Groups and Entities of cataloging information <a href="#_toc58312066" id="_toc58312066"></a>

Cataloging a bibliographic record, according to FRBR and RDA, is broken down into 3 Groups of data Entities (as they call them).

1. Products of intellectual endeavor.
2. Those responsible for the intellectual content, the physical production, the dissemination, and the custodianship of the Group 1 Entities.
3. The subjects of intellectual endeavor.

**Group 1 Entities**

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

![Graphical user interface, application

Description automatically generated](../../.gitbook/assets/7)

The download URLs then become individual _items_. This is important, because the _same manifestation_ of a document could easily be posted to multiple websites, ebook publishers, etc.

**Group 1 Work and Expression entities as JSON objects**

There are very few entities we need to track at the _work_ level.

| **Property**       | **Expected Type** | **Description**                                           |
| ------------------ | ----------------- | --------------------------------------------------------- |
| title              | String            | The title for the item.                                   |
| subtitle           | String            | The subtitle of the document.                             |
| CommonNames        | Thing             | A collection of variant names for the title and subtitle. |
| published\_version | String            | The published version of the document.                    |
| effective\_date    | Date              | The effective date of the document.                       |
| epub\_type         | String            | The type of electronic publication this was found in.     |

**Group 1 Manifestation and Item entities as JSON objects**

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

**Group 2 Entities**

Group 2 entities describe the _who_ surrounding the intellectual content. Who:

* are the authors
* are the editors
* are the publishers/promulgators
* are subsequential hosting websites where the documents can be found

Notice in the above, that the _who_ can be a person or an organization.

**Group 2 Entities as JSON objects**

Following information about the _work_ through _item_, we need to add the _who_ surrounding the intellectual content:

| **Property**                                  | **Expected Type** | **Description**                                                                          |
| --------------------------------------------- | ----------------- | ---------------------------------------------------------------------------------------- |
| Authors                                       | Thing             | A collection of Authors.                                                                 |
| Editors                                       | Thing             | A collection of Editor.                                                                  |
| publisher\_promulgator\_organizations\_id\_fk | Integer           | The publisher id of the document or in the case of laws the promulgator of the document. |
| website\_publisher                            | String            | The website publisher's name the document was found on.                                  |

**Group 3 Entities**

Group 3 entities give us the subjects of the intellectual content, such as the concepts, hierarchical information, etc.

| **Property**         | **Expected Type** | **Description**                                                                                                          |
| -------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------ |
| HierarchicalMetaData | Thing             | MetaData about a JSON Type's hierarchical information. If the record is in a non-hierarchical array this will be nulled. |
| SubjectMattersStubs  | Thing             | A collection of Stub for Subject Matters.                                                                                |

#### The full schema for an Authority Document <a href="#_toc58312067" id="_toc58312067"></a>

The full schema for an Authority Document comprises 8 core tables as shown in the ERD diagram below. While the schema is _more or less_ locked, the RDA standard is still evolving and the schema with it. Therefore, the full schema’s documentation will only be maintained online at GRCschema.org [HERE](https://grcschema.org/AuthorityDocument).

![](<../../.gitbook/assets/8 (1)>)

ERD Diagram for an Authority Document record

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

#### Groups and Entities as a Bibliographic Record display <a href="#_toc58312068" id="_toc58312068"></a>

It is one thing to discuss a bibliographic record in the abstract, and something different to _see it_ as a record being displayed. We will cover where the data originates from for each of the four areas shown below.

![](../../.gitbook/assets/9)

Bibliographic Record display

**1 – Work and Expression entities**

These objects are drawn from the **work** and **expression** entities in Group 1. Notice that Common Name (variant name in RDA) is displayed as an array. That’s because documents can have multiple Common Names. In the data structure, this is a linked sub table. As such, there only needs to be one entry per document, except for Common Names.

The example below shows how this information is filled out for a single document, _Protecting Controlled Unclassified Information in Nonfederal Information Systems and Organizations, NIST Special Publication 800-171, Revision 2_, written by a team at the National Institute of Standards and Technology.

![A picture containing table

Description automatically generated](../../.gitbook/assets/10)

NIST SP 800-171 Work and Expression entities

Notice that the Common Names entity is displayed as an array.

**2 – Agents entities**

These objects are drawn from the **agent** entities in Group 2. Because both authors and editors can be lists, these are maintained as linked sub tables and displayed as arrays.

![A picture containing table

Description automatically generated](../../.gitbook/assets/11)

NIST SP 800-171 Agents entities

**3 – Item and manifestation entities**

These objects are drawn from the **item** and **manifestation** entities in Group 1. The _entire collection_ of this information is displayed as an array and structured as a linked sub table because, as we already know, there can be multiple manifestations and items (especially published locations for the same document) tracked for each work. In the example below we have expanded this to show both published locations for this document (NIST and at DOI.org).

![Text, table

Description automatically generated](../../.gitbook/assets/12)

NIST SP 800-171 Item and Manifestation entities

**4 – Mapped Version entities**

These objects are drawn from the **manifestation** entities in Group 1. Mapped Version information is specific to the federated mapping schema and details which organizations have created a manifestation of a work by mapping the contents of that work. We have not expanded this example because the database doesn’t currently have multiple mapped versions.

![A picture containing table

Description automatically generated](../../.gitbook/assets/13)

NIST SP 800-171 Mapped Version entities

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
