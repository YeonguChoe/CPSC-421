# Encoding objects into a string
* Given $O$ which an object(Example: automaton, graph ...), $\langle O \rangle$ is an encoding of the object into a string.
* For a string that contains multiple objects, we write $\langle O_{1},O_{2},\cdots \rangle$


# Notation of Turing machine

$$
\begin{align}
M=``&\text{On input } w\\
&\text{[Description of algorithm]}"
\end{align}
$$

# Acceptance problem for Deterministic finite automata

$$
\text{Let the language } A_{DFA}=\lbrace \underset{\text{}}{\langle B, w \rangle}|\text{B is a Deterministic finite automaton that accepts w} \rbrace
$$

## Theorem
* $A_{DFA}$ is decidable.
* There is a turing machine that accept and halt for language $A_{DFA}$, and reject and halt for strings that are not inside $A_{DFA}$
### Proof: There is a turing machine $D_{A_{DFA}}$ which is a decider for the language $A_{DFA}$

1. Turing machine(Decider)

$$
\begin{align}
D_{A_{DFA}}=&\text{On input string } s\\
&\text{1. Check input string s has the form <B,w> where B is a DFA and w is a string; reject the string if it is not.}\\
&\text{2. Simulate the DFA B on w}\\
&\text{3. If the DFA B ends in accept state, accept <B,w>; otherwise reject <B,w>}
\end{align}
$$

![Decider for A_DFA](/image/Decider%20for%20A_DFA.png)