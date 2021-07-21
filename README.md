# Regex Tutorial 2021

A regular expression is a special sequence of characters that describe a pattern of text that should be found, or matched, in a string or document. By matching text, we can identify how often and where certain pieces of text occur, as well as have the opportunity to replace or update these pieces of text if needed.

## Summary

Regular expressions: Regular expressions operate by moving character by character, from left to right, through a piece of text. When the regular expression finds a character that matches the first piece of the expression, it looks to find a continuous sequence of matching characters.

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

Components in our code we are using multiple parenthesis``` ()``` , brackets``` []``` , a caret``` ^``` , double backslashes``` \\``` , the letter s, the plus operator``` +``` , a period``` .``` , multiple question marks``` ?``` , the letter i, our file extension names``` jpe?g,png,gif,bmp``` , the pipe character``` |``` , and a dollar sign``` $```. By arranging these characters like they are below, we are telling the computer to perform our explicit task.

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
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. Nesting quantifiers can increase the number of comparisons that the regular expression engine must perform, as an exponential function of the number of characters in the input string. If the *, +, ?, {, and } characters are encountered in a regular expression pattern the regular expression engine interprets them as quantifiers or part of quantifier constructs unless they are included in a character class. To interpret these as literal characters outside a character class, you must escape them by preceding them with a backslash.

<table>
<tr>
<td>Quantifier</td>
<td>Meaning</td>
</tr>
<tr>
<td><code>*</code></td>
<td>O or more</td>
</tr>
<tr>
<td><code>+</code></td>
<td>1 or more</td>
</tr>
<tr>
<td><code>?</code></td>
<td>O or 1</td>
</tr>
<tr>
<td><code>{3}</code></td>
<td>Exactly 3</td>
</tr>
<tr>
<tr>
<td><code>{3,}</code></td>
<td>3 or more</td>
</tr>
<tr>
<td><code>{3,5}</code></td>
<td>3, 4 or 5</td>
</tr>
<tr>
</table>

### Grouping Constructs
Groups are quantified by parenthesis ```()```. Here we are wrapping our entire expression in a group, but first we group inside the main part of our expression what we need to eliminate (white space) as well as our rules to determine at least one one character is being used. Finally we group our evaluator to determine that in-fact our filetype is proceeded with a period, followed by a proper extension type.

### Bracket Expressions
A bracket expression is either a matching list expression or a non-matching list expression. It consists of one or more expressions: ordinary characters, collating elements, collating symbols, equivalence classes, character classes, or range expressions.
|Below is an example of the character uses|
| ------------------------------------- |
| /^(<b>&nbsp;[a-z0-9_\.-]&nbsp;</b>+)@(<b>&nbsp;[\da-z\.-]&nbsp;</b>+)\.(<b>&nbsp;[a-z\.]&nbsp;</b>{2,6})$/ |


### Character Classes
Character classes allow regular expressions to define a set of characters for finding a match within a given string. 

Common Character Classes Include:
- Positve and Negative Character Groups using Bracket Expressions (`[]`) (discussed above in Bracket Expressions)
- Any Character - using the dot character (`.`) in a regex returns a wildcard character that matches any charcter except for \n, which is used to specify a new line. The bracket expression equivalent is: `[A-Za-z0-9_]`
- Decimal Digit Character - using the slash and d characters (`\d`) matches any numeral digit. The bracket expression equivalent is: `[0-9]`.  Whereas using the slash and D characters (`\D`) matches a non-digit character.
- Word Character - using the slash and w characters (`\w`) matches any alphanumeric character including the underscore.  The bracket expression equivalent is: `[A-Za-z0-9_]`. Whereas using the slash and W characters (`\W`) matches a non-word character.
- Whitespace Character - using the slash and s characters (`\s`) matches a single whitespace character, including tabs and line breaks. Whereas using the slash and S characters (`\S`) matches a non-whitespace character.
  
- |Below is an example of the character uses|
| ------------------------------------- |
| /^<b>&nbsp;(&nbsp;</b>[a-z0-9_\.-]+<b>&nbsp;)&nbsp;</b>@<b>&nbsp;(&nbsp;</b>[\da-z\.-]+<b>&nbsp;)&nbsp;</b>\.<b>&nbsp;(&nbsp;</b>[a-z\.]{2,6})$/ |


### The OR Operator
The Alternation Operator ( | or | )

Alternatives match one of a choice of regular expressions: if you put the character(s) representing the alternation operator between any two regular expressions a and b , the result matches the union of the strings that a and b match.

### Flags
A regex usually comes within this form /abc/, where the search pattern is delimited by two slash characters /. At the end we can specify a flag with these values (we can also combine them to each other):
g (global) does not return after the first match, restarting the subsequent searches from the end of the previous match
m (multi-line) when enabled ^ and $ will match the start and end of a line, instead of the whole string
i (insensitive) makes the whole expression case-insensitive (for instance /aBc/i would match AbC)

### Character Escapes
They are used to treat strings of characters in regular expressions as literals. The most common character escapes include "\r" for carriage return, "\n" for new line, "\v" for vertical tab, "\t" for a tab, "\f" for form feed, and "\xNN" for hexadecimal numbers. It also includes the classes discussed in the [Character Classes](#character-classes) section, namely:

- \d: used to specify a class composed of digit characters
- \D: used to specify a class of characters that is not composed of digits
- \w: used to specify a sequence of characters, or a word
- \W: used to specify a sequence of characters, except a word

Character Escapes are useful when handling regular expressions in strings that already include the "\" or the "/" characters; for example, when evaluating strings representing files within folders, or URL addresses.

## Author
My name is Christi Lea. I am currently studying to be a software engineer. Here is my github link. [github.com/Christilea].
# References

* [Regular Expressions cheat sheet](http://web.mit.edu/hackl/www/lab/turkshop/slides/regex-cheatsheet.pdf)
