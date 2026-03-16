We recall a key theorem of invariant distributions, if $\left| I \right|<\infty$ and there exists $i\in I$ such that the limit
$$
\lim_{ n \to \infty } P_{ij}^{(n)}=\pi_{j}
$$
Exists for all $j\in I$, then $\pi=(\pi_{j})_{j\in I}$ is an invariant distribution for $P$
When does this convergence actually happen? Does it always happen?
## Counterexample
Consider the Markov chain:
![[Pasted image 20260316121246.png]]
Clearly this is periodic with period $\hspace{0pt}2$, $X_{n}$ simply alternates between $A$ and $B$, we see that
$$
P_{AA}^{n}=\begin{cases}
1 & n\text{ even} \\
0 & n\text{ odd}
\end{cases}
$$
Therefore $\lim_{ n \to \infty }P_{A A}^{n}$ doesn't exist
Periodicity turns out to be essentially the only problem!
## Theorem
Suppose $P$ is [[Irreducible Markov Chains|irreducible]] and [[period of states|aperiodic]] and suppose $P$ has an [[Invariant Distributions|invariant distribution]] $\pi$. Suppose $(X_{n})_{n\geq 0}$ is $Markov(\lambda,P)$, then for all $j\in I$,
$$
\lim_{ n \to \infty } \mathbb{P}(X_{n}=j)=\pi_{j}
$$
## Remark
In particular, take $\lambda=\delta_{i}$, then $P^{n}_{ij}\to \pi_{j}$ as $n\to \infty$ for all $i$
___
It is almost impossible to state how important this is. It's the key idea between the google search algorithm, the basis of Markov chain Monte Carlo methods and many other applications
## Example

___
Suppose $\mathbb{P}(X_{n}=H)=p \in(0,1)$ and where $Y_{n}$ is the number of heads amongst $X_{0},X_{1},\dots,X_{n}$. FInd
$$
\lim_{ n \to \infty } \mathbb{P}(X_{n}\text{ is a multple of }17)
$$
$(Y_{n})_{n\geq 0}$ is a Markov chain on $\mathbb{N}$. Let $Z_{n}=Y_{n}\mod 17$ 
We calim $(Z_{n})_{n\geq 0}$ is a Markov chain on $I=$