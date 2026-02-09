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
### Remark
While the requirement that $u$ and $v$ belong to $C^{2}(D)$ seem restricting, it is in fact redundant. This is due to one of the fundamental theorems of complex analysis: If $f$ is a holomorphic function in a domain $D$, then it is complex differentiable on $D$ infinitely many times
With that, our proposition above can be reformulated as:
    The real part and imaginary part of a holomorphic function in a domain $D$ are harmonic functions
A testament to the power of complex analysis is that the converse is mostly true
### Theorem
Let $D$ be a [[Connectedness|simply connected]] domain and let $u:D\to \mathbb{R}$ be a harmonic function. Then there exists a harmonic function $v:D\to \mathbb{R}$ such that $f=u+iv$ is holomorphic on $D$ The function $v$ is calle a harmonic conjugate of $u$ and it is unique up to an addition of a real constant
### Corollary
Let $D$ be a simply connected domain and let $u:D\to \mathbb{R}$ be harmonic, then $u\in C^{\infty}(D)$ (we can actually say more, it is in fact [[Analytic Functions|analytic]] in $D$)
### Method to Find Harmonic Conjugates
Consider a harmonic function $u$ in a simply connected set $D$
1. Since $f=u+iv$ is a holomorphic function, $u$ and $v$ need to satisfy the Cauchy-Riemann equations, i.e. $u_{x}=v_{y},u_{y}=-v_{x}$
2. Choose one of the Cauchy-Riemann equations and integrate it to find an expression for $v$ that involves a function of the variable which was kept fixed in the partial derivative; for instance if we consider the equation $u_{x}=v_{y}$, then we can say that:
$$
v(x,y)=\int u_{x}(x,y) \, dy +\psi(x)
$$
    Where $\int u_{x} \, dy$ is the [[Integration#Indefinite Integrals (or Anti- Differentiation Derivative s)|indefinite integral]] of $u_{x}$ with respect to $y$. We choose the Cauchy-Riemann equation that is easier to integrate in this stem
3. Use the second Cauchy-Riemann equation to find an ordinary differential equation for the additional one variable function we found in the previous step to conclude the closed form of $v$; following from the above example, we have
$$
u_{y}(x,y)=-v_{x}(x,y)=-\frac{ \partial  }{ \partial x } \left( \int u_{x}(x,y) \, dt  \right)-\psi'(x)
$$
    which implies that
$$
\psi'(x)=-u_{y}(x,y)-\frac{ \partial  }{ \partial x } \int u_{x}(x,y) \, dy 
$$
    which will give us $v$ up to a constant
### Example
Consider the harmonic function $u=x^{2}-y^{2}+3x$ on $\mathbb{C}$ and find its harmonic cconjugate
Firstly we note that $\mathbb{C}$ is a domain "with no holes", so it is simply connected. Moreover,
$$
u_{x x}+u)_{yy}=2-2=0
$$
So $u$ is indeed harmonic. We follow the steps above to find $v$. As $u$ is fairly simple, we can choose any of the Cauchy-Riemann equations to work with. We'll consider $u_{x}=v_{y}$:
$$
v_{y}=u_{x}=2x+3
$$
$$
 v=2xy+3y+\psi(x)
$$
Using the second Cauchy-Riemann equation, we get
$$
2y+\psi'(x)=v_{x}=-u_{y}=2y
$$
From which we conclude that $\psi'(x)=0$
This implies that $\psi(x)=C$ where $C$ is a real constant. We consclude that
$$
v=2xy+2y+C
$$
We can even recover our holomorphic function $f$!
$$
f(z)=f(x+iy)=x^{2}-y^{2}+3x+2xyi+iy+iC
$$
$$
=(x+iy)^{2}+3(x+iy)+iC=z^{2}+3z+iC
$$
## Holomorphic Functions in the study of Harmonic Functions
Solving Laplace's 