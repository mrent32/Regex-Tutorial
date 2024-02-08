# Regex- What They Are and How They Work

Welcome to my Regex (regular expressions) tutorial! Regex are neat little pieces of code that are very powerful and useful. They utilize characters to ascertain whether certain stipulations are met in code. For example, there are Regex for urls, for email validation, password validation, HTML tag verification, etc. These expressions can be utilized for a wide variety of things and come in very handy. 

## Summary
In this tutorial, I will be breaking down the email verification Regex. This is something that people probably deal with every day unwittingly, and so is a useful tool to have in your arsenal as a developer. I will break down each character, starting from the opening and closing forward slashes to the AlphaNumerics, and all the weird little characters in between. Here is the Regex we will be breaking down. ```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```



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
    Anchors are the position indicators of the expression. They do not match actual characters but instead assert where in the expression something should start or end. The ^ caret is the opening anchor, defining that what comes after it must match to the beginning of the string. The $ dollar sign asserts the closing of the string. Whatever characters come before the $ must match to the regex. For example, `^hello` would match the string 'hello world', but not the string 'world hello'. Alternatively, `world$` would match the string 'hello world', but not 'world hello'.
    
### Quantifiers
    Quantifiers are symbols that determine the number of times a character repeats. The * asterisk symbol specifies that the element will appear zero or more times. So `a*` would match an empty string, or a string of just a thirty times, and everything in between. The + plus sign will match one or more times, so `a+` would match 'a', or 'aaaa', but not an empty string. The ? question mark sign will match the element zero or one time, and asserts that the element is optional. 'a?' would match an empty string, or 'a', but would not match 'aaaa'. The {n} sign matches the character the number of times specified, or n. For example, 'a{5}' would match to 'aaaaa', and nothing else. Conversely, the {n,} matches the element that many times or more. So 'a{5,} would match 'aaaaa', or 'aaaaaa' and everything above that, but would not match to 'aa'. Finally, {n,m} matches the element between the 2 numbers specified. So 'a{2, 5}' would match to 'aa', 'aaaaa', and any number of a's between 2 and 5, but not to 'a'. 
### OR Operator
    The OR operator is very similar to the || operator in Javascript, it signifies that what comes both before and after the pipe is acceptable. So if we have the string 'gr(a|e)y', the OR operator in that string accepts both the words 'grey' and 'gray' as valid. 
### Character Classes
    Character classes represent quite literally, classes of characters in regex. The specific characters desired can be stipulated, such as '[anemgjk]', or, more commonly, all the alphabet can be represented in lower case; '[a-z]'. The alphabet can also be stipulated from one character to a different one and only the ones within that range can be accepted, like this '[f-m]'. Numeric characters can also be asserted, '[0-9]', or its shorthand '\d'. Another shorthand is '\w', which symbolizes any word character, or upper and lower case alphanumeric characters. 
### Flags
    Flags, or otherwise known as modifiers, modify how the characters act. There are many flags and some libraries have different sets and rules for them, but here are some of the common ones. First is the case insensitive flag, (`i`). This flag invalidates case sensitivity, rendering the string effective no matter how it's cased. For example. '/hello/i' would match to 'HELLO', 'hello', and anything in between. The Global ('g') flag allows for that character to be present anywhere within the element. So '/a/g' will match to the string having an 'a' anywhere inside of it. The multiline flag allows for the anchors to match at the beginning and end of each line, rather than just the start and end of the whole string. 
### Grouping and Capturing
    Grouping and capturing allow for stipulating which parts need to be what criteria and in what order in regex. Grouping is accomplished by using parenthesis to enclose a group and treat them as an element with its own set of rules. Within that group then any of the previous elements discussed can be stipulated and combined. Capturing groups is a different type of grouping that also captures the matched text to be later compared or referenced against. So for example if a regex is being used to determine a date within code, using capturing groups can be combined with the javascript method 'match()' to later compare against.
### Bracket Expressions
    Bracket expressions are types of character classes that fall within the square brackets. As outlined above, this could be numbers, '[0-9]', alphabet characters, '[a-z]', upper and lower case characters, and as well arithmetic operators, such as '[+-*/]', for addition, subtraction, multiplication and division.
### Greedy and Lazy Match
    Greedy and lazy match refers to how much or how little specific operators or classes attempt to match to elements within the regex. For example, the '*' and the '+' operators in regex will attempt to match as much as possible with the elements, hence earning the nickname 'greedy' match. In some scenarios, matching as little as possible can be more beneficial. This is where the lazy match comes in. Adding a ? question mark to the quantifier makes it match to as little of the string as possible. For example, if given the regex '.*\d+' to match the string 'abc123def456', it would by default greedy match to the entire string. However, if modified with the lazy match '.*?\d+' it would then only match to the first half of the string, 'abc123', because the ? matches to as little as possible. 
### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)