# Icons

### Participants

The icons in a sequence diagram are called participants. These can be declared by simply typing "participant" followed by the name of the participant.

```
@startuml

'declare the participant then names it "Sean"
participant Sean

@enduml
```

![A participant named Sean](../../../../.gitbook/assets/01Participant.png)

### Participant Types

There are eight participant types.

* participant
* actor
* boundary
* control
* entity
* database
* collections
* queue

```
@startuml

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

![The eight types of participants](../../../../.gitbook/assets/02ParticipantTypes.png)

### Participant Colors

Participants can be given specific colors by adding hex codes to the end of the participant declaration. Participants can be filled with gradients if two colors are used. The participant text can also be changed by using the "as" command. Notice on line seven that these colors can be used on any of the participant icons.

```
@startuml

'This makes Sean's background color cyan.
participant Sean #Cyan

'This makes Zarek's background red.
actor Zarek #FF0000

'The portion in quotes changes Maria's text color and changes the internal text. 
'The hex codes make a purple to black gradient in her background.
participant Maria as "<color:#White>Mia" #561D5E/000000

@enduml
```

![Participants in many colors](../../../../.gitbook/assets/06ParticipantColors.png)

### Participant Text

Participant text can be declared in a text string inside of quotation marks. It can be separated into multiple lines by using a line break and even altered with creole formatting. As of the time of this writing monospace is not supported for participant text.

```
@startuml

'Example of a string as a name.
participant "Sean The New Guy" 

'Example of bold text using creole.
participant "Maria **The Closer**"

'Example of multiline text for a participant
participant "Zarek \nThe Guy With \nCurly Hair"

'All available creole options.
participant  "**Bold** \n//Italics// \n__underline__ \n--strikethrough-- \n~~waved~~"

@enduml
```

![Long text, multiline, and creole formatted participant text](<../../../../.gitbook/assets/07 ParticipantTextFormatting.png>)
