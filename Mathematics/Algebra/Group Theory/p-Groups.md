A $p$-[[Groups|group]] is one such that $\left| G \right|=p^{k}$ with $p$ a prime
## Proposition
If $G$ is a $p$-group, then its [[Centre of a Group|centre]], $Z(G)$ is not trivial
### Proof
By the [[Orbit-Stabiliser Theorem|orbit-stabiliser theorem]], the size of any [[Conjugate Elements|conjugacy classes]] divides $p^{k}$, so it is $p^{i}$ so it is either $\hspace{0pt}1$ or a multiple of $p$
Thus $\left| G \right|$ is equal to the number of conjugacy classes of size $\hspace{0pt}1$ plus the number of other conjugacy classes which are multiples of $p$, so since there exists at least one conjugacy class of size $1$, $\left\{ e \right\}$, the number of conjugacy classes of size $\hspace{0pt}1$ is greater than or equal to $p$
Hence $\left| Z(G) \right|\geq p$
## Corollary
If $\left| G \right|=p^{2}$, then $G$ is abelian
### Proof
Consider $Z(G)$ which is a subgroup of $G$, so by [[Lagrange's Theorem|lagrange's theorem]] $\left| Z(G) \right|=p^{i}$
We know $\left| Z(G) \right|\neq 1$ by the proposition above, if $\left| Z(G) \right|=p^{2}$, then $Z(G)=G$, so $G$ is abelian
So we assume $\left| Z(G) \right|=p$, take $h\not\in Z(p)$
Consider the [[Orbits and Stabilisers#Conjugation Clases and Centralisers|centraliser]] of $h$:
$$
C_{G}(h)=\left\{ g\in G:\middle|: gh=hg \right\}
$$
The centraliser is a subgroup, so its order divides $p^{2}$, and clearly, $C_{G}(h)\supseteq Z(G)$, so
$$
C_{G}(h)\geq p
$$
But it must be greater, since $h\in C_{G}(h),h\not\in Z(G)$, sooooo
$$
\left| C_{G}(h) \right| \geq p+1\implies \left| C_{G}(h) \right| =p^{2}\implies C_{G}(h)=G
$$
But if every element of the group commutes with $h$, then $h$ must be in the centre, which is a contradiction
___
We will in fact see that if $\left| G \right|=p^{2}$, then $G\cong \mathbb{Z} /p^{2}$ or $G\cong \mathbb{Z} /p \times \mathbb{Z} /p$
