# Regex BreakDown: Matching an Email
This BreakDown is designed to help a user understand this regex statment for future use.

## Summary
This is the regular expression, or regex to match an email:
```
^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$
```
This regular expression ensures that an email address adheres to the standard format of "username@domain.tld"

## Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
The anchors in a regular expression define the position within the input where a match must occur.

The caret symbol asserts the beginning of the string. It indicates that the pattern following it must start at the beginning of the input.
```
^
```
The dollar sign asserts the end of the string. It indicates that the pattern preceding it must end at the end of the input.
```
$

```
Combining the two in this statement saays the email most fit the defined pattern and cannot be a larger string.

### Quantifiers
In the email regex statment there are only two quantifiers and they are as follows: 

Quantifiers in regular expressions define the number of occurrences of a character or a group of characters.
```
+
```
The plus quantifer means one or more occurrences of the characters within the square brackets.

```
{2,6}
```
The Curly Braces Quantifier means between 2 and 6 occurrences of the characters within the square brackets.  The reason it would be 2 or 6 is because we passed that into the brackets but that is up to the devoloper as to the number passed.


### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
