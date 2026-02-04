## Definition
Let $f:[a,b]\to \mathbb{R}$ be a [[Regulated Functions|regulated function]], say [[Sequences of Functions|$f_{n}\to f$]] where $f_{n}$ are [[Step Functions|step functions]], then we say the regulated integral of $f$ is:
$$
I(f)=\lim_{ n \to \infty } I(f_{n})
$$
Where $I(f_{n})$ is the integral of the step functions, or the [[Riemann Sums|riemann sums]]
We need to check whether this limit exists however
### Proof
Since we don't know what $I(f_{n})$'s [[Convergence|converge to]], and we don't know if they are [[Convergent Bounded Sequences have Limits in the Bound|monotone and bounded]], we need to use [[Cauchy Sequences|cauchy sequences]], so we will show that the sequence $I(f_{n})=:a_{n}$ forms a cauchy sequence
Take $\varepsilon>0$, we need to find $N$ such that $\forall n,m\geq N$, $\left| a_{n}-a_{m} \right|<\varepsilon$
We can take $N$ to be the same as the one fro the convergence of the regulated function, and let  $n,m\geq N$. For the step functions $f_{n}(x),f_{m}(x)$, take a common refinement of the two underlying partitions $a=x_{0},x_{1},\dots,x_{N}=b$, then we need to check
$$
I(f_{n})-I(f_{m})=\sum_{k=0}^{N}(x_{k+1}-x_{k})f_{n}(x_{k}^{*})-\sum_{k=0}^{N}(x_{k+1}-x_{k})f_{m}(x_{k}^{*})
$$
$$
 \left| I(f_{n})-I(f_{m}) \right| =\sum_{k=0}^{N}(x_{k+1}-x_{k})\left| f_{n}(x_{k}^{*})-f_{m}(x_{k}^{*}) \right| 
$$
$$
= \sum_{k=0}^{N}(x_{k+1}-x_{k})\left| f_{n}(x_{k}^{*})-f(x_{k}^{*})+f(x_{k}^{*})-f_{m}(x_{k}^{*}) \right| 
$$
Which by the [[Triangle Inequality|triangle inequality]] we have:
$$
\leq \sum_{k=0}^{N}(x_{k+1}-x_{k})(\underbrace{ \left| f_{n}(x_{k}^{*})-f(x_{k}^{*}) \right| }_{ <\varepsilon } +\underbrace{ \left| f_m(x_{k}^{*})-f(x_{k}^{*}) \right| }_{ <\varepsilon } )<2\varepsilon \sum_{k=0}^{N}(x_{k+1}-x_{k})=2(b-a)\varepsilon
$$
We know those parts are less than $\varepsilon$ from the definition of $f_{n},f_{m}$ as regulated functions
Hence it is a Cauchy sequence, hence it converges
___
We also need to check that it is independent of the choice of sequence of step functions, as there are many that could converge
### Proof
Take $f_{n}\to f$, $g_{n}\to f$ where $f_{n},g_{n}$ are step functions which converge [[Uniform Convergence|uniformly]], we need
$$
\lim_{ n \to \infty } I(f_{n})=\lim_{ n \to \infty } I(g_{n})
$$
We are going to do the same thing :/
Take $\varepsilon>0$, we need to find $N$ such that $\left| I(f_{n})-I(g_{n}) \right|<\varepsilon \forall n\geq N$, again we take $N$ as in the definition of regulated function for both $f_{n},g_{n}$ (the maximum of those at least, which works for both). For $f_{n},g_{n}$, take a common refinement so we have the same partition for each, then the process is identical:
$$
I(f_{n})-I(g_{n})=\sum_{k=0}^{N}(x_{k+1}-x_{k})f_{n}(x_{k}^{*})-\sum_{k=0}^{N}(x_{k+1}-x_{k})g_{n}(x_{k}^{*})
$$
$$
  \left| I(f_{n})-I(g_{n}) \right| =\sum_{k=0}^{N}(x_{k+1}-x_{k})\left| f_{n}(x_{k}^{*})-g_{n}(x_{k}^{*}) \right| 
$$
$$
 = \sum_{k=0}^{N}(x_{k+1}-x_{k})\left| f_{n}(x_{k}^{*})-f(x_{k}^{*})+f(x_{k}^{*})-g_{n}(x_{k}^{*}) \right| 
$$
$$
 \leq \sum_{k=0}^{N}(x_{k+1}-x_{k})(\underbrace{ \left| f_{n}(x_{k}^{*})-f(x_{k}^{*}) \right| }_{ <\varepsilon } +\underbrace{ \left|g_{n}(x_{k}^{*})-f(x_{k}^{*}) \right| }_{ <\varepsilon } )<2\varepsilon \sum_{k=0}^{N}(x_{k+1}-x_{k})=2(b-a)\varepsilon
$$
___
### Example
Consider $f(x)=x$ on $[a,b]$, then to define $f_{n}(x)$, take the equidistant partition, $x_{k}=a+k \frac{b-a}{n}$ for $k=0,\dots,n$, and let $x_{k}^{*}=x_{k}$, set $f(x)=f(x_{k}^{*})=f(x_{k})$ for $x\in(x_{k},x_{k+1})$, and since $f_{n}\to f$ are lipschitz as it is bounded, they tend uniformly. Take for example $a=0,b=1$, then
$$
I(f_{n})=\sum_{k=0}^{n}\underbrace{ (x_{k+1}-x_{k}) }_{ =\frac{b-a}{n}=\frac{1}{n} }f\left( \underbrace{ x_{k}^{*} }_{ =x_{k}=\frac{k}{n} } \right)=\frac{1}{n^{2}}\sum_{k=0}^{n}k=\frac{1}{n^{2}} \frac{(n+1)n}{2}\to \frac{1}{2}
$$