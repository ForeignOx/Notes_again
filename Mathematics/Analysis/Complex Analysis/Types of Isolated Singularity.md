## Definition
A complex function $f$ has an isolated singularity at $z=a$ if it is not defined at $z=a$ but is holomorphic on some punctured ball $B_{R}^{*}(a)$
Let $f(z)=\sum_{n=-\infty}^{\infty}c_{n}(z-a)^{n}$ be the Laurent series of $f$ on $B_{R}^{*}(a)$, then we say 
- $f$ ha a removable singularity at $z=a$ if $c_{n}=0$ for every $n\leq -1$ (so it is a power series)
- $f$ has a pole of order $k>0$ at $z=a$ if $c_{-k}\neq 0$ but $c_{n}=0$ for all $n<-k$ (so $f(z)=\sum_{n=-k}^{\infty} c_{n}(z-a)^{n}$)
- $f$ has an essential singularity at $z=a$ if there are infinitely many $n<0$ such that $c_{n}\neq 0$
## Example
All the following has isolated singularities at $z=0$
Consider 
$$
f(z)=\frac{e^{ z }-1}{z} = \frac{\sum_{n=0}^{\infty} \frac{z^{n}}{n!}-1}{z} = \sum_{n=1}^{\infty} \frac{z^{n-1}}{n!}=\sum_{m=0}^{\infty} \frac{z^{m}}{(m+1)!}
$$
No particular part, so removable
