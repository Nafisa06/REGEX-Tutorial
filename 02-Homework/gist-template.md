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

The primary way to group a section of a regex is by using parentheses (()). Each section within parentheses is known as a subexpression. A part of a pattern can be enclosed in parentheses (...). This is called a “capturing group”. This effects the regex in two ways.

- It allows finding a part of the match as a separate item in the result array.
- A quantifier after the parentheses applies to the parentheses as a whole.

### Bracket Expressions

A bracket expression is either a matching list expression or a non-matching list expression. It consists of one or more expressions: ordinary characters, collating elements, collating symbols, equivalence classes, character classes, or range expressions.

/^[a-zA-Z0-9._\.-]+  means that the email address must begin with alpha-numeric characters. "a-zA-Z" means both lowercase and uppercase characters are allowed. "0-9" matches any single-digit integer. It may have periods,underscores and hyphens.


@ means that there must be a ‘@’ symbol after initial characters.

In [\da-z\.-]:


\d matches a single character that is a integer/digit.


a-z matches any lowercase letter.

\.- matches the symbols \, ., or -.  

\.: After the second group of characters there must be a period (‘.’). This is to separate domain and subdomain names.

[a-z\.]{2,6}$/ means that the email address must end with two to six alphabets. Having a-z means that only lowercase letters are allowed. Whereas \. matches a single period.

{2,6} indicates the minimum and maximum number of characters. This will allow domain names with 2, 3, 4, 5 and 6 characters.

Everything in a bracket is grouped and read together for validation.  


### Character Classes

A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match. 

\d - Matches a single character that is a digit.  


\. - Matches a single period.


### The OR Operator

The OR operator in regex works by searching for either one value or another. 

For example: [K|C]+atherine will match to either Katherine or Catherine.

There are no OR operators in the above example.

### Flags

Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex. There are six optional flags that can be used, either separately or together and in any order. There are no flags in this regex example.

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
