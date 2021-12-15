# Frames, Panes, Windows, Pages

We’ve seen what we are going to call a _frame_ also called a _window_ (or _pane_ within a window), or even _pages_. The _frame_ is where your content lives within your application. When designing frames, there are several formats you can design for; phone, tablet, desktop, presentation, watch, paper, or social media. For now, we are going to ignore all but one format – the desktop.

## Desktop format

Desktop formats for a frame have some standard sizes.

Desktop – 1440 x 1024

Surface Book – 1500 x 1000

MacBook – 1152 x 700

MacBook Pro – 1440 x 900

iMac – 1280 x 720

For our purposes we will design for the desktop. But we have to make a slight modification because when designing for the user working in a browser on a desktop, you don’t get to use _all of that space._ For anyone who is saving bookmarks, their browser will steal 112 px of horizontal space within the format, leaving 912 px for horizontal space as shown below.

![Standard desktop format](<../../.gitbook/assets/0 (1)>)

### **Balsamiq**

Balsamiq doesn’t have a concept of frames. Everything you do in Balsamiq is designed within their various pages _freeform_. But they _do_ have a **Window** element that you can drag into your page and design _within_. You’ll have to size it appropriately. Below is an example of the Balsamiq window with the appropriate sizing (1440 x 1013) that will produce the appropriate 1440 x 912 interior.

![Balsamiq Window properly sized](<../../.gitbook/assets/1 (1) (1)>)

### **Figma**

Within Figma they have a concept of frames. To create the proper desktop sized frame start by selecting Frame > Desktop, which will create the 1440 x 1024 frame. Then shorten the height to 912 to get the appropriately sized frame.

![Figma Desktop frame](../../.gitbook/assets/2)

#### Layout grids

Balsamiq doesn’t support grids, so this one is just for Figma. You are going to want to have multiple grids on your frame – one for coulmns and the other a standard baseline grid.

**12 column grid**

We’ve found that the most versatile column grid is a 12 column grid with a 64 px margin and a 16 px gutter, as shown below.

![12 column grid](../../.gitbook/assets/3)

**8 px baseline grid**

A baseline grid is one that’s established from the baselines your typography sits on. These appear as visual aids in your design spanning the width of your design and repeating vertically at an even internal. In many design systems, such as [Google’s Material Design](https://material.io/design/layout/spacing-methods.html#baseline), the baseline grid is a foundational part of defining type size and line-height parings, as well as spacing for margins and padding. We overlay this on top of the column grid as shown below.

![8 px baseline grid overlayed on 12 column grid](<../../.gitbook/assets/4 (1) (1)>)
