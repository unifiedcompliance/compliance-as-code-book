# Organization

### Participant Order

Participants can be placed in a specific order with the "order" command regardless of the order in which they are declared.

```
@startuml

'Declare participants
participant "Maria the middle child" order 2
participant "Sean the youngest" order 3
participant "Zarek the oldest" order 1

@enduml
```

![Ordered participants](../../../../.gitbook/assets/11Order.png)

### Sequence Auto-numbering

Sequences can be automatically numbered with the "autonumber" command. They start at number one as a default but can be given a different starting value. \***can these values be negative?**\* They can also be given an increment value.

```
@startuml

'The command to start the auto-numbering sequence
autonumber

'Declare participants
participant Maria
participant Sean
participant Zarek

'With no further parameters, these will be messages 1 and 2
Maria -> Sean : Text
Maria <- Sean : Text

'This command starts the auto number sequence and gives a starting value of 10
autonumber 10

'These two sequences will be numbered 10 and 11
Sean -> Zarek : Text
Sean <- Zarek : Text

'This command starts the auto number sequence at 20 
'And tells the program to go up by increments of 5
autonumber 20 5

'These two sequences will be numbered 20 and 25
Zarek -> Maria : Text
Zarek <- Maria : Text

@enduml
```

![Auto-numbered sequences](../../../../.gitbook/assets/12SequenceNumbering.png)

### Stopping and Resuming Auto-numbers

Autonumbering can be turned off and on using the keywords "stop" and "resume."

```
@startuml

'Declare participants
participant Maria
participant Sean
participant Zarek

'The sequences following this line will be auto-numbered
autonumber

Maria -> Sean : Text
Maria <- Sean : Text

'The sequences following this will not be auto-numbered
autonumber stop

Sean -> Zarek : Text
Sean <- Zarek : Text

'The sequences following this will resume the previous count
'Then increase by an increment of 10
autonumber resume 10

Zarek -> Maria : Text
Zarek <- Maria : Text

@enduml
```

![A break in auto-numbering](../../../../.gitbook/assets/14StopResumeAutonumbering.png)

### Formatting Auto-numbers

Double quotes allow formatting options for auto-numbers. Parentheses, brackets, and leading words can be added to auto-numbers. Default number format can be adjusted with zeroes and hash marks similar to Java's decimal format. Color and emphasis are similar to formatting in HTML.

```
@startuml

'Declare participants
participant Maria
participant Sean
participant Zarek

'The auto numbers following this line will be bold, 
'wrapped in square brackets, and have three digits regardless of value.
autonumber "<b>[000]</b>"

Maria -> Sean : Text
Maria <- Sean : Text

'The auto numbers following this line will be underlined,
'wrapped in parentheses, and will have no extra zeroes as place holders.
autonumber 10 "(<u>#</u>)"

Sean -> Zarek : Text
Sean <- Zarek : Text

'The auto numbers following this line will be italicized,
'red and lead by "Leading Words"
autonumber 20 5 "<font color=red><i>Leading Words #</i></font>"

'These two sequences will be numbered 20 and 25
Zarek -> Maria : Text
Zarek <- Maria : Text

@enduml
```

![Formatted auto-numbers](../../../../.gitbook/assets/13FormattingAutoNumbers.png)
