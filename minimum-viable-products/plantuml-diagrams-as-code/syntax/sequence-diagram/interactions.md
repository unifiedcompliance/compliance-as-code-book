# Interactions

PlantUML gives us seven common interactions as well as a customizable interaction. Five of these interactions behave the same. The other three will require separate explanations.



## Basic Declaration

Interactions are declared with a keyword similar to notes. They are closed with the command word **end**.

#### Example: Interactions Declaration

```
@startuml
'Example: Interactions Declaration

'Declare the opt interaction.
opt

    'Send a message from Sean to Maria and a reply.
    Sean  ->  Maria : Text
    Sean  <-- Maria : Text

'Close the opt interaction
end

'Send a message from Maria to Zarek and a reply.
Maria ->  Zarek : Text
Maria <-- Zarek : Text

'Send a message from Zarek to Sean and a reply.
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Interaction Declaration](../../../../.gitbook/assets/Interactions01\_declaration.png)

## Basic Properties

The five similar interactions have two properties. Only the **operator** is required.

* operator - determines the type of interaction
* header - allows for a message at the top of the body of the interaction

### Operator

The **operator** determines the type of interaction. The **operator** or interaction type is displayed in the upper left corner of the interaction in the sequence diagram. The following five **operators** are also the five similar interactions in PlantUML.&#x20;

* opt
* loop
* par
* break
* critical

You can place interactions within interactions by using more than one **operator** before closing with the **end** command.

#### Example: Interaction Operator

```
@startuml
'Example: Interaction Operator

'Declare the opt interaction.
opt

    'Send a message from Sean to Maria and a reply.
    Sean  ->  Maria : Text
    Sean  <-- Maria : Text

    'Declare the loop interaction.
    loop

        'Send a message from Maria to Zarek and a reply.
        Maria ->  Zarek : Text
        Maria <-- Zarek : Text

    'Close the loop interaction.
    end

'Close the opt interaction.
end

'Send a message from Zarek to Sean and a reply.
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Interaction Operator](../../../../.gitbook/assets/Interactions02\_operator.png)

### Header

The **header** property defines optional text at the top of the interaction body.

#### Example: Interaction Header

```
@startuml
'Example: Interaction Header

'Declare the opt interaction.
'Add a header.
opt Opt Header

    'Send a message from Sean to Maria and a reply.
    Sean  ->  Maria : Text
    Sean  <-- Maria : Text

    'Declare the loop interaction.
    'Add a header.
    loop Loop Header

        'Send a message from Maria to Zarek and a reply.
        Maria ->  Zarek : Text
        Maria <-- Zarek : Text

    'Close the loop interaction.
    end

'Close the opt interaction.
end

'Send a message from Zarek to Sean and a reply.
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Interaction Header](../../../../.gitbook/assets/Interactions03\_header.png)

## Customizable Interaction

The **group** command allows us to create our own **operator**. It also has an optional **header**. The **header** must be enclosed by square brackets.

#### Example: Customizable Interaction

```
@startuml
'Example: Customizable Interaction

'Declare an interaction with a custom operator.
'Add a header.
group search [Search Header]

    'Send a message from Sean to Maria and a reply.
    Sean  ->  Maria : Text
    Sean  <-- Maria : Text

    'Declare an interaction with a custom operator.
    'Add a header.
    group find [Find Header]

        'Send a message from Maria to Zarek and a reply.
        Maria ->  Zarek : Text
        Maria <-- Zarek : Text

    'Close the second interaction.
    end

'Close the first interaction.
end

'Send a message from Zarek to Sean and a reply.
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Customizable Interaction](../../../../.gitbook/assets/Interactions04\_custom.png)

## Alt/Else

The **alt** interaction behaves like the previous interactions but also has the **else** command word. **Else** can also be followed by an optional **header**.

#### Example: Interaction Alt/Else

```
@startuml
'Example: Interaction Alt/Else

'Send a message from Sean to Maria
Sean  ->  Maria : Text

'Declare an alt interaction.
'Add a header.
alt Success Text

    'Send a reply from Maria to Sean.
    Sean  <-- Maria : Text

'Add an else command with a header.
else Failure Text

    'Send a reply from Maria to Sean.
    Sean  <-- Maria : Text

    'Declare the loop interaction.
    'Add a header.
    loop Loop Header

        'Send a message from Maria to Zarek and a reply.
        Maria ->  Zarek : Text
        Maria <-- Zarek : Text

    'Close the loop interaction.
    end

'Close the alt interaction.
end

'Send a message from Zarek to Sean and a reply.
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Interaction Alt/Else](<../../../../.gitbook/assets/Interactions05\_alt\_else (1).png>)

## Reference

The reference interaction behaves similar to notes. It consists of the command word **ref**, **position**, and **text**. The position will always be **over** one or more lifelines. You can make the text single line with a **:** or multiline by using the **end ref** command. The reference interaction can exist inside of other interactions but it cannot contain messages or other interactions.

#### Example: Interaction Reference

```
@startuml
'Example: Interaction Reference

'Declare the opt interaction.
'Add a header.
opt Opt Header

    'Send a message from Sean to Maria and a reply.
    Sean  ->  Maria : Text
    Sean  <-- Maria : Text

    'Declare a reference interaction.
    'Cover Sean.
    'Add single line text.
    ref over Sean : Reference Text

    'Send a message from Maria to Zarek and a reply.
    Maria ->  Zarek : Text
    Maria <-- Zarek : Text

'Close the opt interaction.
end

'Declare a reference interaction.
'Cover all three lifelines.
'Add multiline text.
ref over Sean, Zarek
Reference

Text
end ref

'Send a message from Zarek to Sean and a reply.
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Interaction Reference](../../../../.gitbook/assets/Interactions06\_ref.png)

