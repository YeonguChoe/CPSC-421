# Cartesian product $\times$
* Cartesian product takes two sets and produce a new set that contains all possible ordered pairs of elements.
* $A\times B=\lbrace(a,b)|a \in A\ and\ b \in B \rbrace$

# Power set $\mathcal{P}$
* Power set of a set $S$ is a set of all subsets of $S$.
* $\mathcal{P}(S)=\lbrace x | x \subseteq S \rbrace$

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


# Closure property of regular operation
* If a collection of objects is closed under some operation, then result of applying that operation leaves the collection in the same set.

## Theorem: Union
If $A_{1}, A_{2}$ are regular language, then $A_{1}\cup A_{2}$ is also regular language.

### Proof
1. Lef automaton $M_{1}=(Q_{1},\Sigma_{1},\delta_{1},q_{1},F_{1})$ recognizes language $A_{1}$ and another automaton $M_{2}=(Q_{2},\Sigma_{2},\delta_{2},q_{2},F_{2})$ recognizes language $A_{2}$.
2. Make states that is the cartesian product of states from two machines.

$$
Q_{new}=Q_{1}\times Q_{2}=\lbrace (q_{1},q_{2})|q_{1} \in Q_{1}\ and\ q_{2} \in Q_{2} \rbrace \newline
q_{0}=(q_{1},q_{2}) \newline
$$

3. Make translation for each tuple state and input

$$
\delta_{new} ((q,r),a)=(\delta_{1}(q,a),\delta_{2}(q,a))
$$

4. If one of the machine reaches accept state after running the string, then it is considered as accept state.

$$
F_{new}=(F_{1}\times Q_{2})\cup (F_{2}\times Q_{1})
$$

## Theorem: $\circ$
If $A_{1},A_{2}$ are two regular languages, then $A_{1}\circ A_{2}$ is also regular language.

### Proof
1. create a new NFA, which connect $\varepsilon$-transitions from accept state of the first automaton to the start state of the second automaton

![Proof for concatenation](/image/Proof%20for%20concatenation.png)


## Theorem: $\star$
If $A$ is a regular languages, then $A^{\star}$ is also a regular language.

### Proof
1. Create a new NFA, which connects $\varepsilon$-transition from accept states to start state of previous machine. Then, if a state goes to accept state when following string, it starts over at the automaton.

![Proof for star](/image/Proof%20for%20star.png)

# Deterministic Finite Automaton(DFA)
![Finite automaton](/image/Finite%20automaton.png)
* There is only one path for one string.
* Finite automaton is $(Q,\Sigma,\delta,q_0,F)$ 5 tuple.
* Etymologically, it means "a self-acting machine"
* Automaton is singular and Automata is plural form of automaton.

# Nondetermistic Finite Automaton (NFA)
![Nondeterministic finite automaton](/image/Nondeterministic%20finite%20automaton.png)
* There can be multiple possible path for the same string.
* $\varepsilon$-transition: free movement without reading input symbol
* Accept a string if <u>at least</u> one path ends at accept state
* We can only reject a string if all of the possible paths end up at non-accept state.
* $\Sigma_{\varepsilon}$ is a collection of alphabets and an empty string $\varepsilon$.
* Power set $\mathcal{P}(Q)$ means it is a subset of states.

# Generalized Nondeterministic Finite Automaton (GNFA)
![Generalized nondeterministic finite automata](/image/Generalized%20NFA.png)
* In GNFA, we allows regular expressions as a transition function.
* GNFA transition can read the chunk of string at once.
* GNFA transition can recognize more complex pattern than NFA.

# Converting NFA to DFA
## Theorem
If $A$ is a language of NFA, then A is regular language.

### Proof
1. Given NFA $M=(Q,\Sigma,\delta,q_{0},F)$ which accepts a set of strings A. Create a new DFA $M'$ which have every possible subset of states in the given NFA.

![From NFA to DFA](/image/from%20NFA%20to%20DFA.png)

* set of DFA's states $Q'$ is all the possible subsets of DFA's states.
* DFA's transition function $\delta ' (R,a)$ is  a set of transition functions in NFA that starts at states within $R$ and input symbol $a$.
* starting state of DFA is a subset that only has starting state of NFA.
* set of DFA's accepting states is all of the subsets of $Q'$ which have at least one accept state of NFA.

# Converting regular expression to NFA

## Theorem
* If $R$ is a regular expression and a set of strings $A$ is a language of finite automaton $M$, then $A$ is a regular language.
* If $R$ is a regular expression and $A=L(M)$, then $A$ is a regular language.


### Proof
1. Create an equivalent NFA from regular expression $R$

* If the regular expression only have one state

![Atomic regex](/image/Atomic%20regex.png)

* If the regular expression is a composite of states

![Composite regex](/image/Composite%20regex.png)

# Converting from regular expression to DFA
* Combining (from regular expression to NFA) and (from NFA to DFA), we can get conversion from regular expression to DFA

# Converting from GNFA to regular expression

## Lemma
An GNFA machine always has an equivalent regular expression

### Proof by induction
1. Let $k$ is the number of states in GNFA machine

2. Basic step ($k=2$)
* create GNFA machine

![basic step](/image/from%20GNFA%20to%20regex1.png)
* let the regular expression of the GNFA machine be $R$
3. Inductive step ($k>2$)
* Assume the Lemma is true for $k-1$ and prove for $k$ states, converting $k$ state GNFA to $k-1$ state GNFA
* Given $k$ state GNFA, remove a state which is not the start state and accept state
* add a label for transition to repair the damage by recovering all path that went through removed state

![From GNFA to regex](/image/from%20GNFA%20to%20regex2.png)

# Converting from DFA to regular expression
1. DFA is a type of GNFA $\left( DFA\subset GNFA \subset NFA \right)$. Therefore, all the DFA is a GNFA.
1. Convert from GNFA to regular expression

