## Definition
For a countable collection of states, $I$, we consider $I$-valued [[Random Variables|random variables]] $X:\Omega\to I$, where the distribution of $X$ will be the vector $\lambda:I\to[0,1]$ given by $\lambda(i):=\mathbb{P}(X=i)$
We always think of these distributions as row [[Vectors|vectors]] for simplicity
We encode the random choices using [[Stochastic Matrices|stochastic matrices]]
## Example
Consider this following directed [[Graphs|graph]]:
![[Markov Chains 2026-02-16 12.37.45.excalidraw]]
This has the stochastic matrix:
$$
P=\begin{pmatrix}
P_{AA} & P_{AB} & P_{AC} \\
P_{BA} & P_{BB} & P_{BC} \\
P_{CA} & P_{CB} & P_{CC }
\end{pmatrix}=\begin{pmatrix}
0 & \frac{1}{2} & \frac{1}{2}  \\
\frac{1}{2} & 0 & \frac{1}{2}  \\
\frac{1}{2} & \frac{1}{2} & 0
\end{pmatrix}
$$
This is stochastic as all entries are greater than or equal to zero and all rows sum to 1
## Definition
Given a stochastic matrix $P$, we draw its Markov diagram by drawing a directed graph whose vertices are $V=I$ and by drawing a directed edge from $i$ to $j$ labelled $P_{ij}$ whenever $P_{ij}>0$
## Example
Consider the stochastic matrix
$$
P=\begin{pmatrix}
P_{AA} & P_{AB} & P_{AC} \\
P_{BA} & P_{BB} & P_{BC} \\
P_{CA} & P_{CB} & P_{CC }
\end{pmatrix}=\begin{pmatrix}
0 & 1 & 0 \\
0 & \frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & 0 & \frac{1}{2}
\end{pmatrix}
$$
Which has diagram:
![[Markov Chains 2026-02-16 12.35.52.excalidraw]]
## Definition
A Markov chain on $I$ with initial distribution $\lambda$ and transition matrix $P=(P_{ij})_{i,j}\in I$ is a sequence $(X_{n})_{n\geq 0}$ of $I$-valued random variables such that
-  $\mathbb{P}(X_{0}=i_{0})=\lambda_{i_{0}}$ for any $i_{0}\in I$
- For $n\geq 0$ and any $i_{0},i_{1},\dots,i_{n},i_{n+1}\in I$ with $\mathbb{P}(X_{0}=i_{0},\dots X_{n}=i_{n})>0$, we have
$$
\mathbb{P}(X_{n+1}=i_{n+1} \mid X_{0}=i_{0},\dots,X_{n}=i_{n})=P_{i_{n}i_{n+1}}
$$
    Note that this only depends upon $i_{n}$ and $i_{n+1}$, so knowing $i_{0},\dots,i_{n-1}$ (the past) doesn't affect anything. This is known as the Markov property
We say the same if $(X_{n})_{0\leq n\leq N}$ is a finite sequence satisfying these properties for $0\leq n<N$
## Theorem
$(X_{n})_{n\in\mathbb{N}}$ is $Markov(\lambda,P)$ if and only if
$$
P(X_{0}=i_{0},\dots,X_{n}=i_{n})=\lambda _{i_{0}}P_{i_{0}i}\dots P_{i_{n-1}i_{n}}
$$
For all $i_{0},\dots,i_{n}\in I$, $n\geq 0$, the same is true with the same proof for a finite subset of $\mathbb{N}$
### Proof
We prove this by induction. Suppose firstly that $(X_{n})_{n\in\mathbb{N}}$ is $Markov(\lambda,P)$, we argue by induction on $n$, starting with $n=0$
Base case:
By definition we have $\mathbb{P}(X_{0}=i_{0})=\lambda_{i_{0}}$
Induction step:
We suppose, by induction, that
