## Definition
Let [[Symmetric Groups|$\sigma \in S_{n}$]] be a [[Permutations|permutation]]
$$
\sigma=\begin{pmatrix}
1 & 2 & \dots & n \\
\sigma(1) & \sigma(2) & \dots & \sigma(n)
\end{pmatrix}
$$
A pair $(i,j),i<j,1\leq i,j\leq n$ is an inversion of $\sigma$ if $\sigma(i)>\sigma(j)$
## Example
Consider
$$
\sigma=\begin{pmatrix}
1 & 2 & 3 & 4 \\
2 & 3 & 1 & 4
\end{pmatrix}
$$
Then the inversions of $\sigma$ are $(1,3)$ as $\sigma(1)>\sigma(3)$ and $(2,3)$ as $\sigma(2)>\sigma(3)$
## Odd and Even Permutations
- $\sigma \in S_{n}$ is odd if number of inversions of $\sigma$ is odd
- $\sigma \in S_{n}$ is even if the number of inversions of $\sigma$ is even
- The sign of $\sigma$ is $\text{sgn}(\sigma)=(-1)^{N}$, where $N$ is the number of inversions of $\sigma$
## Lemma
Let $\sigma \in S_{n}$ be any permutation, and $\tau \in S_{n}$ be a transposition, then
$$
\text{sgn}(\sigma \tau)=-\text{sgn}(\sigma)
$$
I.e. multiplication by a transposition changes the parity of the number of inversions
### Proof
$$
\sigma=\begin{pmatrix}
1 & 2 & 3 & \dots & a & \dots & b & \dots & n \\
\sigma(1) & \sigma(2) & \sigma(3) & \dots & \sigma(a) & \dots & \sigma(b) & \dots & \sigma(n)
\end{pmatrix}
$$
So if $\tau=\begin{pmatrix}a & b\end{pmatrix}$ then if$i\neq a,b$, 
$$
\sigma \tau(i)=\sigma(ab)(i)=\sigma(i)
$$
$$
\sigma \tau(a)=\sigma(b)
$$
$$
 \sigma \tau(a)-\sigma(a)

$$
So
$$
\sigma \tau = \begin{pmatrix}
1 & 2 & 3 & \dots & a & \dots & b & \dots & n \\
\sigma(1) & \sigma(2) & \sigma(3) & \dots & \sigma(b) & \dots & \sigma(a) & \dots & \sigma(n)
\end{pmatrix}
$$
Take any $k$:
- $k<a$, then the number of inversions $k$ involed in $\sigma$ and $\sigma \tau$
- Similarly, if $k>b$, then the number of inversions of $kq$ which doesn't concern us
- $a<k<v<\sigma(a)$

Finish proof
## Corollary
Take $\sigma \in _{n}$, write $\sigma$ as a product of transpositions, then $\sigma$ is even if the number of transpositions is even and odd if the number of transpositions is odd
In particular, the parity of the number of transpositions in any expression of $\sigma$ is always the same
### Proof
Clearly, $e$ is even. Multiplication by a transposition changes the sign of a permutation by lemma above, so if $\sigma$ is a product of an even number of transpositions then we change sign an even number of times, so $\sigma$ is even. Otherwise, $\sigma$ is odd
## Examples
$$
\text{sgn}(\begin{pmatrix}
a & b
\end{pmatrix})=-1
$$
$$
\text{sgn}(\begin{pmatrix}
a_{1} & a_{2} & \dots & a_{k}
\end{pmatrix})=\text{sgn}(\begin{pmatrix}
a_{1} & a_{2}
\end{pmatrix}\begin{pmatrix}
a_{2} & a_{3}
\end{pmatrix}\dots \begin{pmatrix}
a_{k-1} & a_{k}
\end{pmatrix})=(-1)^{k-1}
$$
