A [[Polynomials|polynomial]] is irreducible if it is non-constant and does not have a proper factorisation, i.e. $f(x)$ cannot be written as $f(x)=g(x)h(x)$ with $\deg g>0$ and $\deg h>0$
## Definition
Let $R$ be a [[Rings|ring]]. An element $a\in R$ is called irriducible if:
- $r$ is not a [[Units|unit]]
- If $r=ab$, then either $a$ is a unit or $b$ is a unit, $a,b\in R$
Note that $0$ is not irreducible, since $0=0\cdot0$ where each factor is not a unit.
___
By this definition, prime numbers in $\mathbb{Z}$ are captured, but also $-p$ for $p$ prime are irreducible (the negative primes)
The crucial fact about irreducible elements in $\mathbb{Z}$ and $\mathbb{F}[x]$ is:
## Lemma
Let $R$ be either $\mathbb{Z}$ or $\mathbb{F}[x]$ for $\mathbb{F}$ is a field, if $p \in R$ is irreducible and $p|ab,a,b\in R$, then $p|a$ or $p|b$
### Proof
Suppose $p$ is irreducible and $p|ab$. If $\gcd(p,a)\neq 1$, then there is an $m\in R$ such that $m|p,m|a$ and $m$ is not a unit (if the only common divisors are units, then the greatest is $\hspace{0pt}1$ (for $\mathbb{Z}$) or can be rescaled to $\hspace{0pt}1$ (for $\mathbb{F}[x]$))
Since $m|p$, $p=mu,u\in R$, but $p$ is irreducible by hypothesis, but since $m$ is not a unit, $u$ must be a unit
Since $m|a,a=mx,x\in R$, so $a=u^{-1}(mu)x$, hence $mu|a$, i.e. $p|a$
On the other hand, if $\gcd(p,a)=1$, then by the [[Euclidean Algorithm|euclidean algorithm]], $\exists \alpha,\beta$ such that
$$
\alpha p+\beta a=1
$$
$$
\implies \alpha pb+\beta ab=b
$$
We know that $p|ab$, so $p$ divides the whole left hand side, so $p|b$
## Another Lemma
Let $R$ be a commutative ring, let $x\in R$ be irreducible and $u\in R^{\times}$ be a unit, then $ux$ is also irreduciblwe
### Proof
To prove that $ux$ is irreducible, first show it is not a unit
If it were, then $\exists v\in R$ such that $vux=1$, but then $x$ would be a unit (as $vu$ times $x$ would be $\hspace{0pt}1$, which we've assumed it isn't)
Now we need to show that if $ux=ab$, then $a$ is a unit or $b$ is a unit, then
$$
ux=ab\implies x=u^{-1} ab=(u^{-1}a)b
$$
    So either $u^{-1}a\in R^{\times }$ or $b\in R^{\times}$, if $u^{-1}a\in R^{\times}$ then $a\in R^{\times}$, hence $ux$ is irreducible
    