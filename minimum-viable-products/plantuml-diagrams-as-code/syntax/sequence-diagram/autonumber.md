# Autonumber

You can assign your messages sequential numbers automatically with the **autonumber** command.

## Activation

Place the **autonumber** command in your code and the following messages will be numbered sequentially.

#### Example: Autonumber Activation

```
@startuml
'Example: Messages Autonumber

'Activate the autonumber method.
autonumber

'Send a few messages back and forth.
Sean  ->  Maria : Text
Sean  <-- Maria : Text

Maria ->  Zarek : Text
Maria <-- Zarek : Text

Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Autonumber Activation](<../../../../.gitbook/assets/Autonumber01\_activation (1).png>)

## Commands

There are three commands that can follow **autonumber**. They are all optional. You will only need **resume** if you used **stop**, but it's not required. The **inc** command will be covered below in the [Specific Sequence](autonumber.md#specific-sequence) section.

* **stop -** does what is says on the box, stops the sequential numbering
* **resume** - resumes sequential numbering after using **stop**
* **inc** - adds specific increments to specific sequences

#### Example: Stop & Resume

```
@startuml
'Example: Autonumber Stop & Resume

'Activate the autonumber method.
autonumber

'Send a message from Sean to Maria and a reply.
Sean  ->  Maria : Text
Sean  <-- Maria : Text

'Stop the autonumber method.
autonumber stop

'Send a message from Maria to Zarek and a reply.
Maria ->  Zarek : Text
Maria <-- Zarek : Text

'Resume the autonumber method.
autonumber resume

'Send a message from Zarek to Sean and a reply.
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Stop & Resume](../../../../.gitbook/assets/Autonumber02\_stop\_resume.png)

## Properties

All **autonumber** properties are optional. They should appear after the **autonumber** or **resume** commands. They must be used in order even if you don't use all properties. You must have a **start\_number** if you wish to use **increment**. The **format** property contains three optional parts. There is no mandatory order inside of **format**.

* **start\_number** - the initial number used in the **autonumber** sequence
* **increment** - the number added to the **autonumber** sequence with each message
* **format** - determines the format of the sequential numbers consist of three parts
  * **text\_format** - similar to other formatting, usually surrounds the **message** and **number\_format**
  * **message** - displays a message with the sequential numbers
  * **number\_format** - provides a format for the sequential numbers

### Start Number

The **start\_number** property immediately follows either the **autonumber** or **resume** command. It defines the number that will begin the numbering sequence.

#### Example: Start Number

```
@startuml
'Example: Autonumber Start Number

'Activate the autonumber method.
'Start the sequence at 10.
autonumber 10

'Send a message from Sean to Maria and a reply.
Sean  ->  Maria : Text
Sean  <-- Maria : Text

'Stop the autonumber method.
autonumber stop

'Send a message from Maria to Zarek and a reply.
Maria ->  Zarek : Text
Maria <-- Zarek : Text

'Resume the autonumber method.
'Restart the sequence at 20.
autonumber resume 20

'Send a message from Zarek to Sean and a reply.
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

## Specific Sequence

