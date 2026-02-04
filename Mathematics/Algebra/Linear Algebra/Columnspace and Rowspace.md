If [[Matrices|$A\in M_{n\times k}(\mathbb{R})$]], then
## Columnspaces
The columnspace of $A$ is the [[Linear Span|span]] inside $\mathbb{R}^{n}$ of the columns of the matrix $A$, i.e. if
$$
A=\begin{pmatrix}
\underline{u}_{1}&\dots&\underline{u}_{k}
\end{pmatrix}
$$
Then $\text{columnspace}(A)=\text{span}< \underline{u}_{1},\dots \underline{u}_{k} >\subseteq \mathbb{R}^{n}$
Another way of thinking about this is that $\text{columnspace(A)}=\{ A\underline{\lambda}\mid\lambda \in\mathbb{R}^{k} \}\subseteq \mathbb{R}^{n}$
## Columnrank
The columnrank of $A$ is the [[Dimension|dimension]] of the columnspace
## Rowspaces
The rowspace of $A$ is the span inside $\mathbb{R}^{n}$ of the rows of the matrix $A$, so it is a subspace of $\mathbb{R}^k$, more honestly, it's the columnspace of $A^{t}$
$$
A=\begin{pmatrix}
\underline{u}_{1}\\\vdots\\\underline{u}_{k}
\end{pmatrix}
$$
Then $\text{rowspace}(A)=\text{span}< \underline{u}_{1},\dots \underline{u}_{k} >\subseteq \mathbb{R}^{k}$
## Rowrank
The rowrank of $A$ is the dimension of the rowspace
## Lemma
Suppose $\{ \underline{v}_{1},\dots,\underline{v}_{r} \}\in\mathbb{R}^{n}$ is a [[Linear Independence|linearly independnet]] [[Subsets|subset]], and let $P\in M_{n}(\mathbb{R})$ be an [[Matrix Inverses|invertible]] matrix
Then $\{ P\underline{v}_{1},\dots,P\underline{v}_{r} \}\subseteq \mathbb{R}^{n}$ is also linearly independent
### Proof
Suppose $\lambda_{1}P\underline{v}_{1}+\dots+\lambda_{r}P\underline{v}_{r}= \underline{0}$, we want to show all $\lambda=0$, so we start by left multiplying by $P ^{-1}$
$$
P(\lambda_{1}\underline{v}_{1}+\dots+\lambda_{r}\underline{v}_{r})=\underline{0}
$$
$$
\implies P ^{-1}P(\lambda_{1}\underline{v}_{1}+\dots+\lambda_{r}\underline{v}_{r})=P ^{-1}(\underline{0})
$$
$$
\implies \lambda_{1}\underline{v}_{1}+\dots+\lambda_{r}\underline{v}_{r}= \underline{0}
$$
So since $\{ \underline{v}_{1},\dots,\underline{v}_{r} \}$ is linearly independent, each $\lambda_{i}=0$
## Proposition
Let $A\in M_{m\times n}(\mathbb{R})$ and let $P \in M_{n}(\mathbb{R})$ be invertible, then $A$ and $PA$ have the same colrank, rowrank and nullity
- $A$ and $PA$ have the same rowspace
- $A$ and $PA$ have the same colrank
- $A$ and $PA$ have the same nullspace
### Proof
Since invertible matrices are the product of elementary matrices, it suffices to prove this for $P=E$, an elementary matrix
Each row of $EA$ is a [[Linear Combinations|linear combination]] of the rows of $A$, since $EA$ differs from $A$ by an $ERO$, so we certainly have $\text{rowspace}(EA)\subseteq \text{rowspace}(A)$, but also $A=E ^{-1}(EA)$, where $E^{-1}$ is elementary, so $\text{rowspace}(A)\subseteq \text{rowspace}(EA)$ as well

Write $U=\text{colspace}(A)=\{ A \underline{x}\mid \underline{x} \in\mathbb{R}^{k} \}\subseteq \mathbb{R}^{n}$, so $\text{colspace}(PA)=\{ PA\underline{x}\mid \underline{x} \in \mathbb{R}^{k} \}\subseteq \mathbb{R}^{n}$, so if we have for some $\underline{x}$
$$
\underline{u}\in U\iff \underline{u}=A\underline{x}
$$
$$
\iff P\underline{u}=PA\underline{x}
$$
Since $P$ is invertible
$$
\iff P\underline{u}\in \text{colspace}(PA)
$$
Hence $\text{colspace}(PA)=PU:=\{ P\underline{u}\mid \underline{u}\in U \}$, and we want to show whether $\text{dim}(U)=\dim(PU)$
Let $\{ \underline{v}_{1},\dots,\underline{v}_{r} \}\in\mathbb{R}^{n}$ be a [[Basis|basis]] for $U$, (so $\dim(U)=r$), we are claiming that $\{ P\underline{v}_{1},\dots,P\underline{v}_{r} \}\subseteq \mathbb{R}^{n}$ is a basis for $PU$ (so $\dim(PU)=r$)
$\{ P\underline{v}_{1},\dots,P\underline{v}_{r} \}$ is independent by the Lemma above. If $\underline{v}\in PU$, then $\underline{v}=P\underline{u}$ for some $\underline{u}=\lambda_{1}\underline{v}_{1}+\dots+\lambda_{r}\underline{v}_{r}\in U$, so
$$
\underline{v}=P(\lambda_{1}\underline{v}_{1}+\dots+\lambda _{r}\underline{v}_{r})=\lambda_{1}P\underline{v}_{1}+\dots+\lambda_{r}P\underline{v}_{r}
$$
So it is spanning, so overall a basis :)

Suppose that $\underline{u}\in\mathbb{R}^{k}$, then $A\underline{u}= \underline{0}\iff PA \underline{u}=\underline{0}$, so $\text{nullspace}(A)=\text{nullspace}(PA)$
## $\text{rowrank}(A)=\text{colrank}(A)$
### Corollary/Definition
We define the rank of a matrix $A\in M_{n\times k}(\mathbb{R})$, by $\text{rk}(A):=\text{rowrank}(A)=\text{colrank}(A)$
By the proposition, we can consider the [[Row Reduced Echelon Form|RREF]] of $A$, $A'\in M_{n\times k`}(\mathbb{R})$
If there are $m$ rows witha leading $\hspace{0pt}1$, and $n-m$ zero rows, so:
$$
\text{colspace}(A')=\text{span}< \underline{e}_{1},\dots,\underline{e}_{m} > \in \mathbb{R}^{n}
$$
$$
\implies \text{colrank}(A')=m
$$
$$
\text{rowspace}(A')=\text{span}< \underline{r}_{1},\dots \underline{r}_{m} > \subseteq \mathbb{R}^{k}
$$
Where $\underline{r}_{i}$ is the $i$th row of $A'$, where we have discarded columns rows of zeros, so we only have $m$ of them, but note $\{ \underline{r}_{1},\dots,\underline{r}_{m} \}$ is linearly independent by looking at the coordinates of the leading 1's, so $\text{rowrank}(A')=m$

#Mathematics #LinAlg #Definition #Theorem 