## Definition
A [[Subgroups|subgroup]] $H\subset G$ is normal if
$$
ghg^{-1}\in H~\forall h\in H,g\in G
$$
We denote this $H\lhd G$
## Remark
Taking the inverse of $g$, $H\lhd G$ iff $g^{-1}hg\in H$
## Example
For example the special linear group $SL(n,\mathbb{R})$ is a normal subgroup of $GL(n\mathbb{R})$, the [[General Linear Group|general linear group]], since
$$
\det(g^{-1}hg)=(\det g)^{-1}\det h\det g=\det h
$$
So it $\det h=1$ ($h\in SL(n,\mathbb{R})$), so is $\det(g^{-1}hg)$ for any $g\in GL(n,\mathbb{R})$
___
If $G$ is [[Abelian Groups|abelian]], $H\subseteq G$ is a subgroup, then for all $h\in H,g\in G$, $ghg^{-1}=h\in H\implies H\unlhd G$
___
Let $G=D_{n},H=\left< r \right>=\left\{ e,r, \dots,r^{n-1} \right\}$, this is also a normal subgroup We see this, as $h=r^{c},g=r^{a}s ^{b}$,
If $b=0$, then 
$$
ghg^{-1}=r^{a}r^{c}r^{-a}\in\left< r \right>=H
$$
If $b=1$, then 
$$
ghg^{-1}=r^{a}s r^{c} s r^{-a}=r^{a} r^{-c}r^{-a}\in  \left< r \right>  =H
$$
Yey
___
If $G=\left< g_{1},\dots ,g_{k} \right>,H\subseteq G$ is a subgroup, then $H\unlhd G$ iff
$$
g_{i}hg_{i}^{-1}\in  H\forall h\in H,\forall i=1,\dots ,k
$$
So we need to check the generators only
