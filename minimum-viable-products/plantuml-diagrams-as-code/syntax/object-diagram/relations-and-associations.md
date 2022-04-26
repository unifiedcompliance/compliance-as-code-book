# Relations and Associations

## Declaring Relations

A basic relation contains two entities and a line showing the relation between them.

#### Example: Declaring Object Relations

```
@startuml
'Example: Declaring Object Relations

'Declare two objects.
object Object01
object Object02

'Create a relation between the two object.
Object01 - Object02

@enduml
```

![Declaring Object Relations](../../../../.gitbook/assets/Relations01\_declaration.png)

## Parts of Relations

Relations are comprised of three parts. Label is the only optional part.

* **entity** - the object for which a relation can be described in an object diagram, must have two
* **connection** - visual description of the relation between entities
* **label** - textual description of the relation between entities

## Entities

The connected entities can be objects, fields, map tables, cells, or packages. Objects, map tables, and packages are defined by their **name**. Fields and cells are defined by the parent object name followed by two colons (::) and the field or cell **text**.

* object
* field
* map table
* cell
* package

#### Example: Relation Entities

```
@startuml
'Example: Relation Entities

'Create two objects with fields.
object Object01 {
    Field01
}

object Object02 {
    Field02
}

'Create a map table with two cells.
map MyMapTable {
    Cell01 => Cell02
}

'Create a relation between the two objects.
Object01 - Object02

'Create a relation between the second object and a cell in the map table.
Object02 - MyMapTable::Cell01

@enduml
```

![Relation Entities](../../../../.gitbook/assets/Relations02\_entities.png)

## Labels

This text describes the relation between the connected **entities**.  You can format **labels** with creole syntax for emphasis and markup language for color and emphasis. You can define colors with a standard color name or hex code. **Labels** are not required.

#### Example: Relation Labels

```
@startuml
'Example: Relation Labels

'Create three objects.
object Object01 
object Object02
object Object03

'Create a relation between the first two objects.
'Use a label to explain that relation.
'Use creole to emphasize the text.
Object01 - Object02 : **Relation** //Text//

'Create a relation between the second two objects.
'Use a label to explain that relation.
'Use markup to add color and emphasis to the text.
Object02 - Object03 : <color #561D5E><b>Relation</b> <i>Text</i></color>

@enduml
```

![Relation Labels](../../../../.gitbook/assets/Relations03\_connections.png)

## Connections

The connection is the line between the entities. It can carry a lot of information. The only required portion of the connection is the dash (-) between the entities.

* **arrow\_head** - determines the shape of the arrow head, one may be on each end of the connection
* **line\_type** - determines the type of line between the **entities**
* **line\_orientation** - determines the direction of the second entity in relation to the first entity
* **line\_color** - determines the color of the line making the connection
* **line\_thickness** - determines the thickness of the line between the entities

## Associations

Link to/from specific objects including packages.
