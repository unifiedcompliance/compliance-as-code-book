# Organization

PlantUML provides many organizational options for sequence diagrams. There are tools for visually grouping information. It even has a nice page break option in case you need to print, make a pdf, or a presentation.

## Title

Titles are created with the **title** command followed by the **text** for the diagram title. Title supports creole syntax for emphasis and markup language for color and emphasis. You can define colors with a standard color name or hex code.&#x20;

Titles can be single line or multiline. Use **\n** for manual line breaks. For automatic line breaks use the **end title** command. You will need to define color and emphasis for every line break.

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

## Header & Footer with Page Numbers

You can add a header and footer with the words **header** and **footer**. Follow each with the desired **text**. You can use creole for emphasis in the header. &#x20;

This is a great place to use the values of **%page%** and **%lastpage%**. We will use a page break here to show that the page values are working. For more on this, see [Page Break](organization.md#page-break) below.

#### Example: Header & Footer with Page Numbers

```
@startuml
'Example: Header and Footer with Page Numbers 

'Add a header.
'Use creole for emphasis.
header **Header** __Text__

'Add a footer with page number variables.
footer Page %page% of %lastpage%

'Send some messages and replies.
Sean  ->  Maria : Text
Sean  <-- Maria : Text
Maria ->  Zarek : Text

newpage

Maria <-- Zarek : Text
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Header and Footer with Page Numbers](../../../../.gitbook/assets/Organization04\_header.png)

![Header and Footer with Page Numbers](../../../../.gitbook/assets/Organization04\_header\_001.png)

## Page Break

You can add a page break with the **newpage** command. This command has an optional **text** field. The **text** field will change the **title** of the new page. This **text** field is not as robust as an actual **title**. To create a multiline **title** here you must use manual **\n** line breaks. It does support creole syntax for emphasis and markup language for color and emphasis. You can define colors with a standard color name or hex code. You will need to define color and emphasis for every line break.

#### Example: Page Break

```
@startuml
'Example: Page Break

'Add a title.
title
Original
Title
Text
end title

'Send some messages and replies.
Sean  ->  Maria : Text
Sean  <-- Maria : Text
Maria ->  Zarek : Text

'Make a page break with a new multiline title.
'Emphasize and color the title.
newpage <font color=561D5E><b>New</b></font>\nTitle\nText

'Send some messages and replies.
Maria <-- Zarek : Text
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Page Break 1 of 2](../../../../.gitbook/assets/Organization05\_page\_break.png)

![Page Break 2 of 2](../../../../.gitbook/assets/Organization05\_page\_break\_001.png)

## Dividers

You can add dividers to a sequence diagram with four equal signs. The divider has an optional text field. To utilize **text** place it in the middle of the equal signs. The divider supports ||| To create a multiline **divider** use manual **\n** line breaks. The **divider** supports creole syntax for emphasis and markup language for color and emphasis. You can define colors with a standard color name or hex code. The default font for dividers is bold so adding code for bold emphasis will do nothing.

#### Example: Dividers

```
@startuml
'Example: Organization

'Send a message from Sean to Maria and a reply.
Sean  ->  Maria : Text
Sean  <-- Maria : Text

'Make a divider with no text.
====

'Send a message from Maria to Zarek and a reply.
Maria ->  Zarek : Text
Maria <-- Zarek : Text

'Make a divider with multiline text.
'Add emphasis and color.
== //Divider//\n<font color=561D5E>Text</font> ==

'Send a message from Zarek to Sean and a reply.
Zarek ->  Sean : Text
Zarek <-- Sean : Text

@enduml
```

![Dividers](../../../../.gitbook/assets/Organization06\_Divider.png)

## Spacing

## Delays

## Boxes

## Time Duration

