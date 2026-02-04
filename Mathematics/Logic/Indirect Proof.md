Let $A$ be a [[Proposition|proposition]], indirect proof is that not(not$A$) is equivalent to $A$, so rather than showing that $A$ is true, we show not $A$ is false
For all $x$ we have $A(x)$, negation is that there exists $x$ such that not $A(x)$
There is $x$ such that $B(x)$ negates to for all $x$ we have not $B(x)$
For all $x$ there is $y$ with $C(x,y)$ negates to there is $x$ such that for all $y$ we have not $C(x,y)$
The negation of $A\implies B$ is $A\cap \text{not}B$, which we can show with a truth table:

| $A$ | $B$ | $A\implies B$ | not $B$ | $A$ and not $B$ |
| --- | --- | ------------- | ------- | --------------- |
| T   | T   | T             | F       | F               |
| T   | F   | F             | T       | T               |
| F   | T   | T             | F       | F               |
| F   | F   | T             | T       | F               |
So we can see that this is true 
## Example
There is no [[Rational Numbers|rational]] $x$ with $x^{2}=2$
The negation is that "there is rational $x$ with $x^{2}=2$", then $x=\frac{p}{q}$ with $p \in\mathbb{Z},q\in\mathbb{N}$ with $\frac{p}{q}$ being a fraction in its lowest form, so do the process $\frac{p_{i}}{q_{i}}=\frac{\frac{p_{i-1}}{2}}{\frac{q_{i-1}}{2}}$ until one of them is not divisible by $\hspace{0pt}2$.
$x^{2}=2\implies \frac{p^{2}}{q^{2}}=2\implies p^{2}=2q^{2}$, so $p^{2}$ is even, hence $p$ is even or $p=2k$ then $p^{2}=4k^{2}=2q^{2}\implies q^{2}=2k^{2}$, so $q^{2}$ is even, hence $q$ is even, buuuuuut this is not cool because $p$ and $q$ are meant to be in their lowest form and that isn't happenin yo
So the proper way of putting this is
For all rational $x$ we have $x^{2}\neq 2$, negation is: "there is rational $x$ with $x^{2}=2$" which we then showed is not possible
___
There is no polynomial
$$
p(x)=a_{n}x^{n}+a_{n-1}x^{n-1}+\dots+a_{0}
$$
with integer coefficients of degree at least $\hspace{0pt}1$ such that $p(0),p(1),p(2),\dots$ are all prime numbers
Assume the contrrary, and let $p(0)=p$ where $p$ is prime, then $a_{0}=p$, and hence $p(kp)$ is divisible by $p$ for all $k\geq 1$. Because we assumed that all these numbers are prime, it follows that $p(kp)=p$ for all $k\geq 1$, so $p(x)$ takes the same value infinitely many times hence a contradiction
___
Let $F=\left\{ E_{1},E_{2},\dots,E_{s} \right\}$ be a family of subsets with $r$ elements of some set $X$. Show that if the intersection of any $r+1$ (not necessarily disctinct) sets in $F$ is nonempty, then the intersection of all sets in $F$ is nonempty
Assume for a contradiction that $\bigcap_{i=1}^{s}E_{i}=\emptyset$. Consider the set $E_{1}=\left\{ x_{1},x_{2},\dots,x_{r} \right\}$. Because none of the $x_{i}$ lies in the intersection of all the $E_{j}$'s (this intersection being empty), it follows that for each $i$, we can find some $E_{j_{i}}$ such that $x_{i}\not\in E_{j_{i}}$. Then
$$
E_{1}\cap E_{i_{1}}\cap E_{i_{2}}\cap\dots \cap E_{i_{r}}=\emptyset
$$
since, at the same time, this intersection is included in $E_{1}$. But this contradicts the hypothesis. Hence contradiction.


#Mathematics #Logic 