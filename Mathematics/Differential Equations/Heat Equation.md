The heat equation is a [[Second Order Partial Differential Equations|second order]] [[Linear Partial Differential Equations|linear PDE]] of the form
$$
u_{t}=k^{2}u_{xx}
$$
$$
\implies u_{x x }-\frac{1}{k^{2}}u_{t}=0
$$
So $A=0,B=C=0$,
$$
M=\begin{pmatrix}
1&0\\0&0
\end{pmatrix},\det(M)=0
$$
So the heat equation is parabolic
The general shape to solutions look something like:
![[Heat Equation 2025-02-28 15.11.09.excalidraw]]
___
If we write it as:
$$
\frac{ \partial u }{ \partial t } =D\left( \frac{ \partial^{2}u }{ \partial x^{2} } +\frac{ \partial^{2}u }{ \partial y^{2} }  \right)
$$
Then we have added a second spatial variable, so we have $\hspace{0pt}2$ spatial variables, $x$ and $y$
And one temporal variable $t\in(0,\infty)$
Consider $R=[0,L_{x}]\times[0,L_{y}]\times(0,\infty)$ which is a 3D infinitely tall cuboid, but we call this a 2D PDE as it only has $\hspace{0pt}2$ spatial dimensions
This has solutions:
$$
u(x,y,t)=e^{ -D\left( \frac{n^{2}}{L_{x}^{2}}+\frac{m^{2}}{L_{y}^{2}} \right) \pi^{2}t}\cos\left( \frac{n\pi x}{L_{x}} \right)\cos\left( \frac{m\pi y}{L_{y}} \right)
$$
Where $n,m$ are integers, a similar solution involves replacing the $\cos$ term with $\sin$:
$$
u(x,y,t)=e^{ -D\left( \frac{n^{2}}{L_{x}^{2}}+\frac{m^{2}}{L_{y}^{2}} \right) \pi^{2}t}\sin\left( \frac{n\pi x}{L_{x}} \right)\sin\left( \frac{m\pi y}{L_{y}} \right)
$$
We can check this by differentiating and seeing that it satisfies
Since $n$ and $m$ were arbitrary integers, we can sum over all their values, by the [[Principle of Superposition|principle of superposition]], i.e.
$$
u(x,y,t)=\sum_{n=0}^{\infty}\sum_{m=0}^{\infty}C_{nm}e^{ -D\left( \frac{x^{2}}{L_{x}^{2}}+\frac{y^{2}}{L_{y}^{2}} \right)\pi^{2}t }\cos\left( \frac{n\pi x}{L_{x}} \right)\cos\left( \frac{m\pi y}{L_{y}} \right)
$$
A key property of this solution is that if we set $t=0$, we get a [[Fourier Series|Fourier Series]], and thus can represent any square integrable function (we can set an initial shape and then find out what happens to it as we let time run). We can thus expect a lot of complex behaviour
The terms of a Fourier series [[Linear Independence|linearly independent]], so only $\hspace{0pt}0$ if all $C_{nm}=0$, this means that we can describe this complex behaviour in terms of simple functions
## Solution Using Fourier Series
We can write the solution of the heat equation as a fourier series with coefficients changing with time
$$
u(x,y,t)=\sum_{n=0}^{\infty}\sum_{m=0}^{\infty}T_{mn}(t)\cos\left( \frac{n\pi x}{L_{x}} \right)\cos\left( \frac{m\pi y}{L_{y}} \right)
$$
$$
\implies \frac{ \partial u }{ \partial t } =\sum_{n=0}^{\infty}\sum_{m=0}^{\infty} \frac{d T_{mn}}{dt} \cos\left( \frac{n\pi x}{L_{x}} \right)\cos\left( \frac{m\pi y}{L_{y}} \right)
$$
$$
= -D\sum_{n=0}^{\infty}\sum_{m=0}^{\infty}\left( \frac{n^{2}\pi^{2}}{L_{x}^{2}}+\frac{m^{2}\pi^{2}}{L_{y}^{2}} \right)T_{nm}(t)\cos\left( \frac{n\pi x}{L_{x}} \right)\cos\left( \frac{m\pi y}{L_{y}} \right)
$$
By definition of Heat equation,
Bringing htis together, we get:
$$
\sum_{n=0}^{\infty}\sum_{m=0}^{\infty}\left( \frac{d T_{mn}}{dt} +\left( \frac{n^{2}\pi^{2}}{L_{x}^{2}}+\frac{m^{2}\pi^{2}}{L_{y}^{2}} \right)DT_{mn}(t) \right)\cos\left( \frac{n\pi x}{L_{x}} \right)\cos\left( \frac{m\pi y}{L_{y}} \right)=0
$$
To make the whole sum zero, we can demand
$$
\frac{d T_{mn}}{dt} +D\left( \frac{n^{2}\pi^{2}}{L_{x}^{2}}+\frac{m^{2}\pi^{2}}{L_{y}^{2}} \right)T_{mn}=0
$$
This is assuming that the series can only be zero if each coefficient is identically zero
We know this is true of the Fourier series and it relies on the linear independence of the Fourier series, which in turn relies on orthogonality
$$
\implies T_{mn}(t)=a_{nm}e^{ -D\left( \frac{n^{2}\pi^{2}}{L_{x}^{2}}+\frac{m^{2}\pi^{2}}{L_{y}^{2}} \right) t}
$$
The function
When $t=0$, we have a proper Fourier series, so if $f(x,y)=u(x,y,0)$, to the initial conditions,
$$
a_{mn}=\frac{4}{L_{x}L_{y}}\int_{0}^{L_{x}} \int_{0}^{L_{y}} f(x,y)\cos\left( \frac{m\pi x}{L_{x}} \right)\cos\left( \frac{n\pi y}{L_{y}} \right) \, dy  \, dx 
$$
So if we specify the boundary condition to be [[Neumann Boundary Conditions|Neumann]], then we fully specify the solution
### Is this Enough?
Consider
$$
u_{c}=\frac{a_{mn}}{4\pi Dt}e^{ \frac{-(x-2mL_{x})^{2}-(y-2mL_{y})^{2}}{4Dt} }
$$
Is a solution to the heat equation which is not in separable form
Are we missing something? If there are non-separable solutions, how do we find them all?
But we can actually write $u_{c}$ as a Fourier series:

## Proposition
Any solution to the heat equation on $[0,L_{x}]\times[0,L_{y}]$ with homogeneous Dirichlet/Neumann boundary conditions can be represented by a Fourier series
In short, we are not missing anything
### Example
Show that $f(x,y)=(x(L_{x}0x))^{2}(y(L_{y}-y))^{2}$ for $(x,y)\in[0,L_{x}]\times[0,L_{y}]$ is a suitable initial condition for the heat equation and calculate $a_{nm}$
Boundary Check:
$$
\frac{ \partial f }{ \partial x } =2x(L_{x}-x)(L_{x}-2)(y(L_{y}-y-))^{2}
$$
$$
 \frac{ \partial f }{ \partial y } =2y(L_{y}-y)(L_{y}-2y)(x(L_{x}-x))^{2}
$$
If $x=0,\frac{ \partial f }{ \partial x }=0$ if $x=L_{x},\frac{ \partial f }{ \partial x }=0$ similarly for $y$
For the coeefficients
$$
a_{mn}=\frac{4}{L_{x}L_{y}}\int_{0}^{L_{x}} \int_{0}^{L_{y}} f(x,y)\cos\left( \frac{m\pi x}{L_{x}} \right)\cos\left( \frac{n\pi y}{L_{y}} \right) \, dy  \, dx 
$$
We use:
$$
\int_{0}^{L_{x}} x^{2}(L_{x}-x)^{2}\cos\left( \frac{m\pi x}{L_{x}} \right) \, dx =-\frac{12L_{x}^{5}}{(m\pi)^{4}}(1+(-1)^{m})
$$
### Mode Decay/Growth
The function:
$$
\implies T_{mn}(t)=a_{nm}e^{ -D\left( \frac{n^{2}\pi^{2}}{L_{x}^{2}}+\frac{m^{2}\pi^{2}}{L_{y}^{2}} \right) t}
$$
as $t\to \infty$, all modes $T_{mn}(t)\to 0$ except $m=n=0$, where $u(x,y,t\to \infty)\to a_{00}$
Interestingly if $n$ and $m$ are large, they decay faster, so the heat equation simplifies the fine scale details first and eventually gets round to the other stuff
This is known as diffusion
The initial condition only matters in the long run as it determines the final average
There can be mode growth, but not with the heat equation
## Solution Using [[Fourier Transform|Fourier Transforms]]
We want the solution to the initial value problem for on the whole line, so we have $u_{t}=k^{2}u_{x x}$, and $u(x,0)=R(x)$. Start by taking the fourier transform with respect to $x$:
$$
\tilde{u}_{t}=k^{2}(ip)^{2}\tilde{u}=-k^{2}p^{2}\tilde{u}
$$
Which is a [[First Order Ordinary Differential Equations|first order ODE]],  so
$$
\tilde{u}=A(p)e^{ -k^{2}p^{2}t }
$$
$$
 \tilde{u}(p,0)=A(p)=\int_{-\infty}^{\infty} u(x,0) \, dx =\int_{-\infty}^{\infty} R(x)e^{ ipx } \, dx =\tilde{R}(p)
$$
$$
\implies \tilde{u}(p,t)=\tilde{R}(p)e^{ -k^{2}p^{2}t }=\tilde{R}(p)\tilde{g}(p)
$$
Which is a [[Gaussian Integral|gaussian]] in $p$. By the [[Convolution of Functions|convolution]] theorem, $u(x,t)=R(x)*g(x)$, we need to find $g(x,t)$ with fourier transform $\tilde{g}(p,t)=e^{ -k^{2}p^{2}t }$. Recall that
$$
g(x,t)=\Lambda e^{ -bx^{2}-cx }
$$
Has fourier transform:
$$
\tilde{g}(p,t)=\Lambda \sqrt{ \frac{\pi}{b} }e^{ -\frac{1}{4b}(p-ic)^{2} }=e^{ -p^{2}k^{2}t }
$$
$$
\implies c=0,\Lambda=\sqrt{ \frac{b}{\pi} },\frac{1}{4b}=k^{2}t\implies b=\frac{1}{4k^{2}t}
$$
$$
 \therefore g(x,t)=\frac{1}{2k\sqrt{ \pi t }}e^{ -\frac{x^{2}}{4k^{2}t} }
$$
$$
     \therefore  u(x,t)=R*g=\int_{-\infty}^{\infty} R(x')g(x-x') \, dx'=\int_{-\infty}^{\infty} R(x')\underbrace{ \left( \frac{1}{2k\sqrt{ \pi t }}e^{ -\frac{(x-x')^{2}}{4k^{2}t} } \right)  }_{ \text{Heat Kernel!} }\, dx'  
$$
And the heat kernel looks kinda like:
![[Heat Equation 2025-03-18 14.48.11.excalidraw]]
Note that the heat kernel satisfies the heat equation. As $t\to0$, the shape looks like:
![[Heat Equation 2025-03-18 14.49.54.excalidraw]]
Which can be thought about as having a lump of heat at $x'$. So our general solution can be thought of as using $R(x)$ to describe the distribution of spikes of heat 
## Solution Using Bessel Functions on a Disc
Want to solve
$$
\frac{ \partial u }{ \partial t } =D \nabla^{2}u
$$
On $(r,\theta)\in[0,L_{r}]\times [0,2\pi)$
We will set Dirichlet (homogeneous) radial Boundary conditions:
$$
u(L_{r},\theta,t)=0
$$
And we want periodicity in $\theta$
We shall use separation of variables:
$$
u(r,\theta,t)=R(r)\Theta(\theta)T(t)
$$
Plugging into the heat equation, we get:
$$
\frac{\dot{T}}{DT}=\frac{1}{R\Theta}\nabla^{2}(R\Theta)
$$
$$
\implies \frac{\dot{T}}{DT}=-\lambda=\frac{1}{R\Theta}\nabla^{2}(R\Theta)
$$
$$
\implies \dot{T}(t)+D\lambda T(t)=0
$$
$$
 \nabla^{2}(R\Theta)=-R\Theta\lambda
$$
(where $\nabla^{2}=\Delta$ is the [[Second Derivatives for Vector Calculus#Laplacian|laplacian]]), now we solve for the spatial modes:
The laplacian in polar coordinates:
$$
\nabla^{2}y=\frac{1}{r}\frac{ \partial  }{ \partial r }\left( r\frac{ \partial y }{ \partial r }  \right)+\frac{1}{r^{2}}\frac{ \partial^{2}y }{ \partial \theta^{2} }  
$$
In our case, $y(r,\theta)=R(r)\Theta(\theta)$:
$$
\frac{1}{r}\frac{ \partial  }{ \partial r } \left( r\frac{ \partial R\Theta }{ \partial r }  \right)+\frac{1}{r^{2}}\frac{ \partial^{2}R\Theta }{ \partial \theta^{2} } +\lambda R\Theta =0
$$
$$
\implies \Theta  \frac{1}{r}\frac{d }{dr} \left( r \frac{d R}{dr}  \right)+R  \frac{1}{r^{2}}\frac{d ^{2}\Theta}{d\theta^{2}}+\lambda RP=0
$$
$$
\implies \frac{r}{R} \frac{d }{dr} \left( r\frac{d R}{dr}  \right)+\frac{1}{\Theta}\frac{d^{2} \Theta}{d\theta^{2}}+\lambda r^{2}=0 
$$
$$
\implies \frac{r}{R}\frac{d }{dr} \left( r\frac{d R}{dr}  \right)+\lambda r^{2}=-\frac{1}{\Theta} \frac{d ^{2}\Theta}{d\theta^{2}} =\lambda_{\theta}
$$
So we do a further separation as we now have a thing dependent on only $r$ and another dependent on only $\theta$ equal to each other, so we have two eigenequations:
$$
\frac{1}{Rr}\frac{d }{dr} \left(  r \frac{d R}{dr}  \right)=\lambda-\frac{\lambda_{\theta}}{r^{2}}
$$
$$
 -\frac{1}{\Theta}\frac{d ^{2}\Theta}{d\theta^{2}} =\lambda_{\theta}
$$
We have boundary conditions, $R(L_{r})=0$, $\Theta(0)=\Theta(2\pi)$
The $\Theta$ modes:
$$
\frac{d ^{2}\Theta}{d\theta^{2}} =-\lambda_{\theta}\Theta
$$
Which we know has trigonometric solutions ($\lambda_{\theta}>0$); all others cancel immediately:
$$
\Theta(\theta)=A\cos(\sqrt{ \lambda_{\theta} }\theta)+B\sin(\sqrt{ \lambda_{\theta} }\theta)
$$
So applying boundary conditions,
$$
A\cos(0)+B\sin(0)=A=A\cos(2\sqrt{ \lambda_{\theta} }\pi)+B\sin(2\sqrt{ \lambda_{\theta} }\pi)
$$
$$
\implies 2\sqrt{ \lambda_{\theta} }=2n\pi
$$
For some $n\in\mathbb{N}_{0}$
$$
\implies \Theta(\theta)=A\cos(n\theta)+B\sin(n\theta),\lambda_{\theta }=n^{2}
$$
And we can confirm that this satisfies
$$
\frac{d \Theta}{d\theta} (0)=\frac{d \Theta}{d\theta} (2\pi)
$$
Which is a nice property of the laplacian
Next we do the $R$ modes:
$$
r^{2}\frac{d ^{2}R}{dr^{2}} +r\frac{d R}{dr} +(\lambda r^{2}-n^{2})R=0
$$
Which we know as [[Bessel's Equation]] gives that $J_{n}(r)=R_{n}(r)$
And $J_{n}(\sqrt{ \lambda_{x} }L_{r})=0$ by the dirichlet boundary conditions, wo we need $\sqrt{ \lambda_{x} }L_{r}=j_{n,k}$
So $\lambda_{n,k}$ are global eigenvalues that we can relabel. For each bessel function $J_{n}$ there are $\lambda_{n,k}$ eigenvalues for $k\in \overline{n}$
So in summeary, we have general spatial eigenmodes of our solution
$$
u(r,\theta,t)=T(t)\Phi(r,\theta)
$$
Where we say
$$
\Phi_{n,k}(r,\theta)=J_{n}(\sqrt{ \lambda_{k,n} }r)\cos(n\theta)
$$
Or 
$$
\Phi_{n,k}(r,\theta)=J_{n}(\sqrt{ \lambda_{k,n} })\sin(n\theta)
$$
So for full spatial behavior, we sum over $n$ and $k$:
$$
\Phi(r,\theta)=\sum_{n=0}^{\infty}\sum_{k=1}^{\infty}\Phi(n,k)(r,\theta)
$$

We do this for $n>0$, $J_{n}(0)=0$ and $j_{n,0}=0$ (eqwuivalent to $\sin(0x)=0$)
We have $J_{0}(0)=1$ and the homogeneouus dirichlet boundary conditions require $R_{n}(r)=0$, so we cannot have $J_{0}$($\hspace{0pt}0$,r)
Crucially we have an infinite sum of functions $\sin(n\theta),\cos(n\theta),J_{n}(\sqrt{ \lambda_{n,k}r\ })$ which can come from eigenvalue problems, so it has the same structure of as the fourier series
Finally, we solve for the time dependent behaviour:
$$
\dot{T}(t)+D\lambda_{k,n}T(t)=0 
$$
$$
\implies T_{k,n}(t)=C_{k,n}e^{ -D\lambda_{k,n} }
$$
Soooo
$$
u(r,\theta,t)=\sum_{n=0}^{\infty}\sum_{k=1}^{\infty}e^{ -D\lambda_{k,n}t }J_{n}(\sqrt{ \lambda_{k,n} }r)(A_{k,n}\cos(n\theta)+B_{k,n}\sin(n\theta))
$$

