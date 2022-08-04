---
title: ascii-art
description: 
published: true
date: 2022-08-04T21:10:04.788Z
tags: 
editor: markdown
dateCreated: 2022-08-04T16:20:23.888Z
---

```{=mediawiki}
{{Infobox Project
|name = ascii-art
|require = [[go-reloaded]]
|xp = 6.13 kB
|members = 2 -> 3
|type = Basic
}}
```
Ascii-art is a program which consists in receiving a string as an
argument and outputting the string in a graphic representation using
ASCII. Time to write big.

What we mean by a graphic representation using ASCII, is to write the
string received using ASCII characters, as you can see in the example
below:

``` html5

@@@@@@BB@@@@``^^``^^``@@BB$$@@BB$$
@@%%$$$$^^^^WW&&8888&&^^""BBBB@@@@
@@@@@@""WW8888&&WW888888WW``@@@@$$
BB$$``&&&&WWWW8888&&&&8888&&``@@@@
$$``&&WW88&&88&&&&8888&&88WW88``$$
@@""&&&&&&&&88888888&&&&&&88&&``$$
``````^^``^^^^^^````""^^``^^``^^``
""WW^^@@@@^^``````^^BB@@^^``^^&&``
^^&&^^@@````^^``&&``@@````^^^^&&``
``WW&&^^""``^^WW&&&&""``^^^^&&88``
^^8888&&&&&&WW88&&88WW&&&&88&&WW``
@@``&&88888888WW&&WW88&&88WW88^^$$
@@""88&&&&&&&&888888&&``^^&&88``$$
@@@@^^&&&&&&""``^^^^^^8888&&^^@@@@
@@@@@@^^888888&&88&&&&MM88^^BB$$$$
@@@@@@BB````&&&&&&&&88""``BB@@BB$$
$$@@$$$$$$$$``````````@@$$@@$$$$$$
```

-   This project should handle an input with numbers, letters, spaces,
    special characters and \\n.
-   Take a look at the ASCII manual.

## Instructions

-   Your project must be written in **Go**.
-   The code must respect the **good practices**.
-   It is recommended that the code present a **test file**.
-   Some **banner** files with a specific graphical template
    representation using ASCII will be given. The files are formatted in
    a way that is not necessary to change them.
    -   shadow
    -   standard
    -   thinkertoy

## Banner Format {#banner_format}

-   Each character has a height of 8 lines.
-   Characters are separated by a new line `\n`.
-   Here is an example of \' \', \'!\' and \'\"\'(one dot represents one
    space) :

\...\... \...\... \...\... \...\... \...\... \...\... \...\... \...\...

.\_.. \|.\|. \|.\|. \|.\|. \|\_\|. (\_). \.... \....

.\_.\_.. (.\|.). .V.V.. \...\... \...\... \...\... \...\... \...\...

```{=html}
</syntaxhighlight>
```
## Allowed packages {#allowed_packages}

Only the [standard Go packages](Go_standard_library "wikilink") are
allowed

## Reading Material {#reading_material}

-   [2D-arrays](2D-arrays "wikilink")
