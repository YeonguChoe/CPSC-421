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
* Example
    * all strings over $\Sigma=\{0,1\}$ that contains 1: ${(0\cup1)}^{*}1{(0\cup1)}^{*}$
    * all strings having exactly two 1s: $0^{*}10^{*}1$
    * all strings that are even length: $((0\cup1)(0\cup1))^{*}$