## Definition
A manifold is a [[Topology|topological space]] that locally looks like Euclidean space
## Definition
Let $n\in\mathbb{Z}$, given a set $M$, an $n$-dimensional chart on a manifold $M$ is a [[Bijective Functions|bijection]] $\varphi$ from a subset $U\subset M$ to an open subset $\varphi(U)\subset \mathbb{R}^{n}$, defining coordinates $x^{\mu}(p)$ for each $p\in U$
An atlas for $M$ is a collection of charts $\left\{ (U_{a},\varphi_{a}) \right\}$ such that
- $\bigcup_{a}U_{a}=M$ (the charts cover the whole set)
- If $U_{a}\cap U_{b}\neq \emptyset$, then the map $F=\varphi_{a}\circ\varphi ^{-1}_{b}:\mathbb{R}^{n}\to \mathbb{R}^{n}$, ($\tilde{x}^{\mu}(x^{\nu})$) i differentiable where it i defined
A maximal atlas is one containing all the charts satisfying these condition. An $n$-dimensional differentiable manifold is the set $M$ together with a maximal atlas
## Example
Let $M=\mathbb{R}^{2}$, we can take $U=M$ and $\varphi=\mathbb{1}$ to define cartesian coordinates which cover the whole set. A maximal atlas includes other coodinates; for example polar coordinates $(r,\theta)$ which are related to Cartesian coordinates $(x,y)$ by
$$
x=r\cos \theta,~y=r\sin\theta
$$
And the inverses
$$
r=\sqrt{ x^{2}+y^{2} }, ~\theta=\arctan\left( \frac{y}{x} \right)
$$
Excpet at $x=y=0$, where polar coordinates