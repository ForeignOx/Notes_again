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
Solving Laplace's equation in a domain $D$ with boundary conditions i.e. information on the solution on $\partial D$ is a fairly complicated problem
There are a few simply connected domains in which we are able to find an explicit solution by using various intuition and techniques (such as symmetry)
For instance the solution to Laplace's equation with [[Dirichlet Boundary Conditions|Dirichlet boundary conditions]] in the upper half plane:
$$
\begin{cases}
u_{x x }+u_{yy} & x\in \mathbb{R},y>0 \\
u(x,0)=g(x) & x\in \mathbb{R}
\end{cases}
$$
With a continuous and bounded function $g$ is given by
$$
u(x,y)=\frac{y}{\pi}\int_{-\infty}^{\infty} \frac{g(t)}{(x-t)^{2}+y^{2}} \, dt 
$$
But what would happen if we wanted to solve the same provlem in the unit disc $\mathbb{D}$? In the upper unit disc? In a wedge of angular opening $\frac{\pi}{4}$?
Here the power of complex analysis shines
The idea is that since being harmonic in a simple connected domain is essentially being holomorphic, if a given simple connected domain $D$ is "holomorphically equivalent" to $\mathbb{H}$, i.e. we can move from $D$ to $\mathbb{H}$, and vice versa by a holomorphic [[Bijective Functions|bijection]], then we can compose the holomorphic function which is associated to Laplace's equation in $\mathbb{H}$ with this bijection to get the appropriate holomorphic function in $D$
More precisely:
- Assume that $D$ is a simply connected domain such that there exists a bijection $\varphi:D\to \mathbb{H}$ that is holomorphic and whose inverse is also holomorphic. Moreover, assume that $\varphi$ is a continuous bijection from $\overline{D}$ to $\overline{\mathbb{H}}$ and that it inverse is also continuous. Note that this implies that $\varphi(\partial D)=\partial \mathbb{H}$ and $\varphi ^{-1}(\partial \mathbb{H})=\partial D$
- Consider Laplace's equation:
$$
\begin{cases}
u_{xx }+u_{yy}=0 & (x,y)\in  D \\
u=g & (x,y)\in \partial D
\end{cases}
$$
    With a [[Continuity|continuous]] and [[Boundedness|bounded]] function $g$ and define $\tilde{g}(x)=g(\varphi ^{-1}(x,0))$ for any $x\in \mathbb{R}$
- Let $\tilde{U}(z)$ be the holomorphic function in $\mathbb{H}$ that is also continuous on $\overline{\mathbb{H}}$ and whose real part is given by
$$
\tilde{u}(x,y)=\frac{y}{\pi}\int_{-\infty}^{\infty} \frac{\tilde{g}(t)}{(x-t)^{2}+y^{2}} \, dt 
$$
- The function $U(z)=\tilde{U}\circ \varphi(z)$ is a holomorphic function on $D$ and as such its real part $u(x,y)$ is harmonic. Moreover, we notice that for any $x\in\mathbb{R}$,
$$
U(\varphi ^{-1}(x,0))=\mathfrak{R}(U(\varphi ^{-1}(x,0)))=\mathfrak{R}(\tilde{U}(\varphi(\varphi ^{-1}(x,0))))
$$
$$
= \mathfrak{R}(\tilde{U}(x,0))=\tilde{u}(x,0)=\tilde{g}(x)=g(\phi ^{-1}(x,0))
$$
    Since $\varphi ^{-1}(\partial \mathbb{H})=\partial D$, we must have that $u=g$ on $\partial D$ and we found a solution to the Dirichlet problem on D!
### Example
The map
$$
f(z)= \frac{z-i}{z+i}
$$
Is holomorphic in $\mathbb{C}\setminus \left\{ -i \right\}$ and takes $\mathbb{H}$ to $\mathbb{D}$. Consequently, we can use the above method to solve the PDE
$$
\begin{cases}
u_{x x}+u_{yy}=0 & x^{2}+y^{2}<1 \\
u(\cos\theta,\sin\theta)-g(\theta) & \theta \in (-\pi,\pi]
\end{cases}
$$
## Interesting Feature
We know that electric field satisfies the Laplace equation
$$
\nabla^{2}(\phi)=\nabla^{2}\left( \frac{Q}{4\pi\varepsilon_{0}}  \frac{1}{\left| \underline{r}-\underline{r}_{0} \right| }\right)=-\frac{Q}{\varepsilon_{0}}\delta(\underline{r}-\underline{r}_{0})
$$
Which tells us:
$$
\nabla^{2}\left( -\frac{1}{4\pi \left| \underline{r}-\underline{r}_{0} \right| } \right)=\delta(\underline{r}-\underline{r}_{0})
$$
So we found a function $G(\underline{r};\underline{r}_{0})=-\frac{1}{4\pi} \frac{1}{\left| \underline{r}-\underline{r}_{0} \right|}$ satisfying
$$
\nabla^{2}G(\underline{r},\underline{r}_{0})=\delta(\underline{r},\underline{r}_{0})
$$
I.e. $G(\underline{r},\underline{r}_{0})$ is the Green's function for the Laplacian in 3D