# The importance of Federated Linked Data to Compliance as Code

## The importance of Federated Linked Data to Compliance as Code

As described in “A quick visual explanation of Compliance as Code”, Compliance as Code is a part of an ecosystem and data flow that ends with delivering content to the end user \(shown below left\) and begins with a JSON schema \(shown below right\).

![Graphical user interface, application

Description automatically generated](../.gitbook/assets/0%20%283%29.png)

Compliance as Code data flow

Notice in the diagram above that we show _multiple_ API gateways and applications. We’ve done this, as you’ll quickly learn, because the world of Compliance as Code normally involves drawing data from multiple locations when creating many of the output files we use.

To explain, let’s continue our discussion with a real-world scenario. Let’s say that you want to build some form of jobs-related application.

![My Jobs App](../.gitbook/assets/1%20%281%29.png)

You could either build the application using all of your own research and data or reach out through the Internet and connect to existing data from external sources.

![My Jobs App drawing in data](../.gitbook/assets/2%20%281%29.png)

If you build it without connecting to any external data, you can ensure data integrity, but you’ll miss out on a vast array of information others have created.

If you pull in external data, you’ll become somewhat dependent upon continually updating that external data. In addition, if you don’t have an agreement to share your updates with those data providers, you might be overwriting some of your own changes if their structures change.

In this day and age of interconnected data, why not cooperate and coordinate your data?

### What is a Federated _anything_?

There is some merit to the argument that in this day and age of interconnectedness, it’s plausible for groups of people to do things worth doing _only_ if they can get other groups of people who have similar interests to join them. But how do people do something together while still being separate? They **federate**.

The term **federate** is an intransitive verb, to form two or more parties into an alliance; to band together, cohere, cooperate, or ally with each other[1](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fn1-31157).

Notice what those terms aren’t saying? They aren’t saying **become one**. When joining together in a federated manner, the entities coming together only come together so far. Therefore, they retain their own identity and self-governance. While allying with each other, the entities agree to some form of cooperative governance[2](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fn2-31157).

When you federate multiple entities, you are forming them into a single group - with rules for how to govern the group as well as rules for cooperation. In fact, a distinct feature of a federation is that there is a central authority for overall governance that allows for individuated regulations at the local level. A perfect example of this is the United States, wherein individual states have their own government but must allow federal laws to supersede overlapping state laws.

#### A definition of a federated _anything_

Taking our cues from this discussion, we can say that a federated anything is “something that is joined together with other things so that those things can cooperate with each other under a common rule of governance while retaining their original identity and localized governance.”

### Federating data

We’ve come to live in a world where computing power is essentially free, and therefore, we are creating meaningful, valuable data more than any other time in history. Unfortunately, however, most of that data is being created in silos without thought of the data commingling with like data.

Take, for example, the world of job descriptions. We all have our own jobs where titles can be different for the same job description, and those job descriptions will vary between each organization. Is there a central repository for job descriptions that everyone can agree on? Nope. There are multiple repositories, none of which \(now\) communicate with each other to share data. For instance, some major content libraries are

* The US Bureau of Labor Statistics’ Standard Occupational Classification \(SOC\)[3](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fn3-31157).
* O\*NET OnLine job descriptions \(a riff off of the SOC above\)[4](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fn4-31157).
* The US’ National Institute of Standards and Technology’s NICE Cybersecurity Workforce Framework Work Roles[5](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fn5-31157).
* Open Skills Network \(OSN\) ’s database of skills and job descriptions[6](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fn6-31157).
* The myriad job descriptions being written by software tools like **Indeed** and **Jobvite**[7](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fn7-31157).

Do these libraries work with each other? ONET derives its data from the SOC. OSN derives __some __of its data from ONET. NIST’s system doesn’t work with any of them, and neither do Jobvite or Indeed. Does this cause the fracturing of data? Sure does! These organizations will never merge. And yet, what they produce could be made stronger if a modicum of sharing occurred.

A federated approach is needed so that people and organizations can get together, do stuff, and separate again, without having to negotiate the same set of arrangements over and over. So, the choices for sharing data are linking data and federating data.

### What is the difference between Federated Data and Linked Data?

Let’s start with **Linked Data**, the brainchild of Tim Berners-Lee. In 2006 Berners-Lee wrote the definition of Linked Data so that like web pages, “with linked data, when you have some of it, you can find other, related, data” [8](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fn8-31157). In his description, Berners-Lee wrote four rules for linking data:

1. Use URIs as names for things.
2. Use HTTP URIs so that people can look up those names.
3. When someone looks up a URI, supply useful information. Using the standards \(RDF\*, SPARQL\).
4. Include links to other URIs so that they can discover more things.

By following these four rules, any data published on the web can be linked to other data published on the web. Linking data between systems is beneficial for exchanging data of different types or forms[9](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fn9-31157). Linking data allows us a method of finding that data across the web. It is a way to create a network of standards-based, machine-readable data across websites. This method is standardized through protocols such as the JavaScript Object Notation for Linking Data[10](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fn10-31157).

Here’s a quick example of linked data for a **Role**. Notice that the @id element follows rules 1 & 2 above. The @context and @type are examples of rule 3 above.

```text
{
 "Role": {
 "@context": "http://grcschema.org/",
 "@type": "Role",
 "name": "Cyber Defense Incident Responder",
 "element_id": "629",
 "description": "Investigates, analyzes, and responds to cyber incidents within the network environment or enclave.",
 "languagecode_alpha3": "ENG",
 "@id": "https://grcschema.org:3005/api/Role/629/"
 }
}
```

Anyone with API access to the above URL can reference or link to that Role. 

![Linked Roles](../.gitbook/assets/3%20%281%29.png)

However, linking data is one thing. Integrating data is another.

**Federated data** is data that is shared between external sources using some form of data governance. Organizations like Gaia-X, the US Army, and others are focused on integrated yet decentralized data systems that, through federation, achieve transparency and data interoperability[11](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fn11-31157). The world of healthcare is another hotspot for data federation. With the advent of electronic health and medical records, doctors’ offices and hospitals, and research groups are federating their data to ensure input accuracy, shared meaning, and definitions of acceptable uses for the data[12](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fn12-31157). Without the attribute of linked data, Federated data requires whole systems to agree to governance and interoperability to work.

**Federated Linked Data** allows us to decouple the systems from the data.

![Federated Linked Roles](../.gitbook/assets/4%20%281%29.png)

### What is Federated Linked Data?

If you want to exchange data, linked data is all you need. However, suppose you’re going to integrate that linked data. In that case, you’ll need to be able to not only exchange the data you created with data someone else created but also have a method to update that exchanged data as well. So let’s take a look at that Role description again, but this time with additional information so that the data can be shared in a federated fashion.

Here’s the basic information again, as we presented it above. It allows us to link the data from the API to our system.

```text
{
 “Role”: {
 "@context": "http://grcschema.org/",
 "@type": "Role",
 "name": "Cyber Defense Incident Responder",
 "element_id": "629",
 “description”: “Investigates, analyzes, and responds to cyber incidents within the network environment or enclave.”,
 "languagecode_alpha3": "ENG",
 "@id": "https://grcschema.org:3005/api/Role/629/",
```

What follows is what allows us to use the data in a **federated** system.

First, we have the AuthoritySource , which lets us know where the data originates. Notice that the structure for this is linked as well so that we know how to find the source through its IRI.

```text
"AuthoritySource": {
 "@type": "AuthoritySource",
 "@id": "https://grcschema.org:3005/api/AuthoritySource/1/",
 "abbreviation": "NISTNICE",
 "element_id": "1",
 "name": "US’ National Institute of Standards and Technology’s NICE Cybersecurity Workforce Framework Work Roles"
 },
```

Next, this JSON schema has an element for tracking when the record was created, modified, live status, and other metadata necessary for tracking the origination and modification of this data element.

```text
"CoreMetaData": {
 "@type": "CoreMetaData",
 "checksum": "42",
 "created_audit_id": "10265",
 "date_created": "2021-09-02",
 "date_modified": "2021-09-02",
 "live_status": "1",
 "modified_audit_id": "29754",
 "notes": "none",
 "superseded_by": "0",
 "validated": "1"
 }
 }
}
```

\(What we’ve shown above is a slimmed-down version of the actual Role schema managed by GRCSchema.org, located [HERE](http://grcschema.org/Role).\)

The point is, once data is in a structure that tracks its ownership & metadata as well as linking information, that data can then be used by any organization with access to it and be advised when the data changes!

## Research Notes

All research for this section can be found at our research portal [HERE](https://theucf.info/research/federatedlinkeddata).

### Footnotes

1. “Thesaurus Results for FEDERATE.” n.d. Accessed September 27, 2021. [https://www.merriam-webster.com/thesaurus/federate.](https://www.merriam-webster.com/thesaurus/federate) [↩︎](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fnr1-31157)
2. “Difference Between Federation and Republic.” n.d. Compare the Difference Between Similar Terms. Accessed September 27, 2021. [https://www.differencebetween.com/difference-between-federation-and-vs-republic/](https://www.differencebetween.com/difference-between-federation-and-vs-republic/). “Political System - Confederations and Federations.” n.d. Encyclopedia Britannica. Accessed September 27, 2021. [https://www.britannica.com/topic/political-system](https://www.britannica.com/topic/political-system). “The Federation of Australia - Parliamentary Education Office.” n.d. Accessed September 27, 2021. [https://peo.gov.au/understand-our-parliament/history-of-parliament/federation/the-federation-of-australia/](https://peo.gov.au/understand-our-parliament/history-of-parliament/federation/the-federation-of-australia/). [↩︎](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fnr2-31157)
3. “Standard Occupational Classification \(SOC\) System.” n.d. Accessed September 27, 2021. [https://www.bls.gov/soc/2018/\#classification](https://www.bls.gov/soc/2018/#classification). [↩︎](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fnr3-31157)
4. “O\*NET OnLine.” n.d. Accessed September 27, 2021. [https://www.onetonline.org/](https://www.onetonline.org/). [↩︎](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fnr4-31157)
5. paul.hernandez@nist.gov. 2019. “NICE Framework Resource Center.” Text. NIST. November 13, 2019. [https://www.nist.gov/itl/applied-cybersecurity/nice/nice-framework-resource-center](https://www.nist.gov/itl/applied-cybersecurity/nice/nice-framework-resource-center). [↩︎](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fnr5-31157)
6. “OSN Open Skills Network.” n.d. Open Skills Network. Accessed September 27, 2021. [https://www.openskillsnetwork.org/](https://www.openskillsnetwork.org/). [↩︎](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fnr6-31157)
7. “How to Write a Job Description \[Updated for 2021\] \| Indeed for Employers.” n.d. Accessed September 27, 2021. [https://www.indeed.com/hire/how-to-write-a-job-description](https://www.indeed.com/hire/how-to-write-a-job-description). “Talent Acquisition AI and Automation.” n.d. Jobvite. Accessed September 27, 2021. [https://www.jobvite.com/products/ai-and-automation/](https://www.jobvite.com/products/ai-and-automation/). [↩︎](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fnr7-31157)
8. “Linked Data - Design Issues.” n.d. Accessed September 27, 2021. [https://www.w3.org/DesignIssues/LinkedData.html](https://www.w3.org/DesignIssues/LinkedData.html). [↩︎](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fnr8-31157)
9. Abramowicz, Witold, Sören Auer, and Tom Heath. 2016. “Linked Data in Business.” Business & Information Systems Engineering 58 \(5\): 323–26. [https://doi.org/10.1007/s12599-016-0446-0](https://doi.org/10.1007/s12599-016-0446-0). [↩︎](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fnr9-31157)
10. “JSON-LD - JSON for Linking Data.” n.d. Accessed September 27, 2021. [https://json-ld.org/](https://json-ld.org/). “W3C JSON-LD Working Group.” n.d. Accessed September 27, 2021. [https://www.w3.org/2018/json-ld-wg/](https://www.w3.org/2018/json-ld-wg/). [↩︎](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fnr10-31157)
11. “Gaia-X.” n.d. Gaia-X Website. Accessed September 27, 2021. [https://www.gaia-x.eu/node/34](https://www.gaia-x.eu/node/34). Vaughan, Ann. n.d. “STITCHING THE ARMY’S DATA FABRIC.” USAASC \(blog\). Accessed September 27, 2021. [https://asc.army.mil/web/news-stitching-the-armys-data-fabric/](https://asc.army.mil/web/news-stitching-the-armys-data-fabric/). [↩︎](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fnr11-31157)
12. “EMR vs EHR – What Is the Difference?” 2011. Health IT Buzz. January 4, 2011. [https://www.healthit.gov/buzz-blog/electronic-health-and-medical-records/emr-vs-ehr-difference](https://www.healthit.gov/buzz-blog/electronic-health-and-medical-records/emr-vs-ehr-difference). Hulsen, Tim. 2020. “Sharing Is Caring—Data Sharing Initiatives in Healthcare.” International Journal of Environmental Research and Public Health 17 \(9\): 3046. [https://doi.org/10.3390/ijerph17093046](https://doi.org/10.3390/ijerph17093046). “What Is an Electronic Health Record \(EHR\)? \| HealthIT.Gov.” n.d. Accessed September 27, 2021. [https://www.healthit.gov/faq/what-electronic-health-record-ehr](https://www.healthit.gov/faq/what-electronic-health-record-ehr). [↩︎](file:///Applications/iA%20Writer.app/Contents/Frameworks/Kit.framework/Versions/A/Resources/Templates/Copy%20Formatted.iatemplate/Contents/Resources/#fnr12-31157)

