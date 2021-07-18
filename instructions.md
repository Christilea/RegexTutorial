# Regex Tutorial 2021

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [](#)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Grouping Constructs](#grouping-constructs)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
    - [The OR Operator](#the-or-operator)
    - [Flags](#flags)
    - [Character Escapes](#character-escapes)
  - [Author](#author)
## Regex Components

In our code we are using multiple parenthesis``` ()``` , brackets``` []``` , a caret``` ^``` , double backslashes``` \\``` , the letter s, the plus operator``` +``` , a period``` .``` , multiple question marks``` ?``` , the letter i, our file extension names``` jpe?g,png,gif,bmp``` , the pipe character``` |``` , and a dollar sign``` $```. By arranging these characters like they are below, we are telling the computer to perform our explicit task.

```([^\\s]+(\\.(?i)(jpe?g|png|gif|bmp))$)``` 

### Anchors
The final part before our closing parenthesis is the dollar sign ```$```. This declares the end of our string is where our file extension needs to exist. This is mandatory in order for it to become a valid file name and type.
Some anchors include:

- \G: defines the starting point of a search; useful along with the /g flag
- \A: matches the start of a string
- \Z: matches the end of a string
- \z: similar to \Z, but the main difference is that it will not match before a trailing newline at the end of a string
- \b: used to match a word matched by \w and a word not matched by \w
- \B: used to match the position between characters matched by \w


### Quantifiers

### Grouping Constructs
Groups are quantified by parenthesis ```()```. Here we are wrapping our entire expression in a group, but first we group inside the main part of our expression what we need to eliminate (white space) as well as our rules to determine at least one one character is being used. Finally we group our evaluator to determine that in-fact our filetype is proceeded with a period, followed by a proper extension type.

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
