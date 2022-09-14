# Matching an Email - Regex Tutorial

The following tutorial is designed to explain the use of Regular Expressions (regex) for matching an email. 

## Summary

Regular Expressions is a sequence of characters that defines a search pattern. 

 > /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
/**^**([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})**$**/

Anchors start and end the expression. `^` indicates the beginning and `$` indicates the end of the expression.  

### Quantifiers
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
 > /^([a-z0-9_\.-]**+**)@([\da-z\.-]**+**)\.([a-z\.]**{2,6}**)$/

Quantifiers specify the characters in the regex search, and how many times they are expected to appear. Our sample has two quantifiers, `+` and `{2,6}`.
The first quantifier `[a-z0-9_\.-]+` indicates any character in the [] is expected to match one or more times. (the same for [\da-z\.-])
The second quantifier `{2,6}` indicates minimun 2 to maximum 6 characters matching [a-z0-9_\.-] are expected. 

##### Example
- a* will match every character in "alphabet".
- a+ will match only the "a" in "alphabet".
- a? will match every character in "alphabet".
- a{2} will match "alphabet" but will not match in "name".
- a{1,3} will match the "a" in "alphabet" and the 3 "a" in "atlanta".



<!-- ### OR Operator
 > /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ 
 not included -->

### Character Classes
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

 ##### Example



### Flags
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`


### Grouping and Capturing
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

 ##### Example



### Bracket Expressions
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

 ##### Example



### Greedy and Lazy Match
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Boundaries

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

 ##### Example



### Back-references
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

 ##### Example


### Look-ahead and Look-behind
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`



 

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

https://github.com/scrosa22/emailRegEx

![This is an image](https://)