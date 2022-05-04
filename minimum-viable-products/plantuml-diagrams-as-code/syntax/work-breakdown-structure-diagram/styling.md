# Styling

## Styling

Styling WBS diagrams is very similar to adding style tags and classes to HTML. The head of the PlantUML file will contain a style section that sets the format and colors for the WBS diagram. You can use style to set defaults for the entire diagram. They can be determined by depth of node or depth of arrow. They can also be determined by specific node and arrow as identified by a **style\_label** attached to the end of a node.

We will start with a basic diagram with a depth of two.

#### Starting Diagram

```
@startwbs
'Example: Starting Diagram

<style>

</style>

* Top Depth 0

**  1st Branch Depth 1
***     A Depth 2
***     B Depth 2

**  2nd Branch Depth 1
***     C Depth 2
***     D Depth 2

**  3rd Branch Depth 1
***     E Depth 2
***     F Depth 2

@endwbs
```

![Starting Diagram](../../../../.gitbook/assets/Style01\_start.png)

## Basic Styling Syntax

The style section of and WBS diagram is defined by style tags. It begins with \<style> and ends with \</style>. Inside of those tags you must inform PlantUML that you are styling a WBS diagram with a wbsDiagram{} object. The rest of all styling will be contained inside of this object.

All styling inside of the wbsDiagram{} object contains at least one target and one property. In the following example the **node** is the target and the property of that target is the **BackGroundColor**.

#### Example: Basic Styling Syntax

```
@startwbs
'Example: Basic Styling Syntax

<style>
wbsDiagram{
    node {
        BackGroundColor #CD1E1E
    }
}
</style>

* Top Depth 0

**  1st Branch Depth 1
***     A Depth 2
***     B Depth 2

**  2nd Branch Depth 1
***     C Depth 2
***     D Depth 2

**  3rd Branch Depth 1
***     E Depth 2
***     F Depth 2

@endwbs
```

![Basic Styling Syntax](../../../../.gitbook/assets/Style02\_basic\_syntax.png)

## Targets

Targets can be multi-tiered. For example you can target nodes at a specific depth. The following are the seven possible targets.

* **node**
* **arrow**
* **depth**
* **rootNode**
* **leafNode**
* **boxless**
* **style\_label**

### Node

The **node** target allows you to change the styling of nodes.

#### Example: Targeting Nodes

```
@startwbs
'Example: Targeting Nodes

<style>
wbsDiagram{
    //Change the line color of all nodes.
    node {
        LineColor DarkCyan
    }
}
</style>

* Top Depth 0

**  1st Branch Depth 1
***     A Depth 2
***     B Depth 2

**  2nd Branch Depth 1
***     C Depth 2
***     D Depth 2

**  3rd Branch Depth 1
***     E Depth 2
***     F Depth 2

@endwbs
```

![Targeting Nodes](../../../../.gitbook/assets/Style03\_node.png)

### Arrow

The **arrow** target allows you to change the color of the connecting lines.

#### Example: Targeting Arrows

```
@startwbs
'Example: Targeting Arrows

<style>
wbsDiagram{
    //Change the line color of all connections.
    arrow {
        LineColor DarkCyan
    }
}
</style>

* Top Depth 0

**  1st Branch Depth 1
***     A Depth 2
***     B Depth 2

**  2nd Branch Depth 1
***     C Depth 2
***     D Depth 2

**  3rd Branch Depth 1
***     E Depth 2
***     F Depth 2

@endwbs
```

![Targeting Arrows](../../../../.gitbook/assets/Style04\_arrow.png)

### Depth

The **depth** target allows you to change the style of nodes and connections at specific tiers in the diagram. **Depth** starts at the top tier with a value of 0. The **depth** value refers to the node and the connections immediately below it.

#### Example: Targeting Depth

```
@startwbs
'Example: Targeting Depth

<style>
wbsDiagram{
    //Change the line color of all objects at a depth of 0.
    :depth(0) {
        LineColor #561D5E    
    }
    //Change the line color of nodes with a depth of 1.
    //Change the line color of connections with a depth of 1 to a different color.
    :depth(1) {
        node{
            LineColor DarkCyan    
        }
        arrow{
            LineColor #CD1E1E    
        }
    }
}
</style>

* Top Depth 0

**  1st Branch Depth 1
***     A Depth 2
***     B Depth 2

**  2nd Branch Depth 1
***     C Depth 2
***     D Depth 2

**  3rd Branch Depth 1
***     E Depth 2
***     F Depth 2

@endwbs
```

![Targeting Depth](../../../../.gitbook/assets/Style05\_depth.png)

### Root Node

The **rootNode** target allows you to change the style of the top tier node.

#### Example: Targeting Root Node

```
@startwbs
'Example: Targeting Root Node

<style>
wbsDiagram{
    //Change the line color of the top tier node.
    rootNode{
        LineColor #CD1E1E
    }
}
</style>

* Top Depth 0

**  1st Branch Depth 1
***     A Depth 2
***     B Depth 2

**  2nd Branch Depth 1
***     C Depth 2
***     D Depth 2

**  3rd Branch Depth 1
***     E Depth 2
***     F Depth 2

@endwbs
```

![Targeting Root Node](../../../../.gitbook/assets/Style06\_rootNode.png)

### Leaf Nodes

The **leafNode** target allows you to change the style of the final node of every branch. This works regardless of symmetry.

#### Example: Target Left Nodes

```
@startwbs
'Example: Targeting Leaf Nodes

<style>
wbsDiagram{
    //Change the line color of all final tier nodes.
    leafNode{
        LineColor #CD1E1E
    }
}
</style>

* Top Depth 0

**  1st Branch Depth 1
***     A Depth 2
***     B Depth 2

**  2nd Branch Depth 1
***     C Depth 2
***     D Depth 2
****        i. Depth 3
****        ii. Depth 3

**  3rd Branch Depth 1

@endwbs
```

![Targeting Leaf Nodes](../../../../.gitbook/assets/Style07\_leafNode.png)

### Boxless

The **boxless** target allows you to change the style of **boxless** nodes.

#### Example: Targeting Boxless Nodes

```
@startwbs
'Example: Targeting Boxless Nodes

<style>
wbsDiagram{
    //Change the font color of all boxless nodes.
    boxless {
        FontColor #CD1E1E
    }
}
</style>

* Top Depth 0

**  1st Branch Depth 1
***     A Depth 2
***_    B Depth 2

**_ 2nd Branch Depth 1
***     C Depth 2
***     D Depth 2

**  3rd Branch Depth 1
***     E Depth 2
***_    F Depth 2

@endwbs
```

### Style Label

## Properties

* BackGroundColor
* RoundCorner
* LineColor
* LineStyle
* LineThickness
* FontColor
* Padding
* Margin
* HorizontalAlignment
* MaximumWidth
* Shadowing
