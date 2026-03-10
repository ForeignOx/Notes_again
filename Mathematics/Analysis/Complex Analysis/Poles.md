## Lemma: Characterisation Lemma for Poles
Suppose $f$ has an isolated singularity at $z=a$ (so $\exists R>0$ such that $f$ is holomorphic on $B^{*}_{R}(a)$). This singularity is a pole of order $k$ iff there exists a holomorphic function $g:B_{R}(a)\to \mathbb{C}$ with $g(a)\neq 0$ such that
$$
f(z)=(z-a)^{-k}g(z)
$$
For $z\in B_{R}^{*}(a)$
### Proof
If $f$ has a pole of order $k$, then on $B_{R}^{*}(a)$, it has a Laurent eries of the form
$$
f(z)=\sum_{n=-\infty}^{\infty}c_{n}(z-a)^{n}=(z-a)^{-k}\sum_{n=-k}^{\infty}c_{n}(z-a)^{n+k} 
$$
$$
= (z-a)^{-k}\sum_{m=0}^{\infty} c_{m-k}(z-a)^{m}
$$