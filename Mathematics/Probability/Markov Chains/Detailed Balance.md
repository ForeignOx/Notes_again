A useful tool for finding stationary measures and [[Invariant Distributions|distributions]] is the following
## Definition
$\lambda$ and $P$ are in detailed balance if
$$
\lambda_{i}P_{ij}=\lambda_{j}P_{ji}~\forall i,j\in  I
$$
## Lemma
If $\lambda$ is in detailed balance with $P$, then $\lambda$ is invariant for $P$
### Proof
We have
$$
\lambda_{i}P_{ij}=\lambda_{j}P_{ji}
$$
Now taking the sum of both sides over $j$,
$$
\lambda_{i}\underbrace{ \sum_{j\in  I}P_{ij} }_{ =1 }=\sum_{j\in  I}\lambda_{j}P_{ji} 
$$
$$
\implies \lambda_{i}=\sum_{j\in  I}\lambda_{j}P_{ji}
$$