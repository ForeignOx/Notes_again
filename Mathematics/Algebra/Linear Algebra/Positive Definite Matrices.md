A real [[Symmetric and Anti-Symmetric Matrices|symmetric]] $n\times n$ [[Matrices|matrix]] $B$ is called positive definite if $\underline{v}^{\top}B\underline{v}>0$ for all non-zero [[Vectors|vectors]] [[Vectorspace Rn|$\underline{v}\in\mathbb{R}^{n}$]]
## Positive Eigenvalues $\implies$ Positive Definite
A symmetric matrix is positive definite iff its [[Eigenvalues|eigenvalues]] are all positive
### Proof
$\implies$:
For each eigenvalue $\lambda$, pick an [[Eigenvectors|eigenvector]] $\underline{v}$ with $B\underline{v}=\lambda \underline{v}$, then $0<\underline{v}^{\top}B\underline{v}=\lambda \underline{v}^{\top}\underline{v}=\lambda \underline{v}\cdot \underline{v}$, using the normal [[Dot Product|dot product]], but since $\underline{v}\neq 0,\underline{v}\cdot \underline{v}\neq 0$, so $\lambda>0$ 
$\impliedby$:
We will see **here** that given a real $n\times n$ symmetric matrix $B$, one can form a [[Basis|basis]] for $\mathbb{R}^{n}$ formed by the eigenvectors of $B$, with eigenvalue $\lambda_{i}$ and such that $\underline{v}_{i}\cdot \underline{v}_{j}=0$ for $i\neq j$. If we express an arbitrary non-zero vector $\underline{v}$ in this basis as
$$
\underline{v}=\sum_{ i=1} ^{ n}  c_{i}\underline{v}_{i}
$$
With at least one $c_{i}\neq 0$, so we have
$$
\underline{v}^{\top}B\underline{v}=\left( \sum_{ i=1} ^{ n}  c_{i}\underline{v}_{i} \right)\cdot\left( B\sum_{ j=1} ^{ n}  c_{j}\underline{v}_{j} \right)
$$
$$
= \left( \sum_{ i=1} ^{ n}  c_{i}\underline{v}_{i} \right)\cdot\left( \sum_{ j=1} ^{ n}  c_{j}\lambda_{j}\underline{v}_{j} \right)=\sum_{ i=1} ^{ n}  c^{2}_{i}(\underline{v}_{i}\cdot \underline{v}_{i})\lambda_{i}
$$
Where the last equality is derived since $v_{i}\cdot v_{j}=0$ for $i\neq j$. The last line is greater than $\hspace{0pt}0$ if all the eigenvalues are positive

#Mathematics #LinAlg #Definition 