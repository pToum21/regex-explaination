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
Grouping constructs are used to group characters together. They are grouped by using parentheses. Using grouping constructs allows the ability to treat one or more characters as a single unit.

```
^([a-z0-9_\.-]+)
```
This captures the username part of the email address

```
([\da-z\.-]+)
```
 This captures the domain part of the email address.

 ```
 ([a-z\.]{2,6})
 ```
 This captures the top-level domain (TLD) part of the email address. 

 The grouping constructs ( ) are used to capture specific parts of the email address, allowing you to extract and work with the username, domain, and TLD separately.

### Bracket Expressions

### Character Classes
```
[a-z0-9_\.-]
```
This character class matches a single character that is either a lowercase letter (a-z), a digit (0-9), an underscore (_), a dot (.), or a hyphen (-).

```
[\da-z\.-]
```
### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
