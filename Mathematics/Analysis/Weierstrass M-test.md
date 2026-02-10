## Theorem
If we have the [[Series|series]] $\sum_{k=0}^{\infty}f_{k}(x)$ on an [[Intervals|interval]] or [[Domains|domain]] $D$, (where $f_{k}(x)$ is a [[Sequences of Functions|sequence of functions]])
Assuming $f_{k}(x)$ are all [[Boundedness|bounded]]: $\left| f_{k}(x) \right|\leq M_{k}~\forall x\in D$ and $\sum_{k=0}^{\infty} M_{k}$ [[Convergence|converges]], then $\sum_{k=0}^{\infty} f_{k}(x)$ [[Uniform Convergence|converges uniformly]] on $D$
## Proof
By comparison, 
$$
\sum_{k=0}^{\infty} \left| f_{k}(x) \right|  \leq \sum_{k=0}^{\infty} M_{k} <\infty
$$
So $\sum_{k=0}^{\infty} f_{k}(x)$ [[Absolute Convergence|converges absolutely]] to a [[Functions|function]] $f(x)$. We need to show this is uniform
Set 
$$
L=\sum_{k=0}^{\infty} M_{k}=\lim_{ n \to \infty } \sum_{ k=0} ^{ n}  M_{k}
$$
So given $\varepsilon>0$, there exists $N$ such that 
$$
\left| L-\sum_{k=0}^{n}M_{k} \right|=\sum_{k=n+1}^{\infty}M_{k}<\varepsilon ~\forall n\geq N
$$
So we will show
$$
\left| f(x)-\sum_{k=0}^{n}f_{k}(x) \right| <\varepsilon \forall n\geq N
$$
Indeed:
$$
\left| f(x)-\sum_{k=0}^{n}f_{k}(x) \right| =\left| \sum_{k=n+1}^{\infty}f_{k}(x) \right| \leq \sum_{k=n+1}^{\infty}\left| f_{k}(x) \right| \leq \sum_{k=n+1}^{\infty}M_{k}<\varepsilon
$$
So we have uniform convergence
___
This is useful to show [[Continuity|continuity]] of $\sum_{k=0}^{\infty} f_{k}(x)$, w use $M$-test on compact subsets of $I$ 
## Criteria for Lack of Uniform Convergence of a Series
Let $\left\{ f_{n} \right\}_{n\in\mathbb{N}}:D\to \mathbb{C}$ be a given sequence of functions. If $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ doesn't converge uniformly to $f(z)=0$ on $D$, then the sequence $S_{N}(z)=\sum_{n=1}^{N}f_{n}(z)$ does not converge uniforly on $D$
### Proof
