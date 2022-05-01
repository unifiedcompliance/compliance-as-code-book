# Organization

## Packages

Packages are used for organizing objects in the object diagram. It is used for grouping objects together. The most basic package begins with the word "package" followed by the **name** of the package. Any objects belonging to the package are declared inside the body of the package. The body is defined by a set of curly braces.

#### Example: Package Declaration

```
@startuml
'Example: Organization Package Declaration

'Create a basic package with a name.
'Add one object to the package.
package Package1 {

  object Object01

}

@enduml
```

![](../../../../.gitbook/assets/Organization01\_packages.png)

### Name

The **name** is text that appears in the head of the package. The **name** can be a single word without quotation marks or it can be a string with quotation marks. Single word supports creole syntax for emphasis. The string method supports emphasis with creole and markup language. The string method also supports colors with markup language. You can define colors with a standard color name or hex code. See [Text Formatting](../text-formatting.md) for a list of creole and markup options.

#### Example: Package Name

```
@startuml
'Example: Package Name

'Create a basic package with a name.
'Add one object to the package.
'Use creole to emphasize the name.
package "__Package 1__" {

  object Object01

}

'Create a basic package with a name.
'Add one object to the package.
'Use markup to add color and emphasis to the name.
package "<color #561D5E><i>Package 2</i></color>" {

    object Object02

}

@enduml
```

![Package Name](../../../../.gitbook/assets/Organization02\_package\_name.png)

### Types

The **type** is set immediately after the **name,** wrapped in a double set of less than and greater than signs. There are six package **types**. The default package **type** is a folder.

#### Example: Package Types

```
@startuml
'Example: Package Types

'Create a package with a name for all six package types.
'Add one object to each package.

package Node <<Node>> {
  object Object01
}

package Rectangle <<Rectangle>> {
  object Object02
}

package Folder <<Folder>> {
  object Object03
}

package Frame <<Frame>> {
  object Object04
}

package Cloud <<Cloud>> {
  object Object05
}

package Database <<Database>> {
  object Object06
}

@enduml
```

![Package Types](../../../../.gitbook/assets/Organization03\_package\_type.png)

### Body Color

The **body\_color** property determines the fill color of the drawn package entity. The **body\_color** is defined by a standard color name or hex code. Create a gradient by using two colors. If you use this property _alone_ it must come after a hash (**#**) sign and touch the hash sign. If any other properties follow this place a semicolon (**;**) between them. No spaces are needed.

#### Example: Package Body Color

```
@startuml
'Example: Package Body Color

'Create a package with a name and an object.
'Assign a body_color.
package Package1 #009EA1 {
  object Object01
}

'Create a package with a name and an object.
'Assign a gradient to body_color.
package Package2 #009EA1/white {
  object Object02
}

@enduml
```

![Package Body Color](../../../../.gitbook/assets/Organization04\_package\_color.png)

### Line Color

The **line\_color** property determines the color of the line that draws the box of the package. The **line\_color** is defined by a standard color name or hex code. Create a gradient by using two colors. If you use this property _alone_ it must come after a hash (**#**) sign and touch the hash sign. If any other properties follow this place a semicolon (**;**) between them. No spaces are needed.

Note: **Line\_color** gradients do not perform well on packages. They only affect the line under the package **name**.

#### Example: Package Line Color

```
@startuml
'Example: Package Line Color

'Create a package with a name and an object.
'Assign a line_color.
package Package1 #line:561D5E {
  object Object01
}

'Create a package with a name and an object.
'Assign a gradient to line_color.
package Package2 #line:561D5E/white {
  object Object02
}

@enduml
```

![Package Line Color](../../../../.gitbook/assets/Organization05\_package\_linecolor.png)

### Line Style

The **line\_style** property determines the type of line that draws the box of the class. The **line\_style** is defined by one of the three options below. If you use this property _alone_ it must come after a hash (**#**) sign and touch the hash sign. If any other properties follow this place a semicolon (**;**) between them. No spaces are needed.

* line.dashed
* line.dotted
* line.bold

#### Example: Package Line Style

```
@startuml
'Example: Package Line Style

'Create a package with a name and an object.
'Make the line_style bold.
package Package1 #line.bold {
  object Object01
}

'Create a package with a name and an object.
'Make the line_style dashed.
package Package2 #line.dashed {
  object Object02
}

'Create a package with a name and an object.
'Make the line_style dotted.
package Package3 #line.dotted {
  object Object03
}

@enduml
```

![Package Line Style](../../../../.gitbook/assets/Organization06\_package\_linestyle.png)

### Body

The **body** of the package displays the classes that belong to the package. Classes that belong to the package should be written inside the **body** of the package. Relationships can be written inside or outside of the package body.&#x20;

#### Example: Package Body

```
@startuml
'Example: Package Body

'Create a package with a name and two objects.
'Create a relationship between the objects inside the package.
package PackageA {
  object ObjectA1
  object ObjectA2

  ObjectA1 -- ObjectA2
}

'Create a second package with a name and an object.
package PackageB {
  object ObjectB1
}

'Create a relationship between a object from the first package and a object from the second object.
ObjectA1 - ObjectB1

@enduml
```

![Package Body](../../../../.gitbook/assets/Organization07\_package\_body.png)

### With All Properties

#### Example: Packages With All Properties

```
@startuml
'Example: Packages With All Properties

package __PackageA__ <<Database>> #E6E6E7;line:009EA1;line.dashed {
  object ObjectA1
  object ObjectA2

  ObjectA1 -- ObjectA2
}

package "<color #E6E6E7><i>Package B</i></color>" <<Cloud>> #561D5E|191C1F;line:E6E6E7;line.bold {
  object ObjectB1
}

ObjectA1 - ObjectB1

@enduml
```

![Packages With All Properties](../../../../.gitbook/assets/Organization08\_package\_allProperties.png)



## Visibility

There are three ways to affect the visibility of entities in a class diagram. PlantUML adjusts visibility from the top down. This allows you to hide a large unneeded portion of the diagram and just show what you need.

* hide - hides parts of the class diagram, the parts still take up space in the diagram
* show - shows a part of a class that might otherwise be hidden
* remove - removes parts from the class diagram, they no longer take up space

#### Example: Visibility Starting Point

Use the following code as the starting point for the rest of the visibility examples.

Note: We will be changing the background color to more easily track the size of the diagram. Skin parameters will be covered in their own section.

```
@startuml
'Example: Visibility Starting Point
skinparam BackgroundColor #E6E6E7

object Object1 <<Top>> {
  Field_1
  Field_2
}

object Object2 <<Top>>

object Object3 {
  Field_3
  Field_4
}

object Object4

Object1 -  Object2
Object1 -- Object3

@enduml
```

![Visibility Starting Point](../../../../.gitbook/assets/Organization09\_1\_hide.png)

### Hiding Showing and Removing Objects

You can change the visibility of an object by following the key word with the object **name**. You can change the visibility of several objects at a time by replacing the object **name** with a **stereotype**.

#### Example: Hiding, Showing, and Removing Objects

Notice how the below code leaves space for Object2 because it is only hidden. However the part of the diagram containing Object3 is completely removed because we removed Object3.

```
@startuml
'Example: Hiding Showing and Removing Objects
skinparam BackgroundColor #E6E6E7

object Object1 <<Top>> {
  Field_1
  Field_2
}

object Object2 <<Top>>

object Object3 {
  Field_3
  Field_4
}

object Object4

Object1 -  Object2
Object1 -- Object3

'Hide all <<Top> stereotypes.
hide <<Top>>

'Unhide or show Object1.
show Object1

'Remove Object3.
remove Object3

@enduml
```

![Hiding, Showing, and Removing Objects](../../../../.gitbook/assets/Organization09\_2\_hide.png)

### Hiding and Showing Parts of Objects

You can adjust visibility on parts of classes by placing their property type after the visibility keyword. The following items are adjustable. You can be specify which class to adjust if you place the **name** or **stereotype** of the class before the property type.

* **members** - this will adjust visibility of all fields
* **fields** - this will adjust visibility of all fields
* **stereotype** - this will adjust the visibility of stereotypes in the class head

#### Example: Hiding and Showing Parts of Objects

## Page Breaks?
