# regular-expressions

### Useful links:
[Regular expressions cheatsheet](https://cheatography.com/davechild/cheat-sheets/regular-expressions/) <br />
[Regex online editor](https://regex101.com/)

## Intro
Regular expressions is a powerful tool for effective work with text. 
It is a formal language used for searching characters and substring manipulations.
Regular expressions it is a special string which sets a search pattern.

## 1. Characters and metacharacters

/<span style="color: pink">java</span>/<br />
<span style="color: pink">java</span> \ python ruby1.9 <span style="color: pink">java</span>script c#

<span style="color: pink">/</span> - this symbol is called **delimiter**. It is used at the beginning and at the end of regular expression 
to separate regex from another text. Such matching is called **exact**. Characters combinations
were found in text matching **exactly** with given pattern.
If we add one more character to our search pattern, no matching will be found: <br />

/<span style="color: pink">javab</span>/<br />
java \ python ruby1.9 javascript c#

Now let's use special character (**metacharacter**) - dot <span style="color: pink">.</span> to find **any** character:

/<span style="color: pink">.</span>/<br />
<span style="color: pink">java \ python ruby1.9 javascript c#</span>

Combining special and usual characters need to take into account special characters
behavior. In the following example <span style="color: pink">1.9</span> symbols are set in pattern. 
This pattern doesn't match <span style="color: pink">1.9</span> exact characters combination, but all substrings where <span style="color: pink">1</span> - first character, <span style="color: pink">9</span> - last character 
and any character is in between.

/<span style="color: pink">1.9</span>/

java \ python ruby/<span style="color: pink">1.9</span>/ javascript c#

java \ python ruby/<span style="color: pink">189</span>/ javascript c#

java \ python ruby/<span style="color: pink">1k9</span>/ javascript c#

To use a dot as punctuation mark **character escaping** is needed. It can be achieved with backslash <span style="color: pink">"\"</span> before **metacharacter**:

/<span style="color: pink">1\.9</span>/

java \ python ruby/<span style="color: pink">1.9</span>/ javascript c#

java \ python ruby/189/ javascript c#.

