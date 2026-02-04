A [[Sequences|sequence]] $(x_{n})_{n\in\mathbb{N}}$ is called a Cauchy sequence if:
$$
\forall\varepsilon>0\exists n_{0}\in \mathbb{N}:|x_{m}-x_{n}|<\varepsilon \forall n,m\geq n_{0}
$$
Which is useful because you only look at the sequence, you do not need to know the limit
## Cauchy Sequences are [[Boundedness|Bounded]]
Let $(x_{n})_{n\in\mathbb{N}}$ be a Cauchy sequence. Then $(x_{n})_{n\in\mathbb{N}}$ is bounded
### Proof
very similar to [[Every Convergent Sequence is Bounded]]
## [[Convergence|Convergent]] Sequences are Cauchy Sequences
Let $(x_{n})_{n\in\mathbb{N}}$ be a convergent sequence, then $(x_{n})_{n\in\mathbb{N}}$ is a Caucy sequence
## Cauchy Sequences are Convergent
Let $(x_{n})_{n\in\mathbb{N}}$ be a Cauchy sequence, then $(x_{n})_{n\in\mathbb{N}}$ is a convergent sequence
### Proof
We know that Cauchy sequences are bounded, so $(x_{n})_{n\in\mathbb{N}}$ is bounded. By the [[Bolzano-Weierstrass Theorem|Bolzano-Weierstrass theorem]], there is a convergent [[Subsequences|subsequence]] $(x_{n_{j}})_{j\in\mathbb{N}}$
Let $x=\lim_{ j \to \infty } x_{n_{j}}$, so given $\varepsilon>0$, there exists  a $j_{0}\in\mathbb{N}$ with:
$$
|x_{n_{j}}-x|<\frac{\varepsilon}{2}\forall j\geq j_{0}
$$
Since $(x_{n})_{n\in\mathbb{N}}$ is a Cauchy sequence, there is an $n_{0}\in\mathbb{N}$ with
$$
|x_{n}-x_{m}|<\frac{\varepsilon}{2}\forall n,m\geq n_{0}
$$
So
$$
|x_{n}-x|=|x_{n}-x_{n_{j}}+x_{n_{j}}-x|\leq|x_{n}-x_{n_{j}}|+|x_{n_{j}}-x|
$$
Need $j\geq j_{0}$ and $n_{j}\geq n_{0}$, but both we can arrange by choosing large enough $j$, then
$$
|x_{n}-x|<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon \forall n\geq n_{0}
$$
As required
## Example
Let $a,c>0$, and $(u_{n})_{n\in\mathbb{N}}$ given by $u_{1}=c$ and $u_{n+1}=\frac{1}{2}\left( u_{n}+\frac{a}{u_{n}} \right)$ for $n\geq 1$
To show this is a Cauchy sequence, we want $|u_{n}-u_{m}|<\varepsilon$ for some large $n$ and $m$, but we'll start with something simpler:
$$
u_{n+2}-u_{n+1}=\frac{1}{2}\left( u_{n+1}+\frac{a}{u_{n+1}} \right)-\frac{1}{2}\left( u_{n}+\frac{a}{u_{n}} \right)=\frac{1}{2}\left( u_{n+1}-u_{n}+\frac{au_{n}}{u_{n+1}u_{n}}-\frac{au_{n+1}}{u_{n+1}u_{n}} \right)
$$
$$
= \frac{1}{2}(u_{n+1}-u_{n})\left( 1-\frac{a}{u_{n}u_{n+1}} \right)
$$
We want this second factor to be very smol, so
$$
\left|1-\frac{a}{u_{n}u_{n+1}}\right|<1
$$
Since then:
$$
|u_{n+1}-u_{n+1}|<\frac{1}{2}(u_{n+1}-u_{n})
$$
Now
$$
u_{n}u_{n+1}=\frac{u_{n}}{2}\left( u_{n}+\frac{a}{u_{n}} \right)=\frac{u_{n}^{2}}{2}+\frac{a}{2}>\frac{a}{2}>0
$$
$$
\implies \frac{a}{u_{n}u_{n+1}}<2
$$
Which can be somehow used to show:
$$
\left|1-\frac{a}{u_{n}u_{n+1}}\right|<1
$$
Using [[Proof by Mathematical Induction!!!!!|induction]]:
$$
|u_{n+2}-u_{n+1}|<\frac{1}{2^{n}}|u_{2}-u_{1}|
$$
Assume that $n>m\geq n_{0}\geq 2$,
$$
|u_{n+2}-u_{n+1}|=|u_{n}-u_{n-1}+u_{n-1}-\dots+u_{m+1}-u_{m}|
$$
$$
\leq |u_{n}-u_{n-1}|+|u_{n-1}-u_{n-2}|+\dots+|u_{m+1}-u_{m}|
$$
$$
 <\left( \underbrace{ \frac{1}{2^{n-2}}+\frac{1}{2^{n-3}}+\dots+\frac{1}{2^{m-1}} }_{ <\frac{1}{2^{m-2}} } \right)|u_{2}-u_{1}|

$$
Gets us:
$$
|u_{n}-u_{m}|<\frac{1}{2^{m-2}}|u_{2}-u_{1}|
$$
Let $\varepsilon>0$, choose $n_{0}$ such that
$$
\frac{1}{2^{m-2}}|u_{2}-u_{1}|<\varepsilon
$$
Hence $(u_{n})_{n\in\mathbb{N}}$ is a Cauchy sequence


#Mathematics #Analysis #Definition #Theorem   