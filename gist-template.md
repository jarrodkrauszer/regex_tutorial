# Regex Tutorial

This tutorial will breakdown and explain each piece of a regular expression.

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

Here are some examples of strings that meet all the criteria:

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/``

#a0522d

a0522d

#fff

fff

### Quantifiers

Quantifiers allow us to set the limits of the string our regular expression matches.  We have three quantifiers in our expression `?`, `{6}` & `{3}`.  The `?` is the quantifier that follows the `#`.  This tells the string can contain 0 to 1 occurrence of the `#` character.  The next quantifier we see is the `{}` quantifier that tells us we are looking for an exact number or occurrences in the input string.  `{6}` is looking for exactly 6 occurrences of a valid hexadecimal code and the `{3}` is looking for exactly 3 occurrences. 

Here is an example expression using these quantifiers and strings that match the criteria:

`/^@?[A-Za-z0-9]{6}$``

@AbCdEf

AbCdEf

123456

### OR Operator

In regular expressions the `|` serves as an OR operator which allows the patterns on either side of it to be matched. This means that a valid match can occur if either of the patterns is found. In our expression valid matches can be either 6 characters OR 3 characters. The OR operator provides flexibility in pattern matching, allowing you to define more comprehensive validation rules for your data.


Here is an example of a regular expression that uses an or operator and strings that match the criteria:

`/^[A-Za-z]+$|^[0-9]+$/``

AbCdEf

abcdef

123456

987654

### Character Classes
Character classes are signified by the `[]` and specifies a set of characters that can be matched at a particular position in the input string.  The `[a-f0-9]` character class tells us the input string can include any lowercase letter from a to f and any digit 0-9.  

Here is an example of using character classes and some strings that match the criteria:

`[0-9]x[0-9]``

1x2

5x9

0x7

### Grouping and Capturing
One of the primary purposes of grouping constructs is to capture and remember sub-patterns within the regular expression. The `(` and `)` you see in our expression is a grouping construct or sub-expression.  In our regular expression they group two hexadecimal strings that are valid color codes. Either 3 or 6 digits codes.

Here is an example regular expression and some strings that match the criteria:

`(\d{3})-(\d{2})``

123-45

987-65


### Greedy and Lazy Match
There are two types of matches in regular expressions Greedy and Lazy.  Greedy quantifiers try to match as many characters as possible and Lazy quantifiers try to match as few characters as possible.  Our expression utilizes two Greedy matches.

`{6}` - matches exactly 6 characters

`{3}` - matches exactly 3 characters

## Author

Link to my github profile: [jarrodkrauszer](https://github.com/jarrodkrauszer)

Here is a link to the repo: [Regex Tutorial](https://github.com/jarrodkrauszer/regex_tutorial)
