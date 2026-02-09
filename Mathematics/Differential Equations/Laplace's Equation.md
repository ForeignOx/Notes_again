Laplace's equation is a [[Second Order Partial Differential Equations|second order]] [[Linear Partial Differential Equations|linear PDE]] of the form:
$$
u_{x x}+u_{yy}=0
$$
So $A=C=1,B=0$, so
$$
M=\begin{pmatrix}
1&0\\0&1
\end{pmatrix},\det(M)=1>0
$$
If we have some shape in three dimensional space, the minimal surface is described by Laplace's Equation. For example soap bubbles do this on a wire
![[Laplace's Equation 2025-02-28 15.14.58.excalidraw]]
In two dimensions, this equation describes the behaviour of electric potentials in a chargeless region or that of the velocity potential of an irrational and incompressible fluid
Functions that satisfy Laplace's equations are called Harmonic functions 
## Laplace's Equation and Holomorphic Functions
Harmonic functions have a close connection to [[Holomorphicity|holomorphic]] functions
### Proposition
Let $D\subseteq \mathbb{C}$ be a [[Domains|domain]] and let $f:D\to \mathbb{C}$ be a holomorphic function on $D$
Assume in addition that $f=u+iv$, where $u,v\in C^{2}(D)$
Then $u$ and $v$ are harmonic functions on $D$
#### Proof
Since $u$ and $v$ are differentiable and $f$ is holomorphic, we know that for any $z\in D$, the [[Cauchy-Riemann Equations|Cauchy-Riemann equations]] must be satisfied. In other words,
$$
u_{x}(x,y)=v_{y}(x,y),~u_{y}(x,y)=-v_{x}(x,y)
$$
For any $(x,y)\in D$
Consequently,
$$
u_{xx}(x,y)+u_{yy}(x,y)=v_{xy}(x,y)-v_{yx}(x,y)=0
$$
Where we have used the fact that mixed derivatives of $C^{2}$ functions are equal
Similarly,
$$
v_{x x}(x,y)+v_{yy}(x,y)=-u_{xy}(x,y)+u_{yx}(x,y)=0
$$
We conclude the result
___
While the requirement that $u$ and $v$ belong to $C^{2}(D)$ seem restricting, it is in