---
description: >-
  Relationships show associations between different types of classes. For
  example a class named car has a relationship with a class named wheel.
---

# Relationships

## Declaration

A basic relationship contains two entities and a line showing the relationship between them.

#### Example: Declaring Relationships

```
@startuml
'Example: Declaring Relationships

'Create two classes.
class Car 
class Wheel

'Show a relationship between the two classes.
Car - Wheel

@enduml
```

![Declaring Relationships](../../../../.gitbook/assets/Relationships01\_Declaration.png)

## Parts of Relationships

Classes are comprised of three parts. Label is the only optional part.

* **entity** - the object for which a relationship can be described in a class diagram, must have at least two
* **connection** - visual description of the relationship between entities
* **label** - textual description of the relationship between entities

## Entities

The connected entity can be a class, attribute, or method. Classes are defined by their **name**. Attributes and methods are defined by the class **name** that contains them followed by two semicolons (::) and the attribute or method **text**.

* class
* attribute
* method

#### Example: Relationship Entities

```
@startuml
'Example: Relationship Entities

'Create a class with a method and an attribute.
class Car {
    axle
    go()
}

'Create two more classes.
class Wheel
class Fuel

'Show a relationship between a class and a method.
Fuel - Car::go

'Show a relationship between an attribute and a class.
Car::axle - Wheel

@enduml
```

![Relationship Entities](../../../../.gitbook/assets/Relationships02\_entities.png)

## Label

Though it comes last in syntax we will explain **label** before **connection**. This is a purely aesthetic issue. While **label** is not required much of the **connection** is drawn poorly if there is no **label**. It gets squished together.

* **label\_text** - the text describing the relationship between connected entities
* **read\_direction** - shows the direction a relationship is read

### Label Text

This text describes the relationship between the connected **entities**. **Label\_text** is not required even if **read\_direction** is used.

### Read Direction

A greater than or less than sign (><) used to show the direction a relationship is read. The sign may be placed before or after the label. **Read\_direction** is not required even if **label\_text** is used.

#### Example: Relationship Labels

```
@startuml
'Example: Relationship Labels

'Create a class with a method and an attribute.
class Car {
    axle
    go()
}

'Create two more classes.
class Wheel
class Fuel

'Show a relationship between a class and a method.
'Use a label to explain that relationship.
Fuel - Car::go : requires <

'Show a relationship between an attribute and a class.
'Use a label to explain that relationship.
Car::axle - Wheel : > has

@enduml
```

![Relationship Labels](../../../../.gitbook/assets/Relationships03\_label.png)

## Connection

The connection is the line between the entities. It can carry a lot of information. The only required portion of the connection is the hyphen or dash between the entities.

* **multiplicity** - defines number relationships between the entities, one may be on each end of the connection
* **arrow\_head** - determines the shape of the arrow head, one may be on each end of the connection
* **line\_type** - determines the type of line between the **entities**
* **line\_orientation** - determines the direction of the second entity in relation to the first entity
* **line\_color** - determines the color of the line making the connection
* **line\_thickness** - determines the thickness of the line between the entities

### Multiplicity

Multiplicity defines number relationships between the connected entities. In this example cars have between four to six wheels.

Example: Relationship Multiplicity

```
// Some code
```

Image

### Arrow Head

Text

Example:

```
// Some code
```

Image

### Line Type

Text

Example:

```
// Some code
```

Image

### Line Orientation

Text

Example:

```
// Some code
```

Image

### Line Color

Text

Example:

```
// Some code
```

Image

### Line Thickness

Text

Example:

```
// Some code
```

Image

##

## Written Relationships

extends

implements



## Specific Relationships

class\_1::attribute --> class\_2::attribute&#x20;



move this to entities



## inheritance

the only skinparam covered here

```
@startuml
'Example: Practice
@startuml

skinparam groupInheritance 3

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



