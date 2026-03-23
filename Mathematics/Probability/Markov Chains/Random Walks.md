## Simple Random Walk on $\mathbb{Z}$
The simple random walk on $\mathbb{Z}$ is a [[Markov chains|Markov chain]] with diagram:
![[Pasted image 20260303164012.png]]
Where $0<p=1-q<1$
Consider $f_{0}=\mathbb{P}_{0}(\text{return to }0)$ and let $h_{i}=\mathbb{P}_{i}(\text{hit }0)$, then
$$
f_{0}=qh_{-1}+ph_{1}
$$
Using the [[strong Markov property|strong Markov property]] $h_{1}=q+ph_{1}^{2}$ the smallest solution is $h_{1}=\min\left\{ 1, \frac{q}{p} \right\}$. So if $q=p=\frac{1}{2}$ then $h_{-1}=h_{1}=1$ which implies $f_{0}=1$ and the random walk is [[Recurrence and Transience|recurrent]]
If $q<p$ then $h_{1}<1$ which implies $f_{0}<1$ and transience. Similarly, if $q>p$, then $h_{-1}<1$ and we have transience
___
We can also analyse this random walk by testing whether $\sum_{n=0}^{\infty}P_{00}^{n}$ is finite or infinite. This is a more complicated method, but is useful
Suppose we start at $\hspace{0pt}0$. Obviously, we cannot return to $\hspace{0pt}0$ after an odd number of steps, so $P_{00}^{2n+1}=0$ for all $n$
Any given sequence of steps of length $2n$ from $0$ to $0$ occurs with probability $p^{n}q^{n}$, there being $n$ steps right and $n$ steps left, and the number of such sequences is the number of way sof choosing the $n$ steps from $2n$, thus
$$
P_{00}^{2n}={2n \choose n } p^{n}q^{n}
$$
Stirling's approximation provies an approximation to $n!$ for large $n$, 
$$
n!\sim A\sqrt{ n } \left( \frac{n}{e} \right)^{n}
$$
For some $A\in[1,\infty)$ (we do not need here that $A=\sqrt{ 2\pi }$), thus
$$
P_{00}^{2n}= \frac{(2n)!}{(n!)^{2}}(pq)^{n} \sim \frac{(4pq)^{n}}{A\sqrt{ \frac{n}{2} }}\text{ as }n\to\infty
$$
In the symmetric case $p=q=\frac{1}{2}$, we have that $4pq=1$ and so for some $N$ and all $n\geq N$,
$$
P_{00}^{2n}\geq \frac{1}{2A\sqrt{ n }}
$$
So
$$
\sum_{n=N}^{\infty} P_{00}^{2n}\geq \frac{1}{2A}\sum_{n=N}^{\infty} \frac{1}{\sqrt{  n }}=\infty
$$
Which shows that the random walk is recurrent
On the other hand, if $p\neq q$, then $4pq = r<1$, so by a similar argument, for some $N$,
$$
\sum_{n=N}^{\infty} P_{00}^{2n}\leq \frac{1}{A} \sum_{n=N}^{\infty} r^{n}<\infty
$$
And so the random walk is transient
## Simple Symmetric Random Walk on $\mathbb{Z}^{2}$
The simple random walk on $\mathbb{Z}^{2}$ has diagram:
![[Pasted image 20260303165550.png]]
And transition probabilities:
$$
p_{ij}=\begin{cases}
\frac{1}{4} & \left| i-j \right| =1 \\
0 & \text{otherwise}
\end{cases}
$$
Suppose we start at $0$, let us call the walk $X_{n}$ and write $X_{n}^{+}$ and $X_{n}^{-}$ for the projection of the walk on the diagonal lines $y=\pm x$,
![[Pasted image 20260303165722.png]]
Then $X_{n}^{+}$ and $X_{n}^{-}$ are independent symmetric random walks on $\frac{1}{\sqrt{ 2 }}\mathbb{Z}$ and $X_{n}=0$ iff $X_{n}^{+}=X_{n}^{-}=0$, this makes clear that for $X_{n}$ we have
$$
P_{00}^{2n}=\left( {2n \choose n }\left( \frac{1}{2} \right)^{2n} \right)^{2}\sim \frac{2}{A^{2}n}\text{ as }n\to\infty
$$
# Random Walks on Graphs
Recall a [[Graphs|graph]] $G=(V,E)$ consists of a set of vertices $V$ and edges $E\subseteq V\times V$ (note we don't allow more than one edge for any pair of vertices)
We suppose that we have a Markov chain whereby if $X_{n}=i$, then we choose uniformly amongst all $j\in V$ such that $\left\{ i,j \right\}$ is an edge (i.e. belongs to $E$), and we set $X_{n+1}=j$ 
Therefore the transition matrix is given by
$$
P_{ij}=\begin{cases}
\frac{1}{\deg(i)} & \left\{ i,j \right\}\in  E \\
0 & \text{otherwise}
\end{cases}
$$
Where $\deg(i)$ is the number of edges containing $i$. Note that with self loops, a loop counts as one more in degree
A graph is [[Connectedness of Graphs|connected]] if the associated Markov chain is [[Irreducible Markov Chains|irreducible]]. This is equivalent to the existence of a path between any two vertices
## Theorem
Suppose that $G=(V,E)$ is a graph, and $P$ is the associated Markov chain given above, then the [[Invariant Distributions|stationary measures]] are given by
$$
\pi_{i}=c \deg(i)
$$
For $c>0$ which satisfy the [[Detailed Balance|detailed balance]] equations 
$$
\pi_{i}P_{ij}=\pi_{j}P_{ji}
$$
For $i,j\in V$
### Proof
By [[Detailed Balance#Lemma|this theorem]], we imply need to show that $\pi$, defined by 
$$
\pi_{i}=\deg(i)
$$
Satisfies the detailed balance equations
If $\left\{ i,j \right\}\not\in E$ i.e. there's no edge between $i$ and $j$, then $P_{ij}=P_{ji}=0$ and it's trivial
If $\left\{ i,j \right\}\in E$ i.e. there is an edge between $i$ and $j$, then $P_{ij}=\frac{1}{\deg(i)}$, so
$$
\pi_{i}P_{ij}=\deg(i)  \frac{1}{\deg(i)}=1
$$
And similarly $\pi_{j}P_{ji}=1$, hence detailed balance is satisfied
### Example
Consider the Markov chain in the following diagram
![[Pasted image 20260323222338.png]]
Then 
$$
\deg(1)=\deg(3)=3,~\deg(2)=\deg(4)=\deg(5)=4
$$
So that
$$
P_{ij}=\begin{cases}
\frac{1}{3} & i=1, & j\in \left\{ 2,4,5 \right\} \\
\frac{1}{4} & i=2,  & j\in \left\{ 1,2,4,5 \right\} \\
\frac{1}{3} & i=3, & j\in  \left\{ 2,4,5 \right\} \\
\frac{1}{4} & i=4, & j\in  \left\{ 1,3,4,5 \right\} \\
\frac{1}{4} & i=5, & j\in  \left\{ 1,2,3,4 \right\}
\end{cases}
$$

The sum of degrees is therefore $18$, hence the stationary distribution is given by
$$
\pi=\begin{pmatrix}
\frac{1}{6} & \frac{2}{9} & \frac{1}{6} & \frac{2}{9} & \frac{2}{9}
\end{pmatrix}
$$
Then
$$
\pi P =\begin{pmatrix}
\frac{1}{6} & \frac{2}{9} & \frac{1}{6} & \frac{2}{9} & \frac{2}{9}
\end{pmatrix} \begin{pmatrix}
0 & \frac{1}{3} & 0 & \frac{1}{3} & \frac{1}{3} \\
\frac{1}{4} & \frac{1}{4} & \frac{1}{4} & 0 & \frac{1}{4} \\
0 & \frac{1}{3} & 0 & \frac{1}{3} & \frac{1}{3} \\
\frac{1}{4} & 0 & \frac{1}{4} & \frac{1}{4} & \frac{1}{4} \\
\frac{1}{4} & \frac{1}{4} & \frac{1}{4} & \frac{1}{4} & 0
\end{pmatrix} =\begin{pmatrix}
\frac{1}{6} & \frac{2}{9} & \frac{1}{6} & \frac{2}{9} & \frac{2}{9}
\end{pmatrix}
$$
Yay
Working out htis stationary distribution by solving $\pi P=\pi$ directly would have been much more difficult
___
Suppose that a king moves on an otherwise empty chessboard in discrete time, so at each step it chooses on of the adjacent squares and jumps onto it. This then constitutes a Markov chain
We let
$$
I=\left\{ (x,k):\middle|:x\in \left\{ a,b, \dots,h \right\},k\in \left\{ 1,2,\dots,8 \right\} \right\}
$$
Be the set of squares on the chessboard, so the king is a Markov chain $X_{n}\in I$, this can be viewed as the following graph:
![[Pasted image 20260323225307.png]]
We calculate the degrees:
$$
\deg(i)=\begin{cases}
3 & i\text{ is a corner} \\

\end{cases}
$$