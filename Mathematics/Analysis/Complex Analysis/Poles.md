## Lemma: Characterisation Lemma for Poles
Suppose [[Complex Functions|$f$]] has an [[Isolated Singularity|isolated singularity]] at $z=a$ (so $\exists R>0$ such that $f$ is [[Holomorphicity|holomorphic]] on $B^{*}_{R}(a)$). This singularity is a pole of order $k$ iff there exists a holomorphic function $g:B_{R}(a)\to \mathbb{C}$ with $g(a)\neq 0$ such that
$$
f(z)=(z-a)^{-k}g(z)
$$
For $z\in B_{R}^{*}(a)$
### Proof
If $f$ has a pole of order $k$, then on $B_{R}^{*}(a)$, it has a [[Laurent series|Laurent series]] of the form
$$
f(z)=\sum_{n=-\infty}^{\infty}c_{n}(z-a)^{n}=(z-a)^{-k}\sum_{n=-k}^{\infty}c_{n}(z-a)^{n+k} 
$$
$$
= (z-a)^{-k}\sum_{m=0}^{\infty} c_{m-k}(z-a)^{m}
$$
Which is a [[power series|power series]], so it is holomorphic on $B_{R}(0)$
Define $g(z)=\sum_{m=0}^{\infty}c_{m-k}(z-a)^{m}$, then $g$ is holomorphic with $g(a)=c_{-k}\neq 0$
For the other direction, we just do the same in reverse. If $g$ is holomorphic, then $g$ has a [[Taylor series|Taylor series]] by [[Cauchy-Taylor Theorem|Cauchy-Taylor]], so 
$$
f(z)=(z-a)^{-k}\sum_{m=0}^{\infty}d_{m}(z-a)^{m}
$$
So yeah
## Observation
Assume $h$ has a zero of order $k$ at $z=a$, then by the [[Order of a Zero|characterisation lemma for zeros]], there exists a $g$ holomorphic with $g(a)\neq 0$, such that $h(z)=(z-a)^{k}g(z)$ on $B_{R}(a)$, then by [[Continuity|continuity]], then theree exists $B_{r}(a)$ on which $g(z)\neq 0$, but then,
$$
f(z)=\frac{1}{h(z)}=(z-a)^{-k} \frac{1}{g(z)}
$$
But actually, $\frac{1}{g(z)}$ is holomorphic and nonzero on $B_{r}(a)$
So $f$ has a pole of order $k$ at $z=a$, so we can think of poles as being created by reciprocals of functions, and it turns out, this is the only way they can come about
## Proposition
Suppose $f$ has an isolated singularity at $z=a$ then it is a pole iff there exists $r>0$ and a holomorphic function $h:B_{r}(a)\to \mathbb{C}$ such that $f(z)=\frac{1}{h(z)}$ on $B_{r}^{*}(a)$ and $h$ has a zero of order $k$ at $z=a$
### Proof
For the converse direction, we found this in the above observation.
For the forward, suppose $f$ has a p