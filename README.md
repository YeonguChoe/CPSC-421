# Theory of Computing
## Automaton $M$
![Finite automaton](./image/Finite%20automaton.png)
* Finite automaton은 $(Q,\Sigma,\delta,q_0,F)$인 5 tuple이다.
* 어원적으로 "a self-acting machine"이라는 뜻이다.
* Automaton은 singular이고 Automata는 plural이다.

## Terminology of automaton
![Terminology of automata](./image/Terminology%20of%20automata.png)

|표기 방법|예시|의미|
|-------|---|---|
|$q_n$|$q_1,q_2,q_3...$|state|
|$q_0$|$q_0$|start state|
|$w_i$|1|input symbol|
|$w$|1011101, $w_1w_2w_3w_4w_5$|string: a sequence input symbols|
|$\varepsilon$|""|empty string: string of length 0|
|$\Sigma$|$\{0,1\}$|alphabets: a set of distinct types of symbols|
|$L(M)$|$\lbrace w \|M\ accepts\ w \rbrace$|Language of $M$: If string ends at accept state when we run the string at the automaton, we call the string is in language of machine.|
|$\emptyset$|$L(M)=\lbrace \rbrace =\emptyset$|Empty language: If the automaton doesn't accept any string, the language of machine is empty set|
|$Q$|$\lbrace q_1,q_2,q_3\rbrace$|Finite set of states|
|$\delta(q,a)$|![Transition function](./image/Transition-function.png)|Transition function: $q$: current state, $a$: symbol in a string|
|$F$|$\lbrace q_4,q_{21} \rbrace$|set of accept states|

* $M\ recognizes\ A$ 뜻: Automaton에서 string을 따라 갔을때, accept state에서 끝난다.

### Transition function의 예
![Transition function](./image/Transition%20function.png)

## Regular operation
![Regular operation of automaton](./image/Regular%20operation%20of%20automaton.png)

|표기법|이름|하는 일|
|----|---|-----|
|$\cup$|union|2개의 set을 합친다.|
|$∘$|concatenation|2개의 set에 있는 element들을 모든 경우의 수를 고려해서 붙인다. 연산에 순서가 있다. $A∘B \neq B∘A$|
|$^*$|star operation|set에 있는 element들로 만들수 있는 모든 string의 set|

