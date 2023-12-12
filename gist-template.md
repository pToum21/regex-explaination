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
A Braket Expression in regular expressions is a set of characters enclosed within square brackets [ ]. It represents a single character that must match any one of the characters listed inside the brackets.
```
[a-z0-9_\.-]
```
This Bracket expression matches a single character that is either a lowercase letter (a-z), a digit (0-9), an underscore (_), a dot (.), or a hyphen (-).

```
[\da-z\.-]
```
This Bracket expression matches a single character that is either a digit (\d), a lowercase letter (a-z), a dot (.), or a hyphen (-).

```
[a-z\.]
```
This Bracket expression matches a single character that is either a lowercase letter (a-z) or a dot (.).

### Character Classes
Character classes are specific notation to denote matches of symbols in a certain group. [a-z] a-z A single character between a and z that is case sensitive. [0-9] 0-9 A single character between 0-9.
```
\d
```
This is a shorthand character class that matches any numerical digit (0-9), it is used in the second capturing group: ([\da-z\.-]+) to allow digits in the domain part.

### The OR Operator
The OR operator in regex is defined by using the pipe symbol:
```
|
```
In this example for checking emails there is not a need for an or operator because it is made to match a specific pattern for email addresses.

### Flags
Flags modify how the pattern matching is performed, they re often used to control case sensitivity, enable multi-line mode, and more.

Examples of flags are as follows:
```
i
```
Case-insensitive:
The i flag allows matching of both uppercase and lowercase letters in a case-insensitive manner.
```
g
```
Global:
Finds all matches in the input string, not just the first one.
```
m
```
Multi-line:
Allows the ^ and $ anchors to match the start/end of each line in a multi-line string.
```
u
```
Unicode:
Enables full Unicode matching, including support for Unicode escape sequences.
### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
