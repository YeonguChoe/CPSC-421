# Pushdown automaton(PDA)
* Pushdown automaton is $(Q,\Sigma,\Gamma,\delta,q_{0},F)$ 6 tuple.
* accept string if some thread is in accept state after reading all the input symbols in the string
## Stack operations
* push: write at the top of stack and push every alphabet down
* pop: read an alphabet located at the top of the stack and remove that alphabet

## Schematic diagram
![Pushdown automaton](/image/Pushdown%20automaton.png)
* PDA act like nondeterminicstic finite automaton, so the machine accepts string if there is <u>at least</u> one path that ends at accept state.
* input is a string that PDA is reading.
* PDA have a stack which have unlimited space.


## Transition

$$
\underset{\text{read}}{a},\underset{\text{pop}}{b}\rightarrow\underset{\text{push}}{c}
$$

* Condition to take transition
    * head is pointing at the input symbol $a$ **and**
    * we can pop stack symbol $b$ from stack
* Result of transition
    1. move head to next input symbol
    2. pop stack symbol $b$ from stack
    3. push $c$ at the top of the stack

## Formal definition of PDA
![PDA formal definition](/image/PDA%20formal%20definition.png)

 $$
 \underset{\text{current state}}{Q}\times \underset{\text{input symbol}}{\Sigma_{\varepsilon}}\times \underset{\text{stack symbol at the top of stack}}{\Gamma{\varepsilon}}\rightarrow \underset{\text{new state, new stack symbol at the top}}{\mathcal{P}(Q\times \Gamma_{\varepsilon})}
 $$

|Notation|Example|Meaning|
|-------|---|---|
|$\Sigma$|a|input alphabet|
|$\Gamma$|b|stack alphabet|
|$\delta(q,a,c)$|$\delta(q,a,c)=\lbrace(q_{1},d),(q_{2},e)\rbrace$|Transition function: $q$: current state, $a$: input symbol in a string $c$: stack symbol at the top of stack; example $(q_{1},d)$: go to state $q_{1}$ and push $d$ at the top of stack|
|$\Gamma_{\varepsilon}$||don't do any operation(read/write) on stack|
 

