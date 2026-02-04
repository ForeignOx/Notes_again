Points in [[Vectorspace Rn|$\mathbb{R}^3$]] can be thought of in a few ways
## Intersection of $\hspace{0pt}3$ Planes
Suppose we have $\hspace{0pt}3$ planes $\Pi_{1},\Pi_{2},\Pi_{3}\subseteq \mathbb{R}^3$,
$$
\Pi_{i}=\{ \underline{x} \in \mathbb{R}^3|n_{i}\cdot \underline{x}=l_{i} \}
$$
What are the possibilities for the intersection $\Pi_{1}\cap \Pi_{2}\cap \Pi_{3}$?
- A plane ($\Pi_{1}=\Pi_{2}=\Pi_{3}$)
- A line:
![[Points in R3 2024-10-21 11.17.05.excalidraw]]
- A point:
![[Points in R3 2024-10-21 11.18.28.excalidraw]]
- The empty set (all three are parallel, and distinct) or:
    - Sheaf
    ![[Points in R3 2024-10-21 11.20.02.excalidraw]]
    - Tiangular prism
![[Points in R3 2024-10-21 11.22.05.excalidraw]]
## When do we get that the case where they intersect at a point?
We certainly want the intersection between two of the planes to be a line, so $\Pi_{2}\cap \Pi_{3}=L$
So $\underline{n}_{2}$ and $\underline{n}_{3}$ cannot be parallel. And $L$ has direction vector:
$$
\underline{d}-\underline{n}_{1}\times \underline{n}_{2}
$$
![[Points in R3 2024-10-21 11.26.02.excalidraw]]
Then finally we want to have $L\cap \Pi_{1}=\{ \text{pt} \}$ a set containing a point, this happens exactly when $L$ is not parallel to $\Pi_{1}$, so $\underline{d}$ is not orthogonal to $\underline{n}_{1}$, so:
$$
\underline{n}_{1}\cdot \underline{d}\neq 0
$$
$$
 \underline{n}_{1}\cdot(\underline{n}_{2}\times \underline{n}_{3})\neq 0
$$
Another way of saying this is that the [[Scalar Triple Product|Scalar Triple Product]] is non-zero, so a point satisfies $\hspace{0pt}3$ linear equations

#Mathematics #LinAlg 