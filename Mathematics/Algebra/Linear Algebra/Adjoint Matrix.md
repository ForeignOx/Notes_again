Let [[Matrices|$A \in M_{n}(\mathbb{R})$]], we define the adjoint matrix $\text{Adj}(A)\in M_{n}(\mathbb{R})$ by:
$$
(\text{Adj}(A))_{ij}:=(-1)^{i+j}\det(A_{j,i})
$$
Where $A_{j,i}$ is the $(j,i)$th [[Matrix Minor|minor]] of $A$ (you get $A_{j,i}$ by deleting the $j$th row and the $i$th column of $A$), and $(-1)^{i+j}\det(A_{j,i})$ is the [[Determinants|signed cofactor]] of $A$
The adjoint of $A$ is the [[Transpose|transpose]] of the matrix of signed cofactors 
## Example
$$
\text{Adj}\begin{pmatrix}
a&b\\c&d
\end{pmatrix}=\begin{pmatrix}
d&-c\\-b&a
\end{pmatrix}^{t}=\begin{pmatrix}
d&-b\\-c&a
\end{pmatrix}
$$
This looks suspiciously like the [[Matrix Inverses|inverse]] of a matrix....
## Proposition
Suppose $A\in M_{n}(\mathbb{R})$, then:
$$
A\text{Adj}(A)=\det(A)I_{n}=\text{Adj}(A)A
$$
### Proof
$$
(A\text{Adj}(A))_{rs}=\sum_{k=1}^{n}a_{rk}(\text{Adj}(A))_{ks}=\sum_{ k=1} ^{ n} (-1)^{k+s} a_{rk}\det(A_{s,k})
$$
We now consider the two cases; the diagonal entries which need to be $\det(A)$, and the others that need to be 0
Case 1: $r=s$, we get:
$$
\sum_{ k=1} ^{ n}(-1)^{k+s}a_{sk}\det(A_{s,k})
$$
Which is the definition of $\det(A)$ expanded along row $s$
Case 2: $r\neq s$
$$
\sum_{ k=1} ^{ n}  (-1)^{k+s}a_{rk}\det(A_{s,k})
$$
This is the expansion along row $s$ of a matrix $B$ obtained from $A$ by replacing its $s$th row with its $r$th row:
$$
A=\begin{pmatrix}
\underline{a}_{1}\\\vdots\\\underline{a}_{r}\\\vdots\\\underline{a}_{s}\\\vdots\\\underline{a}_{n}
\end{pmatrix},B=\begin{pmatrix}
\underline{a}_{1}\\\vdots\\\underline{a}_{r}\\\vdots\\\underline{a}_{r}\\\vdots\\\underline{a}_{n}
\end{pmatrix}
$$
And the determinant of $B$ must equal $\hspace{0pt}0$, since it has two equal rows
### Corollary
If $\det(A)\neq 0$, then
$$
A^{-1}=\frac{1}{\det (A)}\text{Adj}(A)
$$
Which is proved automatically by dividing by $\det (A)$
This is useful, not for calculations, but is interesting that you can express the inverse of $A$ as a polynomial of the entries of $A$

#Mathematics #LinAlg #Definition