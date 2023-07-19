# Title Matching an Email Regex Tutorial

A regex, also known as a regular expression, is a sequence of characters used to define a search pattern. It is a tool for pattern matching and manipulation in strings, allowing you to search, match and replace text based on patterns. Regex is commonly used in programming to perform tasks like validation, searching, and extraction.

## Summary

In this summary we will be discussing the matching an email regex: 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This is used to validate and match email addresses. This regex ensures that an input string follows the format of an email address. It typically includes checks for the presence of a username, the `@` symbol, and a domain name. Sometimes this can be complex due to the various formats of email addresses.

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
The regex  `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` uses two anchors, but this is not always required. The anchors used in this regex are the `^` and `$`. These are the start and end anchors, respectfully.

The start anchor asserts the match should start at the beginning of the string and the end anchor stops at the end of the string.

Together these two anchors ensure the entirety of the input string is considered when matching the pattern of the email address.

### Quantifiers
The regular expression `^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$` uses the following quantifiers:

`+` (plus): It is used after the character class `[a-z0-9_\.-]` and `[\da-z\.-]`. The `+` quantifier matches one or more occurrences of the preceding character or character class. It allows matching one or more alphanumeric characters, underscores, dots, or hyphens in the username and domain parts of the email address.

`{2,6}`: It is used after the character class `[a-z\.]`. The `{2,6}` quantifier specifies a range of minimum and maximum occurrences. It matches a sequence of lowercase letters or dots with a minimum of 2 occurrences and a maximum of 6 occurrences. This part is used to match the top-level domain (TLD) of the email address.

To summarize, the `+` quantifier allows one or more occurrences, while the `{2,6}` quantifier specifies a range of occurrences for matching specific patterns within the regex.
### Character Classes
Character classes in a regular expression define a set of characters that can be matched. They're enclosed in square brackets `[]`. In the regular expression you provided, `^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`, we see several character classes and meta sequences:

`[a-z0-9_\.-]` - This character class matches any lowercase letter `a-z`, any digit `0-9`, underscore `_`, dot `.`, or dash `-`.

`\d` - This is a shorthand character class that matches any digit equivalent to `[0-9]`.

`[a-z\.-]` - This character class matches any lowercase letter `a-z`, dot `.`, or dash `-`.

`[a-z\.]` - This character class matches any lowercase letter `a-z` or dot `.`
### Grouping and Capturing
Grouping and capturing are important concepts in regular expressions that allow you to create logical groups within a pattern and capture specific parts of the matched text.

`([a-z0-9_\.-]+)`: This captures one or more lowercase letters, numbers, underscores, periods, or hyphens that appear before the `@` symbol.

`([\da-z\.-]+)`: This captures one or more digits, lowercase letters, periods, or hyphens that appear between the `@` symbol and the dot in the domain name.

`([a-z\.]{2,6})`: This captures two to six lowercase letters or periods that represent the top-level domain.

These groups allow you to extract the username, domain name, and TLD separately from an email address that matches the pattern.

### Bracket Expressions
Bracket expressions are enclosed within square brackets `[]` and define a set of characters that can match a single character at that position in the string.


`[a-z0-9_\.-]`: This character class matches any lowercase letter `a-z`, digit `0-9`, underscore `_`, period `.`, or hyphen `-`.
`[\da-z\.-]`: This character class matches any digit `\d` or `0-9`, lowercase letter `a-z`, period `.`, or hyphen `-`.
`[a-z\.]`: This character class matches any lowercase letter `a-z` or period `.`.

### Greedy and Lazy Match
`+` matches one or more occurrences of the preceding pattern. In this case, `([a-z0-9_\.-]+)` and `([\da-z\.-]+)` use the `+` quantifier. This means that these groups will match as many characters as possible that satisfy the pattern, such as multiple lowercase letters, digits, underscores, periods, or hyphens.
`{2,6}` matches between 2 and 6 occurrences of the preceding pattern. In this case, `([a-z\.]{2,6})` uses the `{2,6}` quantifier. This means that this group will match between 2 and 6 lowercase letters or periods, trying to match as many characters as possible within that range.

## Author

Brought to you by Chelsea Pratte.

https://github.com/callmechelsea/