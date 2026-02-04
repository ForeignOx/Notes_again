## Definition
Let $G$ be a [[Groups|group]], with $H\subseteq G$ a subgroup, then the left cosets of $H$ are sets:
$$
gH=\left\{ gh\mid h\in  H \right\}
$$
Similarly, the right cosets are
$$
Hg=\left\{ hg\mid h\in  H \right\}
$$
If $G$ is [[Abelian Groups|abelian]], then $gH=Hg$, also $eH=He=H$
## Example
Let $G=\mathbb{Z},H=2\mathbb{Z}=\left<  2 \right>$, since $G$ is abelian, the left coset is equal to the right coset
Consider the coset $g+H,g\in G$. Take $g=e$, then 
$$
e+H=0+H=2\mathbb{Z}=\left\{ \text{even numbers} \right\}
$$
$$
 1+H=\left\{ 1+2n\mid n\in \mathbb{Z} \right\}=\left\{ \text{odd numbers} \right\}
$$
$$
 2+H=\left\{ 2+2n\mid n\in \mathbb{Z} \right\}=\left\{ \text{even numbers} \right\}=2\mathbb{Z}
$$
So there are in fact only two cosets, even numbers and odd numbers, we see that there is a simple [[Bijective Functions|bijection]] between them
___
Consider $G=D_{3}=\left< r,s\mid r^{3}=e,s^{2}=e,s rs=r^{-1} \right>$, let $H=\left\{ e,s \right\}$ 
Let's first find the left cosets, we know that
$$
G=\left\{ e,r,r^{2},s,rs,r^{2}s \right\}
$$
So all the possible cosets are:
$$
eH,rH,r^{2}H,sH,rsH,r^{2}sH
$$
But some might coincide; 
$$
eH=H,sH=\left\{ se,ss \right\}=\left\{ s,e \right\}=H
$$
$$
rsH=\left\{ rsh\mid h\in H \right\}=\left\{ r(sh)\mid h\in  H \right\}=\left\{ rh'\mid h'\in  H \right\}=rH
$$
And similarly, $r^{2}H=r^{2}sH$, so there are at most $\hspace{0pt}3$ cosets, $H,rH,r^{2}H$
We know that $H\neq rH$, since $r\in rH,r\not\in H$, also $H_{1}=r^{2}H$
We know $r\in rH$, assume $r\in r^{2}H$, then 
$$
r=r^{2}h,h\in H \iff r^{-1} = h \iff r^{-1}\in  H\iff r\in  H
$$
Which is a contradiction, $rH\neq r^{2}H$ and they are all $\hspace{0pt}3$ distinct cosets.
___
If $G$ is a group and $H\subseteq G$ is a subgroup, then $xH=yH \iff y^{-1}x\in H$
## Lemma
Left cosets form a [[Set Partition|partition]] of $G$; so
$$
G=\bigcup_{g\in  G}gH
$$
And if $g_{1}H_{1}\neq g_{2}H$, then $g_{1}H\cap g_{2}H=\emptyset$
So $G$ is a disjoint [[Union|union]] of (left) cosets which we can write as:
$$
G=\bigsqcup_{g\in G}gH
$$
### Proof
We have two statements to prove
For the first, we have $\forall g\in G,\exists$ left coset $g'H$ such that $g\in g'H$, indeed $g\in gH$ since $g=ge$
For the second we take $g_{1}H,g_{2}H$, assume $g_{1}H\cap g_{2}H\neq \emptyset$, we want to prove they coincide:
$$
x\in g_{1}H\cap g_{2}H
$$
$$
\implies x=g_{1}h_{1}=g_{2}h_{2},h_{1},h_{2}\in  H
$$
$$
g_{1}h_{1}=g_{2}h_{2}\implies g_{1}h_{1}h_{2}^{-1}=g_{2}\implies g_{2}\in  g_{1}H
$$
$$
\implies g_{2}H\subseteq g_{1}H
$$
As
$$
g_{2}h=g_{1}h'h\in g_{1}H
$$
Similarly $g_{1}H\subseteq g_{2}H\implies g_{1}H=g_{2}H$
## Lemma
$\forall g\in G$, $\left| gH \right|=\left| H \right|$, in particular $\left| G \right|=m\left| H \right|$ where $m$ is the number of (left) cosets
### Proof
Let $g_{1}H,g_{2}\mathbf{H}..,g_{m}H$ all be cosets. We define the [[Functions|map]]
$$
f_{i}:g_{i}H\to H
$$
$$
 g_{i}h\mapsto h
$$
We claim this is a bijection for all $i$
[[Surjective Functions|Surjection]]: $h\in H$, then $h=f_{i}(g_{i}H)$
[[Injective Functions|Injection]]: let $f_{i}(g_{i}h)=f_{i}(g_{i}h')\iff h=h'\iff g_{i}h=g_{i}h'$, so $f$ is injective and hence bijective
Thus $\left| g_{i}H \right|=\left| H \right|$
By the previous lemms, all $g_{i}H$ do not intersect, so every $g\in g_{i}H$ for some $i$, so
$$
G=\bigcup_{i=1}^{m} g_{i}H
$$
$$
\implies \left|G  \right|=\sum_{i=1}^{m}\left| g_{i}H \right| =\sum_{i=1}^{m}\left| H \right| =mH 
$$
## Corollary
$\left| H \right| \mid \left| G \right|$, $\left| H \right|$ divides $\left| G \right|$, so we  have [[Lagrange's Theorem|Lagrange's theorem]]


#Mathematics #Group #Definition