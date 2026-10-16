## Definition
An [[Linear Maps|operator]] $\hat{A}$ is a projector if $\hat{A}^{2}=\hat{A}=\hat{A}^{\dagger}$
## Projectors onto [[Subspaces|Subspaces]]
If [[Hilbert Spaces|$V\subseteq \mathcal{H}$]] is a subspace with [[Orthonormal Vectors|orthonormal]] [[basis|basis]] $\ket{v_{1}},\dots,\ket{v_{d}}$, the projector onto $V$ is:
$$
\hat{P}_{V}=\sum_{k=1}^{d}\ket{v_{k}} \bra{v_{k}} 
$$
### Example
Project from 3d to 2d;
$$
P:\underline{v}=\begin{pmatrix}
x \\
y \\
z 
\end{pmatrix}\mapsto \begin{pmatrix}
x \\
y \\
0
\end{pmatrix}
$$
So
$$
P=\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
 0 & 0 & 0
\end{pmatrix}=\begin{pmatrix}
1 \\
0 \\
0
\end{pmatrix}\begin{pmatrix}
1 & 0 & 0
\end{pmatrix}+\begin{pmatrix}
0 \\
1 \\
0
\end{pmatrix}\begin{pmatrix}
0 & 1 & 0
\end{pmatrix}
$$
As $\begin{pmatrix}1 \\ 0 \\ 0 \end{pmatrix}$ and $\begin{pmatrix}0 \\ 1 \\ 0\end{pmatrix}$ is an orthonomal basis for the subspace corresponding to the $xy$-plane
## Proposition
$\hat{P}_{V}$ is a Hermitian projection operator and it keeps the part of a vector lying in $V$ and removes the part orthogonal to $V$:
$$
\hat{P}_{V}\ket{v} =\ket{v} \text{ for }\ket{v} \in V
$$
$$
 \hat{P}\ket{w} =0\text{ for }\ket{w} \bot V
$$
### Proof
$\hat{P}^{\dagger}=\hat{P}$ since 
$$
(\ket{v_{k}} \bra{v_{k}} )^{\dagger}=\ket{v_{k}} \bra{v_{k}} 
$$
And
$$
\hat{P}^{2}_{V}=\sum_{k}\ket{v_{k}}\underbrace{  \braket{ v_{k} | v_{l} }  }_{ =\delta_{kl} }\bra{v_{l}} =\sum_{k}\ket{v_{k}} \bra{v_{k}} =\hat{P}_{V}
$$
If $\ket{v} =\sum_{l}c_{l}\ket{v_{l}} \in V$, then
$$
\hat{P}_{V}\ket{v} =\sum_{k}\sum_{l}c_{l}\ket{v_{k}} \braket{ v_{k} | v_{l} } =\ket{v} 
$$
And if $\ket{w}\bot V$, then every $\braket{ v_{k} | w }=0$, and so
$$
\hat{P}_{V}\ket{w} =\sum_{k}\ket{v_{k}} \braket{ v_{k} | w } =0
$$
## Proposition
Let $\hat{A}$ be a [[Hermitian Matrices|Hermitian]] operator with distinct eigenvalues $a_{1},\dots,a_{m}$, the projectors $\hat{P}_{a_{k}}$ onto its eigenspaces $V_{a_{k}}$ satisfy
$$
\hat{P}_{a_{j}}\hat{P}_{a_{k}}=\delta_{jk}\hat{P}_{a_{k}},~ \sum_{k=1}^{m}\hat{P}_{a_{k}}=\mathbb{1}
$$

### Proof
The first holds because different eigenspaces are orthogonal. The second is the the completeness relation for an orthonormal basis of eigenvectors

