## Definition
Let $G$ be a [[Groups|group]] [[Group Action|acting]] on a [[Sets|set]] $X$, then we define:
- The orbit of $x\in X$:
$$
\text{orb}(x)=\left\{ gx\mid g\in  G \right\}
$$
- The stabiliser of $x\in X$:
$$
\text{stab}(x)=\left\{ g\in G\mid gx=x \right\}
$$
There is some alternate notation: $\text{orb}(x)\sim G(x),Gx$ and $\text{stab}(x)\sim G_{x}$ 
## Lemma
$\text{stab}(x)$ is always a subgroup of $G$
### Proof
$\text{stab}(x)$ is closed under multiplication:
$$
gx=x,hx=x\implies (gh)x=g(hx)=gx=x
$$
The identity $e$ stabilises $x\forall x\in X$
For some $g\in \text{stab}(x),g^{-1}\in\text{stab}(x)$ 
## Examples
Let $G$ be the group of [[Distance Preserving Maps|distance preserving maps]] from $\mathbb{R}^{2}\to \mathbb{R}^{2}$ and take $H$ to be a [[Subsets|subset]] of $G$ to be the set of functions taking the origin $(0,0)$ to itself, then $H=\text{stab}((0,0))$ in $G$
$H$ is a [[Subgroups|subgroup]] of $G$ (closed under composition and has inverses) $H$ acts on $\mathbb{R}^{2}$ (by [[Induced Action|induced action]])
If $x\neq (0,0)$, then $\text{orb}(x)$ is a circle
___
Some examples of $\mathbb{Z}$ acting on $\mathbb{R}$
Transposition, $n*x+n$, 
$$
\text{orb}(x)=\left\{ x+n\mid n\in \mathbb{Z} \right\}=x+\mathbb{Z}
$$
$$
 \text{stab}(x)=\left\{ n\in \mathbb{Z}\mid x+n=x \right\}=\left\{ 0 \right\}
$$
Consider $n*x=(-1)^{n}x$, then
$$
\text{orb}(x)=\left\{ (-1)^{n}x\mid n\in \mathbb{Z} \right\}=\left\{ x,-x \right\}
$$
$$
 \text{stab}(x)=\left\{ n\in \mathbb{Z}\mid (-1)^{n}x=x \right\}=\begin{cases}
2\mathbb{Z} & \text{if }x\neq 0 \\
\mathbb{Z} & \text{if }x=0
\end{cases}
$$
Consider $n*x=2^{n}x$
$$
\text{orb}(x)=\left\{ 2^{n}x\mid n\in  \mathbb{Z} \right\}
$$
$$
 \text{stab}(x)=\left\{ n\in \mathbb{Z}\mid 2^{n}x=x\right\}=\begin{cases}
\left\{ 0 \right\} & \text{if }x\neq 0 \\
\mathbb{Z} & \text{if }x=0
\end{cases}
$$
## Proposition
Let $G$ be a group acting on a set $X$, then for $x,y\in X$,
- $\text{orb}(x)\neq \emptyset$ (orbit is non-empty)
- For any two orbits $\text{orb}(x),\text{orb}(y)$, either these are disjoint, or they coincide
- $X$ is a [[Disjoint Families of Sets|disjoint union of orbits]] 
### Proof
$x\in\text{orb}(x)$ hence $\text{orb}(x)\neq \emptyset$
If $a\in\text{orb}(x)\cap \text{orb}(y)$, then $a=gx,a=hy,g,h\in G$, thus $h^{-1}gx=y$ where $y\in \text{orb}(x)\forall g\in G$ and so $\text{orb}(x )\subseteq\text{orb}(y)$, similarly, $\text{orb}(y)\subseteq \text{orb}(x)$, hence $\text{orb}(x)=\text{orb}(y)$
The third statement follows from the first two
## Cosets as Orbits
Any group $G$ acts on itself by left multiplication, for any $g,x \in G$, we can send $x$ to $gx$. For any $x\in G$, we have $\text{orb}(x)=G$ and $\text{stab}(x)=\left\{ e \right\}$, so this action is not terribly interesting
It gets more interesting if we take a subgroup $H\subseteq G$ and let it act on $G$ by left multiplication. In this case, for $x\in G$:
$$
\text{orb}(x)=\left\{ hx\mid h\in  H \right\}=Hx
$$
Which is the right [[Cosets|coset]] of $H$
Similarly, we can get left cosets by letting $H$ act on $G$ from the right. Note that here again, $\text{stab}(x)=\left\{ e \right\}$
## Conjugation Clases and Centralisers
Another way in which a group can act on itself, namely if $g,x\in G$, we can send $x$ to $gxg^{-1}$. It is easy to check that this is an action of $G$ on itself, called an action by conjugation
The orbit of $x\in G$ under action by conjugation is given by
$$
\text{orb}(x)=\left\{ g xg^{-1}\mid g\in  G \right\}
$$
Which is called the conjugacy class of $x$.
The stabiliser
$$
\text{stab}(x)=\left\{ x\in G\mid g xg^{-1}=x \right\}
$$
Is called the centraliser of $x$, and is usually denoted $C_{G}(x)$
Clearly, the centraliser of $x$ consists of all elements of $G$ commuting with $x$
### Example
Find the conjugacy classes in $D_{5}=\left< r,s\mid r^{5}=e,s^{2}=e,srs ^{-1}=r^{-1} \right>$
For $e\in D_{5}$, $geg^{-1}=e\forall g$ so $\text{orb}(e)=e$
For $r\in D_{5}$, $r^{i}rr^{-i}=r$ but also
$$
(r^{i}s)r(r^{i}s)^{-1}=r^{i}s rs r^{-i}=r^{i}r^{-1} r^{-i}=r^{-1}=r^{4}
$$
$$
\implies \text{orb}(r)=\left\{ r,r^{4} \right\}
$$
For $r^{2}\in D_{5}$,
$$
r^{i}r^{2}r^{-i}=r^{2}
$$
$$
 (r^{i}s)r^{2}(r^{i}s)^{-1}=r^{i} s r^{2} s r^{-i}=r ^{i}r^{-2}r^{-i}=r^{-2}=r^{3}
$$
$$
\implies \text{orb}(r^{2})=\left\{ r^{2},r^{3} \right\}
$$
For $s\in D_{5}$
$$
r^{i}s r^{-i}=r^{i}r^{i}s=r^{2i}s
$$
$$
(r^{i}s)s(r^{i}s)^{-1}=r^{i}s r^{-i}=r^{2i}s
$$
$$
\implies \text{orb}(s)=\left\{ s,r^{2}s,r^{4}s,r^{6}s=rs,r^{8}s=r^{3}s \right\}
$$
Now we have covered all elements, so since the orbits partition the group, we are done
We can also find the stabilisers:
$$
\text{stab}(r)=\left\{ r^{i}s ^{j}\in D_{5}\mid (r^{i}s ^{j})r(r ^{i}s ^{j})^{-1}=r \right\}
$$
$$
= \left< r \right> \cup \left\{ r ^{i}s\in D_{5}\mid r^{i}s r s r^{-i}=r ^{-i}=r \right\}
$$
$$
= \left< r \right> 
$$

