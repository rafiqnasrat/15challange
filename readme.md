# 15challange



## Summary

Regular Expressions are also known as REGEX, It is collection and sequence of characters use for creating patterns and patterns are use for searching in text, It is a powerful pattern by which we can do complicated searches.

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

## REGULAR EXPRESSIONS COMPONENTS

### Anchors

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Anchors expression's are ^ to start and $ to end.

### Quantifiers

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This expression has is a + to communicate there is another sequence to be matched as a greedy quantifier.
Additionally {2,6} as another greedy quantifier to specify the input should be a minimun of 2 characters and a max of 6.

### OR Operator

"OR" syntax is denoted with a vertical line character "|"

If you are looking for programming languages: HTML, CSS, JavaScript the corresponding RegEx would look like: HTML|CSS|JavaScript

### Character Classes

A character class allows you to match any symbol from a certain character set. it is also known as a character set.

Most commonly character classes:

\d - match a digit or character from 0 to 9.
\s - match a whitespace symbol such a space, tab (\t), a newline (\n), etc.
\w - W stand for word character. it matches the ASC|| character [A-Za-z0-9] including Latin alphabets, digits, and the underscore(_).

### Flags

Flags are optional parameters that we can add to a plain expression to make it search in a different way. Each flag is denoted by a single alphabetic character, and serves different purposes in modifying the expression's searching behavior.

i (Ignore Casing) Makes the expression search case-insensitively.
g (Global) Makes the expression search for all occurrences.
s (Dot All) Makes the wild character . match newlines as well.
m (Multiline) Makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning and ending of the whole string.
y (Sticky) Makes the expression start its searching from the index indicated in its last Index property.
u (Unicode) Makes the expression assume individual characters as code points, not code units, and thus match 32-bit characters as well.

### Grouping and Capturing

Grouping is done with the round brackets or parentheses and allows to to group a certain part of the regular expression together.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This expression would be split like so:

1st - ([a-z0-9_\.-]+)

2nd - ([\da-z\.-]+)

3rd - ([a-z\.]{2,6})

### Bracket Expressions

Brackets indicate a set of characters to match. you will often see ranges of the alphabet or numerals. [A-Za-z] [0-9].

([a-z0-9_\.-]+)

This grouping it will look for anything a-z or 0-9

### Greedy and Lazy Match

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This example we have only used greedy quantifiers + and {}, meaning that it will allow the match to expand as long as it needs to go.
If these quantifiers were lazy quantifiers, they would appear as +? or {}?, this will direct the system to make the shortest match.

### Boundaries

The (\b) is an anchor like the caret (^) and the dollar sign ($) it matches a position that is called a "word boundary". the word boundary match is zero-length.

console.log('hello, js!'.match(/\bjs\b/)):

The output would be ["js"]

### Back-references

A back-reference in a regular expression identifies a previously matched group and looks for exactly the same text again. They are specified with a backslash and a single digit. \1

### Look-ahead and Look-behind

In some cases we need to find only  those matches for a pattern that are followed or proceeded by another pattern the syntax for that is called look-ahead and look-behind.

Look-ahead uses syntax that looks like this: X(?=Y). This means "look for X, but match only if followed by Y.

Look-behind is similar bit looks behind to match a pattern only if there is something before it. the syntax looks like: (?<=Y)X. Matches x but only if Y is before it.
