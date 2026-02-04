$\mathbb{R}^n$ is the [[Vectorspaces|vectorspace]] of the [[Real Numbers|real numbers]]
## Definition
$n$-dimensional real space
$$
\mathbb{R}^n:=\left\{  \underline{x}=\begin{pmatrix}
x_{1}\\x_{2}\\\vdots\\ x_{n}
\end{pmatrix}\middle| x_{i}\in \mathbb{R},0\leq i\leq n  \right\}
$$
There are two operations on $\mathbb{R}^n$
$\hspace{0pt}1$. Vector addition
$$
\mathbb{R}^n\times \mathbb{R}^n\to \mathbb{R}^n
$$
$$
(\underline{v},\underline{w})\mapsto  \underline{v}+\underline{w}
$$
$$
\underline{v}+\underline{w}=\begin{pmatrix}
v_{1}\\v_{2}\\\vdots\\v_{n}
\end{pmatrix}
+
\begin{pmatrix}
w_{1}\\w_{2}\\\vdots\\w_{n}
\end{pmatrix}=
\begin{pmatrix}
v_{1}+w_{1}\\v_{2}+w_{2}\\\vdots\\v_{n}+w_{n}
\end{pmatrix}
$$
$\hspace{0pt}2$. Scalar multiplication
$$
\mathbb{R}\times\mathbb{R}^n\to \mathbb{R}^n
$$
$$
(\lambda,\underline{v})\mapsto\lambda \underline{v}
$$
$$
\lambda \underline{v}=\lambda \begin{pmatrix}
v_{1}\\v_{2}\\\vdots\\v_{n}
\end{pmatrix}=\begin{pmatrix}
\lambda v_{1}\\\lambda v_{2}\\\vdots\\\lambda v_{n}
\end{pmatrix}
$$
These operations satisfy the axioms of a real vectorspace
The vectorspace $\mathbb{R}^n$ quite obviously satisfies the vectorspace axioms, especially when you consider:
$$
-\underline{v}=(-1)\begin{pmatrix}
v_{1}\\v_{2}\\\vdots\\v_{n}
\end{pmatrix}=
\begin{pmatrix}
-v_{1}\\-v_{2}\\\vdots\\-v_{n}
\end{pmatrix}
$$
## Is $\mathbb{R}=\mathbb{R}^1$?
There is a very obvious bijection between the two [[Sets|Sets]], but the set $\mathbb{R}^1$ technically has fewer operations soooooooooooooooooooooo nuh uh. except that other guy said yuh uh sooooooo idk \shrugh
## Basis?
$\{ e_{1},\dots,e_{n}q\subseteq \mathbb{R}^{n}  \}\subseteq \mathbb{R}^{n}$ is the standard base, other bases exist, for example, we shaw that:
$$
\left\{  
\begin{pmatrix}
1\\0
\end{pmatrix},\begin{pmatrix}
1\\1
\end{pmatrix}
 \right\}\in \mathbb{R}^{2}
$$

Is a spanning set for $\mathbb{R}^{2}$, since $\text{dim}(\mathbb{R}^{2})=2$, tiis $B$ is in vact a basis for $\mathbb{R}^{2}$

## Theorem
Suppose $\{ \underline{u}_{1},\dots,\underline{u}_{r} \}\subseteq \mathbb{R}^{n}$, then
If $r>n$, then $\{ \underline{u}_{1},\dots,\underline{u}_{r} \}$ is not [[Linear Independence|linearly independent]]
If $r<n$, then $\{ \underline{u}_{1},\dots,\underline{u}_{r} \}$ is not [[Linear Span|spanning]]
Suppose $r=n$, we have that $\{ \underline{u}_{1},\dots,\underline{u}_{r} \}$ is a [[Basis|Basis]] iff:
$$
A=\begin{pmatrix}
\underline{u}_{1}&\underline{u}_{2}&\dots&\underline{u}_{n}
\end{pmatrix}\in M_{n}(\mathbb{R})
$$
Is non-[[Matrix Inverses|singular]] iff [[Determinants|$\det(A)\neq 0$]]
### Proof
The first two are just the previous theorem
The third one: $\{ \underline{u}_{1},\dots,\underline{u}_{r} \}$ is a basis iff $\{ \underline{u}_{1},\dots,\underline{u}_{r} \}$ is linearly independent (again by previous theorem) iff
$$
\lambda_{1}\underline{u}_{1}+\dots+\lambda_{n}\underline{u}_{n}\implies\lambda_{1}+\dots+\lambda_{n}\underline{u}_{n}=\underline{0}\iff \underline{\lambda}=\underline{0}
$$
iff $A$ is invertible; $\det(A)\neq 0$



#Mathematics #LinAlg #Definition