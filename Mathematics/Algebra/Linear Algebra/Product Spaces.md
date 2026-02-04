## Definition
If $W$ is a [[Vectorspaces|vectorspace]], and $A$ is an arbitrary [[Sets|set]], then the set [[Product Sets|$V=W^{A}$]] of all $W$-valued [[Functions|functions]] on $A$ is also a vectorspace, where addition is the natural addition of functions and scalar multiplication is as you'd expect:
$$
(f+g)(a)=f(a)+g(a)
$$
$$
 (xf)(a)=x(f(a))
$$
We can check all the axioms, (but I cba)
## Coordinates
As we have seen for [[Coordinate Functionals|coordinate functionals]], we denote $\pi_{i}$ to be evaluation at $i$ such that
$$
\pi_{i}(f)=f(i)
$$
Now, however, $\pi_{i}$ is vector valued as it is a mapping from $V\to W$, so we call it the $i$th coordinate projection
This map is also linear, in fact, the natural vector operations on $W^{A}$ are uniquely defined by the requirement that the projections $\pi_{i}$ all be linear
We call the value $f(j)=\pi_{j}(f)$ the $j$th coordinate of the vector $f$; this is a clear analogue of how we describe [[Vectorspace Rn|$\mathbb{R}^{n}$]], and we can see the similarity to the set $W^{\overline{n}}$ of all $n$-tuples
$$
\underline{\alpha}=\left( \alpha_{1},\dots,\alpha_{n} \right)  
$$
Of vectors in $W$; it is also designated $W^{n}$, and clearly $\alpha_{j}$ is the $j$th coordinate of the $n$-tuple $\underline{\alpha}$
## Products
There is no reason why we must use the same space $W$ at each index, as we did above, in face, if $W_{1},\dots,W_{n}$ are any $n$ vectorspaces, then the set of all $n$-tuples $\underline{\alpha}=(\alpha_{1},\dots,\alpha_{n})$ such that $\alpha_{j}\in W_{j}$ for $j\in\overline{n}$ is a vectrspace under the same definitions of the operations for the same reasons. That is, the [[Cartesian Product|cartesian product]]
$$
W=W_{1}\times W_{2}\times\dots \times W_{n}
$$
Is also a vectorspace of vector-valued functions
## Examples
Such finite products are very important, for example $\mathbb{R}^{n}$ is the product $\prod_{1}^{n}W_{i}$ with each $W_{i}=\mathbb{R}$, but $\mathbb{R}^{n}$ can also be considered $\mathbb{R}^{m}\times \mathbb{R}^{n-m}$, or even more generally 
$$
\mathbb{R}^{n}=\prod_{i=1}^{p}W_{i},W_{i}=\mathbb{R}^{m_{i}},\sum_{i=1}^{p}m_{i}=n
$$
However, the most important use of finite product spaces arises from the fact that the study of certain phenomena on a vectorspace $V$ may lead in a natural collection $\left\{ V_{i} \right\}_{1}^{n}$ of [[Subspaces|subspaces]] of $V$ such that $V$ is [[Isomorphisms|isomorphic]] to $\prod_{1}^{n}V_{i}$, then the extra structure that $V$ acquires when we regard it as such is used to study the phenomena in question. This comes up with [[Sums and Intersections of Vectorspaces|direct sums]] 
___
We can consider a general Cartesian product of vectorspaces, by considering $\left\{ W_{i}\mid i \in I \right\}$ is any [[Sets of Indices|indexed collection]] of vectorspaces, then the Cartesian product $\prod_{i\in I}W_{i}$ of these is defined to be the set of all functions $f$ with domain $I$ such that $f(i)\in W_{i}$ for all $i \in I$
For example, let $S$ be the unit sphere in $\mathbb{R}^{3}$: $S=\left\{ \underline{x}\mid \sum_{1}^{3}x_{i}^{2}=1 \right\}$, and for each point $\underline{x}$ on $S$, let $W_{\underline{x}}$ be the subspace of $\mathbb{R}^{3}$ tangent to $S$ at $\underline{x}$
By this, we mean the subspace ([[Planes|plane]] through the origin) parallel to the tangent plane, so that the translate $W_{\underline{x}}+\underline{x}$ is the tangent plane
A function $f$ in the product space $W=\prod_{\underline{x}\in S}W_{\underline{x}}$ is a function which assigns to each point $\underline{x}$ on $S$ a vector in $W_{\underline{x}}$, that s, a vector parallel to the tangent plane to $S$ at $\underline{x}$,
Such a function is called a vectorfield on $S$, thus, the product set $W$ is the set of all vectorfields on $S$, and $W$ itself is a vectorspace
Of course, the $j$th coordinate projection on $W=\prod_{i\in S}W_{i}$ is evaluation at $j$, $\pi_{j}(f)=f(j)$, and the natrual vector operations on $W$ are uniquely defined by the requirement that the coordinate projections all be linear
Thus $f+g$ must be that element of $W$ whose value at $j,\pi_{j}(f+g)$ is $\pi_{j}(f)+\pi_{j}(g)=f(j)+f(g)$ for all $j\in I$, and similarly for multiplication by scalars
## Theorem
The cartesian product of a collection of vectorspaces can be made into a vectorspace in exactly one way so that the coordinate projections are all linear
### Proof
With the vector operations determined as in the example above, the proofs of most of the vectorspace axioms hold, they didn't require that all the functions being added have all their values in the same space, but only that the values at a given domain element lie in the same space, so it is true