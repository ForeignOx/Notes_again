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
- satisfies Abel's theorem