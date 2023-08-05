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
![Gneralized nondeterministic finite automata](/image/Generalized%20NFA.png)
* In GNFA, we allows regular expressions as a transition function.
* GNFA transition can read the chunk of string at once.
* GNFA transition can recognize more complex pattern than NFA.
