# Matching an Email - Regex Tutorial

The following tutorial is designed to explain the use of Regular Expressions (regex) for matching an email. 

## Summary

Regular Expressions is a sequence of characters that defines a search pattern. 

 > /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
<!-- - [OR Operator](#or-operator) -->
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
<!-- - [Boundaries](#boundaries) -->
<!-- - [Back-references](#back-references) -->
<!-- - [Look-ahead and Look-behind](#look-ahead-and-look-behind) -->

## Regex Components

### Anchors
> /`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/

Anchors start and end the expression. `^` indicates the beginning and `$` indicates the end of the expression.  

### Quantifiers
> /^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6})`$/

Quantifiers specify the characters in the regex search, and how many times they are expected to appear. Our sample has two quantifiers, `+` and `{2,6}`.
The first quantifier `[a-z0-9_\.-]+` indicates any character in the bracket is expected to match one or more times (the same for [\da-z\.-]).
The second quantifier `{2,6}` indicates minimun 2 to maximum 6 characters matching [a-z0-9_\.-] are expected. 

##### Example
- a* will match every character in "alphabet".
- a+ will match only the "a" in "alphabet".
- a? will match every character in "alphabet".
- a{2} will match "alphabet" but will not match in "name".
- a{1,3} will match the "a" in "alphabet" and the 3 "a" in "atlanta".



<!-- ### OR Operator -->



### Character Classes
> /^([a-z0-9_\.-]+)@([`\d`a-z\.-]+)\.([a-z\.]{2,6})$/

Character classes match types of characters. `\d` is used to match any digit 0-9 character.

##### Example
- `.` Matches any single character.
- `\d` Matches any digit. Equivalent to [0-9].
- `\D` Matches any character that is not a digit. Equivalent to [^0-9].
- `\w` Matches any alphanumeric character from the basic Latin alphabet [A-Za-z0-9].
- `\s` Matches a single whitespace character, including space, tab, form feed, line feed, and other Unicode spaces.


### Flags
> `/`^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`/`

Flags are placed at the end the regex and define additional functionality or limits for the regex. There are six optional flags that can be used, either separately or together and in any order.

 ##### Example
 - g - Global search: the regex should be tested against all possible matches in a string.
 - i - Case-insensitive search: case should be ignored while attempting a match in a string.
 - m - Multi-line search: a multi-line input string should be treated as multiple lines.


### Grouping and Capturing
> /^`([a-z0-9_\.-]+)`@`([\da-z\.-]+)`\.`([a-z\.]{2,6})`$/

Grouping and Capturing is done using parentheses `()` to select search parameters. 

 ##### Example
 - `([a-z0-9_\.-]+)` - Group for email address.
 - `([\da-z\.-]+)` - Group for email provider. 
 - `([a-z\.]{2,6})` - Group for domain extention.
 


### Bracket Expressions
> /^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/

Bracket Expressions are used to find a range of characters to match. As a positive character group, anything inside a `[ ]` will be included. 

 ##### Example
 - `[a-z0-9_\.-]` - Matches any lowercase letters, numbers, underscores, periods or dashes.
 - `[\da-z\.-]` - Matches any single digit, lowercase letters, periods or dashes.
 - `[a-z\.]` - Matches any lowercase letters and period.

### Greedy and Lazy Match
> /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The `+` quantifier allows the search to match one or more of the characters in the expression. Quantifiers by default tell the regex to match as many instances of the expression as possible - this is called ***greedy*** and a greedy quantifier will return the longest match (at the start of the search parameter). Conversely, a ***Lazy*** match will return as few as possible matches and provide the shortest match.


<!-- ### Boundaries -->



<!-- ### Back-references
> /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
Backreference in a regular expression identifies a previously matched group and looks for exactly the same text again -->


<!-- 
### Look-ahead and Look-behind
> /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ -->



 

## Author

This gist was created by S Rosa as a bootcamp completion requirement. Hopefully you have found this gist helpful! 

https://github.com/scrosa22/emailRegEx
