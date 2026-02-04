A fundamental theorem in real analysis is the [[Bolzano-Weierstrass Theorem|Bolzano-Weierstrass theorem]] that states that bouned sequences have converging subsequences. This implies many results for [[Continuity|continuous]] [[Functions|functions]] on closed bounded [[Intervals|intervals]] or more generally, compact sets
## Definition
A non-[[Empty Set|empty]] [[Subsets|subset]] $K$ of $\mathbb{C}$ is called sequentially compact if for any [[Sequences|sequence]] $\left\{ z_{n} \right\}_{n\in\mathbb{N}}$ in $K$, there exists a [[Convergence|convergent]] [[Subsequences|subsequence]] $\left\{ z_{n_{k}} \right\}_{k\in\mathbb{N}}$ whose limit lies in $K$
## Example
$B_{1}(0)=\left\{ z\in\mathbb{C}:\middle|: \left| z \right|<1 \right\}$ is not sequentially compact ,
$$
z_{n}=1-\frac{1}{n}\in B_{1}(0)
$$
But $z_{n}\to 1\not\in B_{1}(0)$
## Heine-Borel Theorem
There is a simple criterion for sequential compactness in $\mathbb{C}$:
A subset $K$ of $\mathbb{C}$ is sequentially compact iff it is closed and bounded (i.e. it is closed and there exists an $M>0$ such that $\left| z \right|\leq M$ for any $z\in K$)
### Remark
This holds in $\mathbb{R}^{n}$ and $\mathbb{C}^{n}$ for any $n\in\mathbb{N}$, it is not true in general metric spaces
### Proof
We'll show that if $K$ is bounded and closed, then it is compact
Let $\left\{ z_{n} \right\}_{n\in\mathbb{N}}\in K$ be given, we write
$$
z_{n}=x_{n}+iy_{n},x_{n},y_{n}\in \mathbb{R}
$$
And see that $\left\{ x_{n} \right\}_{n\in \mathbb{N}}$ and $\left\{ y_{n} \right\}_{n\in\mathbb{N}}$ are real and bounded such that
$$
\max\left\{ \left| x_{n} \right| ,\left| y_{n} \right|  \right\}\leq \left| z_{n} \right| \leq U
$$
Hence $\left\{ x_{n} \right\}$ and $\left\{ y_{n} \right\}$ are bounded
Using Bolzano-Weierstrass, we can find a subsequence $\left\{ x_{n_{k}} \right\}_{k\in\mathbb{N}}$ that converges to some $x\in\mathbb{R}$, so we have
$$
z_{n_{k}}=x_{n_{k}}+iy_{n_{k}}
$$
We know $x_{n_{k}}$ converges, but we don't know about $y_{n_{k}}$, but we do know that it is a bounded sequence
By Bolzano-Weierstrass, there exists a subsequence of $\left\{ y_{n_{k_{j}}} \right\}_{j\in\mathbb{N}}$, that converges to some $y\in\mathbb{R}$
Hence,
$$
z_{n_{k_{j}}}=x_{n_{k_{j}}}+iy_{n_{k_{j}}}
$$
And $x_{n_{k_{j}}}$ still converges to $x$, so altogether, we have a convergent subsequence of $z_{n_{k_{j}}}$ which converges to $z=x+iy$ 
Since $K$ is closed, $\left\{ z_{n_{k_{j}}} \right\}_{j\in\mathbb{N}}\subset K$, and $z_{n_{k_{j}}}\to z$, we must have $z\in K$
### Examples
$B_{1}(0)$ is not closed, so it is not compact
$\mathbb{C}$ is not compact, since it is not bounded
