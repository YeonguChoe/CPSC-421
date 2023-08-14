# Space complexity
## Definition for deterministic turing machine
* number of cells a turing machine $M$ scans over on its tape.
* The head of turing machine visits the maximum $f(n)$ tape cells on all inputs of length $n$.
* A tape cell is a square on tape that can contain a input symbol.

## Definition for Nondeterministic turing machine
* On each branch use maximum $f(n)$ cells on all inputs of length $n$

# Space complexity class

## $SPACE\left ( f(n) \right)$
* Definition: A set of languages that can be finished with at most $f(n)$ cells in 1 tape turing machine.

## $NSPACE\left (  f(n) \right)$
* Definition: A set of languages that can be finished with at most $f(n)$ cells in each branch of nondeterministic 1 tape turing machine.

# PSpace
* Definition: set of languages that can be finished with at most polynomial space cells.
* A set of $SPACE(n^{k})$
* $PSPACE=\cup_{k} SPACE(n^{k})$

# NPSpace
* Definition: set of languages that nondeterministic turing machine use at most polynomial space cells on $n$ length inputs.
* A set of $NSPACE(n^{k})$
* $NPSPACE=\cup_{k} NSPACE(n^{k})$

# Relationship between time complexity and space complexity

## Theorem 1: $Time \left(t(n) \right)\subseteq Space \left( t(n) \right)$
* If a set of languages take maximum $t(n)$ time, then the language uses at most $t(n)$ cells as space.
* Proof: A turing machine that runs within $t(n)$ steps cannot use more than $t(n)$ cells.

## Theorem 2: $Space \left ( t(n) \right )\subseteq Time \left( c^{t(n)} \right)$
* If as set of languages use at most $t(n)$ cells of space, then it takes maximum $({\#\ of\ states})^{t(n)}$ times.
* When reading the $t(n)$ cells, the turing maching can change states $t(n)$ times.

## Theorem 3: $P\subseteq PSpace$
* If a set of languages finish in polynomial time, then the set of languages use polynomial time space.

## Theorem 4: $NP\subseteq PSpace$
* We need to convert nondeterministic turing machine to deterministic turing machine.
* Satisfibility problem needs to store variables in space. Therefore, SAT problem is in PSpace.
* If $A\leq_{P}B$ and $B\in PSPACE$, then $A\in PSPACE$

# co-NP class
* A set of languages that does not have $NP$ languages.
## Theorem: $coNP\subseteq PSPACE$
* If a set of languages are coNP, then the languages use polynomial cell spaces.



# Savitch's Theorem: 
* $NPSPACE \left(f(n) \right)\subseteq SPACE\left(f^{2}(n)\right)$
* If a set of languages use polynomial space $f(n)$ in nondeterministic turing machine, then it use $f^{2} (n)$ space in deterministic turing machine.

# PSPACE-complete
* Definition: A set of languages $B$ is in PSPACE-complete if
    * $B\in PSPACE$
    * If a language $A\in PSPACE$, then $A\leq_{P}B$

