# Group Theory
Let $(G,*)$, $(H,+)$ be [[Groups|groups]], the direct product is the group $(G\times H,\cdot)$ is defined by the elements  of $G\times H$ are the ordered pairs $(g,h)$, with $g\in G,h\in H$. The binary operator is defined component-wise:
$$
(g_{1},h_{1})\cdot(g_{2},h_{2})=(g_{1}* g_{2},h_{1}+h_{2})
$$
This has identity $(e,e)$ and inverse $(g,h)^{-1}=(g^{-1},h^{-1})$
This group has order $\left| G\times H \right|=\left| G \right|\left| H \right|$
We also have $\text{ord}(g,h)=\text{lcm}(\text{ord(g)},\text{ord}(h))$
## Example
$\mathbb{Z}_{2}\times \mathbb{Z}_{2}$ is the direct product of two copies of the [[Cyclic Groups|cyclic group]] of order $\hspace{0pt}2$
$$
\mathbb{Z}_{2}=\left\{ \overline{0},\overline{1} \right\}
$$


| +              | $\overline{0}$ | $\overline{1}$ |
| -------------- | -------------- | -------------- |
| $\overline{0}$ | $\overline{0}$ | $\overline{1}$ |
| $\overline{1}$ | $\overline{1}$ | $\overline{0}$ |
So 
$$
\mathbb{Z}_{2}\times \mathbb{Z}_{2}=\left\{ (\overline{0},\overline{0}),(\overline{1},\overline{0}),(\overline{0},\overline{1}),(\overline{1},\overline{1}) \right\}
$$
Which ends up being [[Isomorphisms|isomorphic]] to the [[Small Groups#$K_{4}$|Klein group]] 
___
Let $\left|  G \right|=4$, then either $G\cong \mathbb{Z} /4$ or $G\cong K_{4}$, which is the group $G=\left\{ e,a_{1},a_{2},a_{3} \right\}$, with $a_{i}a_{j}=a_{k}$ for any distinct $i,j,k$, where $\text{ord}(a_{i})=2$   

# Ring Theory
If $R$ and $S$ are [[Rings|rings]], we can form the direct product $R\times S=\left\{ (r,s)\mid r\in R,s \in S \right\}$, where everything is defined component-wise:
$$
(r,s)+(r',s')=(r+r',s+s')
$$
$$
 (r,s)(r',s')=(rr',ss')
$$
And $(1,1)\in R\times S$ is the multiplicative identity, and $(0,0)\in R\times S$ is the additive identity.
### Example
We have two specific homomorphisms (surjective)
$$
p_{1}:R\times S\to R
$$
$$
 (r,s)\mapsto r 
$$
$$
p_{2}:R\times S\to S
$$
$$
 (r,s)\mapsto s
$$
And $\text{ker}(p_{1})=\left\{ (0,s)\mid s \in S \right\}$, and we can think of $\text{ker}(p_{1})$ as a ring in its own right with identity element $(0,1)$, in fact $\text{ker}(p_{1})\cong S$ by the map $(0,s)\mapsto s$, similarly, $\text{ker}(p_{2})\cong R$ and $\text{ker}(p_{1})\times \text{ker}(p_{2})\cong R\times S$
Note however $\text{ker}(p_{1})$ and $\text{ker}(p_{2})$ are not [[Subrings|Subrings]] 
