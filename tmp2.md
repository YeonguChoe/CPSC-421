# Pushdown automaton(PDA)
## Stack operations
* push: write on the top of stack and push every element down
* pop: read the top element of the stack and remove that element

## Schematic diagram
![Pushdown automaton](/image/Pushdown%20automaton.png)
* PDA act like nondeterminicstic finite automaton, so the machine accepts string if there is <u>at least</u> one path that ends at accept state.
* input is a string that PDA is reading.
* PDA have a stack which have unlimited space.


## Transition

$$
\underset{\text{read}}{a},\underset{\text{pop}}{b}\rightarrow\underset{\text{push}}{c}
$$

* Condition to take transition
    * head is pointing at the input symbol $a$ **and**
    * we can pop $b$ from stack
* Result of transition
    * move head to next input symbol
    * pop $b$ from stack
    * push $c$ at the top of the stack