The [[Sets|set]] (which is also a [[Groups|group]]) of $n\times n$ [[Orthogonal Matrices|orthogonal]] [[Matrices|matrices]] is denoted by
$$
O(n):=\left\{ M\in  GL(n,\mathbb{R})|M^{\top}M=MM^{\top}=I \right\}
$$
It turns out this is the set of rotational and reflective matrices and is a [[Subgroups|subgroup]] of the [[General Linear Group|general linear group]] 
In practice, if $M\in O(n)$, then we can write it as $n$ column [[Vectors|vectors]], and $M^{\top}$ as row vectors:
$$
M=\begin{pmatrix}
\underline{v}_{1}&\dots&\underline{v}_{n}
\end{pmatrix}
$$
$$
M^{\top}=\begin{pmatrix}
\underline{v}_{1}^{\top}\\\vdots\\\underline{v}_{n}^{\top}
\end{pmatrix}
$$
So
$$
(M^{\top}M)_{ij}=\left( \begin{pmatrix}
\underline{v}_{1}^{\top}\\\vdots\\\underline{v}_{n}^{\top}
\end{pmatrix}\begin{pmatrix}
\underline{v}_{1}&\dots&\underline{v}_{n}
\end{pmatrix} \right)_{ij}=\underline{v}_{i}^{\top}\underline{v}_{j}=\underline{v}_{i}\cdot \underline{v}_{j}=(\underline{v}_{i},\underline{v}_{j})=\delta_{ij}
$$
Where $(\underline{v}_{i},\underline{v}_{j})$ is the [[Dot Product|dot product]], $\delta$ is the [[Kronecker Delta Function|Kronecker delta function]], so the comns of $M$ form an [[Orthonormal Vectors|orthonormal]] [[Basis|basis]] of $\mathbb{R}^{n}$ with respect to the standard [[Inner Product|inner product]], the dot product

