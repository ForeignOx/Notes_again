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
### Proof
The Laurent series converges iff the analytic and principle parts converge at $z$
For the analytic part, this is simply a power series. So it converges at just $z=a$ (in which case the Laurent series never converges anywhere not defined there) or there exists $R>0$ such that the analytic part converge when $\left| z-a \right|<R$
For the principle part, we first make the change of variables
$$
\sum_{n=-\infty}^{-1}c_{n}(z-a)^{n}= \sum_{m=1}^{\infty} c_{-m}\left( \frac{1}{z-a} \right)^{m}
$$
If we write $w=\frac{1}{z-a}$, then this is equal to 
$$
= \sum_{m=1}^{\infty} c_{-m}w^{m}
$$
This is also just a power series which converges at just $w=0$ (in which case the Laurent series never converges, as there is no $z$ for which $\frac{1}{z-a}=0$)
Or there exists $R'>0$ such that the power series converges when $\left| w \right|<R'$. Let
$$
r=\begin{cases}
\frac{1}{R'} & R'<\infty \\
0 & R'=\infty
\end{cases}
$$
Then the principle part converges when 
$$
\frac{1}{\left| z-a \right|}<R' \iff \left| z-a \right| > \frac{1}{R'}=r
$$
Thus it converges on an annulus ye
## Corollary
A Laurent series is holomorphic on its annulus of convergence (in particular, a Laurent series converges locally on a disc of convergence of a holomorphic function)
### Proof


## Example
Find the annulus of convergence of the Laurent series:
$$
\sum_{n=-\infty}^{1}3^{n}z^{n}=3z+1+\frac{1}{3} \frac{1}{z}+\frac{1}{9} \frac{1}{z^{2}}+\dots 
$$
$$
= 3z+1+\sum_{n=-\infty}^{-1} 3^{n}z^{n}=3z+1+\sum_{m=1}^{\infty} \left( \frac{1}{3z} \right)^{m}
$$
The analytic part converges on $\mathbb{C}$ and the analytic part converges when $\left| \frac{1}{3z} \right|<1 \iff \left| z \right|>\frac{1}{3}$
So the Laurent series converges on the annulus $A_{\frac{1}{3},\infty}(0)$
Note, we have the closed form expression:
$$
\sum_{n=-\infty}^{1}3^{n}z^{n}=3z+\sum_{m=0}^{\infty} \left( \frac{1}{3z} \right)^{m}=3z+  \frac{1}{1-\left( \frac{1}{3z} \right)}=\frac{9z^{2}}{3z-1}
$$
## Proposition: Uniqueness of Laurent Series
Given a Laurent series of the form $f(z)=\sum_{n=-\infty}^{\infty}c_{n}(z-a)^{n}$ with annulus of convergence $A_{r,R}(a)$. Then the constants $c_{n}$ are unique and given, for any $r<\rho<R$ by
$$
c_{n}=\frac{1}{2\pi i}\oint_{\left| z-a \right| =\rho} \frac{f(z)}{z-a}
$$
For $n\in\mathbb{Z}$
### Proof
Assume there is another expression on $A_{r,R}(a)$ of the form $f(z)=\sum_{n=-\infty}^{\infty}d_{n}(z-a)^{n}$ we want to show $c_{n}=d_{n}$. We have for any $r<\rho<R$,
$$
\oint_{\left| z-a \right| =\rho}  \frac{f(z)}{(z-a)^{n+1}}~dz= \oint_{\left| z-a \right| =\rho}  \frac{1}{(z-a)^{n+1}}\sum_{m=-\infty}^{\infty}c_{m}(z-a)^{m}~dz 
$$
$$
= \oint_{\left| z-a \right| =\rho} \sum_{n=-\infty}^{\infty} c_{m}(z-a)^{m-n-1} ~dz = 2\pi i \sum_{n=-\infty}^{\infty}c_{m} \oint_{\left| z-a \right| =\rho} (z-a)^{m-n-1}~dz  
$$
$$
= 2\pi i c_{n}
$$
As the integral equals zero unless $m=n$
But we can do the exact same thing with $d_{n}$ to get $=2\pi i d_{n}$, so they are equal and hunce unique and stuff innit
## Theorem: Holomorphic Functions on Annuli have Laurent Series
Let $f:A_{r,R}(a)\to C$