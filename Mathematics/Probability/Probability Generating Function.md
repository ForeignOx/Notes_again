## Definition
If $X$ is a [[Discrete Random Variables|discrete]] [[Random Variables|random variable]], with values in $\mathbb{N}_{0}$, then it's [[Probabilities|probability]] [[Generating Functions|generating function]] is
$$
G(s)\equiv G_{X}(s):= \mathbb{E}(s ^{X})=\sum_{k=0}^{\infty}s ^{k}\mathbb{P}(X=k)
$$
For the pmf $\left\{ p_{k} \right\}\equiv \left\{ \mathbb{P}(X=k) \right\}$ of $X$
## Remark
For $\left| s \right|\leq 1$, the generating function $G_{X}(s)$ is bounded, as
$$
\left| G_{X}(s) \right| \leq \sum_{k=0}^{\infty}\mathbb{P}(X=k)\leq 1
$$
Consequently, each probability generating function:
- Can be [[Differentiation|differentiated]]  or [[Integration|integrated]]  term-wise any number of times at each $s$ such that $\left|  s \right|<1$
- possesses the uniqueness property of generating functions
- satisfies Abel's theorem, namely, if the sequence $(a_{n})_{n\in\mathbb{N}}$ is non-negative, and its generating function $G_{a}(s)$ is finite for $\left| s \right|< 1$, then $\lim_{ s \nearrow 1 }G_{a}(s)=\sum_{n=0}^{\infty}a_{n}$ whether the sum is finite or infinite. This standard result is useful if the [[Cauchy-Hadamard Theorem|radius of convergence]] is $\hspace{0pt}1$ as then one has no reason to expect that the limit exists as $s\nearrow 1$ 
## Example
It is straightforward to derive probability generating functions of many distributions, such as
If $\mathbb{P}(X=c)=1$ for some $c\in\mathbb{R}$, then $G(s)-\mathbb{E}(x^{X})=s ^{c}$
If [[Bernoulli Distribution|$X\sim \mathrm{Ber}(p)$]], then $G(s)=\mathbb{E}(s^{X})=(1-p)^{0}+ps=1-p+ps$
If [[Binomial Distribution|$X\sim B(n,p)$]], then $G(s)=\mathbb{E}(s ^{X})=\sum_{k=0}^{n}{n \choose k }p^{k}(1-p)^{n-k}s ^{k}$
If [[Poisson Distribution|$X\sim Po(\lambda)$]] then $G(s)=\mathbb{E}(s^{X})=\sum_{k=0}^{\infty} \frac{\lambda^{k}}{k!}e^{ -\lambda  }s ^{k}=e^{ \lambda(s-1) }$
## Theorem
If $X$ and $Y$ are [[Independence|independent]] random variables with values in $\mathbb{N}_{0}$, and $Z:=X+Y$, then their generating functions satisfy
$$
G_{Z}(s)=G_{X+Y}(s)=G_{X}(s)G_{Y}(s)
$$
### Proof
Recall that if $X$ and $Y$ are discrete random variables and $f,g:\mathbb{N}_{0}\to \mathbb{R}$ are arbitrary functions, then $f(X)$ and $g(Y)$ are independent random variables and 
$$
\mathbb{E}(f(X) g(Y))=\mathbb{E}(f(X))\mathbb{E}(g(Y))
$$
Taking $f(X)=s^{X}$ and $g(Y)=s^{Y}$, we are done
### Example
Let $X\sim Po(\lambda)$ and $Y\sim Po(\mu)$ be independent. Then $Z=X+Y$ is $Po(\lambda+\mu)$
By the example above for the Poisson distribution and the theorem above, we get
$$
G_{Z}(s)=G_{X}(s)G_{Y}(s)=e^{ \lambda(s-1) }e^{ \mu(s-1) }=e^{ (\lambda+\mu)(s-1) }
$$
The result follows by uniqueness
___
If $(X_{k})_{k=1}^{n}$ are [[Independent and Identically Distributed|independent and identically distributed]] with values in $\mathbb{N}_{0}$, 