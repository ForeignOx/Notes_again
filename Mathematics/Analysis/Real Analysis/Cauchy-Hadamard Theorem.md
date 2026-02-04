Given a [[Power Series|power series]] $\sum_{k=0}^{\infty} a_{k}x^{k}$, there exists $R\geq 0$ known as the radius of convergence (possibly $\infty$) such that the series [[Convergence|converges]] [[Absolute Convergence|absolutely]] for $\left| x \right|<R$, and diveres for $\left| x \right|>R$
In fact, we can use the [[Limsup and Liminf|limsup]] to get a value for $R$:
$$
c=\limsup_{ k \to \infty } \sqrt[k]{\left| a_{k} \right|   } 
$$
Then $R=\frac{1}{c}$, (if $c=0$, then $R=\infty$, and if $c=\infty$, then $R=0$) 
## Proof
We apply the [[Root Test|root test]] to our series $\sum_{k=0}^{\infty} a_{k} x^{k}$:
$$
\limsup_{ k \to \infty } \sqrt[k]{ \left| a_{k}x^{k} \right|  }=\limsup_{ k \to \infty } \sqrt[k]{\left| a_{k} \right|   }\left| x \right| =\left| x \right| \limsup_{ k \to \infty }  \sqrt[k]{ \left| a_{k} \right|  }=c\left| x \right| 
$$
This always exists, (it may be infinity)
So if it is less that $\hspace{0pt}1$, it converges absolutely, if greater than $\hspace{0pt}1$, it diverges, so we have instead, convergence if less than $\frac{1}{c}$, and divergence for greater than $\frac{1}{c}$
## Remarks
In practice the [[Ratio Test|ratio test]] works just as well because:
$$
\lim_{ k \to \infty }  \frac{\left| a_{k+1} \right|\left| x \right| ^{k+1} }{\left| a_{k} \right| \left| x \right| ^{k}}=\lim_{ k \to \infty }  \frac{\left| a_{k+1} \right|\left|x \right|  }{\left| a_{k} \right| }=\left| x \right| \lim_{ k \to  \infty }  \frac{\left| a_{k+1} \right| }{\left| a_{k} \right| }
$$
So we have the same case as above. The reason we didn't define it as such, is because the limit may not exist, whereas $\limsup$ always exists. We also have to think about whether the $a_{k}$'s are non-zero
___
At $x=\pm R$, known as the endpoints of the interval of convergence, anything can happen. To check, do not use the ratio or root test, instead substitute and use other tests
## Examples
Consider a polynomial $\sum_{ k=1} ^{ n} a_{k}x^{k}$ converges with $R=\infty$, of course, since $c=0$ as you can just plug in the values
Also $\lim_{ k \to \infty }\sqrt[k]{ \left| a_{k} \right| }=0$ as it simply becomes the limit of a sequence of zeroes past $n$.
___
The [[Geometric Progressions|geometric series]] $\sum_{k=0}^{\infty} x^{k}$, i.e. $a_{k}=1$, no matter what we use, $c=1$, so $R=1$, and it converges to $\frac{1}{1-x}$
And divergence for $\left| x \right|>1$
If $x=\pm1$, then we are looking at $(\pm 1)^{k}$, which clearly diverges
___
Consider the [[Series|Series]] $\sum_{k=0}^{\infty} \frac{x^{k}}{k!}$, we use the ratio test:
$$
\frac{\left| x \right| ^{k+1}}{(k+1)!} \frac{k!}{\left| x \right| ^{k}}=\frac{\left| x \right| }{k+1}\to0<1
$$
So we always have convergence, $R=\infty$, convergence for all $x$
___
Consider $\sum_{k=0}^{\infty} k^{k}x^{k}$, using the root test, we get:
$$
\lim_{ k \to \infty } \sqrt[k]{ \left| k^{k} \right|  }=\infty
$$
So $R=0$, only converges for $x=0$
___
Consider $\sum_{k=0}^{\infty} \frac{k}{3^{k}}x^{k}$, we use ratio test:
$$
\frac{\frac{k+1}{3^{k+1}}\left| x \right| ^{k+1}}{\frac{k}{3^{k}}\left| x \right| ^{k}}=\frac{k+1}{k}\frac{1}{3}\left| x \right| \to \frac{1}{3}\left| x \right| 
$$
So $R=3$, note this is the same if the series was $\sum_{k=0}^{\infty} \frac{1}{3^{k}k}x^{k}$, since the limit becomes
$$
\frac{k}{k+1} \frac{1}{3}\left| x \right| 
$$
This is in fact the case for any ratio of polynomials in $k$ 
It does however, effect the endpoints with drastic repurcussions
## Corollary
If $\sum_{k=0}^{\infty} a_{k}c^{k}$ converges for some $c\in\mathbb{R}$ then $\sum_{k=0}^{\infty} a_{k}x^{k}$ converges $\forall x\in(-\left| c \right|,\left| c \right|)$
### Proof
Must have $\left| c \right|\leq R$, so $(-\left| c \right|,\left| c \right|)\subseteq(-R,R)$
## What Happens at the Endpoints
Assume $\sum_{k=0}^{\infty} a_{k}x^{k}=f(x)$ converges at $x=R$. Is $f(x)$ left-[[Continuity|continuous]] at $x=R$; is
$$
\lim_{ x \to R^{-} }f(x)=f(R) 
$$
By Abel's Theorem, we say yes!