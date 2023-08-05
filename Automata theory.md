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
* Language that is recognized by <u>at least one</u> finite automaton(DFA or NFA) is called regular language

# Non-regular language
* Language that has more pattern for accepted strings
* Example: $\lbrace a^{N}b^{N}|N\ is\ a\ number\rbrace, \lbrace ababb, ababbababb, ababbababbababb ... \rbrace$





