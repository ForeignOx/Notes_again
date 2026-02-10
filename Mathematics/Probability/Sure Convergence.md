## Definition
For a sequence of [[Random Variables|random variables]] in a [[Probability Spaces|probability space]] $(\Omega,\mathfrak{F},\mathbb{P})$ exhibit [[Pointwise Convergence|pointwise]] or sure convergence $X_{n}\to X$ if
$$
X_{n}(\omega)\to X(\omega)\forall \omega \in \Omega
$$
## Remark
Pointwise convergence is a very natural property. In particular, it is preserved by the action of [[Continuity|continuous]] [[Functions|functions]]: 
If $X_{n}\to X$ surely as $n\to \infty$ and $f:\mathbb{R}\to \mathbb{R}$ is continuous, then the sequence $(f(X_{n}))_{n\in\mathbb{N}}$ of random variables converges to $f(X)$ surely
However, sure convergence is a very restrictive condition and is often too strong to do anything useful in probability, for example the expectations on't always converge with the variables
## Example
Let $U(0,1)$ be a [[Uniform Distribution|uniform]] random variable, and let
$$
X_{n}(\omega)=n\mathbb{1}_{\left\{ U(\omega)\leq \frac{1}{n} \right\}}
$$
We claim that $X_{n}\to 0$ pointwise
To show this, lets fix $\omega$ and onsider $U(\omega)\in(0,1)$, suppose 
$$
n> \frac{2}{U(\omega)}\implies U(\omega)\not \leq \frac{1}{n}
$$
So for such $n$, $X_{n}(\omega)=0$ then $\lim_{ n \to \infty }X_{n}(\omega)=0$, but note
$$
\mathbb{E}(X_{n})=\mathbb{E}\left( n\mathbb{1}_{\left\{ U\leq \frac{1}{n} \right\}} \right)=n\mathbb{P}\left( U\leq \frac{1}{n} \right)=1
$$
But $\mathbb{E}(X)=0$ uh oh ://