# Use Case

The **use\_case** is the meat of use case diagrams. It is a set of behaviors that will be performed by an actor or actors in the diagram.

## Declaration

There are two methods for declaring a **use\_case**. One method uses the command word **usecase**. The other method requires placing the **name** of the **use case** inside parentheses.

#### Example:

```
@startuml
'Example: Use Case Declaration

'Declare a use_case with the usecase command.
usecase Check

'Declare a use_case with parentheses.
(Stock)

@enduml
```

![Use Case Declaration](../../../../.gitbook/assets/UseCase01\_Declaration.png)

## Properties

Use cases have eight properties. All are optional except **description**. The properties generally follow the below order.

* **description** - explains the action performed in the use case
* **business** - determines if the use case is a business use case
* **alias** - gives the ability to use a variable to identify the use case
* **stereotype** - applies a stereotype text to the use case
* **fill\_color** - changes the interior color of the use case
* **line\_color** - determines the color of the line used to draw the use case
* **line\_type** - determines the type of line used to draw the use case
* **text\_color** - determines the color of the **description** and **stereotype** text

The **business** property may come before or after **description**. The last four properties follow a hash (**#**) sign and are separated by a semicolon (**;**) if more than one is used. The last three properties can be in any order so long as they are the last three.

### Description

The **description** is text that appears inside the **use\_case** oval. The **description** can be a single word or it can be a string. Multiword strings must be inside parentheses. The string method supports line breaks as well as markup for color and emphasis. You can define colors with a standard color name or hex code.

Note: If color formatting is used inside of the **description** property it will override **text\_color**. See [Text Color](use-case.md#text-color) for example.

#### Example: Use Case Description

```
@startuml
'Example: Use Case Description

'Declare a multline use_case with the usecase command.
usecase (Check\nCustomers)

'Declare a multiword use_case with parentheses.
'Use markup to add color and emphasis.
(<font color=561D5E><b>Stock Shelves</b></font>)

@enduml
```

![Use Case Description](../../../../.gitbook/assets/UseCase02\_description.png)

### Business

The **business** property is turned on by placing a forward slash after the **usecase** command or after the last parentheses around **description**.

#### Example Business Use Case

```
@startuml
'Example: Business Use Case

'Create a business use_case with the usecase command.
usecase/ Check

'Create a business use_case with parentheses.
(Stock)/

@enduml
```

![Business Use Case](../../../../.gitbook/assets/UseCase03\_business.png)

### Alias

The **alias** is exactly that. It is a variable that represents a **use\_case**. It is especially useful if the **use\_case** has a long **description**. The variable for the alias follows the **as** keyword.

There will be an **actor** and an **association** in the following example. This is needed to show the importance of the **alias**. They will not be explained here. See their respective sections of this chapter for proper explanations.

Notice how much easier it is to create an association with the Clock **alias** on line 15. Otherwise you must write the entire **description** as shown for Stock Shelves on line 18.

**Example: Use Case Alias**

```
@startuml
'Example: Use Case Alias

'Create an actor.
:Zarek:

'Create an use case and use markup for color and emphasis.
'Give the use case an alias.
(<font color=561D5E><b>Clock In</b></font>) as Clock

'Create a multiline use case.
(Stock\nShelves)

'Create an association between your actor and the first use case.
Zarek -- Clock

'Create an association between your actor and the second use case.
Zarek -- (Stock\nShelves)

@enduml
```

![Use Case Alias](../../../../.gitbook/assets/UseCase04\_alias.png)

### Stereotype

The **stereotype** field is defined by text between a double set of greater than and less than signs. This adds **stereotype** text above the **description** inside the oval icon. The stereotype text will be displayed in the color of the **text\_color** property.

```
startuml
'Example: Use Case Stereotype

'Create a use_case with a stereotype.
usecase (Clock In) <<General Duty>> 

'Create another use_case with a stereotype.
(Bag Items) <<Cashier Duty>>

@enduml
```

![Use Case Stereotype](../../../../.gitbook/assets/UseCase05\_stereotype.png)

### Fill Color

The **fill\_color** is defined by a standard color name or hex code. It determines the interior color of the actor icon. For the standard stick figure this is the interior of the head. If you use this property _at all_ it must come immediately after a hash (**#**) sign and touch the hash sign. If any other properties follow this place a semicolon (**;**) between them. No spaces are needed.

#### Example: Use Case Fill Color

```
@startuml
'Example: Use Case Fill Color

'Create a use_case with a fill_color. 
usecase (Clock In) #red

'Create a use_case with a fill_color.
(Bag Items) #00FF00

@enduml
```

![Use Case Fill Color](../../../../.gitbook/assets/UseCase06\_fill\_color.png)

### Line Color

### Line Type

### Text Color
