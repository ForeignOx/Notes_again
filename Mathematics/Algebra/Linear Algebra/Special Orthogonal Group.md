The [[Subsets|subset]] of all the [[Orthogonal Matrices|orthogonal]] [[Matrices|matrices]] with [[Determinants|determinant]] $+1$ is known as the special [[Orthogonal Group|orthogonal group]], and is denoted by:
$$
SO(n):=\left\{ M\in O(n)|\det(M)=1 \right\}
$$
It is a [[Subsets|subset]] of the [[General Linear Group|general linear group]] and is sometimes called the special linear group
It turns out this is in fact the set of rotational matrices
$$
SO(1)=\left\{ x\in O(1)|\det(x)=1 \right\}=\left\{ \begin{pmatrix}
1
\end{pmatrix} \right\}
$$
Is trivial

$$
SO(2)=\left\{ A\in O(2)|\det(A)=1 \right\}
$$
Letting 
$$
A=\begin{pmatrix}
a&b\\c&d
\end{pmatrix}
$$
We have $AA^{\top}=I\implies A^{\top}=A^{-1}$, so
$$
A^{-1}=\frac{1}{\det(A)}\begin{pmatrix}
d&-b\\-c&a 
\end{pmatrix}=\begin{pmatrix}
d & -b\\-c & a
\end{pmatrix}=\begin{pmatrix}
a & c\\b & d
\end{pmatrix}
$$
So $d=a,c=-b$, so
$$
A=\begin{pmatrix}
a & b\\-b & a
\end{pmatrix}
$$
With $a^{2}+b^{2}=1,a,b\in\mathbb{R}$. It is convenient to write this as
$$
A=\begin{pmatrix}
\cos\theta & \sin\theta\\-\sin\theta & \cos\theta
\end{pmatrix}
$$
Since $(a,b)$ lie on a unit circle on $\mathbb{R}^{2}$. As transformations, these are rotations of the plane $\underline{x}\mapsto A\underline{x}$
