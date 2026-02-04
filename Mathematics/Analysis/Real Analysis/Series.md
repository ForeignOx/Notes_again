1Let $(a_{k})_{k\in\mathbb{N}}$ be a [[Sequences|sequence]] of [[Real Numbers|real numbers]], then the sequence of partial sums $(s_{n})_{n\in\mathbb{N}}$ is defined as:
$$
s_{n}=\sum_{k=1}^{n}a_{k}
$$
If the sequence of partial sums [[Convergence|converges]], we say the series $\sum_{k=1}^{\infty}a_{k}$ is covergent, and then
$$
\sum_{k=1}^{\infty}a_{k}=\lim_{ n \to \infty }s_{n} 
$$
Otherwise $\sum_{k=1}^{\infty}a_{k}$ is divergent
## Remark
Series can start with a summand different from $a_{1}$, e.g. $\sum_{k=0}^{\infty}a_{k}$ or $\sum_{k=3}^{\infty}a_{k}$, as long as all the terms are defined
$\sum_{k=1}^{\infty}a_{k}$ converges iff $\sum_{k=N}^{\infty}a_{k}$
## Examples
### Geometric Series
For $k\in\mathbb{N}_{0}$, let $a_{k}=q^{k}$ with $q\in\mathbb{R}$, starts with $a_{0}=1$
$$
s_{n}=\sum_{k=0}^{n}q^{k}=\frac{1-q^{n+1}}{1-q}
$$
For $q\neq 1$

#### Proof
Proof by induction, $n=0$, gives 
$$
s_{0}=1=\frac{1-q}{1-q}
$$
Assme true for $n$
$$
s_{n+1}=s_{n}+q^{n+1}=\frac{1-q^{n+1}}{1-q}+\frac{q^{n+1}-q^{n+2}}{1-q}=\frac{1-q^{n+2}}{1-q}
$$
___
For $|q|<1$, $s_{n}$ converges to $\frac{1}{1-q}$, for $|q|>1$, $q^{n+1}$ is unbounded, and so is $s_{n}$, so the series is divergent, for $q=1$, $s_{n}=n+1$, which diverges, for $q=-1$, $s_{n}$ alternates between $\hspace{0pt}1$ and $\hspace{0pt}0$, so is also divergent
### Example 2
For $k\in\mathbb{N}$, let 
$$
q_{k}=\frac{1}{k(k+1)}=\frac{1}{k}-\frac{1}{k+1}
$$
$$
s_{n}=\sum_{k=1}^{n} \frac{1}{k(k+1)} =\sum_{ k=1} ^{ n}\left( \frac{1}{k}-\frac{1}{k+1} \right)=1-\frac{1}{2}+\frac{1}{2}-\frac{1}{3}+\dots+\frac{1}{n}-\frac{1}{n+1}
$$
$$
= 1-\frac{1}{n+1}
$$
So
$$
\sum_{k=1}^{\infty} \frac{1}{k(k+1)}=\lim_{ n \to \infty } \left( 1-\frac{1}{n+1} \right)=1
$$
## If $\sum_{k=0}^{\infty} a_{k}$ is convergent, then $\lim_{ k \to \infty }a_{k}=0$
Proof:
Let $s_{n}=\sum_{k=0}^{\infty} a_{k}$, then $\lim_{ n \to \infty }s_{n}=s$ for some $s \in \mathbb{R}$
Write $a_{n}=s_{n}-s_{n-1}$ for $n\geq 1$, so by [[Calculus of Limits Theorem|CoLT]], $\lim_{ n \to \infty }a_{n}=s-s=0$
This is a criterion for divergence fo a series, it is not a criterion for convergence of a series
## Convergence Criteria
### Comparison Test
Let $N\in\mathbb{N}$, and let $(a_{k})_{k\in\mathbb{N}_{0}}$, $(b_{k})_{k\in\mathbb{N}_{0}}$ be sequences with $0\leq a_{k}\leq b_{k}$ for $k\geq n$:
- If $\sum_{k=0}^{\infty} b_{k}$ is convergent, then $\sum_{k=0}^{\infty} a_{k}$ is convergent
- If $\sum_{k=0}^{\infty} a_{k}$ is divergent, then $\sum_{k=0}^{\infty} b_{k}$ is divergent
#### Proof
Use $\sum_{k=0}^{\infty} a_{k}$ is convergent iff $\sum_{k=N}^{\infty} a_{k}$ is convergent:
For $n\geq N$, let $s_{n}=\sum_{k=N}^{n}a_{k}$ and $t_{n}=\sum_{k=N}^{\infty} b_{k}$, these are monotonically increasing since $0\leq a_{k}\leq b_{k}$
If $\sum_{k=0}^{\infty} b_{k}$ is convergent, then $(t_{n})_{n\geq N}$ also converges, to $t$, $s_{n}\leq t_{n}\leq t$, so the sequence $s_{n}$ is monotonically increasing and [[Boundedness|bounded]], so is convergent by [[Every Increasing Sequence which is Bounded Above, Converges|this theorem]]
Since $s_{n}$ is monotonically increasing, divergence means that $s_{n}$ is unbounded, but then $t_{n}$ is also unbounded, so must also diverge
#### Example
$\sum_{k=1}^{\infty} \frac{1}{k^{2}}$ converges, since:
$$
\frac{1}{n^{2}}=\frac{2}{n^{2}+n^{2}}\leq \frac{2}{n^{2}+n}=\frac{2}{n(n+1)}
$$
We know $\sum_{k=1}^{\infty} \frac{2}{k(k+1)}$ converges to $\hspace{0pt}2$ by [[Calculus of Limits Theorem|CoLT]] and the example above, so by comparison test, we know it also converges
## Theorem
Let $\alpha \in\mathbb{R}$, then
$$
\sum_{ k=1} ^{\infty}  \frac{1}{k^\alpha}
$$
Is convergent iff $\alpha>1$
### Proof
For $\alpha=1$, we know it is divergent, by comparison test, we also get divergence for $\alpha \leq1$
For $\alpha>1$, we need convergence, we will do this by looking at the sequence of partial sums:
$$
s_{n}=\sum_{ k=1} ^{ n}  \frac{1}{k^{\alpha}}
$$
This sequence is monotonically increasing, consider $s_{2n+1}$:
$$
s_{2n+1}=\sum_{ k=1} ^{ 2n+1} \frac{1}{k^{\alpha}}=1+\sum_{ k=1} ^{ n} \left(  \frac{1}{(2k)^{\alpha}}+\frac{1}{(2k+1)^{\alpha}}   \right)
$$
$$
 \leq 1+\sum_{ k=1} ^{ n}  \frac{2}{(2k)^{\alpha}}=1+\sum_{ k=1} ^{ n}  \frac{2^{1-\alpha}}{k^{\alpha}}
$$
$2^{1-\alpha}$ is some constant less than 1:
$$
=1+2^{1-\alpha}\sum_{ k=1} ^{ n}  \frac{1}{k^{\alpha}}
$$
$$
\therefore s_{2n+1}\leq 1+2^{1-\alpha}s_{n}\leq 1+2^{1-\alpha}s_{2n+1}
$$
Since $s_{n}$ is increasing, so $s_{2n+1}\geq s_{n}$
$$
\therefore (1-2^{1-\alpha})s_{2n+1}\leq 1\iff s_{2n+1}\leq \frac{1}{1-2^{1-\alpha}}
$$
As $1-2^{1-\alpha}>0$
Since the sequence is monotonically increasing and has an upper bound, the sequence of partial sums is convergent, hence
$$
\sum_{ n=1} ^{\infty}  \frac{1}{n^{\alpha}}
$$
Is convergent for $\alpha>1$
## Examples
$$
a_{k}=\frac{\sqrt{ k^{2}+1 }}{k^{2}}
$$
Looks like if we let $k$ be big, $1$ is irrellevant, so $\sqrt{ k^{2}+1 }\sim k$, so it tends to $\frac{1}{k}$ which is divergent, so we use comparison tests for divergence:
$$
a_{k}=\frac{\sqrt{ k^{2}+ 1}}{k^{2}}\geq \frac{\sqrt{ k^{2} }}{k^{2}}=\frac{1}{k}
$$
So $\sum_{k=1}^{\infty} a_{k}$ is divergent
___
$$
b_{k}=\frac{\sqrt{ k^{2}-1 }}{k^{2}}
$$
This also looks like it would tend to $\frac{1}{k}$, but we use the comparison theorem like last time, it doesn't work as $\sqrt{ k^{2}-1 }\leq \sqrt{ k^{2} }$, but instead consider:
$$
b_{k}=\frac{\sqrt{ k^{2}-1 }}{k^{2}}\underbrace{ \geq }_{ \text{for }k\geq 2 } \frac{\sqrt{ k^{2}-\frac{1}{2}k^{2} }}{k^{2}}=\frac{1}{\sqrt{ 2 }} \frac{k}{k^{2}}=\frac{1}{\sqrt{ 2 }} \frac{1}{k}
$$
Which is divergent by CoLT
___
$$
c_{k}=\frac{\sqrt{ k^{3}-k+2 }}{4k^{2}-2}=\frac{k^{3/2}\sqrt{ 1-\frac{1}{k^{2}}+\frac{2}{k^{3}} }}{k^{2}\left( 4-\frac{2}{k^{2}} \right)}\sim \frac{1}{\sqrt{ k }}\times c
$$
$$
c_{k}\geq \frac{1}{\sqrt{ k }}\times \frac{\sqrt{ \frac{1}{2} }}{4}
$$
So by comparison test and CoLT, $\sum_{k=1}^{\infty} c_{k}$ diverges

___
$$
d_{k}=\frac{(2k^{2}-2k+9)(k^{2}-4k+3)}{(k^{3}+6k-1)^{2}}\leq \frac{(2k^{2}+9)(k^{2}+3)}{k^{6}}\leq 11k^{2}\times \frac{4k^{2}}{k^{6}}=44\times \frac{1}{k^{2}}
$$
So $\sum_{k=1}^{\infty} d_{k}$ is convergent
___
$$
e_{k}=\frac{k+1}{e^{ k }\sqrt{ k^{3}+1 }}
$$
The $\frac{k+1}{\sqrt{ k^{3}+1 }}\leq 1$, and then the $e^{ k }$ gives a geometric seies, so
$$
e_{k}\leq \frac{1}{e^{ k }}
$$
Which by comparison test, this is converget

#Mathematics #Analysis #Definition #Theorem 