## Definition
We say that a real differentiable map $f:D\to \mathbb{C}$ on a [[Domains|domain]] $D\subseteq \mathbb{C}$ is conformal at $z_{0}$ if it preserves the angle and orientation between any two tangent vectors at $z_{0}$, where by orientation, we mean the relative position of one vector with respect to another (i.e. if the tangent vector of a curge $\gamma_{1}$) was to the left of the tangent vector of the curve $\gamma_{2}$, the tangent vector of the image $\gamma_{1}$ by $f$ will remain to the left of the image of $\gamma_{2}$ by $f$
We say $f$ is conformal on $D$ if it is conformal at all points in $D$
## Remark
If we consider negative angles as well, (and not only take their absolute value) then angle preservation will imply orientation preservation. For instance, in this convention, the angle between the tangent vector of the curve $\gamma_{1}(t)=t$ and that of $\gamma_{2}(t)=it$ at $t=0$ is $\frac{\pi}{2}$ while the angle between the tangent vector of $\gamma_{2}$ and $\gamma_{1}$ at $t_{0}$ is $-\frac{\pi}{2}$
## Examples
Rotations in $\mathbb{R}^{2}$ are conformal, in terms of complex functions this corresponds to the function 
$$
f(z)=e^{ i\theta }z
$$
For some $\theta \in(-\pi,\pi]$
___
Dilations of $\mathbb{R}^{2}$ (stretching or compressing) are conformal. In terms of complex functions, this corresponds to the function
$$
f(z)=\lambda z
$$
For some $\lambda>0$
___
The conjugate function $z\to \overline{z}$ is not conformal as it doesn't preserve orientation
## Lemma - Holomorphic maps are conformal when their derivative is non-zero
Let $f$ be a holomorphic map at $z_{0}$. If $f'(z_{0})\neq 0$, then $f$ is conformal at $z_{0}$
### Proof
Let $\gamma:[0,1]\to \mathbb{C}$ be such that $\gamma(t_{0})=z_{0}$ for some $t_{0}\in(0,1)$. The image of $\gamma$ under the holomorphic map $f$ is a differentiable path $f\circ\gamma$ in a small neighbourhood of $t_{0}$ (since there exists $\varepsilon>0$ such that $f$ is complex differentiable at $B_{\varepsilon}(z_{0})$ and $\gamma(t)$ is in this ball for $t$ close enough to $t_{0}$)
To compute the tangent of the image path at $t_{0}$, we use the chain rule for paths and find that
$$
(f\circ \gamma)'(t_{0})=f'(\gamma(t_{0}))\gamma'(t_{0})=f'(z_{0})\gamma'(t_{0})
$$
Since $f'(z_{0})\neq 0$ we conclude that under $f$ the tangent of the original curve was stretched/compressed by $\left| f'(z_{0}) \right|$ and rotated by $\mathrm{Arg}(f'(z_{0}))$. As this is tre for any path, we conclude that as all tangent vectors of such paths are rotated by the same angle and in the same direction. Consequently, the angle between tangent vectors of differentiable paths that pass through $z_{0}$ remains the same, and their orientation is preserved. We conclude that the map is conformal at $z_{0}$
## Remark
The condition $f'(z)\neq 0$ is necessary, for example $f(z)=z^{2}$ satisfies $f'(0)=0$ and doubles the angle between two rays
___
Is there a converse?
## Proposition - Conformal Maps are Holomorphic
Let $D$ be a domain. If $f$ is conformal at $z_{0}\in D$, then $f$ is complex differentiable at $z_{0}$ and $f'(z_{0})\neq 0$. Therefore if $f$ is conformal on $D$, then $f$ is holomorphic on $D$ and $f'(z)\neq 0$ for all $z\in D$
## Corollary
Let $D$ be a domain. Then $f$ is conformal on $D$ iff $f$ is holomorphic on $D$ and $f'(z)\neq 0$ for all $z\in D$
## Corollary
Any conformal map maps orthogonal grids in the $xy$-plane to orthogonal grids
### Example
Let us show the validity for $f(z)=z^{2}$ when $z\neq 0$ and orthogonal lines that are parallel to the axes
We find that we can write $f=u+iv$ as
$$
u(x,y)=x^{2}-y^{2},v(x,y)=2xy
$$
The line $x=c$ with $x\neq 0$ gives us the curve
$$
(u,v)=(c^{2}-y^{2},2cy)
$$
With $y\in \mathbb{R}$. Consequently, $v=2cy$ ranges over $\mathbb{R}$ and we have that 
$$
u=c^{2}-y^{2}=c^{2}-\frac{v^{2}}{4c^{2}}
$$
The above implies that the image of $x=c$ under $z^{2}$ is a parabola around thee $u$ axis, the ame discussion shows us that the line $y=d$ with $d\neq 0$ gives the parabola
$$
u=\frac{v^{2}}{4d^{2}}-d^{2}
$$
The tangent vectors to the parabolas at the intersection point $(c^{2}-d^{2},2cd)$ are given by $(1,\frac{d}{c})$ and $\left( 1,-\frac{c}{d} \right)$ respectively and are perpendicular