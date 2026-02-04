 ## Prototype Problem via this Method
Consider the [[Linear Partial Differential Equations|linear]] [[Partial Differential Equations|PDE]] 
$$
\frac{ \partial u }{ \partial x } =\mathcal{L}u+h(x,t)
$$
Which is a 1D model of a scalar function $u(x,t)$ on a domain $x\in[a,b],t>0$
### The Operator
The operator $\mathcal{L}$ is a [[Linear Differential Operators|linear differential operator]], satisfying
$$
\mathcal{L}(au_{1}+bu_{2})=a\mathcal{L}u_{1}+b\mathcal{L}u_{2}
$$
If it has derivatives, they are only in the spatial variable $x$
It can represent the spreading, transport and creation/destruction of the scalar $u$
### The Source Term
The function $h(x,t)$ is the source term or forcing term does not depend on $u$, so provides some external change in the rate of change of $u$ and the system as a whole
If $h(x,t)=0$, then the problem is referred to as homogeneous. If it is non-zero, the poblem is instead referred to as inhomogeneous
#### Inhomogeneous-Homogeneous Decomposition
For every inhomogeneous problem, there is an associated homogeneous problem obtained by setting $h(x,t)=0$. If we label the respective solutions $u_{ih}$ and $u_{h}$, then $u_{h}+u_{ih}$ is also a solution to the inhomogeneous problem (by linearity)
### Boundary Conditions
We need $n$ boundary conditions for an $n$th order linear operator. We write this as follows:
$$
BC_{i}[u,a,b]=0
$$
Where $BC_{i}$ are linear operators evaluated at $x=a,b$
Boundary conditions are homogeneous if the dependent variable $u$, or its derivatives are zero on the boundary. Otherwise they are inhomogeneous.
We write $BC_{i}u$ to indicate the boundary operator $BC_{i}$ acting on $u$, and assume it is evaluated at the boundaries
#### Example
$$
BC_{1}[u,a,b]=\frac{ \partial^{2}y }{ \partial x^{2} } |_{x=a}+5u(b,t)=0
$$
$$
 BC_{2}[u,a,b]=u(a,t)+u(b,t)-10=0
$$
### Initial Conditions
The system is complete if we specify an initial condition:
$$
u(x,0)=g(x)
$$
### Solution
Based on solutions to other PDEs we've encountered, we will be bold and assume an infinite series solution:
$$
u(x,t)=\sum_{n=0}^{\infty}C_{n}(t)y_{n}(x)
$$
(we saw that this comes about in some cases from separation of variables)
We assume that we can expand $h(x,t)$ like this also:
$$
h(x,t)=\sum_{n=0}^{\infty}y_{n}(x)h_{n}(t)
$$
(We saw in hte case of $\mathcal{L}=\frac{ \partial^{2} }{ \partial x^{2} }$ this will take the form of a Fourier/Bessel series)
Substituting into our model, we get:
$$
\sum_{n=0}^{\infty} \frac{d C_{n}}{dt} y_{n}=\sum_{n=0}^{\infty}c_{n}(t)\mathcal{L}y_{n}(x)+\sum_{n=0}^{\infty}h_{n}(t)y_{n}(x)
$$
If we assume $\mathcal{L}y_{n}=-\lambda y_{n}$, then we can bring everything together:
$$
\sum_{n=0}^{\infty}\left( \frac{d C_{n}}{dt} +\lambda _{n}c_{n}-h_{n} \right)y_{n}=0
$$
If we further assume $y_{n}(x)$ are [[Linear Independence|linearly independent]], then this is true if each
$$
\frac{d c_{n}}{dt} +\lambda_{n}c_{n}-h_{n}=0
$$
This is a [[First Order Ordinary Differential Equations|first order ODE]], so we use an integrating factor:
$$
\implies c_{n}(t)=e^{ -\lambda nt }\left( c_{n}(0)+\int_{0}^{t} e^{ \lambda nt'} h_{n}(t') \, dt'  \right)
$$
So the solution that
$$
u(x,t)=\sum_{n=0}^{\infty}c_{n}(t)y_{n}(x)
$$
We usually impose the initial condition:
$$
u(x,0)=\sum_{n=0}^{\infty}c_{n}(0)y_{n}(x)=g(x)
$$
The boundary conditions satisfy:
$$
BC_{i}u=\sum_{n=0}^{\infty}c_{n}(t)BC_{i}y_{n}=0
$$
$$
\implies BC_{i}y_{n}=0
$$
### Summary
We proposed a solution to the problem
$$
\frac{ \partial u }{ \partial t } =\mathcal{L}u+h(x,t)
$$
With boundary conditions:
$$
BC_{i}[u]=0
$$
Takes the form
$$
u(x,t)=\sum_{n=0}^{\infty}c_{n}(t)y_{n}(x)
$$
Where the $y_{n}(x)$ satisfy
$$
\mathcal{L}y_{n}=-\lambda y_{n}
$$
With boundary conditions satisfying
$$
BC_{i}y_{n}=0
$$
Where 
$$
c_{n}(t)=e^{ -\lambda nt }\left( c_{n}(0)+\int_{0}^{t} e^{ \lambda nt' }h_{n}(t') \, dt'  \right)
$$
And
$$
h(x,t)=\sum_{n=0}^{\infty} c_{n}(t)y_{n}(x)
$$
The crucial point is that this all hinges on the solution of $\mathcal{L}y_{n}=-\lambda_{n}y_{n}$ and the assumption it provides a countable infinity of functions $y_{n}$ which are linearly independent
### Concrete Example via the Fourier eries
Let
$$
x\in [a,b],\mathcal{L}=\frac{ \partial^{2} }{ \partial x^{2} } ,BC_{1}[u]=\frac{ \partial u }{ \partial x } |_{x=a}=0,BC_{2}[u]=\frac{ \partial u }{ \partial x } |_{x=b}=0
$$
So homogeneous [[Neumann Boundary Conditions|neumann boundary conditions]]
$$
\implies \frac{d ^{2}y_{n}}{dx^{2}} =-\lambda_{n}y_{n},\frac{d y_{n}}{dx} |_{x=a}=0,\frac{d y_{n}}{dx} |_{x=b}=0
$$
So we have the solution
$$
y_{n}=a_{n}\cos\left( \frac{n\pi(x-a)}{b-a} \right),\lambda_{n}=\frac{n^{2}\pi^{2}}{(b-a)^{2}}
$$
So we have a countable infinity of solutions,
$$
\implies u(x,t)=\sum_{n=0}^{\infty}c_{n}(t)\cos\left( \frac{n\pi(x-a)}{b-a} \right)
$$
We can use the Fourier series to get the general
$$
h_{n}(t)=\frac{l}{b-a}\int_{a}^{b} h(x,t)\cos\left( \frac{n\pi(x-a)}{b-a} \right) \, dx
$$
Where $l=2$ if $n>0$, $l=1$ if $n=0$.
And
$$
g(x)=\sum_{n=0}^{\infty} c_{n}(0)\cos\left( \frac{n\pi(x-a)}{b-a} \right)
$$
$$
c_{n}(0)=\frac{l}{b-a}\int_{a}^{b} g(x)\cos\left( \frac{n\pi(x-a)}{b-a} \right) \, dx
$$
The key is that this worked as Fourier orthogonality gives the coefficient formulae
The aim is to show that for a generic
$$
\mathcal{L}y_{n}=\lambda_{n}y_{n}
$$
And the $y_{n}$ have some form of mutual orthogonality. We have to prove this
## Inhomogeneous Problems
We are in a position to outlilne the construction to the BVP
$$
\mathcal{L}u=f(x)
$$
With linear, homogeneous, separated boundary conditions, denoted $BC_{1}(a)=0,BC_{2}(b)=0$
Why do we care?
- Many of these models are examples of steady state models, so the systems eventually settle to some equilibrium
- This addresses the issue of representing $h(x,t)$ that we assumed earlier. We see this:
$$
\sum_{n=0}^{\infty}h_{n}(t)y_{n}(x)=h(x,t)
$$
$$
 \implies \sum_{n=0}^{\infty} h_{n}(t) \frac{\mathcal{L}y_{n}(x)}{r(x)\lambda_{n}}=h(x,t)
$$
$$
\implies \mathcal{L}\sum_{n=0}^{\infty}h_{n}(t) \frac{y_{n}(x)}{r(x)\lambda_{n}}=h(x,t)
$$
Fixing $t=t_{e}$, we can write:
$$
u=\sum_{n=0}^{\infty}h_{n}(t_{e}) \frac{y_{n}(x)}{\lambda_{n}},f=h(x,t_{e})
$$
Then we have an equation in the form $\mathcal{L}u=f$
So seeking to solve $\mathcal{L}u=f$ is equivalent to asking  if we can represent so the function $h(x,t)$ in terms of the eigenfunctions of an operator $\mathcal{L}$. The crucial assumption in our master PDE solution.
There is a potential issue with the $\frac{1}{\lambda_{n}}$ factor. If $\lambda_{0}=0$, then this does not work
___
So we solve our inhomogeneous problem:
$$
\mathcal{L}u=f, BC_{i}(\underline{a})=0
$$
We take the following steps:
1. Solve the eigenvalue problem:
$$
\mathcal{L}y_{n}=\lambda_{n}y_{n}, BC_{i}(\underline{a})=0
$$
    To obtain the eigenvalue, eigenfunction pairs $(\lambda_{j},y_{j})$
2. Solve the adjoint eigenvalue problem:
$$
\mathcal{L}^{*}w_{n}=\lambda w_{n},BC^{*}_{i}(\underline{a})=0
$$
    To obtain $(\lambda_{j},w_{j})$
3. Assume a solution to the full system $\mathcal{L}y=f(x)$ in the form
$$
y=\sum_{i}c_{i}y_{i}(x)
$$
    To determine the coefficients $c_{i}$, we start from $\mathcal{L}y=f$ and take an inner product with $w_{k}$
$$
\mathcal{L}y=f(x)
$$
$$
\implies \left< \mathcal{L}y,w_{k} \right> =\left< f,w_{k} \right> 
$$
$$
\implies \left< y,\mathcal{L}^{*}w_{k} \right> =\left< f,w_{k} \right> 
$$
$$
\implies \left< y,r(x)\lambda_{k}w_{k} \right> =\left< f,w_{k} \right> 
$$
$$
\implies \lambda_{k}\left< \sum_{i}c_{i}y_{i},r(x)w_{k} \right> =\left< f,w_{k} \right> 
$$
$$
\implies \lambda_{k}c_{k}\left< y_{k},r(x)w_{k} \right> =\left< f,w_{k} \right> 
$$
Using orthogonality of the $w_{k}$ for the final step, so we solve the last equality for the $c_{k}$ and we are done:
$$
c_{k}= \frac{\left< f,w_{k} \right> }{\lambda_{k}\left< y_{k},r(x)w_{k} \right> }
$$
If the problem is fully self-adjoint (the operator and boundary conditions), then the problem reduces to:
$$
c_{k}=\frac{\left< f,y_{k} \right> }{\lambda_{k}\left< y_{k},r(x)y_{k} \right> }
$$
## Inhomogenous Boundary Conditions
We can consider the general case of an inhomogeneous system with inhomogeneous boundary conditions, this problem takes the form:
$$
\mathcal{L}u=f(x),B_{i}u=\gamma_{i},i\in  1,2,\dots,n
$$
We can deal with this by sxploiting the linearity of the system to split into a homogenous problem
$$
\mathcal{L}u_{1}=f(x),B_{i}u_{1}=0
$$
Ad a simpler problem with the inhomogenaity
$$
\mathcal{L}u_{2}=0,B_{i}u_{2}=\gamma_{i}
$$
Linearity says that $u(x)=u_{1}(x)+u_{2}(x)$
### Example
Solve 
$$
y''=f(x),r(0)=\alpha,y(1)=0,r(x)=1
$$
This has a solution:
$$
c_{k}= \frac{\left< f,w_{k} \right> }{\lambda_{k}\left< y_{k},r(x)w_{k} \right> }=2\frac{\int_{0}^{1} f(x)\sin(k\pi x) \, dx }{k^{2}\pi^{2}}
$$
And we also have
$$
\mathcal{L}y_{2}=0,y_{2}(0)=\alpha,y_{2}(1)=\beta
$$
So
$$
\frac{d ^{2}u}{dx^{2}}=0,y_{2}=ax+b 
$$
But subsituting boundary conditions:
$$
u=(\beta-\alpha)x+\alpha
$$
Then the full solution is $y(x)+u(x)$
## Existence of the Eigenexpansion via the Fredholm Alternative
We want to know if we can solve $\mathcal{L}u=f,BC_{i}u$ via an eigenexpansion because we don't want to waste our time
### Proposition
The Fredholm Alternative holds
1. Either the homogeneous adjoint problem $\mathcal{L}^{*}w=0$ has a non-trivial solution ($w(x)\neq 0$)
2. Xor the inhomogeneous boundary value problem $\mathcal{L}u=f(x)$ has a unique solution 
One or the other. Note that $\mathcal{L}^{*}w=0$ is the same as $\mathcal{L}^{*}w=\lambda w$ with $\lambda=0$
If it is the first, we still want to know if $\mathcal{L}u=f$ is solvable, in this case the Fredholm has a second branch:
- Either there is a non-unique solution to $\mathcal{L}u=f$ iff $\left< w,f \right> =0$
- If $\left< w,f \right>\neq 0$ then there is no solution to $\mathcal{L}u=f$ with the stated boundary conditions
### Rough Expalanation
Start with 
$$
\left< \mathcal{L}u,w \right> =\left< u,\mathcal{L}^{*}w \right> 
$$
If $\mathcal{L}^{*}w=0$, with $w\neq 0$, then $\mathcal{L}u=0$?
However, if $\left< f,w \right>=0$, then this is ture, $\mathcal{L}u$ doesn't have to be $0$, so we can integrate (maybe) equal $f$
If $\mathcal{L}^{*}w=0$ and $w=0$, then $\left< \mathcal{L}u,w \right>= 0$
The actual theorem requires we show this staisfies $\mathcal{L}u=f$ uniquely, which is much harder
___
The coefficient formula revisited:
The coefficencs are given by:
$$
\lambda_{k}c_{k}\left< y_{k},r(x)w_{k} \right> 
$$
If $\lambda_{k}=0$, then we need $\left< f,w_{k} \right> =0$, if $w_{k}\neq 0$ and $\left<  f,w_{k} \right>\neq 0$ we cannot connect o find our coefficients
### Example
$$
\frac{d ^{2}y}{dx^{2}} +g_{0}^{2}y=\sin x,y(0)=y(\pi)=0
$$
Where $g_{0}$ is a real constant
We can show this is self-adjoint
We start by solving the homogeneous adjoint problem
$$
\implies \frac{d ^{2}w}{dx^{2}} +g_{0}rw=0
$$
Then $w(x)=A\sin(g_{0}x)+B\cos(g_{0}x)$, we have $w(0)=0\implies B=0$, $W(\pi)=0\implies A\sin (G_{0}\pi)=0$
If $g_{0}$ is not an integer, then must have $A=0$ which would leave to a trivial solution, but we want to solve it uniquely
If $g_{0}$ is an integer then we have a non-trivial solution.
In this second case, we o into the second branchof Fredholm and ask is:
$$
\left< w,\sin x \right> =\int_{0}^{\pi} \sin(g_{0}x)\sin x \, dx=  \frac{\sin(g_{0}\pi)}{g_{0}^{2}-1}
$$
Remember that $g_{0}$ is an integer, so if $g_{0}\neq 1$, this is zero and can solve-non-uniquely if $g_{0}=0$, $\left< w,f(x) \right>\neq 0$, so there's no solution
Let's test this:
We solve our original equation by seeking a complimentary solution satisfying the homogeneous part, we already solved this and got:
$$
y_{c}=A\sin(g_{0}x)+B\cos(g_{0}x)
$$
Then we find our particular solution, the right hand sign suggests trying 
$$
y_{p}=a_{1} \sin x+a_{2}\cos x
$$
Which when we plug in, we get:
$$
(a_{1}(g_{0}^{2}-1)-1)\sin x+a_{2}(g_{0}^{2}-1)\cos x
$$
If $g_{0}\neq 1$, $a_{2}=0,a_{1}=\frac{1}{g_{0}^{2}-1}$, so we have a general solution:
$$
y(x)=A\sin(g_{0}x)+B\cos(g_{0}x)+ \frac{1}{g_{0}^{2}-1}\sin x
$$
If $g_{0}$ is not an integer, we can confirm the boundary conditions require $A=B=0$
If $g_{0}$ is an integer, we can confirm that $A$ is left undetermined, so it is non-unique
If $g_{0}=1$, $y_{c}=A\sin x+B\cos x$, so the particular solution is in the complimentary solution, so we need to try the particular solution
$$
y_{p}=a_{1}x\sin x+a_{2}x\cos x
$$
Which when we plug in, we get:
$$
2a_{1}\cos x-(2a_{2}+1)\sin x=\sin x
$$
$$
\implies a_{1}=0,a_{2}=-\frac{1}{2}
$$
So the general solution in that case is:
$$
y(x)=A\sin x+B\cos x-\frac{1}{2}x\cos x
$$
One can confirm that this cannot satisfy the boundary conditions (due to the $x\cos x$, so there was no solution)
Thus Fredholm was right
_____
Say we have our target model
$$
\frac{ \partial u }{ \partial t } =\mathcal{L}u+h(x,t)
$$
If $\frac{ \partial u }{ \partial t }=0$, then we have $\mathcal{L}u+h(x)=0$ in the form $\mathcal{L}u=f$. We've seen that this solution takes the form
$$
u(x)=\sum_{n=0}^{\infty}c_{n}y_{n}(x)
$$
Where $\mathcal{L}y_{n}=-\lambda_{n}y_{n}$
In the time dependent case,
$$
u(x,t)=\sum_{n=0}^{\infty}c_{n}(t)y_{n}(x)
$$
For $\mathcal{L}u=f$, 
$$
\lambda_{n}c_{n}\left< y_{n}(x),r(x)w_{n}(x) \right>=\left< f,w_{n}(x) \right> 
$$
For $\frac{ \partial u }{ \partial t }=\mathcal{L}u+h(x,t)$, then
$$
\frac{d c_{n}}{dt} +\lambda_{n}c_{n}-h_{n}=0
$$
When $h_{n}(t)\left< y_{n},r(x)w_{n} \right>=\left< h(x,t),w_{n} \right>$
Fredholm told us if we can solve $\mathcal{L}u=f$, does it help for the full equation?
Almost... To guarantee that our series works for the time-dependent problem requires $\mathcal{L}$ to be self-adjoint
## Extensions:
We can extend this model in a few ways, for example, extending the time-dependent behaviour, for example
$$
\frac{ \partial^{2}y }{ \partial x^{2} }=\mathcal{L}y+h(x,t) 
$$
Where $y(x,0)=g_{1}(x),\frac{ \partial u }{ \partial t }|_{t=0}=g_{2}(x)$, then the solution method is identical,
$$
u(x,t)=\sum_{n=0}^{\infty}c_{n}(t)y_{n}(x),\mathcal{L}y_{n}=-\lambda_{n}y_{n}
$$
$$
 h(x,t)=\sum_{n=0}^{\infty}h_{n}(t)y_{n}(x)
$$
$$
\implies \frac{d ^{2}c_{n}}{dt^{2}} +\lambda_{n}c_{n}-h_{n}=0
$$
So the last part is the only part that changes, and even more generally, 
$$
\mathcal{L}_{t}u=\mathcal{L}_{x}u+h(x,t)
$$
Where $\mathcal{L}_{t}$ is a linear time dependent operator, $\mathcal{L}_{x}$ is a linear space dependent operator, we have the same steps, but the final step will have
$$
\mathcal{L}_{t}c_{n}+\lambda_{n}c_{n}-h_{n}(t)=0
$$
In fact, if we write $\mathcal{L}^{*}=\mathcal{L}_{t}-\lambda$, then $\mathcal{L}^{*}c_{n}=h_{n}(t)$ which is an inhomogeneous problem that we'e already encountered
Do we need to use Fredholm? Noo
The difference is that the boundary conditions are actually initial conditions, i.e $c_{n}(t=0)=a_{n},\frac{d c_{n}}{dt}(t=0)=b_{n}$, whereas usual boundary conditions are like $y_{n}(a)=0,y_{n}(b)=0$ which have different parameters.
So since we are dealing with just a start-point, the time-dependent part is not a worry
