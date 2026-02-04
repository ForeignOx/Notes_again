An $n\times n$ [[Matrices|matrix]] $P$ is unitary if
$$
P^{*}P=PP^{*}=I
$$
I.e.
$$
P^{-1}=P^{*}
$$
What is the [[Determinants|determinant]] of a unitary matrix?
$$
1=\det(P^{*}P)=\det(P^{*})\det (P)=\left| \det(P) \right| ^{2}
$$
In practivce if 
$$
P=\begin{pmatrix}
\underline{w}_{1}&\dots&\underline{w}_{n}
\end{pmatrix},P^{*}=\begin{pmatrix}
\underline{w}_{1}^{*}\\\vdots\\\underline{w}_{n}^{*}
\end{pmatrix}
$$
$$
(P^{*}P)_{ij}=\underline{w}_{i}\cdot \underline{w}_{j}=\left< \underline{w}_{j},\underline{w}_{i} \right> =\delta_{ij}
$$
