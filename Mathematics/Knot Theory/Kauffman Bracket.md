Note that a Laurent polynomial over $\mathbb{Z}$ in the variable $A$ is an expression
$$
\sum_{k\in \mathbb{Z}}p_{k}A^{k}
$$
where each $p_{k}\in\mathbb{Z}$ and only finitely many of the p$_{k}$ are non-zero (as opposed to [[Laurent series|Laurent series]])
## Definition
Given a link diagram $D$, the bracket polynomial $\left< D \right>$ is a Laurent polyomail in $A$ with integer coefficients defined by 
$$
\left< D \right> :=\sum_{S}A^{e(S)}(-A^{2}-A^{-2})^{b(S)-1}
$$
Where $S$ is a [[Knot Diagram State|state]], $e(S)$ and $b(S)$ are defined per state
## Proposition
The bracket polynomial is the unique polynomial that satisfies:
- $\left< O \right>=1$ where $O$ is a 0 crossing diagram of [[knots|knot]] $U$ 
- $\left< D \perp\!\!\!\perp O \right>=(-A^{2}-A^{-2})\left<  D \right>$
And
![[Kauffman Bracket 2026-10-26 14.38.09.excalidraw]]
### Proof
Note that by applying the third rule repeatedly we arribe at a crossingless diagram and then can use the first and second rules to determine their bracket polynomials
We need to check that the bracket polynomial satisfies all of these as they are both unique objects
The first is trivially satisfied
