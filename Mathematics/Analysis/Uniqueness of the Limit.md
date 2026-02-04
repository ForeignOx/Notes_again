## Theorem
A real [[Convergence|convergent]] [[Sequences|sequence]] $(x_{n})_{n\in\mathbb{N}}$ has precisely $\hspace{0pt}1$ limit
### Proof
Let $x,x'$ be limits of $x_{n}$, with $x\neq x'$
$$
\varepsilon=\frac{|x-x'|}{2}>0
$$
Since $(x_{n})_{n\in\mathbb{N}}$ converges to $x$, there is $n_{0}\in\mathbb{N}$ such that $|x_{n}-x\mid<\varepsilon$ for al $n\geq n_{0}$
We also have convergence to $x'$, so there exists some $n_{1}\in\mathbb{N}$ with $|x_{n}-x'|<\varepsilon$ for all $n\geq n_{1}$
So for $n\geq \text{max}(n_{0},n_{1})$, we now get:
$$
|x-x'|=|x-x_{n}+x_{n}-x'|\leq |x-x_{n}|+|x_{n}-x'|<2\varepsilon=|x-x'|
$$
Which is a contradiction
## Corollary
A sequence $(z_{n})\in\mathbb{C}$ can have at most one limit
### Proof
This holds since it is true in $\mathbb{R}$. Indeed if $\left\{ z_{n} \right\}$ coverges, then $\left\{ \mathfrak{R}(z_{n}) \right\}$ converges. It can converge to a unique limit, say $x$, similarly $\left\{ \mathfrak{I}(z_{n}) \right\}$ converges to a unique limit $y$, hence $z_{n}$ converges to a unique limit $x+iy$

#Mathematics #Analysis #Theorem 