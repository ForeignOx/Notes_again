## Definition
Let $A_{n}$, $n\geq 1$ be a [[Sequences|sequence]] of [[Events|events]], then 
$$
\left\{ A_{n}\text{ eventually} \right\} = \bigcup_{n=1}^{\infty}\left( \bigcap_{k=n}^{\infty}A_{k} \right)=\left\{ \omega \in \Omega :\middle|: \text{for some }n\geq 1,\omega \in A_{k}~\forall n\geq k
\right\}
$$
Informally, $\omega \in\left\{ A_{n}  \text{ eventually}\right\}$ if there is a $N$ such that $\omega \in A_{n}$ for all $n\geq N$
Rewriting the description via indicator functions, we deduce that if $A_{n}$ converges, then the event $\left\{ A_{n}\text{ eventually} \right\}$ contains all $\omega \in\Omega$ belonging to the [[Infinite Sequences of Independent Random Variables|limit set]] $A=\lim_{ n \to \infty }A_{n}$
A different notation for this is:
$$
\liminf_{n\to \infty}A_{n}\equiv \left\{ A_{n}\text{ eventually} \right\}
$$
## Example
Let $X_{n}$ be a sequence of random variables such that $X_{n}(\omega)\to X(\omega)$ as $n\to \infty$ for some $\omega \in\Omega$, let
$$
C=\left\{ \omega \in \Omega :\middle|: X_{n}(\omega)\to X(\omega) \right\}
$$
Suppose $\omega \in C$, then 
$$
\lim_{ n \to \infty }X_{n}(\omega)=X(\omega)
$$
For every integer $k\geq 1$, there is an integer $n_{k}$ such that
$$
\left| X_{n}(\omega)-X(\omega) \right| <\frac{1}{k}
$$
For every $n\geq n_{k}$
Let 
$$
A_{k}=\left\{ \left| X_{n}(\omega)-X(\omega) \right| <\frac{1}{k}\text{ eventually} \right\}
$$
