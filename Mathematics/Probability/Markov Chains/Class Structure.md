## Definition
Recall that we define for [[Markov Chains|Markov chains]]
$$
\mathbb{P}_{i}(A):=\mathbb{P}(A\mid X_{0}=i)
$$
Say $i$ leads to $j$, written $i\to j$, if $\mathbb{P}(X_{n}=j\text{ for some }n\geq 0)>0$
We say $i$ communicates with $j$, written $i\leftrightarrow j$ if $i\to j$ and $j\to i$
## Theorem
For disjoint states $i,j$, the following are equivalent:
- $i\to j$
- $\exists n,i_{0},i_{1},\dots,i_{n}$ with $i_{0}=i,i_{n}=j$ and $P_{i_{0}i_{1}}P_{i_{1}i_{2}}\dots P_{i_{n-1}i_{n}}>0$
- $P^{n}_{ij}>0$ for some $n>0$
### Proof
We start by proving the first and third are equivalent:
$$
\left\{ \omega :\middle|:X_{0}(\omega)=i,X_{n}(\omega)=j \right\}\subseteq \bigcup_{k=0}^{\infty}\left\{ \omega :\middle|: X_{0}(\omega)=i,X_{k}(\omega)=j \right\}
$$
Hence
$$
P_{ij}^{n}\leq \mathbb{P}(X_{n}=j\text{ for some }n\geq 0)\leq \sum_{n=0}^{\infty}\mathbb{P}_{i}(X_{n}=j)=\sum_{n=0}^{\infty}P_{ij}^{n}
$$
Which shows the first and third are equivalent
To show the first and second are equivalent, we have
$$
P^{n}_{ij}=\sum_{i_{1},\dots,i_{n-1}\in  I}P_{ii_{1}}P_{i_{1}i_{2}}\dots P_{i_{n-2}i_{n-1}}P_{i_{n-1}j}
$$
Then we have 
