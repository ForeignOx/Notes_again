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
$$
\mathbb{P}(X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n})=\lambda_{i_{0}}P_{i_{0}i_{1}}\dots P_{i_{n-1}i_{n}}
$$
For all $i_{0},\dots,i_{n} \in I$
We now fix arbitrary $i_{0},i_{1},\dots,i_{n},i_{n+1}\in I$, then we have
$$
\mathbb{P}(X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n})=\lambda_{i_{0}}P_{i_{0}i_{1}}\dots P_{i_{n-1}i_{n}}
$$
We now split into two cases, one wherre the above is $>0$ and one where it is equal to 0
If it is positive, we have
$$
\mathbb{P}(X_{n+1}=i_{n+1}\mid X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n})=\mathbb{P}(X_{n+1}=i_{n+1}\mid X_{n}=i_{n})=P_{i_{n}i_{n+1}}
$$
Hence
$$
\mathbb{P}(X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n}X_{n+1}=i_{n+1})
$$
$$
= \mathbb{P}(X_{n+1}=i_{n+1}\mid X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n})\mathbb{P}(X_{0}=i_{0},\dots,X_{n}=i_{n})
$$
$$
= \lambda _{i_{0}}P_{i_{0}i_{1}}\dots P_{i_{n-1}i_{n}}P_{i_{n}i_{n+1}}
$$
If it is $\hspace{0pt}0$, then
$$
\lambda_{i_{0}}P_{i_{0}i_{1}}\dots P_{i_{n-1}i_{n}}P_{i_{n}i_{n+1}}=0\times P_{i_{n}i_{n+1}}
$$
And
$$
\mathbb{P}(X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n},X_{n+1}=i_{n+1})\leq \mathbb{P}(X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n})=0
$$
Since
$$
\left\{ X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n},X_{n+1}=i_{n+1} \right\}\subseteq \left\{ X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n} \right\}
$$
And either way we have
$$
\mathbb{P}(X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n},X_{n+1}=i_{n+1})=\lambda_{i_{0}}P_{i_{0}i_{1}}\dots P_{i_{n-1}i_{n}}P_{i_{n}i_{n+1}}
$$
And our induction is proven
Now we prove the converse. We suppose that wee have
$$
\mathbb{P}(X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n})=\lambda _{i_{0}}P_{i_{0}i_{1}}\dots P_{i_{n-1}i_{n}}
$$
For all $i_{0},i_{1},\dots,i_{n}\in I$
We want to prove that $(X_{n})_{n\in\mathbb{N}}$ is $Markov(\lambda,P)$
Recall that we need to show:
- $\mathbb{P}(X_{0}=i_{0})=\lambda_{i_{0}}$ for all $i_{0}\in I$. This hold by taking $n=0$
- For all $i_{0},i_{1},\dots,i_{n},i_{n+1}\in I$ with
$$
\mathbb{P}(X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n})>0
$$
    We have
$$
\mathbb{P}(X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n},X_{n+1}=i_{n+1}\mid X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n}) 
$$
$$
= \frac{\lambda_{i_{0}}P_{i_{0}i_{1}}\dots P_{i_{n-1}i_{n}}P_{i_{n}i_{n+1}}}{\lambda_{i_{0}}P_{i_{0}i_{1}}\dots P_{i_{n-1}i_{n}}}=P_{i_{n}i_{n+1}}
$$
Here we are using $\mathbb{P}(X_{0}=i_{0},X_{1}=i_{1},\dots,X_{n}=i_{n})$ to see that the denominator is strictly greater than 0
___
We can view this in terms of linear algebra. 
We write 
$$
\mathbb{P}_{i}(A)=\mathbb{P}(A\mid X_{0}=i)
$$
For probabilities of $Markov(\delta_{i},P)$
Recall that the distributions are row vectors. By convention, $P^{0}=I$ (the $\left| I \right|\times \left| I \right|$ identity matrix)
## Theorem
Let $(X_{n})_{n\in\mathbb{N}}$ be $Markov(\lambda,P)$. For $n,m\geq 0$:
- $\mathbb{P}(X_{n}=j)=(\lambda P^{n})_{j}$
- $\mathbb{P}_{i}(X_{n}=j)=\mathbb{P}(X_{n}=j\mid X_{0}=i)=(P^{n})_{ij}$
We can check, if $\left| I \right|<\infty$, these are vector-matrix and matrix-matrix products. If $\left| I \right|=\infty$, we can use the same formulae:
$$
(\lambda P)_{j}=\sum_{i\in  I}\lambda_{i}P_{ij},~(P^{2})_{ij}=\sum_{k\in  I}P_{ik}P_{kj}
$$
And so on for other values of $n$
One can show that $(P^{2})_{ij}$ is well defined when $\left| I \right|=\infty$ (the sum converges)
## Remark
As we vary $j$, these describe row vector entries - the distribution of $X_{n}$ with the initial distribution $\lambda$ and $\delta_{i}$, respectively. In principle, this gives a way to answer most questions with linear algebra, however, this can lead to very lengthy calculations, and generally isn't the bet way of thining about Markov chains
### Proof
Use that matrix multiplication $A^{n}$ is a sum over paths of length $n$ and the theorem above
## Example
$$
P=\begin{pmatrix}
P_{A A} & P_{AB} \\
P_{BA} & P_{B B}
\end{pmatrix}=\begin{pmatrix}
1-\alpha & \alpha \\
\beta & 1-\beta
\end{pmatrix}
$$
Set up and solve the recurrence relation for $P_{A A}^{n}$
___
## Chapman-Kolmogorov Equations
We have, by matrix multiplication that
$$
P_{ij}^{n+m}=\sum_{k}P_{ik}^{n}P_{kj}^{m}
$$
In other words,
$$
\mathbb{P}(X_{n+m}=j\mid X_{0}=i)=\sum_{k}\mathbb{P}(X_{n}=j|X_{0}=k)\mathbb{P}(X_{m}=k\mid X_{0}=i)
$$
These are called the Chapman-Kolmogorov equations.
## Memorylessness
The Markov property fomalises the memorylessnes aspect of Markov chains, we call the [[Kronecker Delta Function|Kronecker delta]], $\delta_{i}$ the unit mass at $i$
## Theorem
If $(X_{n})_{n\in\mathbb{N}}$ is $Markov(\lambda,P)$ and $\mathbb{P}(X_{m}=i)>0$, then conditional on $X_{m}=i$, the sequence $(X_{m+n})_{n\in\mathbb{N}}$ is $Markov(\delta_{i},P)$ and is independent of $X_{0},X_{1},..,X_{m-1}$
### Proof
For the proof, we will use the idea of an event $A$ determined by $X_{0},\dots,X_{m-1}$
This means $A$ can be written as a union of elementary events $A_{k}$, where elementary events are of the form
$$
A_{k}=\left\{ X_{0}=i_{0},\dots,X_{m-1}=i_{m-1} \right\}
$$
For some $i_{0},\dots,i_{m_{1}}\in I$
So
$$
\bigcup_{k=0}^{\infty}A_{k}
$$
For some elementary events $A_{0},A_{1},\dots$ involving $X_{0},X_{1},\dots,X_{m-1}$
Note that if $\left| I \right| <\infty$, then this is a finite union, a countable union in any case; and any two elementary events (which aren't the same, for the same $m$) are disjoint
We will show that for any event $A$ determined by $X_{0},\dots,X_{m-1}$ and all $i_{m},\dots,i_{m+n}\in I$,
$$
\mathbb{P}(A\cap \left\{ X_{m}=i_{m},X_{m+1}=i_{m+1},\dots,X_{m+n}=i_{m+n}|X_{m}=i \right\})
$$
$$
 =\delta_{i i_{m}}P_{i_{m}i_{m+1}}\dots P_{i_{m+n-1}i_{m+n}}\mathbb{P}(A\mid X_{m}=i)
$$
This is the independence claim, $Markov(\delta_{i},P)$ follows by choosing $A=\Omega=\left\{ X_{0}\in \mathbf{I}..,X_{m-1}\in I \right\}$
We firstly take an elementary event 
$$
A_{k}=\left\{ X_{0}=i_{0},\dots,X_{m-1}=i_{m-1} \right\}
$$
For some $i_{0},\dots,i_{m_{1}}\in I$. We will show that
$$
\mathbb{P}(A_{k}\cap \left\{ X)_{m}=i_{m},X_{m+1}=i_{m+1},\dots,X_{m+n}=i_{m+n} \right\}\mid X_{m}=i)
$$
$$
= \delta_{i i_{m}}P_{i_{m}i_{m+1}}\dots P_{i_{m+n-1}i_{m+n}}\mathbb{P}(A_{k}\mid X_{m}=i)
$$
Clearly, if $i\neq i_{m}$, then both sides are $\hspace{0pt}0$, so now take $i_{m}=i$. Then we have
$$
LHS = \frac{\mathbb{P}(A_{k}\cap \left\{ X_{m}=i_{m},X_{m+1}=i_{m+1},\dots,X_{m+n}=i_{m+n} \right\})}{\mathbb{P}(X_{m}=i_{m})}\delta_{i i_{m}}
$$
$$
= \frac{\mathbb{P}(X_{0}=i_{0},\dots,X_{m-1}=i_{m-1},X_{m}=i_{m},X_{m+1}=i_{m+1},\dots,X_{m+n}=i_{m+n})}{\mathbb{P}(X_{m}=i_{m})}\delta_{i i_{m}}
$$
$$
= \frac{\lambda_{i_{0}}P_{i_{0}i_{1}}\dots P_{i_{m-1}i_{m}}P_{i_{m}i_{m+1}}\dots P_{i_{m+n-1}i_{m+n}}}{\mathbb{P}(X_{m}=i_{m})}
$$
$$
= \frac{\lambda_{i_{0}P_{i_{0}i_{1}}\dots P_{i_{m-1}i_{m}}}}{\mathbb{P}(X_{m}=i_{m})}\delta_{i i_{m}} P_{i_{m}i_{m+1}}\dots P_{i_{m+n-1}P_{i_{m+n}}}
$$
$$
=\frac{\mathbb{P}(A_{k}\cap \left\{ X_{m}=i \right\})}{\mathbb{P}(X_{m=i})}\delta_{i i_{m}}P_{i_{m}i_{m+1}}\dots P_{i_{m+n-1}P_{i_{m+n}}} 
$$
$$
= \mathbb{P}(A_{k}\mid X_{m}=i)\delta_{i i_{m}}P_{i_{m}i_{m+1}}\dots P_{i_{m+n-1}P_{i_{m+n}}}=RHS
$$
And we are done for the finite case
Since $A$ is a countable union of disjoint elementary events, we can use countable additivity to take the sum of both sides of over the elementary events constituting $A$ to see that
$$
\mathbb{P}(A\cap \left\{ X_{m}=i_{m},X_{m+1}=i_{m+1},\dots,X_{m+n}=i_{m+n}\right\}\mid X_{m}=i ) 
$$
$$
= \sum_{k}\mathbb{P}(A_{k}\cap \left\{ X_{m}=i_{m},X_{m+1}=i_{m+1},\dots,X_{m+n}=i_{m+n} \right\}\mid X_{m}=i) 
$$
$$
= \sum_{k}\delta_{i i_{m}}P_{i_{m}i_{m+1}}\dots P_{i_{m+n-1}i_{m+n}}\mathbb{P}(A_{k}\mid X_{m}=i)
$$
$$
= \delta_{i i_{m}}P_{i_{m}i_{m+1}}\dots P_{i_{m}i_{m+1}}\dots P_{i_{m+n-1}i_{m+n}}\mathbb{P}(A\mid X_{m}=i)
$$

