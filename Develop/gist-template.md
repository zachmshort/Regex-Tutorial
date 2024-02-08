# Regex Tutorial

Regular expressions, commonly abbreviated as regex, are powerful tools used in various programming languages and text processing utilities for pattern matching and manipulation. In this tutorial, we'll delve into the intricacies of a specific regular expression used to match email addresses.

## Summary

In this tutorial, we will dissect the regular expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, which is designed to validate email addresses. Each component of this regex plays a crucial role in ensuring the validity of the input. We will explore each part in detail to understand its functionality.

```regex
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

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
Anchors in regular expressions show where a match should occur in the input string. In our email regex, ^ marks the beginning of the string, making sure that the email address starts right there.

### Quantifiers
Quantifiers define how many times a character or group can appear. When we use +, it means "one or more." For instance, [a-z0-9_\.-]+ matches one or more lowercase letters, digits, underscores, dots, or hyphens in the local part of the email address.

### OR Operator
The | symbol works as an OR operator. In our regex, it allows for two possibilities for the domain part of the email address: either a domain consisting of six characters (matching .[a-f0-9]{6}) or a domain consisting of three characters (matching [a-f0-9]{3}).

### Character Classes
Character classes define sets of characters that can match. `[\da-z\.-]` matches a single character that is a digit (`\d`), lowercase letter, dot, or hyphen.

### Flags
Flags in regular expressions modify the behavior of the regex pattern. In our regex /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, there are no flags used.

### Grouping and Capturing
Parentheses `()` are used for grouping and capturing. They allow us to treat multiple characters as a single unit. In our regex, we have three groups: one for the local part, one for the domain, and one for the top-level domain (TLD).

### Bracket Expressions
Bracket expressions, denoted by `[ ]`, match any one of the enclosed characters. `[a-z\.]` matches any lowercase letter or a dot.

### Greedy and Lazy Match
Quantifiers are greedy by default, meaning they match as much as possible. Adding `?` after a quantifier makes it lazy, matching as little as possible. However, in our regex, greediness is not explicitly modified.

### Boundaries
Boundaries, such as `$`, signify the end of the string. `$` ensures that the input string ends after the TLD, preventing additional characters.

### Back-references
Back-references, like `\1`, allow referencing previously captured groups. In our regex, `\1` ensures that the closing tag matches the opening tag for HTML tags.

### Look-ahead and Look-behind
Look-ahead and look-behind assertions, denoted by `(?= )` and `(?<= )`, respectively, check for matches without consuming characters. They are not present in our email regex.

## Author

This tutorial was written by [Zachary Short](https://github.com/zachmshort). You can find more of my work on my [GitHub profile](https://github.com/zachmshort).
