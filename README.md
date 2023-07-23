# Theory of Computing
## 기본 약어
|표기 방법|예시|의미|
|-------|---|---|
|$w_i$|1|input symbol|
|$w$|1011101, $w_1w_2w_3w_4w_5$|string made of a sequence input symbols|
|$\epsilon$|n/a|empty string|
|$\Sigma$|$\{0,1\}$|finite set of alphabets(types of symbols)|
|$L(M)$|n/a|If string ends at accept state when we run the string at the automaton, we call the string is in language of machine.|
|$\emptyset$|$L(M)=\left \{ \right \} =\emptyset$|Empty language: If the automaton doesn't accept any string, the language of machine is empty set|


* $M\ recognizes\ A$ 뜻: string을 따라 갔을때, accept state에서 끝난다.


* $\empty$: empty language
    * 어떤 string도 accept하지 않는 경우, language of machine은 공집합이다.
    * 예: $L(M)=\empty=\{\}$
* $q_1,q_2,q_3...$: state
* $q_0$: start state
* $Q$: Finite set of states
    * 예: $\{q_1,q_2,q_3\}$
* $\delta(q,a)$: transition function
    * $q$: 현재의 state
    * $a$: string에 있는 symbol
* $F$: set of accept states
    * $\{q_4,q_{13}\}$

## Automaton
* 어원적으로 "a self-acting machine"이라는 뜻이다.
