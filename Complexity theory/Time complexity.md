* All the langauges when studying complexity theory is decidible language.

# Worst-case complexity
* Number of steps needed to decide a language(set of input strings of the same length $n$)
* The upperbound of the number of steps needed is called worst-case complexity.

# Example: Time complexity(steps) to decide $A=\lbrace a^{k}b^{k}|k\geq0 \rbrace$

## Proof

$$
\begin{align}
M=&\text{On input }w\\
& \text{1. Scan input string to check it is the form } a^{k}b^{k}\\
& \text{2. Scan for }a,b\\
& \text{3. Cross out }a,b\\
\end{align}
$$

|Operation|Time compexity|
|---------|--------------|
|Scanning input string checking the form|$O(n)$|
|Scanning for a and b|$O(n)$|
|Crossing out a and b|$O(n)$|
|Scanning and crossing a and b|$O(n^{2})$|

* $M$ takes $O(n)+O(n^{2})$. Therefore, time complexity is $O(n^{2})$.

# Time complexity class
## $t(n)$
* Definition
    * function $t:\mathcal{n}\rightarrow \mathcal{n}$
    * TM $M$ always halt within $t(n)$ steps on all inputs of length $n$
* Example: If an turing machine runs on $n^{2}$ time and input is length of 10, then the machine should halt with in 100 steps.

## $Time(t(n))$
* Definition(Time complexity class): A set of all the languages that 1 tape TM decides within time $t(n)$
* Every regular language can be finished in 1 tape turing machine in time $t(n)$, because TM only need to read the input string.

![Time complexity class](/image/Time%20complexity%20class.png)

# The class P
* Definition: A set of all languages that TM can finish in $TIME(n^{k})$ for some $k$.
* Notation: $\cup_{k}\ TIME(n^{k})$
* We also call class P as polynomial time decidable languages.

# PATH
* Definition: A language (set of strings) that have information about a directed graph and starting point and termination point.
* $PATH=\lbrace \langle G,s,t \rangle |$ G is a directed graph with a path from $s$ to $t\rbrace$

## Theorem $PATH\in P$: Finding path problem is P class

* Proof:

$$
\begin{align}
M=&\text{``On input }\langle G,s,t \rangle\\
&\text{1. Mark }s\\
&\text{2. Mark nodes on path until reaching the leaf node}\\
&\text{3. Accept if node t is marked; reject if not}
\end{align}
$$

* It is $O(n^{4})\in P$