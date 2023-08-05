# Regular operation
![Regular operation of automaton](./image/Regular%20operation%20of%20automaton.png)

|Notation|Name|What it does|
|----|---|-----|
|$\cup$|union|Combining two languages(set of strings) to create one new language|
|$∘$|concatenation|Concatenate strings from the first language to second language. Order does matter: $A∘B \neq B∘A$|
|$*$|star operation|generate the set of all possible combinations of elements in original set, including the empty set|

# Regular expression
* Regular expression is built with
    * alphabets in $\Sigma$
    * regular operation ($\cup,∘,*$)
* Reason for using regular expression
    * we can describe complex patterns with compact and easy syntax.
    * if a language can be written in regular expression, then it is a regular language.