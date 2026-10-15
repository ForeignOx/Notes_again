## Definition
A quasi-linear PDE is a PDE of the form
$$
\sum_{\lvert \lvert \underline{\alpha} \rvert \rvert _{1}=k}a_{\underline{\alpha}}(\underline{x},u(\underline{x}),Du(\underline{x}),\dots,D^{k-1}u(\underline{x}))D^{\underline{\alpha}}u(\underline{x})+a_{0}(\underline{x},u(\underline{x}),Du(\underline{x}),\dots,D^{k-1}u(\underline{x}))=0
$$
## Method of Characteristics for Quasilinear 1st Order PDEs
### Goal
The objective is for $\Omega \subseteq \mathbb{R}^{n}$ open, $a:\Omega \times \mathbb{R}\to \mathbb{R}^{n}$, $b:\Omega \times \mathbb{R}\to \mathbb{R}$ are both given, we want a method to solve
$$
\underline{a}(\underline{x},u(\underline{x}))\cdot \underline{\nabla } u(\underline{x})=b(\underline{x},u(\underline{x}))
$$
For $x\in\Omega$ solving for the unknown $u:\Omega\to \mathbb{R}$
We take a given $n-1$-dimensionsal hypersurface $\Gamma \subset \overline{\Omega}$ where we have $u(x)=u_{0}(x)$ for $x\in \Gamma$ is called the Cauchy condition
$\Gamma$ is called a cauchy surface/curve, $u_{0}$ is called the Cauchy datum, and the PDE together with this cauchy condition is called a Cauchy problem
### Example
Let $\beta:\Omega\to \mathbb{R}^{n}$ is given and consider
$$
\begin{cases}
\frac{d }{d\tau} X(\tau)=\beta(X(\tau))  & T>0\\
X(0)=X_{0}\in  \Omega 
\end{cases}
$$
With 
$$
X:(0,T)\to\Omega \subseteq \mathbb{R}^{n}
$$
Suppose this is describing the motion of a fluid and has a classical solution, suppose also that $\rho(x,t)$ classifies the density of a material in $\Omega$ at $(x,t)\in\Omega \times(0,T)$
And we wanted to understand the evolution in time of the density $\rho$
If individual particles are evolving using the ODE
Here $\beta$ is a prescribed velocity field acting on the particles, one can think of wind or something
If you start at $X_{0}$, we get some path with tangent vectors in $\beta$
If the fluid/material is incompressible, this implies $\rho(X(\tau),\tau)=\rho(X_{0},0)=\rho_{0}(X_{0})$
Which imples
$$
\frac{d }{d\tau} \rho(X(\tau),\tau)=0
$$
$$
\implies \partial_{\tau}\rho(X(\tau),\tau)+\underline{\nabla } \rho(X(\tau),\tau)\cdot \underbrace{ X(\tau) }_{ =\beta(X(\tau)) }=0
$$
The heart of the method of characteristics is to convert these ODEs into PDEs, the way it works is that you have taken a total derivative and split it up into partials
And if we are interested only in stationary tates, we set
$$
\underline{\nabla } \rho(X,\tau)\cdot \underline{\beta}(X)=0
$$

We consider some fictitious particles on $\Gamma$, and observe their motion due to the vector field
We want to know if we take a particle in $\Omega$ whether there is a curve that originated on $\Gamma$
We need to introduce
### Remark
If the fluid is not icompressible, then the governing PDE is the so called continuity equation
$$
\partial_{t}\rho+\underline{\nabla} \cdot\rho(x,t) \underline{\beta} (x)=0
$$
In this case, the density is not constant along the particle trajectory
___
Here is the transport equation for $n=1$:
$$
\begin{cases}
\partial_{t}\rho(x,t)+c\partial_{x}\rho(x,t)=0 & x\in  \mathbb{R},t>0,c\in \mathbb{R} \\
\rho(x,0)=\rho_{0}(g) 
\end{cases}
$$
In this case $\beta(x)=c$ and our ODE system reads as
$$
\begin{cases}
\frac{d x}{d\tau} (\tau)=c & \tau \in (0,t) \\
x(0)=x_{0}
\end{cases}
$$
The solution of which is $x(\tau)=x_{0}+c\tau$
Consequently if $x(t)=x$ then $x_{0}=x_{0}(x,t)=x-ct$, so $\rho(x,t)=\rho_{0}(x_{0}(x,t))=\rho_{0}(x-ct)$
In this case essentially $x_{0}$ is acting as a coordinate system, so we can think of our physical coordinates $(x,t)=(c\tau+x_{0},\tau)$ are equal to the new coodinates, so we need $t=\tau$ and $x=c\tau+x_{0}\implies x_{0}=x-ct$
So we have our solution and traced back to the initial state
## Definition
The previou8s ODE system parametrised by $x_{0}$ is the so called system of characteristics associated to the PDE
## Remark
In general the solutio might not be constant along simple chaacteristics and also the velocity field in a quasi-linear 1st order PDE depends on the solution
Therefore one needs to study the solutions along each characteristic together with the system of characteristics