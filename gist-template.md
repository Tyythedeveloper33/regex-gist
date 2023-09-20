# the power of REGEX(regular expression)

A "regex", or better known as "regular expression" is a very good language to match patterns , that are used manipulate text, or even just for searching text. It is very powerful because it allows developers to define patterns of numbers or characters and apply those patterns to strings of text. using regex it can make things easy for developers when it comes to validating data,extracting information, searching for specific words, etc. 

## Summary

so for my choice of Regex I went with the regular expression for matching a email, in this gist I will start off from the start of the expression when it comes to explaining each element thats included individually, so expect them to be in order in which the order the elements are used. also i will explain what the element is, then how the element is integrated into my regular expression and its purpose in my expression. here is my regex:
              `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
  an "anchor", occurring in a  regular expression, is a character or sign that represents a position within a text. It is important to note that Anchors do not match any characters themselves , they are stricly for declaring a position for where the match of the regular expession can occur.
  For instance in my code: I will use ||anchor|| to show the position of the element
                         
                            `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
                           `||/^||                                        ||$/||`

 It is seen that I have two anchor elements in this equation, the first one will be the  ||^||, better known as the caret, this signifies the begining of the regular expression it is from this point after the caret, that the regular expression can be used to match a email this goes until we meet our second anchor which is ||$|| this is know as the dollar sign this is pretty much the opposite of the caret, unlike the caret the regular expression that matches the input of a email must stand before the dollar sign, in other words the dollar sign marks the end of the regex.
### Grouping Constructs
Describing group constructs is also going to touch on other topics aswell so im going to try to keep this one dimensional and easy to understand so people with less understanding can understand!!, grouping constructs are classified by the parentheses ( ),and everything thats included inside of the parenthesis, it can be set up multiple ways , maybe ([]) , maybe  ([]{}). one parenthesis holds the grouping for one grouping constructs.  Any  numbers ,character classes, characters,  quantifiers, metacharacters, or alternation operators within those parentheses. I will get into character classes,   quantifiers later in the gist.
 
  For instance in my code: I will use ||grouping constructs|| to show the position of the element
             `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
         || ([a-z0-9_\.-]+) ||   || ([\da-z\.-]+) ||  || ([a-z\.]{2,6}) || 

 as you can see we have 3 grouping constructs here the first one has [a-z0-9_\.-]+ inside of () , The purpose of this grouping construct is to match a set of characters that represents the first part of a email address for example123@gmail.com , this grouping construct would match example123 (i will explain how when i get into bracket expressions and quantifiers). the 2nd grouping constructs is responsible for matching the 2nd part of the email after the @ sign , its the second group after the literal @ sign so if we had ("gmail")  it would match the 2nd group(i will explain how when i get into bracket expressions and quantifiers), the last group contruct is for the 3rd part of the email, now we all know this usually consist of the .com, .net , etc  basically all 3 of these groups together combined with all of the literal metacharacters we have are the perfect foundation for a standard email address.
### Bracket Expressions(Character Classes)
so going over the grouping constructors i kind of covered bracket expressions, better known as character classes, so how we had our grouping constructs which constained the ([]) in the case the we have charcters, metecharacters inside of the [bracket] this is what is know as the bracket epression, so to go back [a-z0-9_\.-] this bracket expression allows the first part to consist of one or more lowercase letters, with the a-z , digits,with the 0-9, underscores,with the _ , to have a dot  be matched literally we have to include a backslash before the period, or hyphens, with the -. Secondly we have a 2nd bracket expression [\da-z\.-] , i would almost say is identicaal to the 1rst one , \d is equal to 0-9, followed by a-z , meaning any lowercase letter, followed by a literal period or hyphen so if we had @gmail it would essentially match because it matches the a-z. for the 3rd bracket expression [a-z\.] is any lowercase letter or period.
 

### Character Escapes
last I will be covering character escapes, I probably should of covered it first but hopefully this ties together everything you need to know about regex coming to email addresses. character escapes are used to match specific metacharacters(characters with value in regex), Character escapes are typically represented by a backslash "\" followed by a character that specifies which character to match. 
 in my regex:
  I will use ||character escapes|| to show the position of the element
             `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
                        |\.|      |\d| |\.|  |\.|   |\.|

    in this example i only have to explain two types of character iscapes but it is important to notice that even though "@" isnt a metacharacter it is a literal character, meaning it shows up and matches itself exactly, back to the character escapes \. matches a literal "." if it was just . without the \ would actually be a metacharacter , which is a character that holds a specail value in this case UI think "." would be a wildcard for matching any character.  the \d it equal for matching any digit 0-9  now "d" without the backslash isnt treated as a metacharacter, but its treated as a literal character , meaning it would match the input if it had a "d" character in it.
## Author

My name is Tyler Webster i am a 21 year full stack webdeveloper, developing a new skill of useing regular expressions , to build familiarity with them for encounters in work environment. my github - https://github.com/Tyythedeveloper33?tab=repositories
