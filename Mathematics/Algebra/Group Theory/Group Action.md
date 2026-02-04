## Definition
If $G$ is a [[Groups|group]] and $X$ is a [[Sets|set]], an action of $G$ on $X$ is a [[Functions|map]] $G\times X\to X,(g,x)\mapsto g*x$ such that $\forall g,h\in G,x\in X$,
- $g*(h*x)=(gh)*x$
- $e*x=x$
A notation for a group action is $G:X$ 
## Examples
The group [[Symmetric Groups|$S_{n}$]] acts on the set $\overline{n}$ by permutations: for $x\in X,\sigma \in S_{n}$, $x\mapsto\sigma(x)$
___
For [[Dihedral Groups|$D_{n}$]], if we take $(1,2,3)$ to be the vertices of a regular triange, $D_{n}$ represents the transformations of these vertices
___
$\mathbb{Z}$ acting on $\mathbb{R}$
Translation: for $n\in \mathbb{Z},x\in \mathbb{R}$ $n*x=n+x$. We see that this is an action as:
$$
m*(n*x)=m+(n+x)=(m+n)+x=(m+n)*x
$$
$$
 0*x=x+0=x
$$
Another example is $n*x=(-1)^{n}x$:
$$
m*(n*x)=m*(-1)^{n}x=(-1)^{m}(-1)^{n}x=(-1)^{m+n}x=(m+n)*x
$$
$$
 0*x=(-1)^{0}x=x
$$
Or $n*x=2^{n}x$:
$$
m*(n*x)=m*2^{n}x=2^{m}2^{n}x=2^{m+n}x=(m+n)*x
$$
$$
0*x=2^{0}x=x
$$

## Lemma
Let $X$ be a set and $S_{X}$ be the set of all [[Bijective Functions|bijections]] $X\to X$, then
 - $S_{X}$ is a group
 - Given a group $G$, $G$ acts on $X$ iff $\exists$ a [[Homomorphisms|homomorphism]] $G\to S_{X}$
### Proof
$S_{X}$ is clearly a group under [[Composition of Functions|composition]] of bijections which gives associativity, identity and inverses.
For the second part:
Given an action $f:G\times X\to X$ of $G$ on $X$, define a map $\varphi:G\to S_{X}$ by setting $\varphi(g)$ takes $x\in X$ to $g*x$. $\varphi(g)$ is an invertible map as:
$$
\varphi(g^{-1})\varphi(g)=\varphi(g^{-1})g(x)=g^{-1}(g(x))=x
$$
The first condition of a group action gives that $\varphi$ is a homomorphism:
$$
(\varphi(gh))(x)=(\varphi(g)\varphi(h))(x)\forall x
$$
Conversely, given a homomorphism $\varphi:G\to S_{X}$, define an action given by $g*x=(\varphi(g))(x)$. The conditions to be a group action follow from being a homomorphism
## Remark
If $X$ is a finite set with $n$ elements, then $S_{X}$ is [[Isomorphisms|isomorphic]] to [[Symmetric Groups|$S_{n}$]]
Any group $G$ acts on itself via left multiplication:
$$
G\times G\to G,(g,h)\mapsto gh
$$
Thus if $G$ has $n$ elements, we have a homomorphism $\varphi:G\to S_{G}\cong S_{n}$

