## Definition
Let $X$ be a [[Topology|topological space]], we call $X$ a Hausdorff space if whenever $x,y\in x$ with $x\neq y$ then there exist open sets $U,V\subseteq X$ with $x\in U, y\in V,U\cap V=\emptyset$
## Lemma
Let $X$ be a topological space that is [[Metric Spaces|metrizable]], then $X$ is Hausdorff
### Proof
Let $d$ be a metric on $X$ inducing the topology. Then for $x,y\in X$ with $x\neq y$, let $r=d(x,y)>0$, take $U=B\left( x; \frac{r}{2} \right)$ and $V=B\left( y; \frac{r}{2} \right)$, then these are open and we have $x\in U,y\in V$
Assume that $z\in U\cap V$, then $d(z,x)<\frac{r}{2}$ and $d(z,y)<\frac{r}{2}$, so by trangle inequality
$$
r=d(x,y)\leq d(x,z)+d(y,z)<\frac{r}{2}+\frac{r}{2}=r
$$
Giving a contradiction.
## Example
Let $X$ be a topological space with topology $\mathcal{T}$, and $A\subseteq X$. We can define a topology $\mathcal{T}_{A}$ on $A$ by
$$
\mathcal{T}_{A}=\left\{ V\subseteq A:\middle|: \exists U\in  T:V=U\cap A \right\}
$$
We can check that $A=X\cap A$ and $\emptyset=\emptyset\cap A$ are in $\mathcal{T}_{A}$, for unions and intersections, we only need to observe that
$$
\bigcup_{i\in I}(U_{i}\cap A)=\left( \bigcup_{i\in I}U_{i} \right)\cap A
$$
And
$$
\bigcap_{i\in I}(U_{i}\cap A)=\left( \bigcap_{i\in I}U_{i} \right)\cap A
$$
For any collection of subsets of $X$. The resulting topology is called the induced topology or the subspace topology on $A$
Subexammple:
Let $X=\mathbb{R},A\subseteq X, A=[-1,1]$, then $V\subseteq A$ being open means that $V=U\cap A$ is open
So $(0,1]$ is open in $[-1,1]$ by taking $V=(0,2)$ (which is open in $\mathbb{R}$)
