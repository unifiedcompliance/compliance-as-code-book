# Lifelines

Lifelines are the basic building block for sequence diagrams. They are the senders and receivers of messages in the sequence diagram. The lifeline consists of a head with a name and a line drawn vertically down from the head. The default head is a rectangle with a name in it. PlantUML draws a foot as well. The foot is nice aesthetically but is not an official part of UML. We will leave it in our examples for aesthetic reasons.

## Declaring Lifelines

Use the "participant" command followed by a name to declare a default participant. Lifelines will appear left to right by default.&#x20;

#### Example: Declaring Lifelines

```
@startuml 
'Example: Declaring Lifelines

'Declare the default lifeline and name it.
participant Sean
participant Maria
participant Zarek

@enduml
```

![Declaring Lifelines](../../../../.gitbook/assets/01\_Lifelines\_declaringLifelines.png)

## Lifeline Properties

Properties following the participant\_type affect the format of the lifeline head. You are only required to use the participant\_type and name properties. Later, in the shortcut section you will notice that you do not have to declare participants. This helps if you are putting together a quick sequence diagram without any bells or whistles. There is some wiggle room with property order. For the sake of consistency and best practice we will keep them in the below order throughout this book. Below is a list of lifeline properties.&#x20;

* **participant\_type** - determines the head shape based on its classifier
* **name** - the text that appears in the head of the lifeline
* **display\_name** - a method for formatting **name**, comes after **name**
* **formatted\_name** - used in place of **name** and **display\_name**
* **variable\_name** - used as a variable for a lifeline with a long **name**&#x20;
* **back\_ground\_color** - sets the background color of the head
* **stereotype** - allows for the head to display a stereotype
* **order\_number** - adjusts the horizontal order of lifelines

### Participant Type

There are several options for **participant\_type**. Simply replace participant with any other **participant\_type**. The options are indicative of UML classifiers. PlantUML will change the header shape accordingly. Below is a list of participant types.

* participant
* actor
* boundary
* control
* entity
* database
* collections
* queue

#### Example: Participant Type

```
@startuml
'Example: Participant Type

'Declare lifelines with different head shapes.
participant participant
actor       actor
boundary    boundary
control     control
entity      entity
database    database
collections collections
queue       queue

@enduml
```

![Participant Type](../../../../.gitbook/assets/02\_Lifeline\_participant\_type.png)

### Name

The **name** is simply text that appears in the head of the lifeline. The **name** can be a single word without quotation marks or it can be a string with quotation marks. The string method supports line breaks.

#### Example: Name

```
@startuml
'Example: Name

'Declare a lifeline with a simple name
participant Sean

'Declare a lifeline with a name as a string
participant "Maria The Closer"

'Declare a lifleine with a multiline name
participant "Zarek \nThe Guy With \nCurly Hair"

@enduml
```

![Name](../../../../.gitbook/assets/03\_Lifelines\_name.png)

### Display Name

The **display\_name** property follows the "as" keyword. It can be used to display text in the head that is entirely different from the **name**. The **display\_name** property supports creole syntax for emphasis and markup language for color. Oddly PlantUML does not support emphasis with markup in the lifeline head. This lack of markup options is not in alignment with all PlantUML text fields. Luckily we can combine markup and creole. See [Text Formatting](text-formatting.md) for a list of creole and markup options.

#### Example: Display Name

```
@startuml
'Example: Display Name

'Declare a lifeline with bold text using creole.
participant Sean as "**Juanito**"

'Declare a lifeline with purple text using markup.
participant Maria as "<color:#561D5E>Mija Mia</color>"

'Declare a lifeline with bold red text using markup and creole.
participant Zarek as "<color:#FF0000>**Zarek**</color>"

@enduml
```

![Display Name](../../../../.gitbook/assets/04\_Lifelines\_display\_name.png)

### Formatted Name

The **formatted\_name** property replaces **name** and **display\_name**. Similar to **display\_name** it supports creole syntax for emphasis and markup language for color.  Once again PlantUML does not support emphasis with markup in the lifeline head. However we can still combine markup and creole. See [Text Formatting](text-formatting.md) for a list of creole and markup options.

#### Example: Formatted Name

```
@startuml
'Example: Formatted Name

'Declare a lifeline with bold text using creole.
participant "**Juanito**"

'Declare a lifeline with purple text using markup.
participant "<color:#561D5E>Mija Mia</color>"

'Declare a lifeline with bold red text using markup and creole.
participant "<color:#FF0000>**Zarek**</color>"

@enduml
```

![Formatted Name](../../../../.gitbook/assets/05\_Lifelines\_formatted\_name.png)

### Variable Name

A **variable\_name** is just that, a variable. You can assign a lifeline to a variable using the "as" keyword. This practice eases utilization a lifeline with a **formatted\_name**. Otherwise, you have to type the entire lifeline name, including formatting, every time you use that lifeline. To show this we will pass a few messages between our lifelines. Messages will not be explained here. See the [messages](messages.md) section for an in-depth explanation.
