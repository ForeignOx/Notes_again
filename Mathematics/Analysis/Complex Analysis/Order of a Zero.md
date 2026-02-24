## Definition
Suppose [[Complex Functions|$f:U\to \mathbb{C}$]] is [[Holomorphicity|holomorphic]] on an [[open sets|open set]] $U$ and $f(a)=0$ for some $a\in U$. If there exist $k\in \mathbb{N}$ such that
$$
f(a)=f'(a)=\dots=f^{(k-1)}(a)=0
$$
But $f^{(k)}\neq 0$, then we say $f$ has a zero of order $k$ at $z=a$
## Lemma
If $f$ is holomorphic on some ball $B_{r}(a)$ with $f(a)=0$, then either $f(z)=0$ for all $z\in B_{r}(a)$ (identically zero for all $z\in B_{r}(a)$) or there exists $k\in\mathbb{N}$ such that $f$ has a zero of order $k$ at $z=a$
### Proof
If $f$ is holomorphic on $B_{r}(a)$, then by [[Cauchy-Taylor Theorem|Cauchy-Taylor]] it has a convergent [[Power Series|power series]] representation of the form
$$
f(z)=\sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(z-a)^{n}
$$
So if $f$ were not of finite order, then $f^{(n)}(a)=0$ for every $n$. But then $f(z)=0$ for all $z$
## Lemma: Characterisation Lemma for Zeros
Suppose $f$ is holomorphic on some ball. Then $f$ has a zero of orer $k$ at $z=a$ iff there exists a holomorphic $g:B_{r}(a)\to \mathbb{C}$ with
$$
f(z)=(z-a)^{k}g(z)~\forall z\in B_{r}(a)
$$
With $g(a)\neq 0$
### Proof
By Cauchy-Taylor, we may write 
$$
f(z)=\sum_{n=0}^{\infty}c_{n}(z-a)^{n}
$$
where
$$
c_{n}= \frac{f^{(n)}(a)}{n!}
$$
if $f$ has a zero of orderr $k$, then
$$
k=\min\left\{ n\geq 0:\middle|:c_{n}\neq 0 \right\}
$$
Thus
$$
f(z)=\sum_{n=k}^{\infty} c_{n}(z-a)^{n}=(z-a)r
$$

