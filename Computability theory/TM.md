# Turing machine
* Turing machine is a model of general computer.

![Turing machine](/image/Turing%20mahcine.png)

## Feature of Turing machine
1. Head can read and write on input tape
1. Head can move either left or right on the input tape
1. Tape has start, but the infinite to the right.
1. Tape can have blank symbol(˽).
1. Turing machine can accept or reject anytime(not only at the end of string)

## Formal definition of Turing machine
* Turing machine is a 7 tuple $\left (Q,\Sigma,\Gamma,\delta,q_{0},q_{accept},q_{reject} \right)$


|Notation|Example|Meaning|
|-------|---|---|
|$\Sigma$||input alphabet. All of input symbol is from tape alphabet $\left(\Sigma \subseteq \Gamma \right)$; blank symbol(˽) is not allowed in the input alphabet|
|$\Gamma$||tape alphabet|
|$\delta$|$\underset{\text{current state}}Q \times \underset{\text{symbol head is pointing}}{\Gamma} \rightarrow \underset{\text{new state}}{Q} \times \underset{\text{write new symbol at tape}}{\Gamma} \times \underset{\text{move head to left or right}}{\lbrace L,R \rbrace}$|Transition function

