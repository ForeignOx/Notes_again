A non-zero [[Vectors|vector]] $\underline{v}$ is an eigenvector of $A$ with eigenvalue $\lambda \in\mathbb{C}$ if
$$
A\underline{v}=\lambda \underline{v}
$$
Note if $\underline{v}$ is an eigenvector, so is $c\underline{v},\forall c\neq 0$ with the same eigenalue. Note $\underline{0}$ always solves $A \underline{0}=\lambda \underline{0}$ 

To find eigenvectors for a given [[Eigenvalues|eigenvalue]] $\lambda$ for a square matrix, substitute $\lambda$ into:
$$
\begin{pmatrix}
a_{11}-\lambda && a_{12} && \dots && a_{1n} \\
a_{21} && a_{22}-\lambda && \dots && a_{2n} \\
\vdots && \vdots && \ddots && \vdots \\
a_{n1} && a_{n 2} && \dots && a_{nn}-\lambda
\end{pmatrix}
\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}=\begin{pmatrix}
0\\0\\\vdots\\0
\end{pmatrix}
$$
which will generate a set of linear equations, and any values of $x_{1}, x_{2}, \dots, x_{n}$ that satisfies every linear equation will be an eigenvector for $\lambda$ if there are any free parameters, then that value of $x_{k}$ will be 0 

#Mathematics #LinAlg #Definition 