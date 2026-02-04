## Theorem
Let $f_{n}(x)$ be a [[Sequences of Functions|sequence]] of [[Borel Functions|borel]] [[Functions|functions]] that converges to $f(x)$ as $n\to \infty$ where there exists some finite constant $M\geq 0$ such that $\left| f_{n}(x) \right|\leq M$ for all $n\geq 1$, then the sequence of [[Lebesgue Integration|Lebesgue integrals]] of $f_{n}(x)$ converges to the Lebesgue integral of $f(x)$
### Proof
Using the [[Dominated Convergence Theorem|dominated convergence theorem]] with $g(x)=M$, the result is immediate

# For Random Variables
## Theorem
Let [[Random Variables|random variables]] $X$ and $(X_{n})_{n\in\mathbb{N}}$ and a finite constant $M\geq 0$ be such that $\left| X_{n}(\omega) \right|\leq M$ for all $\omega \in \Omega$ and $n\geq 1$. If [[Sure Convergence|$X_{n}(\omega)\to X(\omega)$]] for each $\omega \in \Omega$, then [[Expectation|$\mathbb{E}(X_{n})\to \mathbb{E}(X)$]]  as $n\to\infty$
### Proof
Same as above; using the dominated convergence theorem with $Y=M$, the result is immediate
## Remark
As with [[Monotone Convergence Theorem|monotone convergence theorem]], and dominated convergence theorem the result holds if the assumptions are relaxed to their [[Almost Sure Convergence|almost sure]] versions:
$$
\mathbb{P}(\left\{ \omega \in \Omega :\middle|:\left| X_{n}(\omega) \right| \leq M~\forall n\geq 1 \right\})=1
$$
$$
 \mathbb{P}(\left\{ \omega \in \Omega :\middle|:X_{n}(\omega)\to X(\omega) \right\})=1
$$
___
The bounded convergence theorem also holds in the even more relaxed assumption [[Convergence in Probability|$X_{n}\overset{p}\to X$]]


