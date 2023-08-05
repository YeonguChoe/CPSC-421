
## Deterministic Finite Automaton(DFA)
![Finite automaton](/image/Finite%20automaton.png)
* Finite automaton is $(Q,\Sigma,\delta,q_0,F)$ 5 tuple.
* Etymologically, it means "a self-acting machine"
* Automaton is singular and Automata is plural form of automaton.


## Nondetermistic Finite Automaton (NFA)
![NFA](/image/NFA.png)

### Nondeterminism
* $\varepsilon$-transition: free movement without reading input symbol
* Accept string if <u>at least</u> one path ends at accept state

## Generalized Nondeterministic Finite Automaton (GNFA)
* In GNFA, we allows regular expressions as a transition function.