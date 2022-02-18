# Organization

PlantUML provides many organizational options for sequence diagrams. There are tools for visually grouping information. It even has a nice page break option in case you need to print, make a pdf, or a presentation.

## Title

Titles are created with the **title** command followed by the **text** for the diagram title. Title supports creole syntax for emphasis and markup language for color and emphasis. You can define colors with a standard color name or hex code.&#x20;

Titles can be single line or multiline. Use **\n** for manual line breaks. For automatic line breaks use the **end title** command.

Titles can also contain images. Use the **\<img>** markup tag to insert images in the title text. You can adjust the size of the image with the **{scale}** property.

#### Example: Title With Manual Line Breaks and Creole

```
@startuml
'Example: Title With Manual Line Breaks and Creole

'Create a multiline title with manual line breaks.
'Use creole to emphasize the text.
title **Title** \n__Text__

'Send some messages and replies.
Sean  ->  Maria : Text
Sean  <-- Maria : Text
Maria ->  Zarek : Text
Maria <-- Zarek : Text
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Title With Manual Line Breaks and Creole](../../../../.gitbook/assets/Organization01\_title\_manual\_lines.png)

#### Example: Title With Automatic Line Breaks and Markup

```
@startuml
'Example: Title With Automatic Line Breaks and Markup

'Create a multiline title with automatic line breaks.
'Use markup to emphasize and color the text.
title 
<u:red><font color=cyan>Title</font></u>
<font color=561D5E><b> Text </b></font>
end title

'Send some messages and replies.
Sean  ->  Maria : Text
Sean  <-- Maria : Text
Maria ->  Zarek : Text
Maria <-- Zarek : Text
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Title With Automatic Line Breaks and Markup](../../../../.gitbook/assets/Organization02\_title\_auto\_lines.png)

#### Example: Title Image

```
@startuml
'Example: Title With Images

'Create a multiline title with automatic line breaks.
'Add text and an image with different sizes.
title 
An Image
<img:https://www.unifiedcompliance.com/wp-content/themes/tardigrade//images/cch_logo_icon.png>

A Resized Image
<img:https://www.unifiedcompliance.com/wp-content/themes/tardigrade//images/cch_logo_icon.png{scale=0.5}>
end title

'Send some messages and replies.
Sean  ->  Maria : Text
Sean  <-- Maria : Text
Maria ->  Zarek : Text
Maria <-- Zarek : Text
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Title With Images](../../../../.gitbook/assets/Organization03\_title\_images.png)

## Header

## Footer

## Spacing

## Delays

## Boxes

## Time Duration

## Page Break

## Divider

