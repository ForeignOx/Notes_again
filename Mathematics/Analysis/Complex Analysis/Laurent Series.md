## Definition
A laurent [[series|series]] is an expression, in terms of the [[Complex Numbers|complex variable]] $z$ of the form
$$
\sum_{n=-\infty}^{\infty}c_{n}(z-a)^{n}
$$
For $c_{n},a\in\mathbb{C}$
Given a Laurent series of this form, $a$ is called the centre of the Laurent series, the sum
$$
\sum_{n=-\infty}^{-1} c_{n}(z-a)^{n}
$$
Is called the principle part, and the sum
$$
\sum_{n=0}^{\infty}c_{n}(z-a)^{n}
$$
Is called the analytic part
## Notation
We say a Laurent series converges to a point $z\in\mathbb{C}$ iff both
$$
\sum_{n=0}^{N}c_{n}(z-a)^{n}\text{ and } \sum_{n=-M}^{-1}c_{n}(z-a)^{n}
$$
Converge as $N\to \infty$ and $M\to \infty$ respectively, that is, the Laurent series converges iff the principle and analytic parts both converge
## Proposition
Given a Laurent seires of the form $\sum_{n=-\infty}^{\infty} c_{n}(z-a)^{n}$ that is not a power series, (so the principle part is not zero), then either
- the Laurent series converges nowhere
- there exists an [[Annuli|annulus]] $A_{r,R}(a)$ such that the Laurent series converges absolutely on $A_{r,R}(a)$ and diverges when $\left| z-a \right|<r$ or $\left| z-a \right|>R$
    - In this case, $A_{r,R}(a)$ is called the annulus of convergence of the Laurent series around $z=a$