## Background
Given a [[Subgroups|subgroup]] $H\subseteq G$, we want to define a quotient [[Groups|group]] $G /H$ whose elements are [[Cosets|cosets]] under the operation:
$$
(g_{1}H,g_{2}H)\to g_{1}g_{2}H
$$
The issue is that this doesn't work for all cosets, so we need to state some conditions on $H$ for the [[Functions|map]] to be well defined, so we need:
$$
(g_{1}h_{1}H,g_{2}h_{2}H)\to g_{1}g_{2}H
$$
For some $h_{1},h_{2}\in H$, but 
$$
(g_{1}h_{1}H,g_{2}h_{2}H)\to g_{1}h_{1}g_{2}h_{2}H
$$
So we need $\forall g_{1},g_{2}\in G,h_{1},h_{2}\in H$, 
$$
g_{1}g_{2}H=g_{1}h_{1}g_{2}h_{2}H
$$
We know that $gH=fH$ iff $gf^{-1}\in H$, so we need
$$
(g_{1}g_{2})^{-1}g_{1}h_{1}g_{2}h_{2}\in  H
$$
$$
 \iff g_{2}^{-1}g_{1}^{-1}g_{1}h_{1}g_{2}h_{2}\in  H 
$$
$$
 \iff g_{2}^{-1}h_{1}g_{2}h_{2} =h'\in  H
$$
$$
 \iff g_{2}^{-1}h_{1}g_{2}=h'h_{2}^{-1}\in  H
$$
So our condition for this to be a well defined map, we need $\forall g_{2}\in G,h_{1}\in H$ we have
$$
g_{2}^{-1}h_{1}g_{2}\in  H
$$
So we need [[Normal Subgroups|$H\lhd G$]]
## Definition
For some group  $G$, normal subgroup $N\lhd G$, the quotient group $G /N$ of left cosets $gN$ has operation
$$
(g_{1}N,g_{2}N)=g_{1}g_{2}N
$$
We can see that associativity is inherited from the group, the identity is of course $eN=N$, and the inverse is given by $(gN)^{-1}=g^{-1}N$
___
There is a canonical [[Homomorphisms|homomorphism]]
$$
\varphi:G\to G /N,\varphi(g)=gN
$$
This has [[Kernel|kernel]]
$$
\text{ker}(\varphi)=N
$$
## Lemma
If $\varphi :G\to H$ is a group homomorphism, then 
$$
\text{ker}(\varphi)\lhd G
$$
Conversely if $N\lhd G$, then $\exists$ a group $H$ and a homomorphism of groups $\theta:G\to H$, such that
$$
N=\text{ker}(\varphi)
$$
### Proof
If $\varphi:G\to H$ $g\in \text{ker}(\varphi)$
- First, we know that $\text{ker}(\varphi)$ is a subgroup of $G$, as if $g_{1}\in\text{ker}(\varphi),g_{2}\in\text{ker}(\varphi)$, then $\varphi(g_{1}g_{2})=\varphi(g_{1})\varphi(g_{2})=e\cdot e=e$, so we have closure, also we have $\varphi(g)=e\implies \varphi(g^{-1})=e$
- Now we need $\text{ker}(\varphi)\lhd G$, if $g\in \text{ker}(\varphi)$, we need $fgf^{-1}\in \text{ker}(\varphi)\forall f\in G$. Equivalently, $\varphi(fgf^{-1})=e\forall f\in G$, which we can check
$$
\varphi(fgf^{-1})=\varphi(f)\varphi(g)\varphi(f^{-1})=\varphi(f)\varphi(f^{-1})=\varphi(f f^{-1})=\varphi(e)=e
$$
    Remark, we proved that $\varphi(f^{-1})=(\varphi(f))^{-1}$
So we have proved that $\text{ker}(\varphi)\lhd G$
For the converse, let $N\lhd G$, then $N=\text{ker}(\varphi),\varphi:G\to G /N$
## Lemma
Let $\left| G \right|<\infty$, $N\lhd G$, then $\left| G /N \right|=\frac{\left| G \right|}{\left| N \right|}$
### Proof
This follows from the lemma above, both sides are counting the number of left cosets
### Remark
Even if $\left| G \right|=\infty$, we can write $\left| G/N \right|=[G:N]$, the [[Index of Groups|index of the group]] 