## Definition
Let [[Sets|$S$]] be a fixed [[Domain|domain]], and let $\mathfrak{F}$ be a family of [[Subsets|subsets]] of $S$
The union of $\mathfrak{F}$, or the union of all the sets in $\mathfrak{F}$ is the set of all elements belonging to at least one set in $\mathfrak{F}$
We designate the union $\bigcup \mathfrak{F}$ or $\bigcup_{A\in \mathfrak{F}}A$, and thu we have:
$$
\bigcup \mathfrak{F}=\left\{ x\mid(\exists A^{\in \mathfrak{F}})(x\in  A) \right\}
$$
$$
 y\in \bigcup \mathfrak{F} \iff(\exists A^{\in  \mathfrak{F}})(y\in A)
$$
We often consider the family $\mathfrak{F}$ to be [[Sets of Indices|indexed]]. That is, we assume given a set $I$ and a [[Surjective Functions|surjective]] mapping $i \mapsto A_{i}$ from $I$ to $\mathfrak{F}$, so that $\mathfrak{F}=\left\{ A_{i}\mid i \in I\right\}$
The union of the indexed collection is designated $\bigcup_{i \in I}A_{i}$ or $\bigcup \left\{ A_{i}\mid i \in I \right\}$
If $\mathfrak{F}$ is finite, and either it or the index set is listed, then a different notation is used for its union. If $\mathfrak{F}=\left\{ A,B \right\}$, we designate the union $A\cup B$, a notation that displays the listed names, note that we generally have:
$$
A\cup B=\{ x|x\in A \text{ or }x\in B\text{ or }x\in \text{both} \}
$$
If $\mathfrak{F}=\left\{ A_{i}\mid i=1,\dots,n \right\}$, we generally write $A_{1}\cup A_{2}\cup\dots \cup~A_{n}$ or $\bigcup_{i=1}^{n}A_{i}$ for $\bigcup \mathfrak{F}$
We see from the definition that $A\cup B=B\cup A$, and is thus commutative
We also have [[Empty Set|$A\cup \emptyset=A$]]
## Example
$$
\{ -2,-1,0 \}\cup \{ 0,1,2 \}=\{ -1,-2,0,1,2 \}
$$
![[Set Operations 2024-10-07 15.48.18.excalidraw]]


#Mathematics #Set #Definition