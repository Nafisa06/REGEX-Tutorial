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

The characters ^ and $ are both considered to be anchors.

The ^ anchor signifies a string that begins with the characters that follow it. This could be in one of two formats; exact string matches (e.g. ^This, where the strings "This" or "This cat" match and is case sensitive) or a range of possible matches displayed using bracket expression, as in the regex described in this tutorial: ([a-z0-9_\.-]+)

The $ anchor signifies a string that ends with the characters that precede it. Similar to the ^ character, it can be preceded by an exact string or a range of possible matches. In this regex, it matches string ending with ([a-z\.]{2,6}). The anchors ^ and $ force the regex to find its match at the start and end of the subject text, respectively. Placing the whole regex between these characters effectively requires the regex to match the entire subject. This is important when validating user input as without the anchors, all the previous regex will match because they find the strings in the middle of the given text.


### Quantifiers

Quantifiers set the limits of the string that the regex matches, or an individual section of the string. They frequently include the minimum and maximum number of characters that the regex is looking for.

The + quantifier matches the preceding element one or more times. It is equivalent to {1,}. + is a greedy quantifier whose lazy equivalent is +?.

In this regex, it corresponds to [a-z0-9_\.-] and [\da-z\.-].    

The {n} quantifier matches the preceding element exactly n times, where n is any integer. {n} is a greedy quantifier whose lazy equivalent is {n}?.

[a-z\.]{2,6} matches 2 to 6 characters that match the bracket expressions.

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
