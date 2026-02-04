## Law
So if we let [[Sets|$S$]] be a fixed [[Domain|domain]], and let $\mathfrak{F}$ be a family of [[Subsets|subsets]] of $S$
We often consider the family $\mathfrak{F}$ to be [[Sets of Indices|indexed]]. That is, we assume given a set $I$ and a [[Surjective Functions|surjective]] mapping $i \mapsto A_{i}$ from $I$ to $\mathfrak{F}$, so that $\mathfrak{F}=\left\{ A_{i}\mid i \in I\right\}$
The law of De Morgan states that the [[Set Complement|complement]] of an [[Intersection|intersection]] is the [[Union|union]] of the complements:
$$
\left( \bigcap _{i\in  I}A_{i} \right)'=\bigcup_{i\in  I}(A_{i}')
$$
This is an immediate consequence of the rule for [[Proposition#Negation of Quantifiers|negating quantifiers]] and the equivalence between 'not always in' and 'sometimes not in': 
$$
\sim (\forall i)(x\in  A_{i}) \iff(\exists i)(x\not\in  A_{i})
$$
Which says exactly that
$$
x\in \left( \bigcap_{i}A_{i} \right)' \iff x\in  \bigcup_{i}(A_{i}')
$$
If we set $B_{i}=A_{i}'$ and take complements again, we obtain the [[Duality|dual]] form
$$
\left( \bigcup_{i\in  I}B_{i} \right)' = \bigcap_{i \in  I}(B_{i}')
$$
## Similar Such Laws
Other principles of quantification yield the laws:
$$
B\cap \left( \bigcup_{i \in  I}A_{i} \right)=\bigcup_{i\in  I}(B\cap A_{i})
$$
from $P\text{ and }(\exists x)Q(x) \iff(\exists x)(P\text{ and }Q(x))$,
$$
B\cup\left( \bigcap_{i \in  I}A_{i} \right)=\bigcap_{i \in  I}(B\cup A_{i})
$$
$$
B\cap\left( \bigcap_{i \in  I}A_{i} \right)=\bigcap_{i \in I}(B\cap A_{i})
$$
$$
B\cup\left( \bigcup_{i \in  I}A_{i} \right)=\bigcup_{i\in  I} (B\cup A_{i})
$$
In the case ofd two sets, these laws imply the following familiar laws of set algebra:
$$
(A\cup B)'=A'\cap B'

$$
$$
 (A\cap B)'=A'\cup B'
$$
$$
 A\cap(B\cup C)=(A\cap B)\cup(A\cap C)
$$
$$
 A\cup(B\cap C)=(A\cup B)\cap(A\cup C)
$$
Also:
$$
\bigcup_{i=1}^{n}(X\setminus A_{i})=X\setminus \bigcap_{i=1}^{n}A_{i}
$$
$$
\bigcap_{i=1}^{n}(X\setminus A_{i})=X\setminus \bigcup_{i=1}^{n}A_{i}
$$




#Mathematics #Set #Law 