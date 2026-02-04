Eigenvalues are associated with [[Eigenvectors]], and represent a special set of scalar values associated with the system of linear equations such that, for a matrix $A$: 
$$
A \underline{x}=\lambda \underline{x}
$$
Where $\lambda$ is an eigenvalue of $A$, and $\underline{x}$ is an eigenvector of $A$ corresponding to $\lambda$
## Square Matrices
To calculate eigenvalues for an $n\times n$ square matrix, we use the following method:
If A has an invariant line through the origin, then for some non-zero eigenvector, we can say 
$$
\begin{pmatrix}
a_{11} && a_{12} && \dots && a_{1n} \\
a_{21} && a_{22} && \dots && a_{2n} \\
\vdots && \vdots && \ddots && \vdots \\
a_{n1} && a_{n 2} && \dots && a_{nn}
\end{pmatrix}
\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}=\lambda\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}=\begin{pmatrix}
\lambda && 0&& \dots&&0 \\
0&&\lambda&&\dots &&0 \\
\vdots && \vdots && \lambda && \vdots \\
0&&0&&\dots&&\lambda
\end{pmatrix}\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}
$$
$$
\implies \begin{pmatrix}
a_{11} && a_{12} && \dots && a_{1n} \\
a_{21} && a_{22} && \dots && a_{2n} \\
\vdots && \vdots && \ddots && \vdots \\
a_{n1} && a_{n 2} && \dots && a_{nn}
\end{pmatrix}
\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}-\begin{pmatrix}
\lambda && 0&& \dots&&0 \\
0&&\lambda&&\dots &&0 \\
\vdots && \vdots && \lambda && \vdots \\
0&&0&&\dots&&\lambda
\end{pmatrix}\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}=\begin{pmatrix}
0\\0\\\vdots\\0
\end{pmatrix}
$$
By distributivity:
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
Which means we have $(A-\lambda I)$ multiplying by a non-zero vector and getting the zero vector, meaning that $A-\lambda I$ is singular, if it weren't, we could let $B=A-\lambda I$, which would have an inverse $B^{-1}$, so
$$
B\underline{x}=\underline{0}
$$
$$
\implies B^{-1}B\underline{x}=B^{-1}\underline{0}
$$
$$
 \implies\underline{x}=\underline{0}
$$
But $\underline{x}\neq \underline{0}$
## Characteristic Polynomial
$p_{A}(t)=\det(A-tI)$ is a polynomial in $t$ since the calculation of [[Determinants|determinant]] causes the linear terms to be multiplied with each other. For example consider 
$$
a=\begin{pmatrix}
a&b\\c&d
\end{pmatrix}
$$
$$
\implies \det(A-tI)=\det \begin{pmatrix}
a-t&b\\c&d-t
\end{pmatrix}=(a-t)(d-t)-bc
$$
$$
= t^{2}-(a+d)t+ad-bc
$$
It is known as the charactersitic polynomial of $A$. If $A$ is $N\times N$, it's a polynomial of degree $N$, and contains information about eigenvalues. In fact $\lambda$ is an eigenvalue of $A\iff\lambda$ is a root of $p_{A}(t)$. We have derived the one of the directions above, let's check the other way: if $t^{*}\in\mathbb{C}$ is a root of $p_{A}(t)\implies \det(A-t^{*}I)=0\implies A-t^{*}I$ is singular, so there is at least one $\underline{v}\neq  \underline{0}$ such that $(a-t^{*}I)\underline{v}=\underline{0}\implies A\underline{v}=t^{*}\underline{v}\implies t^{*}$ is an eigenvalue
## Multiplicity of the Eigenvalue
Any degree $N$ polynomial $p(t)$ can be written as $p(t)=a(t-\lambda_{1})^{k_{1}}(t-\lambda_{2})^{k_{2}}\dots(t-\lambda_{p})^{k_{p}}$ where $a\neq 0$ and $\lambda_{1},\dots,\lambda_{p}$ are the distinct roots of $p(t)$, $\lambda_{i}\in\mathbb{C},\lambda_{i}\neq\lambda_{j}$ if $i\neq j$, $k_{i}\in\mathbb{N},1\leq k_{i}\leq N,\sum_{i=1}^{p}k_{i}=N$. Clearly $p(\lambda_{i})=0$
### Algebraic Multiplicity
The algebraic multiplicity of the eigenvalue $\lambda_{i}$ is $k_{i}$. Suppose we have an eigenvalue $\lambda$ with algebraic multiplicity $k_{\lambda}$, then$p_{A}(t)=(t-\lambda)^{k_{\lambda}}Q(t)$ with $Q(\lambda)\neq 0$ and degree of $Q=N-k_{\lambda}$
### Geometric Multiplicity
There are $p_{\lambda}$ [[Linear Independence|linearly independendent]] eigenvectors of $A$ with eigenvalue $\lambda$, where $1\leq p_{\lambda}\leq k_{\lambda}$, $p_{\lambda}$ is called the geometric multiplicity of $\lambda$ and is defined to be the [[Dimension|dimension]] of the [[Eigenspaces|eigenspace]]
### Algebraic Multiplicity $\geq$ Geometric Multiplicity
For every eigenvalue $\lambda$, $k_{\lambda}\geq p_{\lambda}$
#### Proof
Suppose geometric multiplicity of $\lambda$ is $p$ then let $\underline{v}_{1},\dots,\underline{v}_{p}$ be independent eigenvectors with this eigenvalue:
$$
A\underline{v}_{i}=\lambda \underline{v}_{i}
$$
For $i=1\dots p$
Complete the [[Basis|Basis]] with $\underline{w}_{1},\dots,\underline{w}_{n-p}$ (if $A$ is $n\times n$), so $\left\{ \underline{v}_{1},\dots,\underline{v}_{p},\underline{w}_{1},\dots,\underline{w}_{n-p} \right\}$ spans $\mathbb{R}^{n}$. In this basis,
![[Eigenvalues 2025-01-30 10.12.55.excalidraw]]
So we calculate the determinant columnwise, so 
$$
\det(A-tI)=(\lambda-t)^{p}\det(C-tI)
$$
So we have our result (?) see notes to consolidate perchance

## Geometrical Interpretations
### Reflection
Consider a $3\times{3}$ matrix $M$ that represents a reflection, we know that $\det M=-1$ as orientation is not preserved and volume doesn\'t change. We know its eigenvalues must be 1, 1 and -1 as there is an eigenplane which is unaffected by the transformation and then the other is for the invariant lines which represent the reflection perpendicular to the plane. To find the plane of reflection of a matrix, solve
$$
M\underline{x}=1\underline{x}\implies(M-I)\underline{x}=\underline{0}
$$
### Rotation
For a $2\times 2$ rotation matrix, the two eigenvalues will be real for $0^{\circ}$ or $180^{\circ}$, for $0^{\circ}$, they will be 1 and 1, for $180^{\circ}$, they will be -1 and -1, and for both, the entire plane will be the set of eigenvectors
For a $3\times 3$ rotation matrix, one eigenvalue will be 1 and the other two will be complex, the eigenvectors will be a zero vector with a non-zero value for the axis of rotation, so for example for a rotation about the $z-$axis, an eigenvector would be:
$$
\begin{pmatrix}
0\\0\\1
\end{pmatrix}
$$

#Mathematics #LinAlg #Definition #Theorem 