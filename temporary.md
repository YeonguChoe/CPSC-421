# Converting NFA to DFA
## Theorem
If $A$ is a language of NFA, then A is regular language.

### Proof
1. Given NFA $M=(Q,\Sigma,\delta,q_{0},F)$ which accepts a set of strings A. Create a new DFA $M'$ which have every possible subset of states in the given NFA.

![From NFA to DFA](/image/from%20NFA%20to%20DFA.png)

* set of DFA's states $Q'$ is all the possible subsets of DFA's states.
* DFA's transition function $\delta ' (R,a)$ is  a set of transition functions in NFA that starts at states within $R$ and input symbol $a$.
* starting state of DFA is a subset that only has starting state of NFA.
* set of DFA's accepting states is all of the subsets of $Q'$ which have at least one accept state of NFA.

# Converting regular expression to NFA

## Theorem
* If $R$ is a regular expression and a set of strings $A$ is a language of finite automaton $M$, then $A$ is a regular language.
* If $R$ is a regular expression and $A=L(M)$, then $A$ is a regular language.


### Proof
1. Create an equivalent NFA from regular expression $R$

* If the regular expression only have one state
![Atomic regex](/image/Atomic%20regex.png)

* If the regular expression is a composite of states
![Composite regex](/image/Composite%20regex.png)

# Converting from regular expression to DFA
* Combining (from regular expression to NFA) and (from NFA to DFA), we can get conversion from regular expression to DFA

# Converting from GNFA to regular expression

## Lemma
An GNFA machine always has an equivalent regular expression

### Proof by induction
1. Let $k$ is the number of states in GNFA machine
1. Basic step ($k=2$)
    * create GNFA machine
    ![basic step](/image/from%20GNFA%20to%20regex.png)
    * let the regular expression of the GNFA machine be $R$
1. Inductive step ($k>2$)
    * Assume the Lemma is true for $k-1$ and prove for $k$ states, converting $k$ state GNFA to $k-1$ state GNFA
        1. Given $k$ state GNFA, remove a state which is not the start state and accept state
        1. add a label for transition to repair the damage by recovering all path that went through removed state
        ![From GNFA to regex](/image/from%20GNFA%20to%20regex2.png)

# Converting from DFA to regular expression
1. DFA is a type of GNFA $\left( DFA\subset GNFA \subset NFA \right)$. Therefore, all the DFA is a GNFA.
1. Convert from GNFA to regular expression
