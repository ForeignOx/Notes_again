## Definition
A quasi-linear PDE is a PDE of the form
$$
\sum_{\lvert \lvert \underline{\alpha} \rvert \rvert _{1}=k}a_{\underline{\alpha}}(\underline{x},u(\underline{x}),Du(\underline{x}),\dots,D^{k-1}u(\underline{x}))D^{\underline{\alpha}}u(\underline{x})+a_{0}(\underline{x},u(\underline{x}),Du(\underline{x}),\dots,D^{k-1}u(\underline{x}))=0
$$
## Method of Characteristics for Quasilinear 1st Order PDEs
### Goal
The objective is for $\Omega \subseteq \mathbb{R}^{n}$ open, $a:\Omega \times \mathbb{R}\to \mathbb{R}^{n}$, $b:\Omega \times \mathbb{R}\to \mathbb{R}$ are both given, we want a method to solve
$$
a(x,u(x))\cdot \underline{\nabla } u(x)=b(x,u(x))
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
The heart of the method of characteristics is to convert these ODEs into PDEs

