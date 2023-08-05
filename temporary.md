# Closure property
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