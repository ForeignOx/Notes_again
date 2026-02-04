A bilinear form $B$ on a [[Vectorspaces|real vectorspace]] $V$ is a mapping assigning to each pair of [[Vectors|vectors]] $\underline{u},\underline{v}\in V$ a [[Real Numbers|real number]] $B(\underline{u},\underline{v})$ 
$$
B:V\times V\to \mathbb{R}
$$
$$
\underline{u},\underline{v}\mapsto B(\underline{u},\underline{v})
$$
 satisfying the following for all $\underline{u},\underline{v},\underline{w}\in V$, and all $\lambda \in\mathbb{R}$:
 - $B(\underline{u}+\underline{v},\underline{w})=B(\underline{u},\underline{w})+B(\underline{v},\underline{w})$
 - $B(\underline{w},\underline{u}+\underline{v})=B(\underline{w},\underline{u})+B(\underline{w},\underline{v})$ 
 - $B(\lambda \underline{u},\underline{v})=B(\underline{u},\lambda \underline{v})=\lambda B(\underline{u},\underline{v})$ 
So it is [[Linear|linear]] in both its arguments
## Encoding with Matrices
We can always encode a bilinear form via a [[Matrices|matrix]]
You start by picking a [[Basis|basis]] $\left\{ \underline{v}_{1},\dots,\underline{v}_{n} \right\}$ of $V=\mathbb{R}^{n}$ and let $\underline{u}=x_{1}\underline{v}_{1}+x_{2}\underline{v}_{2}+\dots+x_{n}\underline{v}_{n}$, $\underline{v}=y_{1}\underline{v}_{1}+y_{2}\underline{v}_{2}+\dots+y_{n}\underline{v}_{n}$, then if $B$ is a real bilinear form, then
$$
B(\underline{u},\underline{v})=B\left( \sum_{i=1}^{n}x_{i}\underline{v}_{i},\sum_{j=1}^{n}y_{j}\underline{v}_{j} \right)
$$
$$
= \sum_{i=1}^{n}\sum_{j=1}^{n}B(x_{i}\underline{v}_{i},y_{j}\underline{v}_{j})
$$
$$
= \sum_{i=1}^{n}\sum_{j=1}^{n}x_{i}B(\underline{v}_{i},\underline{v}_{j})y_{j}
$$
Then define [[Functional Matrices|$A_{ij}=B(\underline{v}_{j},\underline{v}_{i})$]] (note the index order swap, this is a choice). This is called the matrix form of the bilinear form of $B$ in the basis $\left\{ \underline{v}_{i} \right\}$ 
If we think of $\left\{ x_{i} \right\}$ and $\left\{ y_{j} \right\}$ as components of column vecots $\underline{x}$ and $\underline{y}$, then our sum can be rewritten using the [[Transpose|transpose]]:
$$
B(\underline{u},\underline{v})=(A\underline{x})^{\top}\underline{y}=\underline{y}^{\top}A\underline{x}
$$
## Examples
Given the vectorspace $V\in\mathbb{R}^{n}$ with the [[Standard Basis Vectors|standard bases]], consider the operation $B:V\times V\to \mathbb{R}$, defined by
$$
B(\underline{u},\underline{v})=u_{1}v_{1}
$$
This is a bilinear transformation
Writing this using our matrix equation, we can write
$$
B(\underline{u},\underline{v})=\begin{pmatrix}
u_{1}&u_{2}&\dots&u_{n}
\end{pmatrix}\begin{pmatrix}
1&0&\dots&0\\0&0&\dots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&0&0
\end{pmatrix}\begin{pmatrix}
v_{1}\\v_{2}\\\vdots\\v_{n}
\end{pmatrix}=u_{1}v_{1}
$$
#Mathematics #LinAlg #Definition 