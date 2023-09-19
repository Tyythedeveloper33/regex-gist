# Title (replace with your title)

A "regex", or better known as "regular expression" is a very good language to match patterns , that are used manipulate text, or even just for searching text. It is very powerful because it allows developers to define patterns of  numbers or characters and apply those patterns to strings of text. using regex it can make things easy for developers when it comes to validating data,extracting information, searching for specific words, etc. 

## Summary

so for my choice of Regex i went with the regular expression for matching a email, in this gist i will start off from the start of the expression when it comes to explaining each element thats included individually, so expect them to be in order in which the order the elements are used. also i will explain what the element is, then how the element is integrated into my regular expression and its purpose in my expression. here is my regex:
              `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
  an "anchor", occurring in a  regular expression, is a character or sign that represents a position within a text , or a string of text where a match should occur. it is important to note that Anchors do not match any characters themselves , they are stricly for declaring a position for where the match of the regular expession can occur.
  For instance in my code: I will use ||anchor|| to show the position of the element

                           `||/^||([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})||$/||`

 It is seen that I have two anchor elements in this equation, the first one will be the  ||^||, better known as the caret, this signifies the begining of the regular expression it is from this point after the caret, that the regular expression can be used to match a email this goes until we meet our second anchor which is ||$|| this is know as the dollar sign this is pretty much the opposite of the caret, unlike the caret the regular expression that matches the input of a email must stand before the dollar sign, in other words the dollar sign marks the end of the regex.
### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
