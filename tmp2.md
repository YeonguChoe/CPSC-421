# Context free grammar
* CFG is a computation model that can do more things than finite automaton.

# Terminology of Context free grammar

|Notation|Example|Meaning|
|--------|-------|-------|
|$()\rightarrow()$|$A\rightarrow 0A1$|Production: (substitution) rule used in CFG|
|symbol|$A$|Variable: symbols at the left side of a substitution rule|
|symbol|$0,1$|Terminal: symbols that only exist at the right side of a substitution rule; empty string $\varepsilon$ is not considered a symbol as it is a string.; $A$ appears on the left hand side as well, so it is not a terminal.|
|$S$|$S$|Starting variable: Top left symbol among substitution rules|
|$L(G)$|$\lbrace \emptyset,01,0011,000111...\rbrace$|set of all the generated strings|
|$V$|$\lbrace A,S\rbrace$|Variables|
|$\Sigma$|$\lbrace 0,1\rbrace$|Terminals|
|$R$|$\lbrace S\rightarrow 0S1, S\rightarrow R, R\rightarrow \varepsilon \rbrace$|(substitution) rules|


# Creating string from context free grammar
1. write down starting variable
1. replace all the variables using substitution rules until only terminal remains
1. what is remaining is the generated string

![Example of context free grammar](/image/Example%20of%20CFG.png)
