Let $(x_{n})_{n\in\mathbb{N}}$ be a [[Sequences|sequence]], a subsequence of $(x_{n})_{n\in\mathbb{N}}$ is a sequence $(x_{n_{j}})_{j\in\mathbb{N}}$ with $n_{1}<n_{2}<\dots$; $n_{j}$ monotonically increasing
## Example
Let $x_{n}=(-1)^{n}\left( 1-\frac{1}{n} \right)$, we can look at the subsequence $x_{2n}=1-\frac{1}{2n}$ or $x_{2n+1}=-\left( 1-\frac{1}{2n+1} \right)$
## Proposition
Let $(x_{n})_{n\in\mathbb{N}}$ be a [[Convergence|convergent]] sequence with $\lim_{ n \to \infty }x_{n}=x$, if $(x_{n_{j}})_{j\in\mathbb{N}}$ is a subsequence, then this is also convergent with $\lim_{ j \to \infty }x_{n_{j}}=x$
## Lemma
Every real sequence $(x_{n})_{n\in\mathbb{N}}$ contains a subsequence which is either increasing or decreasing
### Proof
Given a sequence $(x_{n})_{n\in\mathbb{N}}$, call $n_{0}\in\mathbb{N}$ a peak index, if $x_{n_{0}}\geq x_{n}\forall n>n_{0}$ 
Assume our sequence has infinitely many peak indices $n_{1}<n_{2}<n_{3}<\dots$ so $x_{n_{1}}\geq x_{n_{2}}\geq x_{n_{3}}\geq\dots$ which is our required subsequence
If we don't have infinitely many peak indices, we have finitely many: $n_{1}<n_{2}<\dots<n_{k}$, where $n_{k}$ is the last one. Look at $n_{k+1}$, which is not a peak index, so there is $n_{k+2}>n_{k+1}$ with $x_{n_{k+1}}<x_{n_{k+2}}$, and $x_{n_{k+2}}$ is also not a peak index, so there is $n_{k+3}$, and we can keep going to get the required subsequence $(x_{n_{k+j}})_{j\in\mathbb{N}}$, 

#Mathematics #Analysis #Definition