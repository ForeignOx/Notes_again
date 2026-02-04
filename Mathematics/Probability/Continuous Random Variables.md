Let $X:\Omega\to \mathbb{R}$ be a [[Random Variables|random variable]], we call $X$ a continuous random variable, or $X$ has a continuous probability distribution, if there exists a non-negative [[Functions|function]] $f$:
$$
f:\mathbb{R}\to \mathbb{R}
$$
Such that
$$
\mathbb{P}(X \in [a,b])=\int ^{b}_{a} f(t) \, dt 
$$
$f$ is called the probability density function of $X$ or pdf
Let $x \in\mathbb{R}$, choose $a=b=x$:
$$
\mathbb{P}(X=x)=\int _{a}^{a}f(t) \, dt =0
$$
We say that a continuous random variable has no mass a given value, so we can't say:
$$
\mathbb{P}(X=x)=f(x)
$$ But we can think that:
$$
\mathbb{P}(X \in [x,x+dx])\approx f(x)
$$
For small $dx$, you can think of $f(x)$ as the rate of change in that sense:
$$
\frac{d \mathbb{P}(X\in [x,x+dx])}{dx} \approx f(x)
$$
A pdf is always [[Piecewise Functions|piecewise]] [[Continuity|continuous]], but it is not necessarily unique
Piecewise continuous means that there are some discontinuities, but the probability is defined in continuous pieces
Note that:
$$
\mathbb{P}(X \in (a,b))=\mathbb{P}(X \in [a,b))=\mathbb{P}(X\in (a,b])=\mathbb{P}(X \in [a,b])
$$
For now we will assume that pdf is unique except for finitely many points, that is, if $X$ is a random variable, let $f$ and $g$ be potential candidates for the pdf of $X$, then there exists a finite $k\geq 1$ and a sequence $a_{1},a_{2},\dots ,a_{k}$ such that $a_{i}\in\mathbb{R},1\leq i\leq k$ such that $f(x)=g(x)\forall x\not\in\{ a_{1},a_{2},\dots ,a_{k} \}$. The pdf is unique up to a set of measure zeros
## Finite Union of Intervals
Let $B\subseteq \mathbb{R}$, such that $B=\bigcup_{i=1}^{m}[a_{i},b_{i}]$ ($B$ is a finite union of intervals, the intervals may be open or closed or a mixture), then 
$$
\mathbb{P}(X \in B)=\int _{B}f(x) \, dx 
$$
### Corollary
If the intervals are disjoint, we can write it as a sum:
$$
        \mathbb{P}(X \in B)=\sum_{i=1}^{m}\int_{a_{i}}^{b_{i}}f(x)  \, dx 
$$
### Infinities
Note that then we can say:
$$
\mathbb{P}( X \in (-\infty,b])=\int _{-\infty}^{b}f(x) \, dx ,\mathbb{P}(X \in [a,\infty) )=\int _{a}^{\infty}f(x) \, dx 
$$
As we can write:
$$
(-\infty,b]=\bigcup_{n=1}^{\infty}\left( -\infty,b-\frac{1}{n} \right]
$$
Which is a countable union
From this we can say:
$$
\mathbb{P}(X\in\mathbb{R})=\mathbb{P}(-\infty<x<\infty)=\int_{-\infty}^{\infty} f(t) \, dt =1
$$
## Joint Distribution
The joint pdf:
Let $X,Y$ be real valued random variables are jointly continuously distributed if they have a joint probability function:
$$
f:\mathbb{R}^{2}\to \mathbb{R}
$$
Which $f\geq 0$, such that:
$$
\mathbb{P}(X\in [a,b],Y\in [c,d])=\int _{a}^{b}\left( \int _{c}^{d} f(x,y) \, dx  \right) \, dy 
$$
Recall that for a continuous random variable,
$$
\mathbb{P}(X \in [a,b])=\int ^{b}_{a}  \, f(x)dx 
$$
Refers to an area, with two variables, it is instead the volume scale factor
## Theorem
For a set $A\subseteq \mathbb{R}^{2}$, 
$$
\mathbb{P}((X,Y)\in A)=\iint_{A}f(x,y)\,dydx
$$
When $A$ is a finite union of sets of the following type:
$$
\{ x\in [a,b],\phi_{1}(x)\leq y\leq\phi_{2}(x) \},
$$
$$
 \{\psi_{1}(y)\leq x\leq \psi_{2}(y),y\in [c,d] \}
$$
For continuous functions $\phi_{1},\phi_{2},\psi_{1},\psi_{2}$
An interpretation is:
$$
\mathbb{P}(X=0)=0
$$
$$
\mathbb{P}(X\in [x,x+dx])\approx f(x)dx
$$
$$
 \mathbb{P}(X \in [x,x+dx],Y \in [y,y+dy])=f(x,y)dxdy
$$
#### Corollary
$$
\iint_{\mathbb{R}^{2}}f(x,y)=1
$$
$$
\mathbb{R}^{2}=(-\infty,\infty)\times(-\infty ,\infty)=A=\{ -\infty<x<\infty ,-\infty<y<\infty \}
$$
Then the [[marginals|marginal]] densities are given by
$$
f_{X}(x)=\int_{-\infty}^{\infty} f(x,y) \, dy,f_{Y}(y)=\int_{-\infty}^{\infty} f(x,y) \, dx
$$
If $X$ is continuous, $f_{X}$, and $Y$ is continuous, $f_{Y}$, then $(X,Y)$ is not necessarily coninuously distributed, for example, let $X$ be a continuous random variable with pdf $f_{X}$. Define $Y=2X$, Then $(X,Y)$ is not jointly distributed
##### Proof
Suppose not, then there exists a joint pdf, sya $f(x,y)$;
$$
\mathbb{P}(2X=Y)=\iint_{\{ (x,y):y=2x \}}f(x,y)\,dydx=\int_{-\infty}^{\infty}  \,\int _{2x}^{2x}f(x,y) \, dy  dx =0
$$
However, we know that $\mathbb{P}(Y=2X)=1$



#Mathematics #Probability #Definition 