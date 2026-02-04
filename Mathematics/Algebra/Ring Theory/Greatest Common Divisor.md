## For $\mathbb{Z}$
Let $a,b\in\mathbb{Z}:a,b\neq 0$, then the greatest common divisor of $a$ and $b$ is $g\in\mathbb{Z}:g|a\text{ and }g|b$ and for any other $d\in\mathbb{Z}:d|a$ and $d|b$, where $d<g$
We can write this as $\text{gcd}(a,b)$
Formally:
$$
\text{gcd}(a,b)=\max\{d\in\mathbb{Z}^{+}:d|a\text{ and } d|b\}
$$
Note $\text{gcd}(a,0)=a$
### Proof of Existence in $\mathbb{Z}$
$\text{gcd}(a,b)$ exist and can be computed by the [[Euclidean Algorithm|Euclidean Algorithm]]. Moreover if $d=\text{gcd}(a,b)$, then $\exists x,y\in \mathbb{Z}$ such that $ax+by=d$. One can also prove this with $F[x]$, where $F$ is a [[Fields|field]].
## For [[Polynomials|Polynomials]]
Let $\mathbb{F}$ be a field, the greatest common divisor of two polynomials"should be" a polynomial of highest degree that divides the two other polynomials. But such a greatest common divisor would not be unique, since every constant multiple of a GCD would also be a GCD. The way we avoid this is to use the monic polynomial, so there will be a unique monic GCD
### Definition
Let $f(x),g(x)\in\mathbb{F}[x]$ with either $f(x)\neq 0$ or $g(x)\neq 0$, a greatest common divisor of $f(x)$ and $g(x)$ is a polynomial of highest degree that divides both $f(x)$ and $g(x)$
Note that it is not yet obvious that the GCD exists, and if it does, whether it is unique (up to rescaling)


#Mathematics #Definition