# For [[Real Functions|Real Functions]]
## Definition
We say [[Functions|$f(x)$]] on an [[Intervals|interval]] $I$ is the pointwise [[Limit|limit]] of a [[Sequences of Functions|sequence of functions]] if for all $x\in\mathbb{R}$ we have
$$
\lim_{ n \to \infty } f_{n}(x)=f(x)
$$
So
$$
\forall x\in I \forall\varepsilon>0\exists N>0:\forall n\geq N,\left| f_{n}(x)-f(x) \right| <\varepsilon
$$
$N$ depends on $\varepsilon$ and $x$
### Example
Take $f_{n}(x)=x^{n}$ on $I=[0,1]$
$$
\lim_{ n \to \infty } x^{n}=f(x)=\begin{cases}
0&\text{if }x\in [0,1)
\\1&\text{if }x=1
\end{cases}
$$




# For [[Complex Functions|Complex Functions]]
## Definition
Let $D\subseteq \mathbb{C}$ be a given [[sets|set]] and let $\left\{ f_{n} \right\}_{n\in\mathbb{N}}:D\to \mathbb{C}$ be a sequence of functions. We say that $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ converges pointwise on $D$ to $f:D\to \mathbb{C}$ if for any $z\in D$ the limit function
$$
f(z):=\lim_{ n \to \infty } f_{n}(z)
$$
Exists
In other words, for any $z\in D$ and any $\varepsilon>0$ there exists $N(\varepsilon,z)\in\mathbb{N}$ such that if $n>N(\varepsilon,z)$,
$$
\left| f_{n}(z)-f(z) \right| <\varepsilon
$$
Note that in general $N(\varepsilon,z)$ depends on $\varepsilon$ and $z\in\mathbb{C}$
We say that the [[Series|series]] $\sum_{n=1}^{\infty}f_{n}(z)$ conerges pointwise on $D$ to $S:\mathbb{C}\to \mathbb{C}$ if the sequence of functions $\left\{ S_{N} \right\}_{N\in\mathbb{N}}:D\to \mathbb{C}$ defined by 
$$
S_{N}(z)=\sum_{n=1}^{N}f_{n}(z)
$$
Convverges pointwise to the function $S(z)$
## Example
Consider the sequence of functions $f_{n}:\mathbb{C}\to \mathbb{C}$
$$
f_{n}(z)=z^{n}
$$
We claim that
$$
\lim_{ n \to \infty } f_{n}(z)=\begin{cases}
0 & \left| z \right| <1 \\
1 & z =1  \\
\text{no limit} & \left| z \right| =1,z\neq 1 \\
\infty & \left| z \right| >\infty
\end{cases}
$$
Indeed for $z\in\mathbb{C}$ such that $\left| z \right|$