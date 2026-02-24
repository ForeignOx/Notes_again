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
all that remains is to show $f$ is bounded on $\left| z \right|\leq R$, i.e. $\overline{B}_{R}(0)$
By the [[extreme value theorem|extreme value theorem]] since $\left| f \right|$ (being continuous) attains a maximum value on the closed, bounded set $\overline{B}_{R}(0)$, i.e.
$$
\exists K>0: \left| f(z) \right| \leq K ~\forall z\in  \overline{B}_{R}(0)
$$
Thus $\left| f(z) \right|\leq\max\left\{ 1,k \right\}$ for $z\in \mathbb{C}$, hence by [[Lioville's theorem|Lioville's theorem]] $f$ and thus $p$ is constant
## Corollary
Suppose
$$
p(z)=c_{d}z^{d}+c_{d-1}z^{z-1}+\dots+c_{1}z+c_{0}
$$
Then if $d\geq 1$, then there exists $1\leq n\leq d$ and complex numbers $a_{1},\dots,a_{n}$ and natural numbers $k_{1},\dots,k_{n}$ such that
$$
p(z)=c_{d}(z-a_{1})^{k_{1}}(z-a_{2})^{k_{2}}\dots(z-a_{n})^{k_{n}}
$$
With $\sum_{i=1}^{n}k_{i}=d$ and $a_{i}$ and $k_{i}$ are unique up to reordering
## Example
Let
$$
p(z)=z^{2}-4iz-4-2i
$$
This is zero when
$$
0=z^{2}-4iz-4-2i=(z-2i)^{2}-4-2i+4
$$
$$
\implies (z-2i)^{2}=2i=2e^{ i \frac{\pi}{2} }
$$
so $z-2i=\sqrt{ 2 }e^{ i \frac{\pi}{4}+ \frac{2\pi ik}{4} }$
For $n \in \left\{ 0,1 \right\}$
## Remark
If $p(a)=0$ then there is a $k\in \mathbb{N}$ such that $p(z)=(z-a)^{k}Q(z)$ where $Q$ is a polynomial with $Q(a)\neq 0$
## Definition
