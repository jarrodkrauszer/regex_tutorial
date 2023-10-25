# Regex Tutorial

This tutorial will breakdown and explain each piece of a Regex expression.

## Summary

The following regex expression we are going to breakdown is used to validate hexadecimal color codes. It allows for both 3 and 6 digit color codes and can either contain or not contain the # prefix.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

## Table of Contents

- [Regex Tutorial](#regex-tutorial)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [OR Operator](#or-operator)
    - [Character Classes](#character-classes)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
  - [Author](#author)

## Regex Components

### Anchors

There are two anchors being used in our regular expression the `^` and `$`.  The `^` anchor lets us know that the pattern should match at the beginning of the input string.  The `$` anchor lets us know that the pattern should match at the end of the input string.  When used together `^` and `$` ensure that entire input string matches the pattern defined in our expression.

### Quantifiers

Quantifiers allow us to set the limits of the string our regular expression matches.  We have three quantifiers in our expression `?`, `{6}` & `{3}`.  The `?` is the quantifier that follows the `#``.  This tells the string can contain 0 to 1 occurrence of the `#` character.  The next quantifier we see is the `{}` quantifier that tells us we are looking for an exact number or occurrences in the input string.  `{6}` is looking for exactly 6 occurrences of a valid hexadecimal code and the `{3}` is looking for exactly 3 occurrences.  

### OR Operator

The `|` serves as an OR operator which allows the patterns on either side of it to be matched.  Meaning in our expression both 6 digit and 3 digit hexadecimal codes are valid.

### Character Classes
Character classes are signified by the `[]` and specifies a set of characters that can be matched at a particular position in the input string.  The `[a-f0-9]` character class tells us the input string can include any lowercase letter from a to f and any digit 0-9.  

### Grouping and Capturing
The `(` and `)` you see in our expression is a grouping construct or subexpression.  In our regular expression they group two hexadecimal strings that are valid color codes. Either 3 or 6 digits codes.

### Greedy and Lazy Match
There are two types of matches in regular expressions Greedy and Lazy.  Greedy quantifiers try to match as much as possible and Lazy quantifiers try to match as few characters as possible.  Our expression utilizes two Greedy matches.

`{6}` - matches exactly 6 characters
`{3}` - matches exactly 3 characters

## Author

Link to my github profile: [jarrodkrauszer](https://github.com/jarrodkrauszer)

Here is a link to the repo: [Regex Tutorial](https://github.com/jarrodkrauszer/regex_tutorial)


