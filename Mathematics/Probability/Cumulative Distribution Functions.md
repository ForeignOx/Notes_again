For any [[Random Variables|random variable]] $X$, 
$$
\mathbb{P}_{X}(B)=\mathbb{P}(X \in B), B\subseteq \mathbb{R}
$$
We define the cumulative distribution [[Functions|function]] (cdf) as this probability on the [[Intervals|interval]] $(-\infty,x]$:
$$
\mathbb{P}_{X}((-\infty,x])=\mathbb{P}(X\in (-\infty,x])=\mathbb{P}(X\leq x)=F(x)
$$
So a cdf:
$$
F:\mathbb{R}\to[0,1]
$$
$$
 F(X)=\mathbb{P}(X\leq x)
$$
So we can find $X(\omega)$ in the way
Let $-\infty<a\leq b<\infty$,
$$
\mathbb{P}(X \in (a,b])=F_{X}(b)-F_{X}(a)
$$
## Proof
The interval $(a,b]=(-\infty,b]\setminus(-\infty,a]$, so we can write:
$$
\mathbb{P}(X \in (a,b])=\mathbb{P}(X \in (-\infty,b]\setminus(-\infty,a])=\mathbb{P}(X\in (-\infty,b])-\mathbb{P}(X \in \underbrace{ (-\infty,b]\cap(-\infty,a] }_{ (-\infty,a] })
$$
Using the first consequence of [[Probabilities|probability]]
$$
\therefore \mathbb{P}(X \in (a,b])=\mathbb{P}(X \in (-\infty,a])=F_{X}(b)-F_{X}(a)
$$
## Theorem
### [[Continuous Random Variables|Continuous]]:
Let $X$ be a continuous random variable with pdf $f$, then 
$$
F(x)=\mathbb{P}(X\leq x)=\int _{-\infty}^{x}f(t) \, dt
$$
Moreover,
$$
\frac{d F}{dx} (x)=f(x)
$$
$F$ is [[Continuity|continuous]] everywhere except at countably many points, that is $\lim_{ y \to x }F(y)=F(x)$ for countably many $x$
### [[Discrete Random Variables|Discrete]]:
Let $X$ be a discrete random variable with pmf $p$, then 
$$
F(x)=\sum_{t:t\leq x}p(t)
$$
$F(x)$ is piecewise continuous and discontinuities, and the discontinuities are jump discontinuities. $F$ is always right discontinuous (for both discrete and continuous), i.e. at the point of discontinuity,
$$
\lim_{ y \uparrow x } F(y)\neq F(x)
$$
But
$$
\lim_{ y \downarrow x } F(y)=F(x)
$$
For all $x$, so for a discrete random variable,
$$
\mathbb{P}(X=x)=\lim_{ y \uparrow x }F(y)=p(x) 
$$
### Proof
Let $y_{1}\leq y_{2}$ for $y_{1},y_{2}\in\mathbb{R}$, if $\omega \in\left\{ X\leq y_{1} \right\}$, we have
$$
X(\omega)\leq y_{1}\leq y_{2}
$$
$$
\implies \left\{ X\leq y_{1} \right\}\subset \left\{ X\leq y_{2} \right\}
$$
By the definition of probability, this imples that $F_{X}(y_{1})\leq F_{X}(y_{2})$ for all real $y_{1}\leq y_{2}$
Next, for each $\omega \in\Omega$ we have $X(\omega)=-\infty$ iff$X(\omega)=-m$ for each integer $m\geq 1$; consequently
$$
\left\{ X=-\infty \right\}=\bigcap_{m\geq 1}\left\{ M\leq-m \right\}
$$
And the continuity result of [[Monotone Events|monotone events]] implies that $\lim_{ y \uparrow \infty }F_{X}(y)=1$
Now fix arbitrary $y\in \mathbb{R}$, for each integer $m\geq 1$, there is a real $\varepsilon>0$ such that $y<x=y+\varepsilon<y+\frac{1}{m}$, therefore
$$
(\forall m^{\in \mathbb{N}}) ~\bigcap_{x>y}\left\{ X\leq x \right\}\subset \left\{ X\leq y+\frac{1}{m} \right\}
$$
$$
\implies \bigcap_{\varepsilon>0}\left\{ X\leq y+\varepsilon \right\}\subset \bigcap_{m\geq 1}\left\{ X\leq y+\frac{1}{m} \right\}
$$
Similarly, for each real $\varepsilon>0$, there is an integer $m\geq 1$ so that $y<y+\frac{1}{m}<x=y+\varepsilon$, therefore
$$
(\forall x^{>y})~\bigcap_{m\geq 1}\left\{ X\leq y+\frac{1}{m} \right\}\subset \left\{ X\leq x \right\}
$$
$$
\implies \bigcap_{m\geq 1}\left\{ X\leq y+\frac{1}{m} \right\}\subset \bigcap_{\varepsilon>0}\left\{ X\leq y+\varepsilon \right\}
$$
As a result, 
$$
\bigcap_{\varepsilon>0}\left\{ X\leq y+\varepsilon \right\}=\bigcap_{m\geq 1}\left\{ X\leq y+\frac{1}{m} \right\}
$$
And so
$$
\lim_{ \varepsilon \downarrow 0 } F_{X}(y+\varepsilon)=\lim_{ m\uparrow \infty }F_{X}\left( y+\frac{1}{m} \right)\equiv \lim_{ m\uparrow \infty }  \mathbb{P}\left( X\leq y+\frac{1}{m} \right)=\mathbb{P}(X\leq y)\equiv F_{X}(y)
$$



## Theorem 2
Let $F$ be a cdf, then it has the following properties:
- $\lim_{ x \to -\infty }F(x)=0$, $\lim_{ x \to \infty }F(x)=1$
- $F$ is always right continuous
- $F$ is monotonically increasing
### Proof
For the first,
$$
F(x)=\mathbb{P}(X \in (-\infty,x])
$$
We know that
$$
\lim_{ x \to \infty } (-\infty,x]=\mathbb{R}
$$
So
$$
\lim_{ x \to \infty } F(x)=\mathbb{P}(X \in \mathbb{R})=1
$$
Similarly,
$$
\lim_{ x \to -\infty } (-\infty,a]=\emptyset
$$
So
$$
\lim_{ x \to \infty } F(x)=\mathbb{P}(X \in \emptyset)=0
$$
For the second, prove in own time bro
For the third, consider
$$
F(s)=\mathbb{P}(X\leq s)=\mathbb{P}(X \in (-\infty,s])
$$
$$
 F(t)=\mathbb{P}(X\leq t)=\mathbb{P}(X \in (-\infty,t])
$$
If $s\leq t$, $(-\infty,s]\subseteq(-\infty,t]$, then $\mathbb{P}(A)\leq \mathbb{P}(B)$, using this, we get $F(s)\leq F(t)$


#Mathematics #Probability #Definition