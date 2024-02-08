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