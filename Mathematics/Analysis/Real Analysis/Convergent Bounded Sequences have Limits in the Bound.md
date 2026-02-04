Let $(x_{n})_{n\in\mathbb{N}}$ be a [[Sequences|sequence]] such that [[Intervals|$x_{n}\in[a,b]$]] for all $n$. If the sequence [[Convergence|converges]] to $x\in\mathbb{R}$, then $x\in[a,b]$
## Proof
Assume $x<a$, choose $\varepsilon=\frac{a-x}{2}>0$
By convergence, there exists $N_{\varepsilon}\in\mathbb{N}$ with:
$$
|x_{n}-x|<\varepsilon \forall n\geq N_{\varepsilon}
$$
In particular:
$$
x-x_{n}>-\varepsilon
$$
Now
$$
a-x_{n}=a-x+x-x_{n}=2\varepsilon+x-x_{n}>\varepsilon>0
$$
So $a>x_{n}$ which is a contradiction, with a similar argument, we get $x\leq b$. Note that every convergent sequence is bounded, so we can always find some interval containing all the values of a convergent sequence
## Corollary
Let $(x_{n})_{n\in\mathbb{N}}$ and $(y_{n})_{n\in\mathbb{N}}$ be convergent sequences with $x_{n}\leq y_{n}$ for all $n\in\mathbb{N}$, then
$$
\lim_{ n \to \infty } x_{n}\leq \lim_{ n \to \infty } y_{n}
$$
### Proof
Consider $a_{n}=y_{n}-x_{n}$, then $a_{n}\geq 0$, so $\lim_{ n \to \infty }a_{n}\geq 0$ by [[Calculus of Limits Theorem|CoLT]]: $\lim_{ n \to \infty }y_{n}-\lim_{ n \to \infty }x_{n}\geq 0$

#Mathematics #Analysis #Theorem 