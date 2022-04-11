# Organization

## Group Inheritance

The majority of skin parameters will be covered in their own chapter. However, group inheritance has a very specific use for organizing class diagrams. If multiple classes point to the same class the relationship arrow can be merged with the skin parameter **groupInheritance** followed by a number. By changing the number we can determine the threshold for merging relationships. If the threshold is set to two any entity with two or more relationships with the same trajectory will have those relationships merged.

#### Example: No Group Inheritance&#x20;

```
@startuml
'Example: No Group Inheritance

'Create classes with multiple relationships ranging from one to four relationships.
A1 <|-- B1

A2 <|-- B2
A2 <|-- C2

A3 <|-- B3
A3 <|-- C3
A3 <|-- D3

A4 <|-- B4
A4 <|-- C4
A4 <|-- D4
A4 <|-- E4

@enduml
```

![No Group Inheritance](../../../../.gitbook/assets/Organization01\_1\_group\_inheritance.png)

#### Example: Group Inheritance Threshold 2

```
@startuml
'Example: Group Inheritance Threshold 2

'Set the class diagram to merge same trajectory relationships of two or more.
skinparam groupInheritance 2

'Create classes with multiple relationships ranging from one to four relationships.
A1 <|-- B1

A2 <|-- B2
A2 <|-- C2

A3 <|-- B3
A3 <|-- C3
A3 <|-- D3

A4 <|-- B4
A4 <|-- C4
A4 <|-- D4
A4 <|-- E4

@enduml
```

![Group Inheritance Threshold 2](../../../../.gitbook/assets/Organization01\_2\_group\_inheritance.png)

####

#### Example: Group Inheritance Threshold 4

```
@startuml
'Example: Group Inheritance Threshold 4

'Set the class diagram to merge same trajectory relationships of four or more.
skinparam groupInheritance 4

'Create classes with multiple relationships ranging from one to four relationships.
A1 <|-- B1

A2 <|-- B2
A2 <|-- C2

A3 <|-- B3
A3 <|-- C3
A3 <|-- D3

A4 <|-- B4
A4 <|-- C4
A4 <|-- D4
A4 <|-- E4

@enduml
```

![Group Inheritance Threshold 4](../../../../.gitbook/assets/Organization01\_3\_group\_inheritance.png)

## Packages

Packages are used for organizing classes in the class diagram. It is used for grouping classes together. The most basic package begins with the word "package" followed by the **name** of the package. Any classes belonging to the package are declared inside the body of the package. The body is defined by a set of curly braces.

#### Example: Package Declaration

```
@startuml
'Example: Organization Package Declaration

'Create a basic package with a name.
'Add one class to the package.
package Package1 {

  class Class1

}

@enduml
```

![Package Declaration](../../../../.gitbook/assets/Organization02\_package\_declaration.png)

### Name

The **name** is text that appears in the head of the package. The **name** can be a single word without quotation marks or it can be a string with quotation marks. Single word supports creole syntax for emphasis. The string method supports emphasis with creole and markup language. The string method also supports colors with markup language. You can define colors with a standard color name or hex code. See [Text Formatting](../text-formatting.md) for a list of creole and markup options.

#### Example: Package Name

```
@startuml
'Example: Package Name

'Create a basic package with a name.
'Add one class to the package.
'Use creole to emphasize the name.
package "__Package 1__" {

  class Class1

}

'Create a basic package with a name.
'Add one class to the package.
'Use markup to add color and emphasis to the name.
package "<color #561D5E><i>Package 2</i></color>" {

    class Class2

}

@enduml
```

![Package Name](../../../../.gitbook/assets/Organization03\_package\_name.png)

### Types

The **type** is set immediately after the **name,** wrapped in a double set of less than and greater than signs. There are six package **types**. The default package **type** is a folder.

```
'Example: Package Types

'Create a package with a name for all six package types.
'Add one class to each package.

package Node <<Node>> {
  class Class1
}

package Rectangle <<Rectangle>> {
  class Class2
}

package Folder <<Folder>> {
  class Class3
}

package Frame <<Frame>> {
  class Class4
}

package Cloud <<Cloud>> {
  class Class5
}

package Database <<Database>> {
  class Class6
}

@enduml
```

![Package Types](../../../../.gitbook/assets/Organization04\_package\_types.png)

### fill color, head and body?

### line color

### text color

### body

## Name Spaces

name \<html?>

color, head and body?

line color

text color

body

## Visibility

Hide and Show specifics

Hide and Show members

remove classes

remove unlinked

## Class Position

show bad position

show good position

show good position with hidden connections

## Page Breaks

Take biggest previous picture and split into 6

\[ ]\[ ]\[ ]\
\[ ]\[ ]\[ ]
