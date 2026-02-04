A [[Real Numbers|real number]] $x$ has an [[Infinite Continued Fraction]] expansion iff $x$ is [[Irrational Numbers|irrational]]
## Proof
WTS: $x$ is irrational $\implies x=[a_{0};a_{1},\dots]$ for some infinite [[Sequences|sequence]] $\{ a_{k} \}$
Consider $x=a_{0}+\frac{1}{y_{0}}$ for $a_{0}=\lfloor x \rfloor,y_{1}>1,y\in\mathbb{R}$, $y_{1}=a_{1}+\frac{1}{y_{2}}$
From what we showed in [[Rational Numbers as Continued Fractions|this theorem]], we know this process won't terminate as $x$ is irrational. To be sure that this constructed infinite continued fraction converges to the same $x$ we started with, we can use the [[Infinite Continued Fraction#An infinite continued fraction Convergence converges if the sequence of convergents, $ { c_{n} }$ converges|theorem of convergence]], $\left| x-c_{k} \right|$ can be arbitrarily small, so $x$ is the limit of $\{ c_{k} \}$ forward from $\{ a_{k} \}$
Secondly we need to show $x=[a_{0};a_{1},\dots]$ for some infinite continued fraction implies $x \in\mathbb{R}\setminus\mathbb{Q}$
Assume, for a contradiction, $x=\frac{a}{b}$ for $a\in\mathbb{Z}$, $b\in\mathbb{Z}^+$, we know $x$ has an infinite continued fraction expansion, so $\left| x-c_{k} \right|\neq 0$. Consider $\left| x-c_{k} \right|$:
$$
\left| x-c_{k} \right|=\left| \frac{a}{b}-\frac{p_{k}}{q_{k}} \right|=\left| \frac{aq_{k}-bp_{k}}{bq_{k}} \right|\geq \frac{1}{bq_{k}}
$$
As the numerator is the maximum product/sum of integers, denominator is strictly positive
By [[Convergents#A real number $x$ with convergents $c_{n}= frac{p_{n}}{q_{n}}$ satisfies $ x-c_{n} < frac{1}{q_{n}q_{n+1}}$|this lemma]], 
$$
\left| x-c_{k} \right|<\frac{1}{q_{k}q_{k+1}}
$$
$$
\implies \frac{1}{bq_{k}}\leq \left| x-c_{k} \right|<\frac{1}{q_{k}q_{k+1}}
$$
And hence $q_{k+1}<b$, but $\{ a_{k} \}$ is unbounded ($q_{k}\geq k$, so as $k\to \infty,q_{k}\to \infty$), so this inequality cannot hold for all $q_{k+1}$, so the infinite continued fraction $x$ must be irrational

#Mathematics #Fractions #Theorem 