# Regex: Confirming Email Addresses

This tutorial will describe how the following rejex, short for regular expression, confirms the characters of a person's email addresses. 

## Summary

The regex I will be using in this tutorial is:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This line helps define a specfic search pattern that will return a match for email formating. Each seperate component of this regex enforces that a user enters a correct email address that follows the following pattern: email@website.com.


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
This tutorial uses literal notation when constructing the regex object.

### Anchors

Anchors are unique characters in a regex expression. They do not meet any of the qualified characters and indicate the qualified character's position.  

**REGEX:** `/ ^ ([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6}) $ /`

In this snippet, the ^ and $ represent anchors. These anchors help the search engine determine the beginning and end of the email address. 

### Quantifiers

Quantifiers determine how many times the characters, phrases, groups, etc. can be repeated.

In this tutorial, the only quantifier used is **+**. This quantifier ensures that the code after the symbol matches the code before it.

**REGEX:** `/^([a-z0-9_\.-] + )@([\da-z\.-] + )\.([a-z\.]{2,6})$/`

    name + @website + .domain

### Grouping Constructs

Grouping Constructs help capture the substrings within the expression. In this tutorial, the parenthesis are the grouping constructs, and each set of parenthesis dictate a seperate group. To determine the seperate strings within the email see the following breakdown of the snippet: 

**REGEX**:  `/^ ([a-z0-9_\.-]+) @ ([\da-z\.-]+) \. ([a-z\.]{2,6}) $/` 

    ( name ) @ ( website ) . ( domain )


### Bracket Expressions

Bracket expressions are characters, [], that help determine if characters can or can not be included in the email. 

**REGEX**:  `/^( [a-z0-9_\.-] +)@( [\da-z\.-] +)\.( [a-z\.] {2,6})$/` 

For example, within the first bracket expression the we can conclude the following: 

    [a-z0-9_\.-] 
       a-z: only lower case letters
       0-9: all numbers 
       _\.-: only the state characters apply 

### Character Classes

Character Classes help you describe the alphanumeric character set that is included within the email. For example, in the email matching regex we use a-z and 0-9 which includes all numbers and lowercase letters. 

**REGEX**:  `/^( [a-z0-9_\.-] +)@( [\da-z\.-] +)\.( [a-z\.] {2,6})$/`

    [a-zA-Z]: all characters
    [0-9]: all numbers
    [a-z]: all lowercase
    [A-Z]: all uppercase 
    \d: matches one digit
    \. : matches a one period  



## Author

The author is, Hannah Culver-Zawislak. A student at Georgia Tech's Full Stack Bootcamp. 

https://github.com/hculv 

Preview: https://github.com/hculv/email-matching-regex/blob/main/gist-regex.md
