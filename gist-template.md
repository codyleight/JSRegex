# Regex in Javscript

Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects. As a Developer it is important to know and understand some Regex patterns as they are extremely usefull and prevent you from inventing the wheel.

## Summary

I will be covering the Email Validation regex in javascript, as a Developer can imagine this is an extremely common Regex. We can use this Regex to get us started and then go through it piece by piece.

const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;

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

### Anchors

Anchors are special characters that match a specific position in the string. In email validation, we typically use the ^ anchor to match the start of the string and the $ anchor to match the end of the string. These anchors ensure that the entire string is validated as an email address.

In our Example this is indicated right after and before our backslash /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;

### Quantifiers

Quantifiers, are used to show how many times our pattern will occur. /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/; In our example we are looking at the +- symbols.
for our first part [a-zA-Z0-9._%+-] this lets our first part of our email occur atleast one more time if not more.
For this part [a-zA-Z0-9.-] since we don't need domain names types we only allow one.


### Grouping Constructs
Grouping Constructs, group together characters and patterns together to apply quantifiers and operations to the groups.
For example [a-zA-Z0-9._%+-]+ would be our local part of our email since we have a + Quanitifier at the end we are looking for multiple characters.
For our Domain part of our email: @[a-zA-Z0-9.-]+ We do quite the same as above and allow multiple characters to be entered. 
At last ([a-zA-Z]{2,}): we use the {2,} Quanitifier to ensure a minimum length. Example: .com .net etc all have 3+



### Bracket Expressions
Bracket Expressions [] define a set of characters that can be matched at a specific position of the string. For our email regex, it is used to define the valid characters for the local and domain name of an email adress.
[a-zA-Z0-9._%+-] , [a-zA-Z0-9.-] , and [a-zA-Z]:
For our first bracket expression, it matches any alphanumeric character, period, underscore, percent sign, plus sign, or hyphen., second we take off some special characters.
and our final we only allow letters. When breaking it down it looks alot more readable.


### Character Classes
Character Classes are used to define set of characters. They are typically enclosed in our brackets as well.
In our email example, we set a range of characters we can use [a-z], [A-Z] and [0-9].
Example: [a-z] our lowercase alphabet, [A-Z] would obviously be our captilized alphabet after. and [0-9] is our numeric keys.

### The OR Operator
OR Operator is used to specificy alternative patterns to match. While we do not have this in our email-regex example it is an extremely useful tool in regex's.

### Flags
Flags allow you to modify the behavior of the pattern matching, flags are added after the closing slash of the regex. Some examples include i - case sensitive flag so instead of having both [a-z] and [A-Z] we could just include that at the end. There are also other usefull flags that can be added as well.
Flags are another powerful tool in regex's, however our email regex does not have an example of them but could easily be added!

### Character Escapes
Character Escapes in Regex, allow you to match specific characters that have meaning in our regex. We have a good example of that in our regex 
/^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/; when comparing right at our DOT in our email.
\. will return a dot character. Normally, a dot . in a regex pattern matches any character except newline.

## Author

Cody Thompson
Github: https://github.com/codyleight
Repo for Regex in Javascript: https://github.com/codyleight/JSRegex
Gist Link: https://gist.github.com/codyleight/e0cb9a2bc420c3b2c45d30a2f090ba03

