# Non-regular language
* We cannot construct a finite automaton that counts the number of input symbol.
* Non-regular language is a set of strings that constructed automaton machine need to know the structure of the whole string.

# Showing a set of strings is not a regular language
* We always need to write <u>proof</u> to show the set is not a regular language.

## Pumping Lemma
* There are specific properties that all the <u>regular language</u> have as minimum requirement.
* Property
    * For all strings in a regular language which is longer than specific length, we can modify that string and still exist within the same language.
    * Way of modification
        1. take a string in the language, longer than $p$
        1. divide the string into three parts like $s=xyz$ where $y$ part can be pumped multiple times. (This $y$ part cannot be a empty string)
    * If you find this middle part $y$ which can be pumped, then the language is a regular language.

### Proof
1. Let's say DFA machine $M$ recognizes a set of strings $A$. And let $p$ be the number of states in $M$.
1. Then, the string longer than $p$ will repeat a state more than once.
1. We call looping transition function in the machine to be $y$.
1. Then, that $y$ part can be repeated multiple times.  

![Proof of pumping lemma](/image/Proof%20of%20pumping%20lemma.png)

# Example of using of the pumping lemma
## Show the set $D=\lbrace0^{k}1^{k}|k\geq0\rbrace$ is a non-regular language
### Proof by contradiction
1. Assume $D$ is a regular language.
1. According to pumping lemma, there should be parts that we can divide into three parts and repeat the second part multiple times.
1. However, there is no such $y$ part in the string.

![Example](/image/Example.png)
