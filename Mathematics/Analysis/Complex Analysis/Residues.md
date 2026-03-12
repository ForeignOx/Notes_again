If $f$ has a pole at $z=a$ and $\gamma$ is a circular contour around $a$ in annulus of convergence of the Laurent series of $f$ around $a$, then
$$
\oint_{\gamma} f(z)~dz=\oint_{\gamma}\sum_{n=-k}^{\infty}c_{n}(z-a)^{n}~dz 
$$
$$
= \sum_{n=-k}^{\infty} c_{n} \oint_{\gamma}(z-a)^{n}~dz= c_{-1}\oint_{\gamma} \frac{1}{z-a}~dz=2\pi ic_{-1}
$$
Since the integral is zero unless $n=-1$ by [[Cauchy-Goursat Theorem|Cauchy-Goursat]]
Which is interesting as in the only bit that the integral can see is $c_{-1}$
## Definition
Suppose $f$ is [[Meromorphicity|meromorphic]] on a [[domains|domain]] $D\subseteq \mathbb{C}$, with a [[poles|pole]] $a\in D$, we write
$$
f(z)=\sum_{n=-k}^{\infty} c_{n}(z-a)^{n}
$$
For the [[Laurent series|Laurent series]] of [[Complex Functions|$f$]] around $z=a$, then the residue of $f$ at $z-a$, denoted by $\mathrm{Res}_{z=a}(f)$ is defined by
$$
\mathrm{Res}_{z=a}(f):=c_{-1}
$$
## Proposition: Rules for Calculating Res