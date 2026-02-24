An important class of [[Holomorphicity|entire]] [[functions|functions]] are non-constant [[polynomials|polynomials]] of the form
$$
p(z)=c_{d}z^{d}+c_{d-1}z^{z-1}+\dots+c_{1}z+c_{0}
$$
where $c_{i}\in \mathbb{C}$, $c_{d}\neq 0$ and $d\geq 1$ is the degree
## Proposition
If $p:\mathbb{C}\to \mathbb{C}$ is a non-constant polynomial (with complex coefficients) then
$$
\left| p(z) \right| \to \infty \text{ as }\left| z \right| \to \infty
$$
## Theorem
Every non-constant polynomial (with complex coefficients) has a complex root. That is, there exists $a\in\mathbb{C}$ such that $p(a)=0$
### Proof
By contradiction. First note by the above proposition, $\exists R>0$ such that $\left| p(z) \right|>1$ wheneber $\left| z \right|>R$. Fix this $R$
Assume $p$ has no root (so $p(z)\neq 0$ on $\mathbb{C}$)
In particular,
$$
f(z):=\frac{1}{p(z)}
$$
Is entire. We aim to show $f$ is bounded
Note for $\left| z \right|>R$, we have 
$$
\left| f(z) \right| =\frac{1}{\left| p(z) \right| }<1
$$
