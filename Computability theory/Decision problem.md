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

# Acceptance problem
* A set of strings that contain information about machine $M$, which takes input symbol $w$

# $A_{DFA}$

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

# $A_{NFA}$

$$
\text{Let the language } A_{NFA}=\lbrace \underset{\text{}}{\langle B, w \rangle}|\text{B is a Nondeterministic finite automaton that accepts w} \rbrace
$$

## Theorem
* $A_{NFA}$ is decidable.
* There is a turing machine that accept and halt for language $A_{NFA}$, and reject and halt for strings that are not inside $A_{NFA}$
### Proof: There is a turing machine $D_{A_{NFA}}$ which is a decider for the language $A_{NFA}$

1. Turing machine(Decider)

$$
\begin{align}
D_{A_{NFA}}=&\text{On input string } s\\
&\text{1. Convert NFA B into equivalent DFA } B'\\
&\text{2. Run turing machine } D_{A_{DFA}} \text{on input  }\langle B',w \rangle\\
&\text{3. Accept if } D_{A_{DFA}} \text{ accepts.; otherwise reject.}
\end{align}
$$

# $A_{TM}$
* Let $A_{TM}=\lbrace \langle M,w \rangle|M \text{ is a Turing Machine and } M \text{ accepts input string } w \rbrace$
* Given a turing machine $M$, the turing machine accepts input string $w$.

## Theorem 1: $A_{TM}$ is not a decidable language.
### Proof by contradiction
1. Assume some turing machine $H$ decides $A_{TM}$
    * $H$ on $\langle M,w \rangle$
        * Accept if $M$ accepts $w$
        * Reject if $M$ rejects $w$
2. Construct a turing machine $D$ using $H$

$$
\begin{align}
D=&\text{``On input } \langle M \rangle \\
&\text{1. Simulate }H \text{ on input } \langle M, \langle M \rangle \rangle\\
&\text{2. Accept if }H \text{ rejects}\\
&\text{3. Reject if }H \text{ accepts}\\
\end{align}
$$

3. Therefore,
    * $D$ accepts $\langle M \rangle$ if and only if $M$ doesn't accept $\langle M \rangle$
    * $D$ accepts $\langle D \rangle$ if and only if $D$ doesn't accept $\langle D \rangle$

4. When we make a table out of it.

![A_TM undecidibility](/image/ATM%20undecidibility.png)

5. At the left bottom cell,
* $D$ accepts $\langle D \rangle$ if and only if $D$ doesn't accept $\langle D \rangle$ does not make sense.
* Therefore, it is a contradiction.


## Theorem 2: $A_{TM}$ is a Turing-recognizable language.
### Proof: The following TM $U$ recognizes $A_{TM}$

$$
\begin{align}
U=&\text{``On input } \langle M,w \rangle \\
&\text{1. Simulate }M \text{on input }w\\
&\text{2. Accept if }M \text{ halts and accepts}\\
&\text{3. Reject if }M \text{ halts and rejects"}\\
\end{align}
$$

![Universal turing machine](/image/Universal%20turing%20machine.png)