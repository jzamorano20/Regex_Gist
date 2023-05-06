# Regex_Gist
Regular expressions, commonly known as regex, are a powerful tool used in computer science and programming to search and manipulate text data. With regex, you can easily search for patterns and specific pieces of information within a text document, such as emails, phone numbers, and URLs. Regex can also be used to validate and clean data, as well as to replace or transform specific parts of a text. Learning regex can greatly enhance your abilities as a programmer or data analyst, and it is widely used in various fields including web development, data science, and system administration. In this introduction, we will cover the basics of regex, how it works, and some common use cases.

## Summary

With what was previously stated in the intro im going to be breaking downa and explaing a certain regex. To a matching type in this case we will be matching a URL.
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

The line above is the regex for matching a URL.
A break down of this regex.
1. '^' - This matches the beginning of a line.
2. '(https?:\/\/)?' - This matches an optional http:// or https:// at the beginning of the URL.
3. '([\da-z\.-]+)' - This matches one or more alphanumeric characters, dots, or hyphens in the domain name.
4. '\.([a-z\.]{2,6})' - This matches a period followed by the top-level domain, which can be between 2 and 6 letters or dots.
5. '([\/\w \.-]*)*' - This matches any additional path or query string in the URL, including slashes, alphanumeric characters, spaces, dots, or hyphens.
6. '\/?$' - This matches an optional trailing slash at the end of the URL, followed by the end of the line.

So, in summary, this regex pattern matches a wide range of URLs that can start with http:// or https://, followed by a domain name and an optional path or query string. It can be useful for validating or extracting URLs from text data.

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
A regex is considered a literal, with that stated it means a pattern must be wrapped in slash characters (\). 
### Anchors
The anchors in the given regex are as follow the "^" or caret symbol and "$" or  dollar sign.Anchors have specail meaning in regex as they dont match any charcter. Rather they match the beginning or end of the text. The caret top matches at thr beginning of the text 
### Quantifiers
Quantifiers are special charcters that define how many times a particular charcater or group of charcters should apperar in a string. These specify the quanitity of a preceding character or group of characters that should be mstched in order for the pattern to be a match.
list of Quantifiers
| Quantifiers | Character|
|------------|----------|
| + | macthes the pattern one or more times|
| * | macthes the pattern zero or more times |
| ? | matches the pattern zero or one time |
| {} | curly brackets can provide 3 different ways to set limits for a match |
| {n}| matches the pattern exactly n number of times |
| {n,} | matches the pattern at least n number of times |
| {n,x} | matches from a minimum of n number of times and X a maximum number of times |   

Or you can be lazy and just use the ? symbol after to match few occurrences as possible.
### Grouping Constructs

In regular expressions (regex), grouping constructs are used to group together parts of a pattern. This allows you to apply operators and quantifiers to a group of characters or subpatterns.
There are 2 types parentheses and non-capturing.

Parentheses are used to create a capturing group, which captures the matched content and allows you to retrieve it for further processing. A capturing group is a subpattern within a larger pattern that is enclosed in parentheses

Non-capturing groups are similar to capturing groups, but they do not capture the matched content.They are denoted using the syntax (?:subpattern). They are useful when you want to group together a set of characters or subpatterns but dont need to capture the matched content.

Grouping constructs can be nested to create more complex patterns. Overall, grouping constructs help you to create more flexible and powerful regular expressions.
### Bracket Expressions
In regular expressions (regex), bracket expressions are used to specify a set of characters that you want to match in a string.

Bracket expressions are denoted using square brackets.Bracket expressions allow you to specify a set of characters to match without having to list them all individually. They are useful when you want to match a range of characters or a specific set of characters in a string.You can also use negation in bracket expressions by using a caret (^) symbol at the beginning
| Expression | Description |
|------------| ------------| 
| [a-z] | find any character between the brackets |
| [^a-z] | find any character NOT between the brackets |
| [0-9] | find any character between the brackets (any digit) |
|[^0-9] | find any character not between the brackets (any non-digit) |
|.(x|y).| find any of the alternatives specified |

### Character Classes
These define a set of characters any which can occur in an input string to fulfill a match.These are similar to the bracket expressions in the sense of the positive and negative character groups. Some other common character classes are
| expressions | Description |
| ----------- | ----------- |  
| . | Matches any character expect the newline character (\n) |
| \d | matches any arabic numeral digit. same as bracket [0-9] |
| \w | Matches any alphanumeric character (collection of letters and numbers from basic latin alphabet) including the underscore(_). Similar to the bracket expression [A-Za-z0-9_].|
| \s | Matches a single whitespace character, including tabs and line breaks. |

Similar to brackets you can negate the previous expressions by capitalizing the letter character. Example is (\D) that would mean match non-digit character.
### The OR Operator

### Flags
A regex must be wrapped in a slash, expect flags they are the one expection to this rule.Flags are placed at the end of a regex, after the second slash and define additional functionally or limits for the regex. There are 6 optional flags they can be used separately or together and in any order. 
| Expression | Description |
| ---------- | ----------- | 
| g-Global search | the regex should be tested against all possible matches in the string |
| i-Case-insensitive search | case should be ignored while attempting a match in a string |
| m-Multi-line-search| a multi-line input string should be treated as multiple lines |


### Character Escapes
The (\) backslash in a regex escapes a character that would otherwise be interpreted literally. This is common when looking for a string with specail characters that are the same as a particular component of a regex. Its important to note that all special characters including the backslash lose their special significance inside bracket expressions. 
## Author
Jose Zamorano 
GitHub link 
https://github.com/jzamorano20
