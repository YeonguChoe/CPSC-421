# Deterministic Finite Automaton(DFA)
![Finite automaton](/image/Finite%20automaton.png)
* There is only one path for one string.
* Finite automaton is $(Q,\Sigma,\delta,q_0,F)$ 5 tuple.
* Etymologically, it means "a self-acting machine"
* Automaton is singular and Automata is plural form of automaton.

# Nondetermistic Finite Automaton (NFA)
![NFA](/image/NFA.png)
* There can be multiple possible path for one string.
* $\varepsilon$-transition: free movement without reading input symbol
* Accept a string if <u>at least</u> one path ends at accept state

# Generalized Nondeterministic Finite Automaton (GNFA)
* In GNFA, we allows regular expressions as a transition function.