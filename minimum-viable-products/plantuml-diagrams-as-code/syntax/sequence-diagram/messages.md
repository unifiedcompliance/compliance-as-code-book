# Messages

Messages are the basic action of sequence diagrams. They are portrayed by arrows going from a sender to a receiver.&#x20;

Lifelines will not be declared in this section unless required for an explanation. This will keep our code blocks smaller and easier to read.

## Declaration

In PlantUML, you declare messages by drawing an arrow with the characters on your keyboard. Place the arrow between the **sender** and the **receiver** with the arrow pointing at the **receiver**.&#x20;

#### Example: Message Declaration

```
@startuml
'Example:Message Declaration

'Send a few basic messages.
Sean  ->  Maria
Maria ->  Zarek

@enduml
```

![Message Declaration](../../../../.gitbook/assets/Messages01\_declaration.png)

## Direction

Arrows can be drawn right to left or left to right. This is nice as it allows you to customize how you want to format your messages. You can always keep senders on one side of your messages like the top of our example. You can also let your arrows go back and forth while your senders stay in the same place on consecutive lines like the bottom of our example. There is also the unadvised option of not picking a method. Do what makes sense for you and your team.

#### Example: Message Direction

```
@startuml
'Example: Message Direction

'Send a few messages back and forth between Sean and Maria.
'Keep Sean on the left of the code.
Sean  ->  Maria
Sean  <-  Maria
Sean  ->  Maria

'Send a few messages back and forth between Maria and Zarek.
'Keep the arrow pointing to the right in the code.
Maria -> Zarek
Zarek -> Maria
Maria -> Zarek

@enduml
```

![Message Direction](../../../../.gitbook/assets/Messages02\_direction.png)



## Properties

The minimum requirements for a message are **sender**, **line\_type**, **head\_type**, and **receiver**. As we did with lifelines we will keep all message properties except **message\_text** in the below order throughout this book. Keep in mind the order is sender to receiver as shown above, not necessarily left to right. The **message\_text** property is always furthest to the right.

* **sender** - the entity sending the message, usually a participant's lifeline
* **line\_type** - determines if the message arrow has a solid or dashed line
* **color** - sets the color of the message arrow
* **head\_type** - determines the shape of the arrow head
* **receiver** - the entity receiving the message at the pointy end of the arrow, usually a participants lifeline
* **message\_text** - the text that appears with the message arrow

### Senders & Receivers

Senders and receivers are usually the participants with lifelines discussed in the previous section. There are a few exceptions. Messages that come from or go to places outside the scope of the current diagram have gates as their sender or receiver at the edge of the diagram. Other messages may get lost or we may not know where they come from. These lost and found messages are sent or received from a circle. See the list of senders and receivers below.

* **name** - the name of a lifeline
* \[ - signifies a gate touching the left side of the sequence diagram can be a sender or receiver
* ] - signifies a gate touching the right side of the diagram can be a sender or receiver
* o - used as the **sender** of a found message or the **receiver** of a lost message, this is a lower-case letter o

#### Example: Sender & Receiver

