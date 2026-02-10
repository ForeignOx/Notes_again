The wave equation is a [[Second Order Partial Differential Equations|second order]] [[Linear Partial Differential Equations|linear PDE]] of the form
$$
u_{tt}=c^{2}u_{x x}
$$
$$
\implies c^{2}u_{ x x}-u_{tt}=0
$$
$$
\implies M=\begin{pmatrix}
c^{2}&0\\0&-1
\end{pmatrix}
$$
$$
\implies \det(M)=-c^{2}<0
$$
So the Wave equation is a hyperbolic PDE
On the whole line, the general solution is:
$$
u(x,t)=f(x-ct)+g(x+ct)
$$
We can think of this as having two lumps $f$ and $g$, moving along a line at speed $c$ towards each other:
![[Wave Equation 2025-02-27 14.53.07.excalidraw]]
## Derivation
![[Wave Equation 2025-03-03 14.15.45.excalidraw]]
If you have a thin string which lies along the $x$-axis, and is moved a small distance in an orthogonal direction (for example plucking the strings on a musical instrument) called $u$. Acceleration is $\ddot{u}$, but $u=u(x,t)$, so this is in fact $\frac{ \partial^{2}u }{ \partial t^{2} }$. The string is uniform with [[Density|density]] (mass per unit length) $\rho$; so the mass of the piece from $x$ to $\delta x$ is $\rho\delta x$. The force comes from the [[Tension|tension]] along the string: it is a vector $\underline{T}$ with constant magnitude $T$. The force acts on a piece of string between $x$ and $x+\delta x$
We will assume $\theta$ is small since there was only a small displacement. The $x$-component of the force involves $T\cos(\theta)$ (positive at $x+\delta x$, but negative at $x$); but $\cos(\theta)= 1-\frac{\theta^{2}}{2}+\dots \approx1$, so no net $x$-component. The $u$-component is $T\sin(\theta)(x+\delta x)-T\sin(\theta)x$, so the equation of motion is:
$$
(\rho\delta x)\frac{ \partial^{2}u }{ \partial t^{2} } =T(\sin(\theta)(x+\delta x)-\sin(\theta)x)
$$
However, since $\theta$ is small, we can say $\sin\theta \approx\theta \approx \tan\theta=\frac{\delta u}{\delta x}$, and by dividing by $\rho\delta x$, our equation becomes:
$$
\frac{ \partial^{2}u }{ \partial t^{2} } =\frac{T}{\rho} \frac{1}{\delta x}\left( \frac{\delta u}{\delta x}(x+\delta x)-\frac{\delta u}{\delta x}(x) \right)
$$
Now we take the limit as $\delta x\to0$, where we say (assume) that $\frac{\delta u}{\delta x}=\frac{ \partial u }{ \partial x }$, and we also use the definition of the derivative that:
$$
\lim_{ \delta x \to 0 }  \frac{f(x+\delta x)-f(x)}{\delta x}=\frac{ \partial f }{ \partial x } 
$$
Where we put $f=\frac{ \partial u }{ \partial x }$, so we get
$$
\frac{ \partial^{2}u }{ \partial t^{2} } =\frac{T}{\rho}\frac{ \partial^{2}u }{ \partial x^{2} } 
$$
Which we tend to rewrite:
$$
u_{tt}=c^{2}u_{x x}
$$
Where $c=\sqrt{ \frac{T}{\rho} }$ is the wave speed
## General Solution
Let $f(p)$ be a function of one variable $p$, and take $u(x,t)=f(x-ct)$, (so we are letting $p=x-ct$) then we can substitute this in after doing a bit of brunt work using the [[Chain Rule|chain rule]]:
$$
\frac{ \partial u }{ \partial x } =\frac{d f}{dp} \frac{ \partial p }{ \partial x } =\frac{d f}{dp} 
$$
$$
\implies \frac{ \partial^{2}u }{ \partial x^{2} } =\frac{ \partial  }{ \partial x } \left( \frac{d f}{dp}  \right)=\frac{d ^{2}f}{dp^{2}} 
$$
$$
\frac{ \partial u }{ \partial t } =\frac{d f}{dp} \frac{ \partial p }{ \partial t } =\frac{d f}{dp} (-c)
$$
$$
\implies \frac{ \partial^{2}u }{ \partial t^{2} }-0c\frac{ \partial  }{ \partial t } \left( \frac{d f}{dt}  \right)=-c\frac{d ^{2}f}{dp^{2}} (-c)=c^{2}\frac{d ^{2}f}{dp^{2}}  
$$
So this equation must be a solution to the wave equation as:
$$
\frac{ \partial^{2}u }{ \partial t^{2} } -c^{2}\frac{ \partial^{2}u }{ \partial x^{2} } =c^{2}\frac{d ^{2}f}{dp^{2}} -c^{2}\frac{d ^{2}f}{dp^{2}} =0
$$
So $u(x,t)=f(x-ct)$ represents a wave travelling along the string for any $f(p)$. Take for example $f(p)$ :
![[Wave Equation 2025-03-03 14.46.26.excalidraw]]
Then we can make the same shape for
![[Wave Equation 2025-03-03 14.47.22.excalidraw]]
We can consider $t=10$,
![[Wave Equation 2025-03-03 14.49.40.excalidraw]]
This is a wave travelling rightwards with speed $c$, but the profile is the same
Another solution of the wave equation is obtained by taking any function $g(q)$ and putting
$$
u(x,t)=g(x+ct)
$$
Which is a wave of fixed shape moving in negative direction at speed $c$
Since the wave equation is [[Linear|Linear]] in $u$, if $u_{1},u_{2}$ are solutions, then so is $u=u_{1}+u_{2}$, so for any $f(p),g(q)$, the function
$$
u(x,t)=f(x-ct)+g(x+ct)
$$
We claim that this is the general solution
We need to prove that if we specify initial conditions at $t=0$, namely $u(x,0)=R(x)$, the initial position, and $\frac{ \partial u }{ \partial t }(x,t)|_{t=0}=S(x)$, the initial velocity, then we need to find $f(p),g(q)$ such that
$$
u(x,t)=f(x-ct)+g(x+ct)
$$
Has those initial conditions
### Proof
We have 
$$
u(x,0)=f(x)+g(x)=R(x)
$$
$$
\dot{u}(x,0)=c(g'(x)-f'(x))=S(x)
$$
By integrating with respect to $x$, we get
$$
-cf(x)+cg(x)=\int_{0}^{x} S(x) \, dx 
$$
So we can solve these to get:
$$
f(x)=\frac{1}{2}\left( R(x)-\frac{1}{c}\int_{0}^{x} S(x) \, dx  \right)
$$
$$
 g(x)=\frac{1}{2}\left( R(x)+\frac{1}{c}\int_{0}^{x} S(x) \, dx  \right)
$$
Which proves that $f(x-ct)+g(x+ct)$ is the general solution
## D'Alembert's Formula
We've shown that
$$
u(x,t)=\frac{1}{2}\left( R(x-ct)-\frac{1}{c}\int_{0}^{x-ct} S(x) \, dx  \right)+\frac{1}{2}\left( R(x+ct)+\frac{1}{c}\int_{0}^{x+ct} S(x) \, dx  \right)
$$
And since $\int_{0}^{a}-\int_{0}^{b}=\int_{b}^{a}$, we have
$$
u(x,t)=\frac{1}{2}(R(x-ct)+R(x+ct))+\frac{1}{2c}\int_{x-ct}^{x+ct} S(x) \, dx 
$$
### Proof Using [[Fourier Transform|Fourier Transforms]]
If we have $u_{tt}=c^{2}u_{x x},u(x,0)=R(x),u_{t}(x,0)=S(x)$, then we can take fourier transforms of both sides to get:
$$
\tilde{u}_{tt}=c^{2}(ip)^{2}\tilde{u}=-c^{2}p^{2}\tilde{u}
$$
Which is an ODE, in fact it is [[Simple Harmonic Motion|SHM]], so
$$
\tilde{u}(p,t)=A(p)\cos(cpt)+B(p)\sin(cpt)
$$
$$
 \tilde{u}(p,0)=A(p)=\tilde{R}(p)
$$
$$
 \tilde{u}_{t}(p,t)=-cpA(p)\sin(cpt)+cpB(p)\cos(cpt)
$$
$$
 \tilde{u}_{t}(p,0)=cpB(p)=\int_{-\infty}^{\infty} u_{t}(x,0)e^{ -ipx } \, dx =\int_{-\infty}^{\infty} S(x)e^{ -ipx } \, dx =\tilde{S}(p)
$$
Soooo
$$
\tilde{u}(p,t)=\tilde{R}(p)\cos(cpt)+\frac{\tilde{S}}{pc}\sin(cpt)
$$
So we need to find some function $u(x,t)$ which has this as its fourier transform. Note
$$
\tilde{R}(p)\cos(pct)=\frac{\tilde{R}(p)e^{ icpt }}{2}+\frac{\tilde{R}(p)e^{ -icpt }}{2}
$$
Which by shift theorem is the fourier transform of
$$
\frac{1}{2}R(x+ct)+\frac{1}{2}R(x-ct)
$$
Next we consider
$$
\frac{\tilde{S}(p)\sin(pct)}{pc}=\tilde{S}(p)\tilde{g}(p)
$$
If we can find $g(x)$ with Fourier Transform $\tilde{g}(p)$, then by the [[Convolution|convolution]] theorem, $S(x)*g(x)$ will have this fourier transform. We can recall that the fourier transform of:
$$
F(x)=\begin{cases}
1 & \left| x \right| <1\\0 & \left| x \right| >1
\end{cases}
$$
Is
$$
\tilde{F}(p)=\frac{2\sin(p)}{p}
$$
Then if we let $g(x)=KF(bx)$ for $b>0$, then by the scaling theorem:
$$
\tilde{g}(p)=\frac{K}{b}\tilde{F}\left( \frac{p}{b} \right)=\frac{\frac{K}{b}2\sin\left( \frac{p}{b} \right)}{\frac{p}{b}}=\frac{2K\sin\left( \frac{p}{b} \right)}{p}=\frac{\sin(pct)}{pc}
$$
$$
\implies K=\frac{1}{2c},b=\frac{1}{ct}
$$
Therefore
$$
g(x)=\frac{1}{2x}F\left( \frac{x}{ct} \right)=\begin{cases}
\frac{1}{2c} & \left| \frac{x}{ct} \right| <1\\0 & \text{otherwise}
\end{cases}
$$
So now we need
$$
S(x)*g(x)=\int_{-\infty}^{\infty} S(x')g(x-x') \, dx'=\frac{1}{2c}\int_{x-ct}^{x+ct} S(x') \, dx'
$$
$$
 \therefore u(x,t)=\frac{1}{2}(R(x+ct)+R(x-ct))+\frac{1}{2c}\int_{x-ct}^{x+ct} S(x') \, dx'   
$$
## 2D Solution With Separation of Variables
Let $u(x,y,t)=X(x)Y(y)T(t)$
Then we perform the separation:
$$
\frac{\ddot{T}}{c^{2}}XY=X''YT+Y''XT
$$
$$
\implies \frac{\ddot{T}}{cT}=\frac{X''}{X}+\frac{Y''}{Y}
$$
This can only be satisfied for all $x,y,t$ if
$$
\frac{\ddot{T}}{CT}=-\lambda_{t}
$$
$$
\frac{X''}{X}=-\lambda_{x}
$$
$$
 \frac{Y''}{Y}=-\lambda_{y}
$$
So we need $\lambda_{t}=\lambda_{x}+\lambda_{y}$ (the minus sign is a common convention to solve ODEs with positive $\lambda$), we are caling the $\lambda$'s [[Eigenvalues|eigenvalues]]
$$
\implies X''+\lambda_{x}X=0
$$
$$
 Y''+\lambda_{y}Y=0
$$
$$
 \ddot{T}+c^{2}\lambda_{t}T=0
$$
With [[Neumann Boundary Conditions|Neumann boundary conditions]],
$$
X'(0)=X'(L_{x})=Y'(0)=Y'(L_{y})=0
$$
We solve for the spatial modes:
$$
X''+\lambda_{x}X=0
$$
If $\lambda_{x}>0$, assume $X=Ae^{ kx }\implies k^{2}+\lambda_{k}=0\implies k=\pm i\sqrt{ \lambda_{x} }$, so by de Moivre:
$$
X=A_{1}e^{ i\sqrt{ \lambda_{x} } x}+A_{2}e^{ -i\sqrt{ \lambda_{x} }x }=A\cos(\sqrt{ \lambda_{x} }x)+B\sin(\sqrt{ \lambda_{x} }x)
$$
So using our initial conditions,
$$
X'(0)=B\sqrt{ \lambda_{x} }=0\implies B=0
$$
$$
 X'(L_{x})=\sin(\sqrt{ \lambda_{x} }L_{x})=0
$$
$$
\implies \sqrt{ \lambda_{x} }=\frac{n\pi}{L_{x}}\implies \lambda_{x}=\frac{n^{2}\pi^{2}}{L_{x}^{2}}
$$
For $n\in\mathbb{N}_{0}$, So
$$
X(x)=A\cos\left( \frac{n\pi}{L_{x}}x \right)
$$
Which is our eigenfunction for the eigenvalue $\lambda_{x}$
If $\lambda_{x}<0$, then
$$
X(x)=Ae^{ \sqrt{ \lambda_{x} }x }+Be^{ -\sqrt{ \lambda_{x} }x }
$$
Applying boundary conditions,
$$
X'(0)=A\sqrt{ \lambda_{x} }-B\sqrt{ \lambda_{x} }=0
$$
$$
 X'(L_{x})=A\sqrt{ \lambda_{x} }e^{ \sqrt{ \lambda_{x} }L_{x} }-B\sqrt{ \lambda_{x} }e^{ -\sqrt{ \lambda_{x} } L_{x}}
$$
Which requires $A=B=0$
If $\lambda_{x}=0$, then $X(x)=Ax+B$, which satisfies the boundary conditions only if $A=0$, so we don't really care 
The $Y$ equation thankfully is identical, so $Y(y)=B\cos\left( \frac{n\pi}{L_{y}}y \right)$ 
So in general the spatial eigenmodes of $u$ take the form:
$$
\Phi(x,y)=X_{m}(x)Y_{n}(y)=a_{mn}\cos\left( \frac{m\pi x}{L_{x}} \right)\cos\left( \frac{n\pi y}{L_{y}} \right)
$$
And
$$
\lambda_{mn}=\lambda_{x}+\lambda_{y}=\left( \frac{m\pi}{L_{x}} \right)^{2}+\left( \frac{n\pi}{L_{y}} \right)^{2}
$$
For any combination of $m,n\in \mathbb{N}_{0}$
Finally we look for our temporal nodes, we need $\lambda_{t}=\lambda_{x}+\lambda_{y}$, so we know $\lambda_{t}$:
$$
\lambda_{t}^{nm}=\left( \frac{m\pi}{L_{x}} \right)^{2}+\left( \frac{n\pi}{L_{y}} \right)^{2}
$$
The crucial point is that the boundary conditions determined the values of $\lambda_{x},\lambda_{y}$, in turn they determine $\lambda_{t}$
$$
\ddot{T}_{mn}+c^{2}\lambda_{mn}T_{mn}
$$
For $(m,n)\neq (0,0)$,
$$
T_{mn}(t)=A_{mn}\cos(c\omega_{mn}t)+B_{mn}\sin(c\omega_{mn}t)
$$
Where $\omega_{mn}=\sqrt{ \lambda_{mn} }$
We could also have $m=n=\lambda_{mn}=0$, so
$$
\ddot{T}_{00}=0\implies T_{00}(t)=A_{00}+B_{00}t
$$
Note that $c^{2}\lambda_{mn}$ cannot be negative, so no exponential solutions
Sooo our general separated solution is:
$$
u(x,y,t)=A_{00}+B_{00}t
$$
$$
 +\sum_{m=0}^{\infty}\sum_{n=0}^{\infty}(A_{mn}\cos(c\omega_{mn}t)+B_{mn}\sin(c\omega_{mn}t))\left( \cos\left( \frac{mnx}{L_{x}} \right)\cos\left( \frac{n\pi y}{L_{y}} \right) \right)
$$
Where 
$$
\omega_{mn}=\sqrt{ \left( \frac{m\pi}{L_{x}} \right)^{2} +\left( \frac{n\pi}{L_{y}} \right)^{2}}
$$
We usually decide $B_{00}=0$ and rule our linear growth as this is rare to encounter in real life, as we would have unbounded growth... Mathematically it's chill
There are any spacial modes, the fourier series is not the most general object one can work with
## Examples
An infinite string is plucked, so $S(x)=0$, with $R(x)=e^{ -x^{2} }$. Then
$$
u(x,t)=\frac{1}{2}e^{ -(x-ct)^{2} }+\frac{1}{2}e^{ -(x+ct)^{2} }
$$
```desmos-graph
R\left(x\right)=e^{-x^{2}}
S\left(x\right)=0
t=1.8
c=2.3
\frac{1}{2}\left(R\left(x-ct\right)+R\left(x+ct\right)\right)+\frac{1}{2c}\int_{x-ct}^{x+ct}S\left(a\right)da
```
Instead, strike the string, so $R(x)=0$, take $S(x)=xe^{ -x^{2} }$, here $\int S(x)  \, dx=-\frac{1}{2}e^{ -x^{2} }$ and
$$
u(x,t)=-\frac{1}{4c}(e^{ -(x+ct)^{2} }-e^{ -(x-ct)^{2} })
$$
```desmos-graph
R\left(x\right)=0
S\left(x\right)=xe^{-x^{2}}
t=1.8
c=1
\frac{1}{2}\left(R\left(x-ct\right)+R\left(x+ct\right)\right)+\frac{1}{2c}\int_{x-ct}^{x+ct}S\left(a\right)da
```
___
Solve $4\frac{ \partial^{2}u }{ \partial t^{2} }=\frac{ \partial^{2}u }{ \partial x^{2} }$ with $u(x,0)=\frac{1}{1+x^{2}}$, and $\frac{ \partial u }{ \partial t }(x,t)|_{t=0}=\frac{x}{(1+x^{2})^{2}}$, this has the solution
$$
\int S \, dx =\int \frac{x}{(1+x^{2})^{2}} \, dx =-\frac{1}{2} \frac{1}{1+x^{2}}=-\frac{1}{2}R(x)
$$
(note $c=\frac{1}{2}$), so
$$
u(x,t)=\frac{1}{2}R(x+ct)+\frac{1}{2}R(x-ct)-\frac{1}{2}R(x+ct)+\frac{1}{2}R(x-ct)=R(x-ct)=\frac{1}{1+(x-ct)^{2}}
$$
$$
=\frac{1}{1+\left( x-\frac{t}{2} \right)^{2}}
$$
## String with $\hspace{0pt}1$ Boundary Condition
Say the string lies on $x\geq 0$ and is fixed at $x=0$ by the boundary condition $u(0,t)=0\forall t$. The general solution
$$
u(x,t)=f(x-ct)+g(x+ct)
$$
Satisfies this boundary condition iff $f(-ct)+g(ct)=0\forall t$ (substitute $x=0$). This means however that $f$ and $g$ are no longer independent:
$$
g(q)=-f(-q)
$$
So one of the functions, say $f$, is arbitrary, whereas $g$ is not or vice versa.
For example take $f(p)=e^{ -p^{2} }$, then
$$
u(x,t)=e^{ -(x-ct)^{2} }-e^{ -(x+ct)^{2} }
$$
And we can check that 
$$
u(0,t)=e^{ -(ct)^{2} }-e^{ -(ct)^{2} }=0
$$
```desmos-graph
f\left(x\right)=e^{-x^{2}}|hidden
c=1
u\left(x\right)=f\left(x-ct\right)-f\left(x+ct\right)
t=5.08
```
![[Wave Equation 2025-03-17 14.20.32.excalidraw]]
## String with Two Boundary Conditions
For two boundary conditions, a string will create harmonics, which we can usually solve with [[Fourier Series|fourier series]]
