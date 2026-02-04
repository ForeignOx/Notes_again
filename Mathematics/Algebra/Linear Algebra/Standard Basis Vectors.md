These are [[Vectors|Vectors]] in [[Vectorspace Rn|$\mathbb{R}^n$]], and for $1\leq i\leq n$, we define $\underline{e}_{i}\in\mathbb{R}^n$ by:
$$
\underline{e}_{1}=\begin{pmatrix}
1\\0\\\vdots\\0
\end{pmatrix}
$$
$$
\underline{e}_{2}=\begin{pmatrix}
0\\1\\\vdots\\0
\end{pmatrix}
$$
$$
\vdots
$$
$$
\underline{e}_{n}=\begin{pmatrix}
0\\0\\\vdots\\1
\end{pmatrix}
$$
![[Standard Basis Vectors 2024-10-08 11.17.26.excalidraw]]
Where the $i$th term from the top is a $\hspace{0pt}1$
We can express any vector $\underline{x}\in\mathbb{R}^n$ uniquely as a linear combination of the standard basis vectors, i.e:
$$
\underline{x}=\begin{pmatrix}
x_{1}\\x_{2}\\\vdots\\x_{n}
\end{pmatrix}=x_{1}\begin{pmatrix}
1\\0\\\vdots\\0
\end{pmatrix}+x_{2}\begin{pmatrix}
0\\1\\\vdots\\0
\end{pmatrix}+\dots+x_{n}\begin{pmatrix}
0\\0\\\vdots\\1
\end{pmatrix}=x_{1}\underline{e}_{1}+x_{2}\underline{e}_{2}+\dots+x_{n}\underline{e}_{n}
$$
The $x_{i}$ terms, the coefficiets are sometimes called the cartesian coordinates of the vector $\underline{x}$

#Mathematics #LinAlg #Definition