# Schema



The schema for PlantUML diagrams is very simple. In essence, outside of the _core_ schema elements diagramming as code has these _specific_ elements”

* **name** the name of the file in question.
* **description** the textual content of the diagram.
* **diagram\_type** the type of the diagram, such as _Deployment, Class, Activity_, etc.

The whole schema is below (not much to it). We’ve explained the main parts above, the rest can be found at [GRCSchema.org/PlantUML](https://grcschema.org/PlantUML):

```
{
  "PlantUML": {
    "@context": "http://grcschema.org/",
    "@type": "PlantUML",
    "diagram_type": "Activity",
    "name": "Sign-In Process",
    "element_id": "629",
    "description": "@startuml\n:This;\n:That;\n@enduml",
    "languagecode_alpha3": "ENG",
    "@id": "https://ucfcac/api/PlantUML/629/",
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

**Diagram Type** is drawn from a list of the available diagram types supported by PlantUML. The list, as of this publishing, is

* Activity
* Archimate
* AsciiMath
* Class
* Component
* Deployment
* Gantt
* JSON
* MindMap
* Object
* Use Case
* State
* Timing
* YAML
* WBS
* ERD

When sharing these documents within a federated system, the schemas for an _Account1, Organization2,_ and _Person3_ must also be taken into consideration.

#### ERD

The ERD for connecting the PlantUML table to the various account tables is shown below4.

![PlantUML ERD](https://www.complianceascode.net/wp-content/uploads/2021/10/PlantUML-ERD.png)

### Footnotes

1. [https://grcschema.org/account](https://grcschema.org/account) ↩︎
2. [https://grcschema.org/organization](https://grcschema.org/organization) ↩︎
3. [https://grcschema.org/person](https://grcschema.org/person) ↩︎
4. In the ERD Users and Persons are one in the same as a Person is a published User. ↩︎