# REGEX Tutorial - Matching an Email

This tutorial will explain how regex can be used to match an email by discussing important concepts used in regular expressions and using examples.

## Summary
Regular expressions are sequences of metacharacters, denoting a pattern. These patterns can be of various kinds: a mix of letters with digits, special characters and different language characters. One common way to use regex is to use it to identify if a user has entered something correctly in a form such as an email. 

We will be using the following regex as an example:</br>

 `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Example of accepted email: </br>
`lu_cia-22@gmail.net.ar`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Character Escapes](#character-escapes)


## Regex Components

### Anchors
Anchors are the first and last elements in a regex.  
The first anchor `^` signifies the start of the string. </br>
The last anchor `$` signifies the end of the string. </br>
For example, in this regex it shows that we are starting with `^([a-z0-9_\.-]+)` and ending with `([a-z\.]{2,6})$`.

### Quantifiers
This regex uses two quantifiers `{2,6}` and `+`. </br>
In `([a-z0-9_\.-]+)` and `([\da-z\.-]+)` means that any character within the brackets should match one or more times.  </br>
The quantifier in `([a-z\.]{2,6})` is looking for a string between 2 -6 characters.

Examples of accepted values for `([a-z\.]{2,6})`: 
* com
* net.ar

### Character Classes
Character class in a regex defines a set of characters. The character class used in this regex is `\d` which matches any single digit from 0-9. 

Examples of accepted values for `([\da-z\.-]+)`: 
* gmail
* gmail90
* gmail-90

### Grouping and Capturing
Since regular expressions can get complicated, one way to check multiple parts is to group them by sections. </br>
The way that you group a section of a regex is by using parenthesis `()`. </br>
Each section within a parenthesis is known as a subexpression or grouping constructs.</br>
For example, in our regex the first group would be `([a-z0-9_\.-]+)`, the second group would be `([\da-z\.-]+)` and the last group would be `([a-z\.]{2,6})`.


### Bracket Expressions
Anything inside the brackets `[]` represent the characters we want to match. </br>
The pattern does not require the string to follow every one of the requirements, it just shows which ones are accepted.</br>
We can use the group `([a-z0-9_\.-]+)` as an example.
Since regex is case sensitive this example shows that we want to match any lowercase letter from a-z. </br>
The regex will also accept any number from 0-9 and any special character such as an underscore, backslash, period, or hyphen.

## Character Escapes
The `\` backslash is used to escape a special character that would otherwise be interpreted literally. </br>
The backslash is used 3 times in our regex to escape the period. One example of this is in the first group `([a-z0-9_\.-]+)`.

## Author
The tutorial was made by Lucia Gil.
If you have any questions, please [email](mailto:${luciagil5952@gmail.com}) me.
For my repository, please visit my [github](https://github.com/LuciaMGil).
