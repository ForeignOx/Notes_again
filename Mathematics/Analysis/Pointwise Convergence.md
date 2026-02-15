## Definition (for sequences)
Let $D\subseteq \mathbb{C}$ be a given [[sets|set]] or [[Intervals|interval]] and let $\left\{ f_{n} \right\}_{n\in\mathbb{N}}:D\to \mathbb{C}$ (or $\mathbb{R}$) be a [[Sequences of Functions|sequence of functions]]. We say that $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ converges pointwise on $D$ to $f:D\to \mathbb{C}$ if for any $z\in D$ the [[Convergence|limit]] [[functions|function]]
$$
f(z):=\lim_{ n \to \infty } f_{n}(z)
$$
Exists
In other words, for any $z\in D$ and any $\varepsilon>0$ there exists $N(\varepsilon,z)\in\mathbb{N}$ such that if $n>N(\varepsilon,z)$, $\left| f_{n}(z)-f(z) \right| <\varepsilon$
And in fewer words, if
$$
(\forall z\in  D )(\forall\varepsilon>0)(\exists N(\varepsilon,z)\in \mathbb{N}): n>N(\varepsilon,z)\implies \left| f_{n}(z)-f(z) \right| <\varepsilon
$$
Note that in general $N(\varepsilon,z)$ depends on $\varepsilon$ and $z\in\mathbb{C}$
## Definition (for series)
We say that the [[Series|series]] $\sum_{n=1}^{\infty}f_{n}(z)$ conerges pointwise on $D$ to $S:\mathbb{C}\to \mathbb{C}$ if the sequence of functions $\left\{ S_{N} \right\}_{N\in\mathbb{N}}:D\to \mathbb{C}$ defined by 
$$
S_{N}(z)=\sum_{n=1}^{N}f_{n}(z)
$$
Convverges pointwise to the function $S(z)$
## Example
Take $f_{n}(x)=x^{n}$ on $I=[0,1]$
$$
\lim_{ n \to \infty } x^{n}=f(x)=\begin{cases}
0&\text{if }x\in [0,1)
\\1&\text{if }x=1
\end{cases}
$$

___
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
Indeed for $z\in\mathbb{C}$ such that $\left| z \right|<1$, we have that
$$
0\leq \left| f_{n}(z) \right| =\left| z \right| ^{n}\to{0}
$$
Using the [[Squeeze Theorem|squeeze theorem]] we conclude that $\left\{ \left| f_{n}(z) \right| \right\}_{n\in\mathbb{N}}$ converges to $\hspace{0pt}0$, and consequently so does $\left\{ f_{n}(z) \right\}_{n\in\mathbb{N}}$
Notice that if we use the $\varepsilon,N$ definition, we get that for any $z\neq 0$,
$$
\left| f_{n}(z)-0 \right| =\left| z \right| ^{n}<\varepsilon \iff n>\frac{\log\varepsilon}{\log(\left| z \right| )}
$$
i.e. $N(\varepsilon,z)=\frac{\log \varepsilon}{\log \left| z \right|}$ which goes to infinity as $\left| z \right|$ goes to $1$. Turning our attention to $z=1$, we see
$$
f_{n}(1)=1\to 1
$$
Next we consider the case $\left| z \right|>1$ and find that
$$
\left| f_{n}(z) \right| =\left| z \right| ^{n}\to \infty
$$
So by definition in $\hat{\mathbb{C}}$ we have that $\left\{ f_{n}(z) \right\}_{n\in\mathbb{N}}$ we have that $\left\{ f_{n}(z) \right\}_{n\in\mathbb{N}}$ converges to $\infty$ (which is not in $\mathbb{C}$)
Lastly, we consider the case $\left| z \right|=1$ and $z\neq 1$. We can write $z=e^{ i\theta }$ with $\theta \neq 0$ and notice that
$$
f_{n+1}(z)=e^{ i(n+1)\theta }=e^{ i\theta }e^{ in\theta }=e^{ i\theta }f_{n}(z)
$$
Consequently, if $f_{n}(z)\to \xi$, then
$$
\xi=\lim_{ n \to \infty } f_{n+1}(z)=e^{ i\theta }\lim_{ n \to \infty } f_{n}(z)=e^{ i\theta }\xi
$$
Since $e^{ i\theta }\neq 1$, by the uniqueness of limits we must have $\xi=0$, which is impossible since
$$
\left| \xi \right| =\lim_{ n \to \infty } \left| f_{n}(z) \right| =\lim_{ n \to \infty } \left| e^{ in\theta } \right| =1
$$
Which concldes that in this case we have no limit
## Remark
The above problem illustrates a big problem wee have with pointwise convergence - it doesn't retain important topological properties such as continuity: our original sequence $f_{n}(z)$ was continuous on $\mathbb{C}$ and converged pointwise on $\mathbb{D}\cup \left\{  1 \right\}$. The limit function, however, was not continuous at $z=1$. We need a better notion that will allow us to transfer topological properties from the sequence of functions to the limit