---
layout: post
title:  "A general view of Regular Expressions"
date:   2017-04-06 02:42:44 +0000
---

Regular expressions are the key to powerful, flexible, and efficient text processing. They can be seen as simple as a text editor’s search command or as powerful as a full text processing language.  
Typical use case would be validation/cleaning of user input, restructuring of input, looking for substrings within input, parsing various text files, reading configuration files…

**Regular Expression Flavors. **
Many programming languages have their own implementation of regular expression engine. These come with different features, limitations and flavors - specific details can be found on https://en.wikipedia.org/wiki/Comparison_of_regular_expression_engines.
Ruby seems to have support full features similar to JavaScript.

**Regular Expressions and Ruby.**
In Ruby regular expressions are objects of type Regexp class and you typically create them by writing a pattern between slash characters (/pattern/). You can assign it to a variable to  repeatedly use the same regular expression, or use the literal regex directly. To test if your regex matches (part of) a string, you can either use the =~ operator or call the regex object’s match function.

In Ruby, a regular expression is written in the form of /pattern/modifiers, where “pattern” is the regular expression itself and “modifiers” are a series of character indicating different options. In Rubular the modifiers are named as options at the bottom of the regex quick reference table. Multiple modifiers can be combined by stringing them together as in /regex/ and they are optional.

Full regular expressions are composed of two types of characters: the special characters are called metacharacters, while the rest are called literal or normal text characters. Except for special characters (^, $, ? , ., /, \, [, ], {, }, (, ), +, *), all characters match themselves. Note that If you want to use metacharacters as a literal in a regex, you need to scape them with a backslash, otherwise they have special meanings.

Pattern-matching characters can be group into various categories:
* Position matching: Anchors, Boundaries and Delimiters ^, $, \A, \z, \b 
To match a sub-string that occurs at a specific location within the larger string. 
* Character classes matching []
Individual characters can be combined into character classes to form more complex matches, by placing them in designated containers such as [].
Character classes match one out of several characters.
Predefined character classes are: \d \D \s \S \w \W and . 
Ranges can be define with a hyphen, e.g. [a-Z]
* Repetition matching or quantifiers ?,*, +, {} 
To match character(s) that occurs in certain repetition.
* Alternation | and grouping matching ()
To group characters to be considered as a single entity or add an “OR” logic to the matching pattern

**When are Regex not that great.**
Sometimes Regex can become quite complex and the developer should try to break up the text processing parts in smaller blocks. When a complex text format is to be processed then Regex can be inappropriately used by the developer. 
Once a Regex is beyond a few hundred characters, then maintenance, changeability and potential performance is impacted.
https://blog.codinghorror.com/regex-use-vs-regex-abuse/

