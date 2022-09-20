# REGEX Tutorial - Matching an Email

Introductory paragraph (replace this with your text)

## Summary
Regular expressions are sequences of metacharacters, denoting a pattern. These patterns can be of various kinds: a mix of letters with digits, special characters and different language characters.
One common way to use regex is to use it to identify if a use has entered something correctly in a form such as an email. 


The regex in this tutorial will be used to match an email.


* Matching an Email: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

In the example above: 
The anchor `^` shows we are at the beginning of the string. 

+ means 1 or more of previous expression.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Anchors are the first and last elements in a regex.  
The first anchor `^` signifies that it is the start of the string. </br>
The last anchor `$` signifies that it is the end of the string. </br>
In this regex it shows that we are starting with `^([a-z0-9_\.-]+)` and ending with `([a-z\.]{2,6})$`.
### Quantifiers
This regex uses two quantifiers `{2,6}` and `+`. </br>
In `([a-z0-9_\.-]+)` and `([\da-z\.-]+)` means that any character within the brackets should match one or more times.  </br>
The quantifier `{2,6}` is looking for a string between 2 -6 characters for `[a-z\.]`.

### Character Classes
The character class used in this regex is `\d` which matches any single digit from 0-9. 

### Flags

### Grouping and Capturing
The way that you group a section of a regex is by using parenthesis `()`.
In our regex the first capturing group would be `([a-z0-9_\.-]+)`, the second group would be `([\da-z\.-]+)` and the last group would be `([a-z\.]{2,6})`.

### Bracket Expressions
Anything inside the brackets `[]` represent the characters we want to match. 
The pattern does not require the string to follow every one of the requirements, it just shows which ones are accepted.
Since regex is case sensitive `[a-z0-9_\.-]` shows that we want to match any lowercase letter from a-z. 
It will also accept any number from 0-9 and any special character such as an underscore, backslash, period, or hyphen.


### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
