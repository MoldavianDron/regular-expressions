# regular-expressions

### Useful links:
[Regular expressions cheatsheet](https://cheatography.com/davechild/cheat-sheets/regular-expressions/) <br />
[Regex online editor](https://regex101.com/)

## Intro
Regular expressions is a powerful tool for effective work with text. 
It is a formal language used for searching characters and substring manipulations.
Regular expressions it is a special string which sets a search pattern.

## 1. Characters and metacharacters

/***java***/ \
***java***> \ python ruby1.9 ***java***script c#

***/*** - this symbol is called **delimiter**. It is used at the beginning and at the end of regular expression 
to separate regex from another text. Such matching is called **exact**. Characters combinations
were found in text matching **exactly** with given pattern.
If we add one more character to our search pattern, no matching will be found: <br />

/***javab***/ \
java \ python ruby1.9 javascript c#

Now let's use special character (**metacharacter**) - dot <span style="color: pink">.</span> to find **any** character:

/***.***/ \
***java \ python ruby1.9 javascript c#*** 

Combining special and usual characters need to take into account special symbols
behavior. In the following example ***1.9*** symbols are set in pattern. 
This pattern doesn't match ***1.9*** exact symbol combination, but all substrings where ***1*** - first character, ***9*** - last character 
and any character is in between.

/***1.9***/

java \ python ruby/***1.9***/ javascript c#

java \ python ruby/***189***/ javascript c#

java \ python ruby/***1k9***/ javascript c#

To use a dot as punctuation mark **character escaping** is needed. It can be achieved with backslash ***\\*** before **metacharacter**:

/***1\.9***/

java \ python ruby/***1.9***/ javascript c#

java \ python ruby/189/ javascript c#.

