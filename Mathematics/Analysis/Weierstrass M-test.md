## Theorem
If we have the [[Series|series]] $\sum_{k=0}^{\infty}f_{k}(z)$ on an [[Intervals|interval]] or [[Domains|domain]] $D$, (where $f_{k}(z)$ is a [[Sequences of Functions|sequence of functions]])
Assuming $f_{k}(z)$ are all [[Boundedness|bounded]]: $\left| f_{k}(z) \right|\leq M_{k}~\forall z\in D$ and $\sum_{k=0}^{\infty} M_{k}$ [[Convergence|converges]], then $\sum_{k=0}^{\infty} f_{k}(z)$ [[Uniform Convergence|converges uniformly]] on $D$
## Proof
By comparison, 
$$
\sum_{k=0}^{\infty} \left| f_{k}(z) \right|  \leq \sum_{k=0}^{\infty} M_{k} <\infty
$$
So $\sum_{k=0}^{\infty} f_{k}(z)$ [[Absolute Convergence|converges absolutely]] to a [[Functions|function]] $f(z)$. We need to show this is uniform
Set 
$$
L=\sum_{k=0}^{\infty} M_{k}=\lim_{ n \to \infty } \sum_{ k=0} ^{ n}  M_{k}
$$
So given $\varepsilon>0$, there exists $N$ such that 
$$
\left| L-\sum_{k=0}^{n}M_{k} \right|=\sum_{k=n+1}^{\infty}M_{k}<\varepsilon ~\forall n\geq N
$$
So we will show
$$
\left| f(z)-\sum_{k=0}^{n}f_{k}(z) \right| <\varepsilon \forall n\geq N
$$
Indeed:
$$
\left| f(z)-\sum_{k=0}^{n}f_{k}(z) \right| =\left| \sum_{k=n+1}^{\infty}f_{k}(z) \right| \leq \sum_{k=n+1}^{\infty}\left| f_{k}(z) \right| \leq \sum_{k=n+1}^{\infty}M_{k}<\varepsilon
$$
So we have uniform convergence
___
This is useful to show [[Continuity|continuity]] of $\sum_{k=0}^{\infty} f_{k}(z)$, we use $M$-test on compact subsets of $I$ 
## Criteria for Lack of Uniform Convergence of a Series
Let $\left\{ f_{n} \right\}_{n\in\mathbb{N}}:D\to \mathbb{C}$ be a given sequence of functions. If $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ doesn't converge uniformly to $f(z)=0$ on $D$, then the sequence $S_{N}(z)=\sum_{n=1}^{N}f_{n}(z)$ does not converge uniforly on $D$
### Proof
We have that
$$
f_{n}(z)=S_{n}(z)-S_{n-1}(z)
$$
Where we define $S_{0}(z)=0$. If $\left\{ S_{N} \right\}_{N\in\mathbb{N}}$ converge uniformly on $D$ to $S$, then
$$
0\leq \sup_{z\in  D}\left| f_{n}(z) \right| \leq \sup_{z\in  D}\left| S_{n}-S(z)+S(z)-S_{n-1}(z) \right| 
$$
$$
 \leq \sup_{z\in  D}(\left| S_{n}(z)-S(z) \right| +\left| S_{n-1}(z)-S(z) \right| )
$$
$$
 \leq \sup_{z\in  D}\left| S_{n}(z)-S(z) \right| +\sup_{z\in  D}\left| S_{n-1}(z)-S(z) \right| \to 0
$$
As $n\to\infty$
The squeeze theorem implies that $\lim_{ n \to \infty }\sup_{z\in D}\left| f_{n}(z) \right|=0$ and consequently $\left\{ f_{n} \right\}$ converges uniformly to $f(z)=0$ on $D$
We conclude that if $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ doesn't converge uniformly to $f(z)=0$ on $D$, so the series can't converge uniformly
## Example
Show that 
$$
\sum_{n=1}^{\infty} \frac{\left| 2z \right| ^{3n}}{3^{2n}n^{2}}
$$
Converges uniformly to a function on $\mathbb{D}$
Denoting $f_{n}(z)= \frac{\left| 2z \right| ^{3n}}{3^{2n}n^{2}}$ we find that on $\mathbb{D}$,
$$
\left| f_{n}(z) \right| \leq \frac{2^{3n}}{3^{2n}n^{2}}=\left( \frac{8}{9} \right)^{n} \frac{1}{n^{2}}\leq \left( \frac{8}{9} \right)^{n}
$$
Since $\sum_{n=1}^{\infty}\left( \frac{8}{9} \right)^{n}<\infty$ we conclude the result from Weierstrass' M-test
## Theorem: Version for [[Locally Uniform Convergence|Local Uniform Convergence]]
Let $\left\{  f_{n} \right\}_{n\in\mathbb{N}}:D\to \mathbb{C}$ be a given sequence of functions. assume that for any $z_{0}\in D$, three exists an open set $U_{z_{0}}$, a sequence of non-negative real numbers $\left\{ M_{n}(U_{z_{0}}) \right\}_{n\in\mathbb{N}}$ and $n_{0}(U_{z_{0}})\in \mathbb{N}$ that may depend on $U_{z_{0}}$ (but not on $z\in U_{z_{0}}$) such that for all $n\geq n_{0}(U_{z_{0}})$:
$$
\left| f_{n}(z) \right| \leq M_{n}(U_{z_{0}})~\forall z\in  U_{z_{0}}\cap D
$$
and
$$
\sum_{n=n_{0}}^{\infty}M_{n}(U_{z_{0}})<\infty
$$
Then $S_{N}(z)=\sum_{n=1}^{N}f_{n}(z)$ converges locally uniformly on $D$ to some limit function $s:D\to \mathbb{C}$ which we denote by
$$
S(z)=\sum_{n=1}^{\infty}f_{n}(z)
$$
In particular, if all the functions $f_{n}(z)$ are continuous on $D$, then $S(z)$ is also continuous on $D$
## Theorem: Criteria for Lack of Local Uniform Convergence of a eries
Let $\left\{ f_{n} \right\}_{n\in\mathbb{N}}:D\to \mathbb{C}$ be a given sequence of functions. If $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ doesn't converge locally uniformly to $f(z)=0$ on $D$, then the sequence $S_{N}(z)=\sum_{n=1}^{N}f_{n}(z)$ does not converge locally uniformly on $D$
## Example
Show that the series $\sum_{n=1}^{\infty} \frac{\left( z+\frac{1}{z} \right)^{n}}{n!}$ converges locally uniformly to a continuous function on $\mathbb{C}^{*}$
We start by noticing that $\mathbb{C}^{*}$ is open, so we can use the simplified version of the local uniform convergence. It will be enough for us to show that for any $0<r<R<\infty$ the series converges uniformly on $A_{r,R}=\left\{ z\in\mathbb{C}:\middle|: r<\left| z \right|<R \right\}$ since for any $z_{0}\in \mathbb{C}^{*}$, we can find $r(z_{0})<R(z_{0})$ such that $z_{0}$ is in the open set $A_{r(z_{0}),R(z_{0})}$
To show the uniform convergence on $A_{r,R}$, we will utilise the Weierstrass M-test. By doing this, we will also conclude the continuity of the limit function since $\frac{\left( z+\frac{1}{z} \right)^{n}}{n!}$ is continuous on $\mathbb{C}^{*}$
On $A_{r,R}$, we have that
$$
\left| \frac{\left( z+\frac{1}{z} \right)^{n}}{n!} \right| \leq \frac{\left( \left| z \right| +\frac{1}{\left| z \right| } \right)^{n}}{n!}\leq \frac{\left( R+\frac{1}{r} \right)^{n}}{n!}=M_{n}(r,R)
$$
Since
$$
\sum_{n=0}^{\infty}M_{n}(r,R)=\sum_{n=0}^{\infty} \frac{\left( R+\frac{1}{r} \right)^{n}}{n!}=e^{ R+\frac{1}{r} }<\infty
$$
We can use the Weierestrass M-test to conclude that $\sum_{n=1}^{\infty} \frac{\left( z+\frac{1}{z} \right)^{n}}{n!}$ converges uniformly on $A_{r,R}$