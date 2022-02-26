# Actor

Actors are the second of two primary objects in use case diagrams. They represent an entity, person or otherwise, that interacts that is involved with an action called a use case.

## Declaration

There are two methods for declaring actors. One method uses the command word **actor**. The other method requires placing the **name** of the actor between two colons.&#x20;

#### Example: Actor Declaration

```
@startuml
'Example: Actor Declaration

'Declare an actor with the actor command.
actor Zarek

'Declare an actor using colons.
:Ivy:

@enduml
```

![Actor Declaration](../../../../.gitbook/assets/UseCase01\_actor\_declaration.png)

## Properties

Actors have eight properties. All are optional except **name**. The properties generally follow the below order.&#x20;

* **name** - the name of the entity, can be a person or object such as a database
* **business** - determines if the actor is a business actor
* **alias** - gives the ability to use a variable to identify the actor
* **stereotype** - applies a stereotype text to the actor
* **fill\_color** - changes the interior color of the actor
* **line\_color** - determines the color of the line used to draw the actor
* **line\_type** - determines the type of line used to draw the actor
* **text\_color** - determines the color of the **name** and **stereotype** text

The **business** property may come before or after **name**. The last four properties follow a hash (**#**) sign and are separated by a semicolon (**;**) if more than one is used. The last three properties can be in any order so long as they are the last three.

### Name

The **name** is simply text that appears below the actor icon. The **name** can be a single word it can be a string. Multiword strings must be inside of colons. The string method supports line breaks as well as markup for color and emphasis. If you use markup for color in the **name** property it will override the **text\_color** property. You can define colors with a standard color name or hex code.

#### Example: Actor Name

```
@startuml
'Example: Actor Name

'Create an actor with a multiline name.
actor :Zarek\nStocker:

'Create an actor and use markup for color and emphasis in the name.
:<font color=561D5E><b>Ivy Cashier</b></font>:

@enduml
```

![Actor Name](../../../../.gitbook/assets/UseCase02\_actor\_name.png)

### Business

The business property is turned on by placing a forward slash after the **actor** key word or after the last colon around **name**. This simply adds a slash mark to the body of the actor icon. Make sure the forward slash is touching the character to its left with no space between.&#x20;

#### Example: Business Actor

```
@startuml
'Example: Business Actor

'Create a business actor with the actor command.
actor/ Zarek

'Create a business actor with colons.
:Ivy:/

@enduml
```

![Business Actor](../../../../.gitbook/assets/UseCase03\_actor\_business.png)

### Alias

The **alias** is exactly that. It is a variable that represent an actor. It is especially useful if the actor has a long **name**. The variable for the alias follows the **as** keyword.

There will be a **use\_case** and an **association** in the following example. This is needed to show the importance of the **alias**. They will not be explained here. See their respective sections of this chapter for proper explanations.

Notice how much easier it is to create an association with the Ivy **alias** line 18. Otherwise you must write the entire **name** as shown for Zarek on line 15.

**Example: Actor Alias**

```
@startuml
'Example: Actor Alias

'Create an actor with a multiline name.
actor :Zarek\nStocker:

'Create an actor and use markup for color and emphasis.
'Give the actor an alias.
:<font color=561D5E><b>Ivy Cashier</b></font>: as Ivy

'Create a use case.
(Clock In)

'Create an association between your first actor and the use case.
:Zarek\nStocker: -- (Clock In)

'Create an association between your second actor and the use case.
Ivy -- (Clock In)

@enduml
```

![Actor Alias](../../../../.gitbook/assets/UseCase04\_actor\_alias.png)

### Stereotype

The **stereotype** field is defined by text between a double set of greater than and less than signs. This adds **stereotype** text above the **actor** icon. The stereotype text will be displayed in the color of the **text\_color** property.

#### Example: Actor Stereotype

```
@startuml
'Example: Actor Stereotype

'Create an actor with a stereotype.
:Zarek: <<Stocker>> 

'Create another actor with a stereotype.
actor Ivy <<Cashier>>

@enduml
```

![Actor Stereotype](../../../../.gitbook/assets/UseCase05\_actor\_alias.png)

### Fill Color

The **fill\_color** is defined by a standard color name or hex code. It determines the interior color of the actor icon. For the standard stick figure this is the interior of the head. If you use this property it must come immediately after a hash (**#**) sign and touch the hash sign.

#### Example: Actor Fill Color

```
@startuml
'Example: Actor Fill Color

'Create an actor with a fill_color. 
:Zarek: #red

'Create an actor with a fill_color.
actor Ivy #00FF00

@enduml
```

![Actor Fill Color](../../../../.gitbook/assets/UseCase06\_actor\_fill\_color.png)

### Line Color

### Line Type

### Text Color
