Suppose we have [[Systems of Linear Equations|$A\underline{x}=\underline{b}$]] for [[Matrices|$A\in M_{n}(\mathbb{R})$]] and [[Determinants|$\det(A)\neq 0$]]; $A$ is [[Matrix Inverses|invertible]]
The unique solution to $A\underline{x}=\underline{b}$ is given by:
$$
x_{i}=\frac{\det(\underline{a}_{1},\dots,\underline{a}_{i-1},\underline{b},\underline{a}_{i+1},\dots,\underline{a}_{n})}{\det(A)}
$$
Where:
$$
A=\begin{pmatrix}
\underline{a}_{1}&\underline{a}_{2}&\dots&\underline{a}_{n}
\end{pmatrix}
$$
Where each $\underline{a}_{i}$ are column [[Vectors|vectors]]
## Proof
$A\underline{x}=\underline{b}$, so, using what we know about the [[Adjoint Matrix|adjoint matrix]],
$$
\underline{x}=A^{-1}\underline{b}=\frac{1}{\det(A)}\text{Adj}(A)\underline{b}
$$
$$
\implies x_{i}=\frac{1}{\det(A)}\sum_{ k=1} ^{ n}  \text{Adj}(A)_{ik}b_{k}=\frac{1}{\det(A)}\sum_{ k=1} ^{ n}  (-1)^{i+k}b_{k}\det(A_{k,i})
$$
$$
=\frac{\det(\underline{a}_{1},\dots,\underline{a}_{i-1},\underline{b},\underline{a}_{i+1},\dots,\underline{a}_{n})}{\det(A)}
$$
We get the numerator by performing the expansion of $\det$ along the $i$th column

#Mathematics #LinAlg #Theorem 