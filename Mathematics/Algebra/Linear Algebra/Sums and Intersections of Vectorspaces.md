Suppose $V$ is a [[Vectorspaces|vectorspace]], and $U,W\subseteq V$ are [[Subspaces|subspaces]], then
$$
U+W:=\{ \underline{u}+\underline{w}\mid \underline{u}\in U,\underline{w}\in W \}\subseteq V
$$
One can think of the sum as the [[Linear Span|span]] of the union; it is the smallest subspace of $V$ containing $U$ and $W$
$$
U\cap W:=\{ \underline{u}\in V\mid \underline{u}\in U,\underline{u}\in W \}\subseteq V
$$
## Proof
yeh
## Example
Consider two planes $\Pi_{1},\Pi_{2}\in\mathbb{R}^{3}$ through the origin, $\Pi_{1}\cap \Pi_{2}=L$ which is a $\hspace{0pt}1$ dimensional line, $\Pi_{1}+\Pi_{2}=\mathbb{R}^{3}$, which is three-dimensional space. Note that each plane is two-dimensional and the sum of their two dimensions is the sum of the dimensions of the intersection and the sum; $2+2=1+3$
## Proposition
Suppose $U,W\subseteq V$ are finite dimensional subspaces, then $U\cap W$ and $U+W$ are also finite dimensional, and
$$
\dim(U)+\dim(W)=\dim(U+W)+\dim(U\cap W)
$$
### Proof
First note that $U\cap W\subseteq U$ and $U$ is finite dimensional, therefore $U\cap W$ is finite dimensional
Let $\{ \underline{v}_{1},\dots,\underline{v}_{k} \}$ be a basis for $U\cap W$, extend this to a basis $\{ \underline{v}_{1},\dots,\underline{v}_{k},\underline{u}_{1},\dots,\underline{u}_{l} \}$ of $U$
and to a basis of $W$; $\{ \underline{v}_{1},\dots,\underline{v}_{k},\underline{w}_{1},\dots,\underline{w}_{m} \}$
Claim:
$$
B=\{ \underline{v}_{1},\dots,\underline{v}_{k},\underline{u}_{1},\dots,\underline{u}_{l},\underline{w}_{1},\dots,\underline{w}_{m} \}
$$
is a basis for $U+W$, so 
$$
\dim(U+W)+\dim(U\cap W)=(k+l+m)+k=(k+l)+(k+m)=\dim(U)+\dim(W)
$$
Certainly $B$ spans $U+W$, is $B$ linearly independent??
Suppose
$$
\lambda_{1}\underline{v}_{1}+\dots+\lambda_{k}\underline{v}_{k}+\mu_{1}\underline{u}_{1}+\dots+\mu_{l}\underline{u}_{l}+\eta_{1}\underline{w}_{1}+\dots+\eta_{m}\underline{w}_{m}=\underline{0}
$$
So we have
$$
\underbrace{ \lambda_{1}\underline{v}_{1}+\dots+\lambda_{k}\underline{v}_{k}+\mu_{1}\underline{u}_{1}+\dots+\mu_{l}\underline{u}_{l} }_{ \in U }=\underbrace{ -(\eta_{1}\underline{w}_{1}+\dots+\eta_{m}\underline{w}_{m}) }_{ \in W }\in U\cap W
$$
So 
$$
-(\eta_{1}\underline{w}_{1}+\dots+\eta_{m}\underline{w}_{})=\lambda_{1}'\underline{v}_{1}+\dots+\lambda_{k}'\underline{v}_{k}
$$
$$
\implies \lambda_{1}'\underline{v}_{1}+\dots+\lambda_{k}'\underline{v}_{k}+\eta_{1}\underline{w}_{1}+\dots+\eta_{m}\underline{w}_{m}=\underline{0}
$$
But this is is a basis for $W$, so since they are linearly independent, so $\lambda_{1}'=\dots=\lambda_{k}'=\eta_{1}=\dots=\eta_{m}=0$
So the original linear combination becomes:
$$
\lambda_{1}\underline{v}_{1}+\dots+\lambda_{k}\underline{v}_{k}+\mu_{1}\underline{u}_{1}+\dots \mu_{l}\underline{u}_{l}=\underline{0}
$$
Hence $\lambda_{1}=\dots=\lambda_{k}=\mu_{1}=\dots=\mu_{l}=0$
## Example
Consider $V=M_{2}(\mathbb{R})$, $U,L\subseteq V$:
$$
U=\left\{  \begin{pmatrix}
a&b\\0&d
\end{pmatrix}\mid a,b,d\in \mathbb{R}  \right\}\text{ (upper triangular)}
$$
$$
L=\left\{  \begin{pmatrix}
a&0\\c&d
\end{pmatrix}\mid a,c,d\in \mathbb{R}  \right\}\text{ (lower triangular)}
$$
$$
D=U\cap L = \left\{   \begin{pmatrix}
a&0\\0&d
\end{pmatrix}\mid a,d\in \mathbb{R}  \right\}\text{ (diagonal)}
$$
These are each subspaces of $V$, with bases as follows;
For $U$:
$$
\left\{  \begin{pmatrix}
1&0\\0&0
\end{pmatrix},\begin{pmatrix}
0&1\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix} \right\}
$$
For $L$:
$$
\left\{  \begin{pmatrix}
1&0\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\1&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix}  \right\}
$$
For $D$:
$$
\left\{  \begin{pmatrix}
1&0\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix}  \right\}
$$
So $\dim(U)=3$, $\dim(L)=3$, $\dim(U\cap L)=\dim(D)=2$, $\dim(U+L)=3+3-2=4$, so $U_{L}=M_{2}(\mathbb{R})$
## Direct Sums
Suppose $U,W\subseteq V$ are subspaces that satisfy $U+W=V$, $U\cap W=0=\{ \underline{0} \}$, then we call $V$ the 'direct sum' of $U$  and $W$, and write
$$
V=U \oplus W
$$
## Proposition
If $V$ is finite dimensional, and $U,W\subseteq V$ are subspaces, then the following are pairwise equivalent:
1. $V=U\oplus W$
2. If $\{ \underline{u}_{1},\dots,\underline{u}_{l} \},\{ \underline{w}_{1},\dots,\underline{w}_{k} \}$ are bases for $U$ and $W$ respectively, then $\{ \underline{u}_{1},\dots,\underline{u}_{l},\underline{w}_{1},\dots,\underline{w}_{k} \}$ is a basis for $V$
3. $V=U+W$ and $\dim(V)=\dim(U)+\dim(W)$
4. Every $\underline{v}\in V$ can be written uniquely as $\underline{v}=\underline{u}+\underline{w}$ for some unique choice of $\underline{u}\in U,\underline{w}\in W$

### Proof
$1\iff2\iff 3$ follows from the proposition above, and $1 \iff 4$ is on a problem sheet :(
### Exapmle
$V=M_{n}(\mathbb{R})$, $S=\{ A\in V \mid A^{\top}=A \}$, $T=\{ A\in V\mid A^{\top} = -A \}$
$S$ is the $n\times n$ symmetric matrices, $T$ is the $n\times n$ antisymmetric matrices
$S,T\subseteq V$ are subspaces, also $V=S\oplus T$
#### Proof
Check definition:
If $A\in V$, then 
$$
A=\underbrace{ \frac{1}{2}(A+A^{\top}) }_{ \in S }+\underbrace{ \frac{1}{2}(A-A^{\top}) }_{ \in T }
$$
As:
$$
\left( \frac{1}{2}(A+A^{\top}) \right)^{\top}=\frac{1}{2}(A^{\top}+(A^{\top})^{\top})=\frac{1}{2}(A^{\top}+A)
$$
and
$$
\left( \frac{1}{2}(A-A^{\top}) \right)^{\top}=\frac{1}{2}(A^{\top}-(A^{\top})^{\top})=\frac{1}{2}(A^{\top}-A)=-\frac{1}{2}(A-A^{\top})
$$
Suppse $A\in S\cap T$, then $A=A^{\top}=-A$, so $ZA=0$

#Mathematics #LinAlg #Definition #Theorem 