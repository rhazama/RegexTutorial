# Learn Regex With Me
What is regex you ask? Regex is short for “regular expression” and in simple terms, finds patterns in searches. Regex extracts information from any text just by searching for matches of a specific search pattern. These patterns could include validation to parsing/replacing strings, passing through translating data to other formats, and web scraping. Regex is able to be used by many other programming languages including JavaScript, Java, VB, C #, C / C++, Python, Perl, Ruby, Delphi, R, Tcl, and more! 
To learn more, checkout the following gist: https://gist.github.com/rhazama/6e0327ab95dc2ec3ee57e7f95d25c269

## Summary
In this Regex tutorial, we will be matching an email. We will be verifying the email is valid by matching a certain search pattern. 
We will be using the folliwing code for this example: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
Anchors are used to match postiions within expressions. Anchor symbols include: ^$  
<br />
In the example code:  /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ we see the "^" indicates the start of the code and "$" represents the end of the expression.

### Quantifiers
Quantifiers will match the amount of repeating character, groups, or character class occurances in strings. Quantifier symbols include *+?{}  
<br />
In our code: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ the + symbol signals the next sequence and the {2,6} sybolizes the minimum (2) and maximum (6) number of characters in the expressions.

### Character Classes
Character classes allow you to connect symbols with character sets. digits, word characters, and white spaces such as /d, /w /s and * are a few examples. 
<br />
In our example code: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ the \d symbolizes the digits 0-9.

### Grouping and Capturing
Grouping and capturing help show smaller groups within the main expression. 
<br />
In the example code: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ it is grouped in three sections:
The first set is shown with the expression: [a-z0-9_\.-]
The second set represents the email domain (e.g. google, hotmail, yahoo, etc): [\da-z\.-]
The third set interprets the extention domain (e.g. .com, .net, .org, etc): ([a-z\.]{2,6})

### Bracket Expressions
Bracket expressions are shown through brackets which show a matching or nonmatching list.
<br />
In our code: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ we see three brackets:
Within the first bracket [a-z0-9_\.-] we see case sensative characters a-z, number characters 0-9, underscores, periods, and hyphens _.-
Within the second bracket [\da-z\.-] includes all digits /d, characters from a-z, periods and hyphens .-
Within the third bracket [a-z\.] includes characters a-z, and periods .

### Greedy and Lazy Match
The greed and lazy match identify quantifiers. Greedy quantifiers are the default and connect many with the largest amount of matches. Lazy quantifiers (non-greedy) match elements with very few in the smallest amount of matches. To make the expression greedy to lazy, add an extra ? to the expression.
<br />
In our example code: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ we see that we use the greedy quantifier. The "+" helps match the following element one or more times and "{}" specifically matches the elements 2-6 times.

## Author
Hey I'm Ryan Hazama, a full stack web developer based in LA. Some other hobbies I have include videography, hip hop dance, and hunting for the best breakfast burrito. If you'd like to connect or see more of my work, feel free to check out my Github: https://github.com/rhazama
