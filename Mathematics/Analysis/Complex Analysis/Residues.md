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
\mathrm{Res}_{z=a}(f)= \frac{g^{(k-1)}(a)}{(k-1)!}
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
The denominator has zeros at $z=n\pi$ and these are order $\hspace{0pt}1$, so simple zeros, by rule $\hspace{0pt}2$ with $g(z)=1,h(z)=\sin z$, 
$$
\mathrm{Res}_{z=a}(f)= \frac{g(a)}{h'(a)}=\frac{1}{\cos(n\pi)}=(-1)^{n}
$$
### Proof
We have $f(z)=\sum_{n=-1}^{\infty}c_{n}(z-a)^{n}$ so
$$
(z-a)f(z)=\sum_{n=-1}^{\infty}c_{n}(z-a)^{n+1}=\sum_{m=0}^{\infty}c_{m-1}(z-a)^{m}
$$
Which is a [[power series|power series]] which is holomorphic at $z=a$ with value
$$
\lim_{ z \to a } (z-a)f(z)=c_{-1}
$$
For the second rule, if $f=\frac{g}{h}$ with $g(a)\neq 0$ and $h(a)=0,h'(a)\neq 0$, then by rule $\hspace{0pt}1$,
$$
\mathrm{Res}_{z=a}(f)=\lim_{ z \to a } (z-a)f(z)=\lim_{ z \to a }  \frac{(z-a)g(z)}{h(z)} 
$$
$$
= \lim_{ z \to a }  \frac{g(z)+(z-a)g'(z)}{h'(z)}= \frac{g(a)+(a-a)g'(a)}{h'(a)}=\frac{g(a)}{h'(a)}
$$
By [[L'Hopital's Rule|L'hopital's]]
For the third, if
$$
f(z)=\frac{g(z)}{(z-a)^{k}}
$$
With $g$ holomorphic, so has Taylor seroes at $z=a$, say $g(z)=\sum_{n=0}^{\infty}a_{n}(z-a)^{n}$ so
$$
f(z)=\sum_{n=0}^{\infty} a_{n}(z-a)^{n-k}=\sum_{m=-k}^{\infty} a_{m+k}(z-a)^{m}
$$
So $c_{m}=a_{m+k}$ and we want 
$$
c_{-1}=a_{k-1}= \frac{g^{(k-1)(a)}}{(k-1)!}
$$