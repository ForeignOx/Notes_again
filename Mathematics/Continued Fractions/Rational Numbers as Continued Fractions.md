A positive [[Real Numbers|real]] number $x$ has a [[Finite Continued Fraction]]  $\iff x \in \mathbb{Q}$ 
## Proof
If $x=[a_{0};a_{1},a_{2},\dots,a_{n}]$ for $a_{0}\in\mathbb{Z},a; \in\mathbb{Z}^+$, by simple algebra, we see [[Rational Numbers|$x \in \mathbb{Q}$]]
Suppose $x=\frac{a}{b}$ for some $a\in\mathbb{Z}$, $b\in\mathbb{Z}^+$, applying the euclidean algorithm:
$$
a=q_{1}b+r_{1}
$$
$$
b=q_{2}r_{1}+r_{3}
$$
$$
r_{1}=q_{3}r_{2}+r_{3}
$$
$$
\vdots
$$
$$
r_{n-2}=q_{n}r_{n-1}+r_{n}
$$
$$
r_{n-1}=q_{n+1}r_{n}+0
$$
Compare with the [[Divisor Algorithm]]:
$$
\frac{a}{b}=q_{1}+\frac{r_{1}}{b}
$$
call$\frac{r_{1}}{b}=\frac{1}{y_{1}}$
$$
y_{1}=\frac{b}{r_{1}}=q_{2}+\frac{r_{2}}{r_{1}}
$$
$$
y_{2}=\frac{r_{1}}{r_{2}}=q_{3}+\frac{r_{3}}{r_{2}}
$$
$$
\vdots
$$
$$
y_{n-1}=\frac{r_{n-1}}{r_{n-1}}=q_{n}+\frac{r_{n}}{r_{n-1}}
$$
$$
y_{n}=\frac{r_{n-1}}{r_{n}}=q_{n+1}
$$
such that $r_{n}=gcd(a,b)$
Hence
$$
x=\frac{a}{b}=[q_{1};q_{2},\dots,q_{n+1}]
$$

#Mathematics #Fractions #Theorem 