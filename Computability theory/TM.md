# Turing machine
* Turing machine is a model of general computer.

![Turing machine](/image/Turing%20mahcine.png)

## Feature of Turing machine
1. Head can read and write on input tape
1. Head can move either left or right on the input tape
1. Tape has start, but the infinite to the right.
1. Tape can have blank symbol(˽).
1. Turing machine can accept or reject anytime(not only at the end of string)
1. On input $w$, the turing machine $M$ can end up
    * halt (in accept state or reject state)
    * run forever with loop
1. Turing machine has possibile 3 output on one input $w$
    * accept (at $q_{accept}$)
    * reject by halting (entering $q_{reject}$)
    * reject by looping


## Formal definition of Turing machine
* Turing machine is a 7 tuple $\left (Q,\Sigma,\Gamma,\delta,q_{0},q_{accept},q_{reject} \right )$


|Notation|Meaning|
|-------|---|
|$\Sigma$|input alphabet. All of input symbol is from tape alphabet $\left(\Sigma \subseteq \Gamma \right)$; blank symbol(˽) is not allowed in the input alphabet|
|$\Gamma$|tape alphabet|
|$\delta$|Transition function

### Transition function
$$
\delta: \underset{\text{current state}}Q \times \underset{\text{symbol head is pointing}}{\Gamma} \rightarrow \underset{\text{new state}}{Q} \times \underset{\text{write new symbol at tape}}{\Gamma} \times \underset{\text{move head to left or right}}{\lbrace L,R \rbrace}
$$

* Example
    * $\delta(q,a)=(r,b,R)$
        * If current state is at $q$ and the head is pointing at $a$,
            1. move state to $r$
            1. write $b$ at the location of the tape which had $a$
            1. move head to the right.


# Decider
* Turing machine that halts on all inputs.

# Turing recognizable and decidable

|Language classification|Meaning|
|--------------|-------|
|Turing-recognizable|there exists a TM which will accept and halt for all of strings in the language.; For strings not in language, TM doesn't need to halt for strings.|
|Turing-decidable|there exists a TM which will accept and halt for all strings in the language.;The TM reject and halts for the strings that are not in language.|


# Multitape turing machine
![Multitape turing machine](/image/Multitape%20TM.png)

* Turing machine having more than one tapes
    * One tape is input tape
    * Rest of the tapes are work tapes
* Multitape turing machine has heads for each tapes and head can move simultaneously.
* Having more tape doesn't mean machine can recognize more inputs.

# $\text{Multitape TM}\rightarrow \text{Single tape TM}$
![from MTM to STM conversion](/image/Multitape%20TM%20to%20Single%20tape%20TM.png)
## structure conversion
1. Put each tape of multiple TM to blocks and end that block with blank symbol.
2. Record head position of each block with dotted symbol.
## rule conversion
In order to simulate multitape turing machine's single step,
    1. scan entire tape to find dotted symbols
    2. scn again to update according to transition function of multitape turing machine
    3. shift blocks as needed
    4. accept/reject following the rule of multitape turing machine. 

# Nondeterministic turing machine
![NTM](/image/NTM%20tree.png)
* NTM is the same as Deterministic TM except for transition function.
* NTM accepts when there is <u>at least</u> one path that results in accept state.
* NTM rejects if nothing ends up in accept state.

$$
\delta_{NTM}:Q\times \Gamma \rightarrow \mathcal{P}(Q\times R\times \lbrace L,R \rbrace)
$$

# $\text{NTM}\rightarrow \text{DTM}$
![From NTM to DTM](/image/from%20NTM%20to%20DTM.png)

1. put each thread into blocks
1. put dotted symbol for head location
1. put the starting state of each block at the beginning of each block
1. If a thread accepts, then accept the language.

# Turing enumerator
![Turing enumerator](/image/Turing%20enumerator.png)

* Deterministic turing machine with a printer and a single tape.
* The single tape is filled with blank symbols.
* On the printer side, it prints strings.
* Language of enumerator is the set of strings printer prints.
* Turing enumerator is a generator not the recognizer.

# Theorem
* $A$ is Turing recognizable if and only if $A$ is the language of some Turing enumerator $E$.

## Proof: $E\rightarrow TM$
1. Whenever $E$ prints some string $x$, check if $x$ is the input string of the Turing machine.
2. If the TM's input symbol $w$ is the same as $x$, then accept. If they are different, continue printing.

## Proof: $TM\rightarrow E$
1. Test strings made from $\Sigma^{\star}$ to a Turing machine
2. Whenever the TM accepts, the enumerator prints accepting string.

# Church-Turing thesis
* Algorithm and Turing machine is the same thing.



