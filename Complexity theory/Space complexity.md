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