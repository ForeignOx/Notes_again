## Definition
A complex function $f$ has an isolated singularity at $z=a$ if it is not defined at $z=a$ but is holomorphic on some punctured ball $B_{R}^{*}(a)$
Let $f(z)=\sum_{n=-\infty}^{\infty}c_{n}(z-a)^{n}$ be the Laurent series of $f$ on $B_{R}^{*}(a)$, then we say 
- $f$ has a removable singularity at $z=a$ if $c_{n}=0$ for every $n\leq -1$ (so it is a power series)
- $f$ has a pole of order $k>0$ at $z=a$ if $c_{-k}\neq 0$ but $c_{n}=0$ for all $n<-k$ (so $f(z)=\sum_{n=-k}^{\infty} c_{n}(z-a)^{n}$)
- $f$ has an essential singularity at $z=a$ if there are infinitely many $n<0$ such that $c_{n}\neq 0$
## Example
All the following has isolated singularities at $z=0$
Consider 
$$
f(z)=\frac{e^{ z }-1}{z} = \frac{\sum_{n=0}^{\infty} \frac{z^{n}}{n!}-1}{z} = \sum_{n=1}^{\infty} \frac{z^{n-1}}{n!}=\sum_{m=0}^{\infty} \frac{z^{m}}{(m+1)!}
$$
No particular part, so removable
## Lemma
Suppose $f$ has an isolated singularity at $z=a$, the singularity is reovable iff $f$ extends to a holomorfic function at $z=a$
### Proof
By definition there exist $R>0$ such that $f$ is holomorphic on $B^{*}_{R}(a)$, so it has a Laurent serie on $B^{*}_{R}(a)$ by a previous theorem. This Laurent series is a power series 
$$
g(z)=\sum_{n=0}^{\infty}c_{n}(z-a)^{n}
$$
By another theorem, $g$ converges on $B_{R}(a)$ (and matches $f$ on $B_{R}^{*}(a)$) so $g$ is the analytic continuation of $f$ to $B_{R}(a)$
For the other direction if $f$ extends to a holomorphic function $g$ on $B_{R}(a)$, then by Cauchy-Taylor, $g$ has a power series on $B_{R}(a)$ which matches $f$ on $B_{R}^{*}(a)$. This is the Laurent series on $f$
## Proposition
Suppose $f$ has an isolated singularity at $z=0$, this singularity is removable iff
$$
\lim_{ z \to a }  (z-a)f(z)=0
$$
### Proof
Assume removable. By the lemma above, $f$ extends to a holomorphic function at $z=0$, by defining say $f(a):=w$, then by continuity,
$$
\lim_{ z \to a } (z-a)f(z)=(a-a)f(a)=0\cdot w=0
$$
For the other direction, suppose $\lim_{ z \to a }(z-a)f(z)=0$, let
$$
f(z)=\sum_{n=-\infty}^{\infty} c_{n}(z-a)^{n}
$$
Be the Laurent series of $f$ around $z=a$. If it has coefficients  given by
$$
c_{n}=\frac{1}{2\pi i}\oint_{\left| z-a \right| =\rho} \frac{f(z)}{(z-a)^{n+1}}~dz
$$
For $n\in\mathbb{Z}$ for any $\rho \in B_{R}^{*}(a)$
By the [[ML Inequality|ML inequality]], for $n\leq -1$,
$$
0\leq \left| c_{n} \right| \leq \frac{L(\gamma)}{2\pi} \sup_{\left| z-a \right| =\rho}\left|  \frac{f(z)}{(z-a)^{n+1}} \right| 
$$
$$
\implies \left| c_{n} \right| \leq \frac{2\pi \rho}{2\pi}\sup_{\left| z-a \right| =\rho} \left| \frac{f(z)}{(z-a)^{n+1}} \right| =\rho\sup_{\left| z-a \right| =\rho} \frac{\left| (z-a)f(z) \right| }{\left| z-a \right| ^{n+2}} 
$$
$$
= \frac{1}{\rho^{n+1}} \sup_{\left| z-a \right| =\rho}\underbrace{  \left| (z-a)f(z)U \right|  }_{ \to 0\text{ by assumption} }
$$
as $\rho\to 0$, and $\frac{1}{\rho^{n+1}}$ tends to $0$ if $n\leq-2$ and if $n=-1$ it tends to $\hspace{0pt}1$, so $\left| c_{n} \right|\to 0$ as $\rho\to 0$
## Example
$f(z)=\frac{\sin z}{z}$ has a singularity at $z=0$, we have
$$
\lim_{ z \to 0 } zf(z)=\lim_{ z \to 0 } \sin z=\sin 0=0
$$
Yay
___
$f(z)=\frac{e^{ z }-1}{z}$, now
$$
\lim_{ z \to 0 } zf(z)=\lim_{ z \to 0 } (e^{ z }-1)=1-1=0
$$
Yayy
___
Suppose $f:0\to \mathbb{C}$ is holomorphic on a domain and pick $w\in D$, define the [[Difference Quotient Function|difference quotient function]]
$$
g(z)=\frac{f(z)-f(w)}{z-w}
$$
This is holomorphic on $D\setminus \left\{ w \right\}$
Then $z=w$ is an isolated singularity of $g$. Moreover,
$$
\lim_{ z \to w }  (z-w)g(z)=\lim_{ z \to w } f(z)-f(w)=f(w)-f(w)=0
$$
So removable yay


