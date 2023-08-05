# Cartesian product $\times$
* Cartesian product takes two sets and produce a new set that contains all possible ordered pairs of elements.
* $A\times B=\lbrace(a,b)|a \in A\ and\ b \in B \rbrace$

# Terminology of automaton
![Terminology of automata](./image/Terminology%20of%20automata.png)

|Notation|Example|Meaning|
|-------|---|---|
|$q_n$|$q_1,q_2,q_3...$|state|
|$q_0$|$q_0$|start state|
|$w_i$|1|input symbol|
|$w$|1011101, $w_1w_2w_3w_4w_5$|string: a sequence input symbols|
|$\varepsilon$|""|empty string: string of length 0|
|$\Sigma$|$\{0,1\}$|alphabets: a set of distinct types of input symbols|
|$L(M)$|$\lbrace w \|M\ accepts\ w \rbrace, \lbrace01101,11001,110\rbrace $|Language of $M$: Language is a set of strings that ends at accept state when we run on a automaton.;Also use expression: $M\ recognizes\ L(M)$.|
|$\emptyset$|$L(M)=\lbrace \rbrace =\emptyset$|Empty language: If the automaton doesn't accept any string, the language of machine is empty set|
|$Q$|$\lbrace q_1,q_2,q_3\rbrace$|set of states|
|$\delta(q,a)$|$\delta:Q\times \Sigma \rightarrow Q$|Transition function: $q$: current state, $a$: input symbol in a string|
|$F$|$\lbrace q_4,q_{21} \rbrace$|set of accept states|

* $M\ recognizes\ A$: When following the string in an automaton, it ends at accept state.

## Transition function example
![Transition function](./image/Transition%20function.png)


# Regular language
* Language that is recognized by <u>at least one</u> finite automaton is called regular language

# Non-regular language
* Language that has more pattern for accepted strings
* Example: $\lbrace a^{N}b^{N}|N\ is\ a\ number\rbrace, \lbrace ababb, ababbababb, ababbababbababb ... \rbrace$


# Regular operation
![Regular operation of automaton](./image/Regular%20operation%20of%20automaton.png)

|Notation|Name|What it does|
|----|---|-----|
|$\cup$|union|Combining two languages(set of strings) to create one new language|
|$\circ$|concatenation|Concatenate strings from the first language to second language. Order does matter: $A\circ B \neq B\circ A$|
|$\star$|star operation|generate the set of all possible combinations of elements in original set, including the empty set|

# Regular expression
* Regular expression is built with
    * alphabets in $\Sigma$
    * regular operation ($\cup,\circ,\star$)
* Reason for using regular expression
    * we can describe complex patterns with compact and easy syntax.
    * if a language can be written in regular expression, then it is a regular language.
* Example
    * all strings over $\Sigma=\{0,1\}$ that contains 1: ${(0\cup1)}^{\star}1{(0\cup1)}^{\star}$
    * all strings having exactly two 1s: $0^{\star}10^{\star}1$
    * all strings that are even length: $((0\cup1)(0\cup1))^{\star}$


