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

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)