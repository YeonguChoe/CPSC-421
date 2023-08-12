# Pumping Lemma for CFL
* pumping lemma is used for proving the language is not context free.
## Condition for pumping lemma
![Pumping lemma for CFL](/image/Pumping%20lemma%20for%20CFL.png)
1. Every context free language which have $length\geq p$ can be seperated into $uvxyz$. and $v$ and $y$ can be pumped the same number of times and still in the same language.
1. $v$ and $y$ together cannot be empty strings. At least, one of them should be non empty string.
1. length of $vxy$ section should be less than $p$


## Proof by picture
![Proof for pumping lemma for CFL](/image/Proof%20for%20pumping%20lemma%20for%20CFL.png)

* $E$ is the start variable.
* $R$ is a variable, which will be replaced by other terminals.
* upper $R$ is generating the big portion of string($vxy$)
* lower $R$ is generating the small portion of string($x$)
