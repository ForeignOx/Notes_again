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
## Proposition: Rules for Calculating Residues
Suppose $f$ is meromorphic with a pole at $z=a$, then
- **Rule 1**: If the pole is order $\hspace{0pt}1$, then
$$
\mathrm{Res}_{z=a}(f)=\lim_{ z \to a } (z-a)f(z)
$$
- **Rule 2**: If we can write $f(z)=\frac{g(z)}{h(z)}$ where $g,h$ are holomorphic and $g(a)\neq 0$ and $h$ has a zero of order $\hspace{0pt}1$ at $z=a$, then
$$
\mathrm{Res}_{z=a}(f) = \frac{g(a)}{h'(a)}
$$
- **Rule 3:** If $f(z)=\frac{g(z)}{(z-a)^{k}}$ for some $k>0$ with $g$ being holomorphic at $z=a$, then
$$
\mathrm{Res}_{z=a}(f)= \frac{g^{(k-1)(a)}}{(k-1)!}
$$
## Examples
Consider 
$$
f(z)=\frac{1}{z^{2}-9}=\frac{1}{(z-3)(z+3)}
$$
Which has poles of order $\hspace{0pt}1$ at $z=\pm 3$, then by rule $\hspace{0pt}1$, 
$$
\mathrm{Res}_{z=3}(f)=\lim_{ z \to 3 } (z-3)f(z)=\lim_{ z \to 3 }  \frac{1}{z+3}=\frac{1}{6}
$$
___
Consider
$$
f(z)=\sin z
$$
The denominator 