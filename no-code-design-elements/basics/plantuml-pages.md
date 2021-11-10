# PlantUML Pages

Plant UML pages are specifically designed to utilize the UCF's Plant UML Plugin for bubble.io and other no-code applications. The window below highlights the two fields necessary for PlantUML to function, and how those fields should be displayed.

![PlantUML implementation](https://www.complianceascode.net/wp-content/uploads/2021/11/PlantUML-Plugin.png)

BOTH files should stretch horizontally and vertically with the page as it stretches.

1. This is the graph display field and is drawn using GraphViz. Notice at the bottom right it has a plus/minus set of icons in order to increase or decrease the view’s zoom.
2. This is the text entry field in which the UML content is entered. This field should be scrollable.
3. This is the vertical resize bar and should allow dragging up or down to resize the _top_ graph field vertically.

PlantUML has already been integrated with a variety of tools, as shown on their website [HERE](https://plantuml.com/running).

A pretty good example of it in use is found at the sujoyu page in GitHub accessible [HERE](http://sujoyu.github.io/plantuml-previewer/).

## Connecting the PlantUML diagrams to the Standardized Account table

The schema for PlantUML diagrams is very simple. In essence, outside of the _core_ schema elements diagramming as code has these _specific_ elements”

* **name** the name of the file in question.
* **description** the textual content of the diagram.
* **diagram\_type** the type of the diagram, such as _Deployment, Class, Activity_, etc.

The whole schema is below (not much to it). We’ve explained the main parts above, the rest can be found at [GRCSchema.org/PlantUML](https://grcschema.org/PlantUML):

![PlantUML JSON](https://www.complianceascode.net/wp-content/uploads/2021/11/PlantUMLJSON.png)

The ERD for connecting the PlantUML table to the various account tables is shown below.

![PlantUML ERD](https://www.complianceascode.net/wp-content/uploads/2021/10/PlantUML-ERD.png)
