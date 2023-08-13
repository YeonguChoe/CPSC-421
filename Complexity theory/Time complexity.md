* All the langauges when studying complexity theory is decidible language.

# Worst-case complexity
* Number of steps needed to decide a language(set of input strings of the same length $n$)
* The upperbound of the number of steps needed is called worst-case complexity.

# Example: Time complexity(steps) to decide $A=\lbrace a^{k}b^{k}|k\geq0 \rbrace$

## Proof

$$
\begin{align}
M=&\text{On input }w\\
& \text{1. Scan input string to check it is the form } a^{k}b^{k}\\
& \text{2. Scan for }a,b\\
& \text{3. Cross out }a,b\\
\end{align}
$$

|Operation|Time compexity|
|---------|--------------|
|Scanning input string checking the form|$O(n)$|
|Scanning for a and b|$O(n)$|
|Crossing out a and b|$O(n)$|
|Scanning and crossing a and b|$O(n^{2})$|

* $M$ takes $O(n)+O(n^{2})$. Therefore, time complexity is $O(n^{2})$.
