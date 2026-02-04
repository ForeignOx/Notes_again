## [[Linear Partial Differential Equations|Linear]] [[Partial Differential Equations|PDEs]] of Two Variables
If we have some function $u(x,t)$, then we have a general partial differential equation:
$$
Au_{xx}+2Bu_{xt}+Cu_{tt}+Du_{x}+Eu_{t}+Fu=0
$$
Where $A,B,C,D,E,F$ could depend on $x,t$
PDEs are classified according to the sign of
$$
\det(M),M=\begin{pmatrix}
A&B\\B&C
\end{pmatrix}
$$
### Hyperbolic PDE
If $\det(M)<0$, then the PDE is hyperbolic. An equation of this form is the [[Wave Equation|Wave equation]]
These describe propagation along lines
### Parabolic PDE
If $\det (M)=0$, then the PDE is parabolic. An equation of this form is the [[Heat Equation|Heat equation]] 
### Elliptic PDE
If $\det(M)>0$, then the PDE is elliptical. An equation of this form is [[Laplace's Equation|Laplace's Equation]]
___
A linear PDE solution space is an infinite-[[Dimension|dimensional]] [[Vectorspaces|vectorspace]], so
$$
u(x,t)=\sum_{i} a_{i}u_{i}(x,t) 
$$
Which is an infinite sum (or an integral)
We need to specify $\infty$ of $a_{i}$ numbers (or functions) to pin down $u$
___
## Important Examples
Consider an IVP on the whole line $x$, for example the transverse displacement of infinitely long string obeys the wave equation $u_{tt}=c^{2}u_{x x}$:
![[Second Order Partial Differential Equations 2025-02-28 15.25.24.excalidraw]]
We can define the initial position $u(x,0)=R(x)$, and the initial velocity $u_{t}(x,0)=S(x)$
If instead we have an infinitely long bar of metal, we might want to use the heat equation to model its heat, so it obeys $u_{t}=k^{2}u_{x x}$
![[Second Order Partial Differential Equations 2025-02-28 15.28.04.excalidraw]]
For the heat equation on the whole line we need $u(x,0)=R(x)$
If we switch to finite pieces of string/metal, we instead do things on an interval $x\in[a,b]$ and we can consider the $xt$-plane:
![[Second Order Partial Differential Equations 2025-02-28 15.29.55.excalidraw]]
For the wave equation, at $t=0,u(x,0)=R(x)$ for $a\leq x\leq b$, and $u_{t}(x,0)=S(x)$ for $a\leq x\leq b$
But we need to specify what happens at the endpoints; boundary conditions: 
- $u(b,t)=0$ would be known as a fixed end Dirichlet boundary condition
- $u_{x}(b,t)=0$ would be known as a fixed end Neumann boundary condition
- And the same thing but at $x=a$
For the heat equation, it's the same except for the first part, we don't need $u_{t}$, so only $u(x,0)=R(x)$
For Laplace's equation, we have a similar sort of thing, but we either specify $u$ or a normal derivative of $u$ on boundary
## Method of Separation of Variables
The solution space will look like:
$$
u(x,t)=\sum_{i}a_{i}u_{i}(x,t)
$$
Where the $u_{i}(x,t)$ are our [[Basis|basis]] [[Functions|functions]]. We will choose basis functions of the form:
$$
u_{i}(x,t)=X_{i}(x)T_{i}(t)
$$
Such that we can separate out $x$ and $t$
___
### Example
For a string lying between $x=0,x=\pi$, this has transverse displacement and obeys the wave equation $u_{tt}=c^{2}u_{x x}$ at ends $u(0,t)=u(\pi,t)=0$
We can impose initial conditions $u_{t}(x,0)=0$,
$$
u(x,0)=R(x)=\begin{cases}
x&0\leq x\leq \frac{\pi}{2}\\ \pi-x&  \frac{\pi}{2}\leq x\leq \pi
\end{cases}
$$
So we look for a solution satisfying these of the form $u(x,t)=X(x)T(t)$, we substitue into the wave equation:
$$
u_{tt}=X\ddot{T}=c^{2}u_{x x}X''T
$$
Dividing through by $c^{2}XT$:
$$
\frac{X\ddot{T}}{c^{2}XT}=\frac{c^{2}X''T}{c^{2}XT}
$$
$$
\implies \frac{\ddot{T}}{c^{2}T}=\frac{X''}{X}
$$
Since these are two functions of different variables, they can only be equal if they are both constant, so our PDE has become $\hspace{0pt}2$ ODEs, yayy:
$$
X''=\lambda X
$$
$$
 \ddot{T}=\lambda c^{2}T
$$
Hmm these look like [[Eigenvalues|eigenvalue]]/eigenfunction equations.
From our initial conditions, we also have:
$$
u(0,t)=X(0)T(t)=0
$$
$$
 u(\pi,t)=X(\pi)T(t)=0
$$
We assume $T(t)\neq 0$, so we have
$$
X(0)=X(\pi)=0
$$
If $\lambda=n^{2}>0$, then
$$
X''=n^{2}X
$$
$$
\implies X=Ce^{ nx }+De^{ nx }=A\sinh(nx)+B\cosh(nx)
$$
$$
X(0)=0=B\implies X=A\sinh(nx)
$$
$$
 X(\pi)=A\sinh(nx)=0\implies A=0
$$
So $X=0$ in this case. This is not very interesting so we consider more stuff:
If $\lambda=0$, then
$$
X=Ax+B
$$
But $X(0)=X(\pi)=0$ means that we have a straight line going through $(0,0),(0,\pi)$ which must mean $X=0$, also uninteresting
If $\lambda=-n^{2}<0$, then
$$
X''=-n^{2}X
$$
$$
\implies X=A\cos(nx)+B\sin(nx)
$$
$$
 X(0)=0=A\implies X=B\sin(nx)
$$
$$
 X(\pi)=B\sin(n\pi)=0
$$
Vanishes for non-zero $B$ when $n\in\mathbb{N}$, therefore $X=A\sin(nx)$
We also have
$$
\ddot{T}=-n^{2}c^{2}T
$$
$$
\implies T=A_{n}\cos(nct)+B_{n}\sin(nct)
$$
So
$$
u(x,t)=X(x)T(t)=\sin(nx)(A_{n}\cos(nct)+B_{n}\sin(nct))
$$
So there are many solutions depending on $n$, in fact infinite solutions for each $n$. We can think of the $\sin(nx)\cos(nct)$ and $\sin(nx)\sin(nct)$ as the basis vectors, and we take a [[Linear Combinations|linear combination]] of them. So we can claim that if we sum all of them together, we have a general general solution:
$$
\sum_{n=1}^{\infty} \sin(nx)(A_{n}\cos(nct)+B_{n}\sin(nct)) 
$$
For example for $n=1$ we have a linear combination:
$$
A_{1}\sin(x)\cos(ct)+B_{1}\sin(x)\sin(ct)
$$
Which is made up of two terms, the first of which, at $t=0$ has displacement, but no velocity, then the second term has velocity, but no displacement (by taking the time derivative)
This is essentially a wobbly line like so:
![[Second Order Partial Differential Equations 2025-03-04 14.19.09.excalidraw]]
For $n=2$, we instead have:
$$
A_{2}\sin(2x)\cos(2ct)+B_{2}\sin(2x)\sin(2ct)
$$
And looks like:
![[Second Order Partial Differential Equations 2025-03-04 14.22.08.excalidraw]]
Which is double the frequency, so we can think of it as playing an octave higher. Similarly $n=3$ looks like:
![[Second Order Partial Differential Equations 2025-03-04 14.23.08.excalidraw]]
Now we consider the time derivative, the velocity:
$$
u_{t}(x,t)=\sum_{n=1}^{\infty}\sin(nx)(-ncA_{n}\sin(nct)+ncB_{n}\cos(nct))
$$
Using our initial contitions:
$$
u_{t}(x,t)=0=\sum_{n=1}^{\infty}ncB_{n}\sin(nx)\implies B_{n}=0
$$
So
$$
u(x,t)=\sum_{n=1}^{\infty}A_{n}\sin(nx)\cos(nct)
$$
We also have 
$$
u(x,0)=R(x)=\sum_{n=1}^{\infty} A_{n}\sin(nx) 
$$
Which is periodic with period $2\pi$. Now $\sin$ is odd, so this sum is in fact the odd extension of $R(x)$
![[Second Order Partial Differential Equations 2025-03-04 14.29.41.excalidraw]]
So we can work out the coefficients of using the half-range $\sin$ series;
$$
A_{n}=\frac{2}{\pi}\int _{0}^{\pi}R(x)\sin(nx) \, dx 
$$
$$
= \frac{2}{\pi}\int_{0}^{\pi/2} x\sin(nx) \, dx +\frac{2}{\pi}\int_{\frac{\pi}{2}}^{\pi} (\pi-x)\sin(nx)  \, dx =\frac{4}{\pi n^{2}}\sin\left( \frac{n\pi}{2} \right)
$$
Soooo
$$
u(x,t)=\sum_{n=1}^{\infty} \frac{4}{\pi n^{2}}\sin\left( \frac{n\pi}{2} \right)\sin(nx)\cos(nct)
$$
$$
= \frac{4}{\pi}\sin(x)\cos(ct)-\frac{4}{9\pi}\sin(3x)\cos(3ct)+\dots
$$
(note the first overtone vanishes)
```desmos-graph
c=1
t=15
y=\sum_{n=1}^{100}\frac{4}{\pi n^{2}}\sin\left(\frac{n\pi}{2}\right)\sin\left(nx\right)\cos\left(nct\right)
```
___
Further example
Consider if we have a piano that we are hitting with a piano, so for some $(0,\varepsilon)$ we give it velocity
![[Second Order Partial Differential Equations 2025-03-04 14.37.56.excalidraw]]
We have these conditions:
$$
u_{tt}=c^{2}u_{x x}
$$
$$
 u(0,t)=u(\pi,t)=0
$$
$$
 u(x,0)=0
$$
$$
 u_{t}(x,0)=S(x)=\begin{cases}
1&0\leq x\leq \varepsilon\\0&\varepsilon <x\leq \pi
\end{cases}
$$
We have our first two identical to the previous example, so we already know the general solution will be:
$$
u(x,t)=\sum_{n=1}^{\infty}\sin(nx)(A_{n}\cos(nct)+B_{n}\sin(nct))
$$
$$
u(x,0)=0=\sum_{n=1}^{\infty}A_{n}\sin(nx)\implies A_{n}=0
$$
$$
 u(x,t)=\sum_{n=1}^{\infty}\sin(nx)B_{n}\sin(nct)
$$
$$
u_{t}(x,t)=\sum_{n=1}^{\infty}\sin(nx)(ncB_{n})\cos(nct)
$$
$$
 u_{t}(x,0)=S(x)=\sum_{n=1}^{\infty}ncB_{n}\sin(nx)=\sum_{n=1}^{\infty}D_{n}\sin(nx)
$$
We can use Fourier series again to find the $D_{n}$'s but we also know that
$$
X(x)=\sin(nx)
$$
Solves
$$
X''=-n^{2}X
$$
Which is an [[Eigenfunctions|eigenfunction]] of [[Linear Differential Operators|$\mathcal{L}=\frac{d }{dx^{2}}$]], so we can guess that we have the [[Inner Product|inner product]]
$$
(f,g)=\int_{0}^{\pi} fg \, dx 
$$
So we need to show $\mathcal{L}$ is [[Self-Adjoint|self-adjoint]], 
$$
(\mathcal{L}f,g)=(f,\mathcal{L}g)
$$
$$
(\mathcal{L}f,g)=(f'',g)=\int_{0}^{\pi} f''g \, dx =[f'g-fg']_{0}^{\pi}+\int_{0}^{\pi} fg'' \, dx 
$$
And if $f,g$ are $0$ at $x=0,\pi=0$, so 
$$
[f'g-fg']_{0}^{\pi}+\int_{0}^{\pi} fg'' \, dx =0+(f,\mathcal{L}g)
$$
Which is what we wanted, so our eigenfunctions are orthogonal, i.e. 
$$
(\sin(nx),\sin(mx))=\delta_{nm}
$$
(Using the [[Kronecker Delta Function|Kronecker delta here]])
Soooo
$$
S(x)=\sum_{n=1}^{\infty}D_{n}\sin(nx)
$$
And we can consider the dot product with the eigenfunctions:
$$
(S(x),\sin(mx))=\sum_{n=1}^{\infty}D_{n}(\sin(nx),\sin(mx))=D_{m}(\sin(mx),\sin(mx))
$$
As all other terms vanish, soo
$$
D_{m}=\frac{(S(x),\sin(mx))}{(\sin(mx),\sin(mx))}=\frac{\int_{0}^{\pi} S(x)\sin(mx) \, dx }{\int_{0}^{\pi} \sin ^{2}(mx) \, dx }=\frac{2}{\pi}\int_{0}^{\pi} S(x)\sin(mx) \, dx 
$$
Which is what we would have gotten with Fourier, and now we substitute:
$$
=\frac{2}{\pi}\int_{0}^{\varepsilon} \sin(mx) \, dx =\frac{2}{\pi m}(1-\cos(m\varepsilon))=B_{m}mc
$$
So
$$
u(x,t)=\sum_{n=1}^{\infty}B_{n}\sin(nx)\sin(nct)=\sum_{n=1}^{\infty} \frac{2}{\pi n^{2}c}(1-\cos(n\varepsilon))\sin(nx)\sin(nct)
$$
___
If we have a bar of metal which lies between $x=0$ and $x=\pi$, it's temperature $u(x,t)$ satisfies the heat equation and initial conditions: 
- $u_{t}=k^{2}u_{x x}$
- $u(0,t)=0$ left-hand side kept at $0^{\circ}$
- $u_{x}(\pi,t)=0$ right-hand side insulated
- $u(x,0)=100$, starts at $100^{\circ}$
We look for a solution to the general heat equation satisfying those end conditions in the form:
$$
u(x,t)=X(x)T(x)
$$
The heat equation implies
$$
X\dot{T}=k^{2}X''T
$$
Dividing through by $k^{2}XT$
$$
\implies \frac{X\dot{T}}{k^{2}XT}=\frac{k^{2}X''T}{k^{2}XT}
$$
$$
\implies \frac{\dot{T}}{k^{2}T}=\frac{X''}{X}
$$
So we have a function of $t$ on the left-hand side, and a function of $x$ on the right-hand side, so both must be constant:
$$
X''=\lambda X
$$
$$
 \dot{T}=\lambda k^{2}T
$$
We are also looking for a solution which solves the end-conditions
$$
u(0,t)=0=X(0)T(t)
$$
$$
 u_{x}(\pi,t)=0=X'(\pi)T(t)
$$
We can't have $T$ vanishing as this is boooring, so $X(0)=0,X'(\pi)=0$
So we need to solve $X''=\lambda X$ subject to $X(0)=X'(\pi)=0$, we do this by considering three cases:
If $\lambda=n^{2}>0$, then $X=A\sinh(nx)+B\cosh(nx)$, letting $X(0)=B=0$, gives us $B$ vanishing. $X'(\pi)=An\cosh(n\pi)\implies A=0$, so this condition gives us nothing :(
If $\lambda=0$, then $X=Ax+B$, $X(0)=B=0$, $X'(\pi)=A=0$, so this also gives nothing
If $\lambda=-n^{2}<0$ gives $X=A\sin(nx)+B\cos(nx)$, $X(0)=B=0$, then $X'(\pi)=An\cos(n\pi)=0$, which vanishes when $n=m+\frac{1}{2},m\in\mathbb{N}_{0}$, so our solution is:
$$
X=\sin\left( \left( m+\frac{1}{2} \right)x \right)
$$
When $m=0,X=\sin\left( \frac{x}{2} \right)$, which looks like:
![[Second Order Partial Differential Equations 2025-03-06 14.18.54.excalidraw]]
And we have 
$$
\lambda=-n^{2}=-\left( m+\frac{1}{2} \right)^{2}
$$
We also have
$$
\dot{T}=\lambda k^{2}T=-\left( m+\frac{1}{2} \right)^{2}k^{2}T
$$
$$
\implies T\propto e^{ -k^{2}\left( m+\frac{1}{2} \right)^{2}t }
$$
So
$$
u(x,t)=\sin\left( \left( m+\frac{1}{2} \right)x \right)e^{ -k^{2}\left( m+\frac{1}{2} \right)^{2}t }
$$
So we have solutions for each $n$, so by the principle of superposition, we have a general solution (for any heat equation with those initial conditions):
$$
u(x,t)=\sum_{m=0}^{\infty}A_{m}\sin\left( \left( m+\frac{1}{2} \right)x \right)e^{ -k^{2}\left( m+\frac{1}{2} \right)^{2}t }
$$
At $t=0$, we have $u(x,0)=100$, substituting this gets:
$$
u(x,0)=100=\sum_{m=0}^{\infty}A_{m}\sin\left( \left( m+\frac{1}{2} \right)x \right)
$$
One can do this with Fourier series, but the $m+\frac{1}{2}$ is messing things up so it will be hard :(
We will instead do this using orthogonality. Since $\sin\left( \left( m+\frac{1}{2} \right)x \right)$ is an eigenfunction of,
$$
\mathcal{L}X=\frac{d ^{2}}{dx^{2}}X=\lambda X=-\left( m+\frac{1}{2} \right)^{2}X 
$$
So we take
$$
(f,g)=\int_{0}^{\pi} fg \, dx 

$$
Assuming $f,g=0$ at $x=0$, and also $f',g'=0$ at $x=\pi$. Now we can show whether $\mathcal{L}$ is self-adjoint
$$
(\mathcal{L}f,g)=(f'',g)=\int_{0}^{\pi} f''g \, dx =[f'g-fg']_{0}^{\pi}+\int_{0}^{\pi} fg'' \, dx =\int_{0}^{\pi} fg'' \, dx=(f,g'') =(f,\mathcal{L}g)
$$
So $\mathcal{L}$ is self-adjoint, so, $\sin\left( \left( m+\frac{1}{2} \right)x \right)$ will be orthogonal to $\sin\left( \left( n+\frac{1}{2} \right)x \right)$ if $n=m$;
$$
\left( \sin\left( \left( m+\frac{1}{2} \right)x \right),\sin\left( \left( n+\frac{1}{2} \right)x \right) \right)=\delta_{mn}
$$
Now
$$
\left( 100,\sin\left( \left( n+\frac{1}{2} \right)x \right) \right)=\sum_{m=0}^{\infty}A_{m}\left( \sin\left( \left( m+\frac{1}{2} \right)x \right) ,\sin\left( \left( n+\frac{1}{2} \right) \right)\right)
$$
Where all terms $n\neq m$ vanish, so
$$
=A_{n}\left( \sin\left( \left( n+\frac{1}{2} \right)x \right),\sin\left( \left( n+\frac{1}{2} \right)x \right) \right)
$$
$$
 \therefore A_{n}= \frac{\left( 100,\sin\left( n+\frac{1}{2} \right)x \right)}{\left( \sin\left( \left( n+\frac{1}{2} \right)x \right),\sin\left( \left( n+\frac{1}{2} \right)x \right) \right)}
$$
$$
= \frac{2}{\pi}\int_{0}^{\pi} 100\sin\left( \left( n+\frac{1}{2} \right)x \right) \, dx =\frac{200}{\pi\left( n+\frac{1}{2} \right)}\left[ -\cos\left( \left( n+\frac{1}{2} \right) \right)x \right]_{0}^{\pi}
$$
$$
\implies\sum_{m=0}^{\infty} \frac{200}{\pi\left( m+\frac{1}{2} \right)}\sin\left( \left( m+\frac{1}{2} \right)x \right)e^{ -k^{2}\left( m+\frac{1}{2} \right)^{2}t }
$$
The terms tend to $0$ as $m\to \infty$, and with more and more terms it will go from periodic motion to not, and after a very short time, we can say that
$$
u\approx \frac{400}{\pi}\sin\left( \frac{x}{2} \right)e^{ -\frac{k^{2}}{4}t }
$$
```desmos-graph
k=0.4
t=5
\sum_{n=0}^{100}\frac{2}{\pi\left(n+\frac{1}{2}\right)}\sin\left(\left(n+\frac{1}{2}\right)x\right)e^{-k^{2}\left(n+\frac{1}{2}\right)^{2}t}
\frac{4}{\pi}\sin\left(\frac{x}{2}\right)e^{-\frac{k^{2}}{4}t}
```
___
Suppose we have a cube potato with side $\pi$, where $0\leq x,y,z\leq \pi$, then it satisfies the heat equation in 3-dimensions:
- $u_{t}=k^{2}(u_{x x}+u_{yy}+u_{zz})$
- $u=0$ when $x,y,z=0$ or $\pi$, as we keep the potato in a freezing room
- $u(x,y,z,0)=100$, we start with the potato being hot
When will $u\left( \frac{\pi}{2},  \frac{\pi}{2},  \frac{\pi}{2},t_{c} \right)=50$?
We start by solving the initial conditions:
$$
u(x,y,z,t)=X(x)Y(y)Z(z)T(t)
$$
$$
\implies \frac{XYZ\dot{T}}{k^{2}XYZT}=\frac{k^{2}(X''YZT+XY''ZT+XYZ''T)}{k^{2}XYZT}
$$
$$
\implies \frac{\dot{T}}{k^{2}T}=\frac{X''}{X}+\frac{Y''}{Y}+\frac{Z''}{Z}
$$
So all have to be constants since they are functions of other variables:
$$
X''=\lambda_{1}X
$$
$$
 Y''=\lambda_{2}Y
$$
$$
 Z''=\lambda_{3}Z
$$
$$
 \dot{T}=k^{2}(\lambda_{1}+\lambda_{2}+\lambda_{3})T
$$
And we know $X(0)=X(\pi)=Y(0)=Y(\pi)=Z(0)=Z(\pi)=0$, and we've done this before, so we know that
$$
X=\sin(mx),Y=\sin(ny),Z=\sin(lz)
$$
For $m,n,l\in\mathbb{N},\lambda_{1}=-m^{2},\lambda_{2}=-n^{2},\lambda_{3}=-l^{2}$, so
$$
\dot{T}=-k^{2}(m^{2}+n^{2}+l^{2})T
$$
$$
\implies T=e^{ -k^{2}(m^{2}+n^{2}+l^{2})t }
$$
So by the principle of superposition, we combine all these:
$$
u=\sum_{m,n,l}A_{mnl}\sin(mx)\sin(ny)\sin(lz)e^{ -k^{2}(m^{2}+n^{2}+l^{2})t }
$$
Substituting $u(x,y,z,0)=100$, gives
$$
100=\sum_{m,n,l}A_{mnl}\sin(mx)\sin(ny)\sin(lz)
$$
So using the same method as usuall, we find
$$
A_{mnl}=100  \left( \frac{4}{\pi} \right)^{3}  \frac{1}{mnl}
$$
Where $m,n,l$ are all odd, or $0$ otherwise, so we can consider the first term since the others die out really quickly, so
$$
u\approx 100  \left( \frac{4}{\pi} \right)^{3}\sin(x)\sin(y)\sin(z)e^{ -3k^{2}t }=50
$$
$$
\implies t_{c}=\frac{0.4726}{k^{2}}
$$
If we did this with a sphere, we'd get $t_{s}=\frac{0.5336}{k^{2}}$; $t_{c}=88\%t_{s}$
___
A membrane is stretched on a frame above the square region of the $xy$-plane $0<x<\pi$, $0<y<\pi$. Its vertical displacement is given by $u(x,y)$, which obeys Laplace's equation $u_{xx}+u_{yy}=0$. The frame is such that $u(0,y)=u(\pi,0)=0$ for $0<y<\pi$, $u_{y}(x,0)=0$ and $u(x,\pi)=1$ for $0<x<\pi$
![[Second Order Partial Differential Equations 2025-03-07 15.48.39.excalidraw]]
Look for solution in separable form
$$
u(x,y)=X(x)Y(y)
$$
$$
 X''Y+Y''X=0
$$
$$
\implies \frac{X''}{X}=-\frac{Y''}{Y}
$$
$$
\implies X''=\lambda X
$$
$$
 Y''=-\lambda Y
$$
Subject to $X(0)=X(\pi)=0$, we have options for $\lambda$
If $\lambda=n^{2}>0$, then $X=A\cosh(nx)+B\sinh(nx)$ which would imply that $A,B=0$, so we don't care
If $\lambda=0$, then $X=A+Bx$, which means $A,B=0$, so we don't care
If $\lambda=-n^{2}<0$, then $X=A\cos(nx)+B\sin(nx)$, which with our conditions gives $X=\sin(nx),n\in\mathbb{Z}$
So $Y''=-\lambda Y$ gives
$$
Y=A\cosh(ny)+B\sinh(ny)
$$
So
$$
u(x,y)=\sum_{n=1}^{\infty}\sin(nx)(A_{n}\cosh(ny)+B_{n}\sinh(ny))
$$
$$
u_{y}(x,y)=\sum_{n=1}^{\infty}\sin(nx)(nA_{n}\sinh(ny)+nB_{n}\cosh(ny))
$$
$$
 u_{y}(x,0)=0=\sum_{n=1}^{\infty}\sin(nx)nB_{n}\implies B_{n}=0
$$
$$
\implies u(x,y)=\sum_{n=1}^{\infty}A_{n}\sin(nx)\cosh(ny)
$$
$$
 u(x,\pi)=1=\sum_{n=1}^{\infty}\underbrace{ A_{n}\cosh(n\pi) }_{ =D_{n} }\sin(nx)\implies \sum_{n=1}^{\infty}D_{n}\sin(nx)=1
$$
$$
\implies D_{n}=\frac{2}{\pi}\int_{0}^{\pi} \sin nx \, dx =-\frac{2}{\pi n}[\cos(nx)]_{0}^{\pi}=\frac{2}{\pi}(1-(-1)^{n})
$$
Which is $\frac{4}{\pi n}$ for odd $n$, and $0$ for even $n$, so
$$
u(x,y)=\sum_{n=0}^{\infty} \frac{4}{\pi(2n+1)\cos((2n+1)\pi)}\sin((2n+1)x)\cosh((2n+1)y)
$$
