# Theory of Computing

## Terminology of automaton
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

### Transition function example
![Transition function](./image/Transition%20function.png)


## Regular language
### Regular expresion
![Regular operation of automaton](./image/Regular%20operation%20of%20automaton.png)

|Notation|Name|What it does|
|----|---|-----|
|$\cup$|union|Combining two languages(set of strings) to create one new language|
|$∘$|concatenation|Concatenate strings from the first language to second language. Order does matter: $A∘B \neq B∘A$|
|$^*$|star operation|generate the set of all possible combinations of elements in original set, including the empty set|

### Regular language
* Language that is recognized by <u>at least one</u> finite automaton(DFA or NFA) is called regular language

### Non-regular language
* Language that has more pattern for accepted strings
* Example: $\lbrace a^{N}b^{N}|N\ is\ a\ number\rbrace, \lbrace ababb, ababbababb, ababbababbababb ... \rbrace$

## Types of automaton
1. DFA
1. NFA
1. GNFA
1. PDA
1. Turing machine

## Deterministic Finite Automaton(DFA)
![Finite automaton](./image/Finite%20automaton.png)
* Finite automaton is $(Q,\Sigma,\delta,q_0,F)$ 5 tuple.
* Etymologically, it means "a self-acting machine"
* Automaton is singular and Automata is plural form of automaton.


## Nondetermistic Finite Automaton (NFA)
![NFA](./image/NFA.png)

### Nondeterminism
* $\varepsilon$-transition: free movement without reading input symbol
* Accept string if <u>at least</u> one path ends at accept state

## Generalized Nondeterministic Finite Automaton (GNFA)
* In GNFA, we allows regular expressions as a transition function

## Pumping Lemma
### Statement
* If a language is regular, every string in the language have a section that can be repeated any number of times and still within the language.
* All strings in the language can be repeated if that string is as long as the pumping length $p$.

### Usage
method for proving the language is non-regular

## Context Free Grammars (CFGs)


## Context Free Language

## Pushdown Automata (PDA)

## Turing machines (TMs)


## Multi-tape Turing machine

## Nondeterministic Turing machine

================여기까지 정리 하기===================

## Quantified Boolean Formula(QBF)

## Cook-Levin Theorem

## Space compexity (In depth needed)
* PSPACE


## Savitch's theorem


# L vs NL problem (Like P vs NP)
## Logarithmic space


## NL

## coNL