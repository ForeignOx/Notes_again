## Definition
Let [[Sets|$S$]] be a fixed [[Domain|domain]], and let $\mathfrak{F}$ be a family of [[Subsets|subsets]] of $S$
The family $\mathfrak{F}$ is disjoint if distinct sets in $\mathfrak{F}$ have no elements in common, i.e. if
$$
(\forall X,Y^{\in  \mathfrak{F}})(X\neq Y\implies X\cap Y=\emptyset)
$$
For an [[Sets of Indices|indexed]] family $\left\{ A_{i} \right\}_{i \in I}$, the condition becomes
$$
i\neq j\implies A_{i}\cap A_{j}=\emptyset
$$
If $\mathfrak{F}=\left\{A,B \right\}$, we simply say that $A$ and $B$ are disjoint
## Useful Identities
Given[[Functions| $f:U\to V$]] and an indexed family $\left\{ B_{i} \right\}$ of subsets of $V$, we have the following:
$$
f^{-1}\left( \bigcup_{i}B_{i} \right)=\bigcup_{i}f^{-1}(B_{i})
$$
$$
 f^{-1}\left( \bigcap_{i}B_{i} \right)=\bigcap_{i}f^{-1}(B_{i})
$$
And, for a single set $B\subseteq V$,
$$
f^{-1}(B')=(f^{-1}(B))'
$$
For example,
$$
x\in  f^{-1}\left( \bigcap_{i}B_{i} \right) \iff f(x)\in  \bigcap_{i}B_{i} \iff (\forall i)(f(x)\in  B_{i})
$$
$$
 \iff (\forall i)(x\in  f^{-1}(B_{i})) \iff x\in \bigcap_{i}f^{-1}(B_{i})
$$
The first, but not the other two of the three identities above when $f$ is replaced by any [[Relations|relation]] $R$
It follows from the commutative law for [[Proposition|quantifiers]]; $(\exists x)(\exists y)A \iff(\exists y)(\exists x)A$
The second identity fails for a general $R$ because $(\exists x)(\forall y)$ and $(\forall y)(\exists x)$ have different meanings



#Mathematics #Set #Definition