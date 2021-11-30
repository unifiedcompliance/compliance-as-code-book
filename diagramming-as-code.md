# Diagramming as Code

Diagramming as Code is done in a syntax supported by [PlantUML](https://plantuml.com). **** PlantUML is an open source, plain-text diagramming syntax. One you might not have heard about but one you _absolutely need_.

### Why do I need a diagramming syntax?

That’s answered by looking at the use cases:

#### I’m a data architect and

* I want to create (insert diagram type here) diagrams that my team can easily edit.
* I want to create a visualization of my JSON or YAML files.

#### I’m a project manager and

* I want to create activity flows that I can share with my team so we can jointly edit them.
* I want to create Work Breakdown Structures (WBS) that my team can easily edit.

#### Analysis

Each of these use cases calls for a way to **visualize** something _and_ **easily edit** that visualization. Typically, one would have a couple of different diagramming tools to do this, each of which would need some training (and a license per user) to take advantage of them. But, of course, this is now the world of Compliance as Code. So why not _diagrams as code_? _What if_ you could use **text** and a few snippets of formatting around that text to turn that text into various forms of diagramming? For example to visualize something as simple as:

> _This_ communicates with _That_

To visualize this in PlantUML, you simply need a few pointers and the type of diagram you want to draw. Here are some example visualizations of the above text.

**Activity**

Activity diagrams are flowcharts to represent the flow from one activity to another activity.

```
@startuml
:This;
:That;
@enduml
```

![This-That Activity](https://www.complianceascode.net/wp-content/uploads/2021/10/this-that-activity.png)

Everything begins and ends with @xxxuml. In between, there isn’t much difference in the text of what is added, only the formatting. So in the sequence diagram that follows, we add the communication text and slightly reformat how _This_ and _That_ are written.

**Sequence**

Sequence diagrams illustrate how messages flow through a system, also known as event diagrams. It enables the visualization of several dynamic scenarios. A sequential sequence of events occurs between two lifelines, meaning both lifelines are present at the same time. According to UML, there is an upper and lower lifeline, and the message flow is represented by three vertical dotted lines at the bottom of the page.

```
@startuml
This -> That : Communication
@enduml
```

![Sequence](https://www.complianceascode.net/wp-content/uploads/2021/10/this-that-sequence.png)

Again, for the use case diagram, we simply re-format how _This_ and _That_ are written.

**Use Case**

Use case diagrams illustrate how the system’s users interact with it. An application, system, or process that interacts with people, organizations, or external systems may benefit from developing a use case diagram.

```
@startuml
:This: -> :That: : Communication
@enduml
```

![Use Case](https://www.complianceascode.net/wp-content/uploads/2021/10/this-that-UseCase.png)

Here are several other methods that can be used:

**Class**

Class diagrams enable the conceptualization of application structure and the implementation of details in programming code. It is also possible to use class diagrams for data modeling.

```
@startuml
This -|> That: Communication
@enduml
```

![Class](https://www.complianceascode.net/wp-content/uploads/2021/10/this-that-Class.png)

**Component**

Component diagrams represent the different parts of a UML diagram. In contrast to describing the system’s functionality, it represents the components used to achieve that functionality.

```
@startuml
[This] -> [That]: Communication
@enduml
```

![Component](https://www.complianceascode.net/wp-content/uploads/2021/10/this-that-component.png)

**Deployment**

Deployment diagrams are a kind of structure diagram used in modeling the physical aspects of an object-oriented system. For example, they are often used to model the static deployment view of a system (topology of the hardware).

```
@startuml
folder This
file That
This -> That: Communication
@enduml
```

![Deployment](https://www.complianceascode.net/wp-content/uploads/2021/10/this-that-deployment.png)



Other, slightly different formats can be used as well.

**Work Breakdown Structure**

Work breakdown structures define everything a project needs to accomplish, organized into multiple levels, and displayed graphically.

```
@startwbs
+ This
++ That
+++ A sub-task
++ Some other Thing
@endwbs
```

![WBS](https://www.complianceascode.net/wp-content/uploads/2021/10/this-that-WBS.png)

As you can see, PlantUML allows users to specify various types of diagrams in a simple text format similar to programming languages. It is the most popular text format for diagramming. As we showed above, it supports many different diagram types, separates each diagram element according to its function, and uses a simple, human-readable language.

### The schema for diagramming as code

The schema for diagramming as code is straightforward. In essence, outside of the _core_ schema elements diagramming as code has these _specific_ elements:

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

### How do we use diagramming as code?

Easily enough, you can create your own code-based diagrams using Plant UML by going to PlantUML’s website by clicking [HERE](http://www.plantuml.com/plantuml). This will start a new page for you, and you can diagram away. If you need to learn more about the various formats, you can click [HERE](https://plantuml.com).

If you want to learn more, you can visit our research site. Our bibliography for this topic is found by clicking [HERE](https://theucf.info/research/PlantUML).

If you want your own application that allows your team to create and track your diagrams as code, look at the section [PlantUML Diagrams as Code](minimum-viable-products/plantuml-diagrams-as-code/)!
