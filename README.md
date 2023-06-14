# Regex For Beginners

This is a short tutorial on regular expression or also called regex. I will pick a specific regex so we can break down each part of that expression and describe what they do. This we help us understand the search pattern the regex defines. 

## Summary

First we will define what a regex is. A regular expression or regex are a series of special characters that define a search pattern. The regex we will be looking at in this tutorial is for matching a hex value. The regex follows as: 

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Since a regex is considered a literal, it must be wrapped in the slash characters(/).

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

Anchors have a special meaning in regex. They do not match any characters but they match a position before or after characters. In this matching a hex value example we have two anchors. The first is (^), this anchor matches the beginning of the string. So in this example the string must start with the # character. The next anchor we have is ($). This anchor signifies a string that ends with the characters that precede it. In this example that is everything in the parentheses.

### Quantifiers

Quantifiers set the limits of the string that your regex matches or an individual section of the string. They frequently include the minimum and maximum number of characters that you can use. In this example we have three quantifiers. The first is the (?) near the beginning of the string. All this quantifiers is doing is telling the regex that we want the pattern to match zero or one time. Next quantifier we have is the ({6}). This quantifier is telling the regex that the pattern needs to match exactly six times. The next quantifier is ({3}) and its doing the same as the ({6}) meaning the regex needs to match exactly three times. 

### Grouping Constructs

Grouping constructs is best describe as a way to break the regex in sections. The primary way you a group a section is by using parentheses. But in this example we only one grouping constructs since this regex makes use of the OR operator(|).

### Bracket Expressions

Anything in a bracket expression([ ]) represents the range of characters that we want to match. Since we are using the OR operator in this regex we have two bracket expressions but the range of characters are the same with [a-f0-9]. We use a hyphen(-) between the alphanumeric characters to represent a range of those possible characters. So the first part of the bracket expression([a-f]) means that the string can only contain those lowercase characters. The next part of the bracket expression([0-9]) means that the string can only contain any number between 0-9.

### Character Classes

A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match. In this example we are not using any character classes. But examples of character classes are ., \d, \w, and \s. The (.) class matches any character except the newline(\n). The (\d) class matches any Arabic numeral digit. This class is like the bracket expression ([0-9]). The (\w) class matches any alphanumeric character from the basic Latin alphabet. This includes underscores(_) and both lower and uppercase. And last is the (\s) class that matches a single whitespace character, including tabs and line breaks. 

### The OR Operator

The OR operator acts like a boolean OR. Matches the expression before or after the (|). In our example the regex will try to match either the first part ([a-f0-9]{6}) or(|) the second part ([a-f0-9]{3}). Which the only different between the two are the quantifiers ({6}) and the ({3}).

### Flags

Flags define additional functionality or limits for the regex. Flags are placed at the end of a regex after the second slash. In this example there are no flags used. But in regex there are six optional flags that can used either separately or together and in any order. But we will only go over the three you are most likely to encounter. First we have the flag (g) that means global search or that the regex should be tested against all possible matches in a string. Next we have the flag (i). This means a case-insensitive search so case should be ignored while attempting a match in a string. Lastly we have the flag (m). This means a multi-line search so a multi-line input string should be treated as multiple lines.

### Character Escapes

In regex the backslash \ escapes a character that otherwise would be interpreted literally. This is useful when looking for strings with special characters that are the same as a particular component of a regex. But all special characters, including the backslash, lose their special significance inside bracket expressions. In this example we do not use any backslashes. 

## Author

My name is Alfredo Jimenez and I am a student at the UNCC Full-Stack Coding Bootcamp. New to the coding world but trying to learn as much as I can one line of code at a time. You can find all my past and current projects at: https://github.com/AlfredoJi. 