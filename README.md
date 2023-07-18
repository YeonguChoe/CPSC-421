# 기본 약어
* $w_i$: input symbol
    * 예: 1
* $w$: string(input symbol로 만들어진 문자열)
    * 예: 1011101, $w_1w_2w_3w_4w_5$
* $\epsilon$: empty string
* $\Sigma$: finite set of alphabets(input symbol의 종류)
    * 예: $\{0,1\}$
* $L(M)$: language of machine
    * string을 automaton에서 작동시켰을때 accept state에서 끝나는 string
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

# 오토마톤
* 어원적으로 "a self-acting machine"이라는 뜻이다.
