# Regex Tutorial- Matching an email address

Regex, or regular expressions are useful in extracting information from any text by searching for one or more matches of a specific search pattern. They are also frequently used to validate input. In this tutorial, I will explain a regex functions by breaking down each part of the expression and describing what it does.

## Summary

In this tutorial, I will be describing the following expression: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. This regex can be used to verify that a user input is a valid email address. 

Each part of this regex has an unique responsibility to make sure that an user enters an email address that begins with an unspecified number of characters preceding the @ symbol, followed by a domain.


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

Regex are made up of several components. A regex is considered a literal, so the pattern must be wrapped in slash characters (/), as below.
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The above regex includes the following:
 

Anchors ^ $
Captures and Groups ([a-z0-9_\.-]+)
Quantifiers + {}
Bracket Expressions [ ]
Character Classes [a-z\d] etc

These components will be described with greated detail below.


### Anchors



### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
