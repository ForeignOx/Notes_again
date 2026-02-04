If $V$ is a finite dimensional [[Vectorspaces|vectorspace]], we define its dimension, $\text{dim}(V)$ to be the [[Cardinality of Sets|cardinality]] of any [[Basis|basis]] of $V$
$V$ is finite-dimensional if it has a finite spanning set
## Examples
$\text{dim}(\mathbb{R}^{n})=n$, as $n=|\{ \underline{e}_{1},\dots,\underline{e}_{n} \}|$
___
$\text{dim}(\mathbb{R}[x]_{n})$ as a basis: $\{ 1,x,x^{2},\dots,x^{n} \}$ which has cardinality $n+1$ as we go through powers of $x$ from $\hspace{0pt}0$ to $n$
___
$\text{dim}(M_{m\times n}(\mathbb{R}))=mn$, as it has a basis: $\{ E^{ij}\mid 1\leq i\leq m,1\leq j\leq n \}$
___
Consider $U\subseteq \mathbb{R}[x]_{n}$, $U:=\{ p\in\mathbb{R}[x]_{n}\mid p(1)=0 \}$, this is a [[Subspaces|subspace]] (which we can check). Calculus tells us $p \in U\iff(x-1)|p$, so $U=\{ (x-1)q\mid q\in\mathbb{R}[x]_{n-1} \}$, so $U$ has a basis: 
$$
\{ (x-1),(x-1)x,\dots,(x-1)x^{n-1} \}
$$
Which we can check to be [[Linear Span|spanning]] and [[Linear Independence|linearly independent]], so $\text{dim}(U)=n$
___
$\text{sym}_{2}(\mathbb{R})\subseteq M_{2}(\mathbb{R})$ has basis:
$$
\left\{  \begin{pmatrix}
1&0\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix},\begin{pmatrix}
0&1\\1&0
\end{pmatrix}  \right\}
$$
Which we can check to be spanning and linearly indipendent, so $\text{dim}(\text{sim}_{2}(\mathbb{R}))=3$
## Theorem
Suppose that $V$ is a finite dimensional vectorspace, and that $U\in V$ is a subspace of $V$, then $U$ is also finite dimensional, $\text{dim}(U)\leq \text{dim}(V)$
### Proof
If $U$ were not finite dimensional, then it doesn't contain a finite basis, i.e. it doesn't contain any maximal linearly independent subset
Hence $U$ contains arbitrarily large linearly independent subsets, hence so does $V$, but any linealy independent subset of $V$. But any linearly indep;nendnt subset, since $V$ has a spanning set of $\text{dim}(V)$ elements, so we have a contradiction, thus $U$ is of finite dimension
Suppowe $\text{dim}(U)>\text{dim}(V)$, then $U$ contaisnsa basis for $U$ (and so $V$) contains a basis for $U$ of $\text{dim}(U)$ elements, but this is a linearly idependent subset with more elements than are spanning set given by a basis of $V$, giving us a contradiction
The other direction (iff):
Let $V\subseteq U$, let $A$ be a basis for $U$. If $B$ is not a basis for $B$, then it is not maximal linearly independnent subset of $V$, so then we can find a linearly independent subset of $U$, with
$$
\text{dim}(B)=\text{dim(U)}+1=\text{dim}(V)
$$
elements, but this has more elements than a basis
## Theorem
Let $V$ be a vectorspace, with dimension of $\text{dim}(V)=k$, let $S=\{ \underline{v}_{1},..,\underline{v}_{l} \}\subseteq V$
If $l>k$, then $S$ is not linearly independntm If $l<k$ then $S$ is not spanning
If $l=k$, then these statements are pairwise equivalent:
- $S$ is a basis for $V$
- $S$ is linearly independent
- $S$ is a spanning set for $V$
### Proof
Let there be $V$ containing a basis, hence a spanning set of $k$ elements, hence the second statement follows from steinitz
$V$ contains a basis, hence a linearly independnent set of $k$ elements, hence this follows from steinitz
Assume the second statement, $S$ must be a maximal linearly independent set since linearly independent sets have at most $k=l$ elements, then $S$ is  basis
$S$ must be a minimal spanning set since spanning sets have at least $k=l$ elements

#Mathematics #LinAlg #Definition 