An $n$th order [[Linear|linear]] ordinary [[Differential Equations|differential equation]] can be written
$$
\frac{d ^{n}y}{dx^{n}} +p_{1}(x)\frac{d ^{n-1}y}{dx^{n-1}}+p_{2}(x)\frac{d ^{n-2}y}{dx^{n-2}} +\dots+p_{n-1}(x)\frac{d y}{dx} +p_{n}(x)y(x)=C(x) 
$$
If $C\neq 0$, then they are inhomogeneous. If $C=0$, they are homogeneous.
Linear is a constraint on how the independent variable, $y$, appears (only have $y$ or one of its derivatives appearing in each term)
The general solution to an $n$th order differential equation has $n$ parameters in it
Linear equations are non-linear equation because of the principle of superposition, so the solution space of a linear homogeneous ODE is a [[Vectorspaces|vectorspace]]. Hence, if I find $n$ [[Linear Independence|linearly independent]] solutions $y_{1},\dots,y_{n}$ to my equation, they are a [[Basis|Basis]] for my solution space, so the general solution is a [[Linear Combinations|linear combination]] of these:
$$
y(x)=\alpha_{1}y_{1}(x)+\alpha_{2}y_{2}(x)+\dots+\alpha_{n}y_{n}(x)
$$
The general form of solution of an inhomogeneous equation is
$$
y(x)=y_{PI}+y_{CF}=y_{PI}+(\alpha_{1}y_{1}(x)+\alpha_{2}y_{2}(x)+\dots+\alpha_{n}y_{n}(x))
$$
Where $y_{PI}$ is a solution to the inhomogeneous equation, and $y_{CF}$ is the general solution to the homogeneous equation. Note that this is an affine space
In general, if $p_{1},\dots,p_{n}$ are not constants, the solutions cannot be written in terms of elementary functions
For a particular solution, you need to specify $\alpha_{1},\alpha_{2},\dots,\alpha_{n}$, the $n$ boundary conditions
## Series Solutions
In order to allow for a wide-class of solutions, we can consider [[Series|series]] solutions by substituting $y=\sum_{k=0}^{\infty} a_{k}x^{k}$ and solving the [[Recurrence Relations|recurrence relation]] for $a_{k}$
## Using [[Fourier Transform|Fourier Transforms]] to help with Inhomogeneous ODEs
If we take derivatives of $f(x)$ in $x$-space, this corresponds to multiplying $\tilde{f}(p)$ by $ip$ in $p$-space, so a differential equation in $x$-space becomes an algebraic equation
So we can solve for $\tilde{y}(p)$ and then return to $x$-space to get a solution $y(x)$
### Example
$$
\frac{d y}{dx} +3y=f(x)
$$
Taking the fourier transform of both sides gies:
$$
ip\tilde{y}=3\tilde{y}=\tilde{f}(p)
$$
$$
\implies \tilde{y}(p)=\frac{\tilde{f}(p)}{ip+3}=\tilde{f}(p)\tilde{g}(p)
$$
Where $\tilde{g}(p)=\frac{1}{ip+3}$
So if I can find $g(x)$ such that $\tilde{g}(p)=\frac{1}{ip+3}$, then using the [[Convolution of Functions|convolution]] theorem, we find that the fourier transform of $f*g$ is $\tilde{f}(p)\tilde{g}(p)$ i.e. we can take $y=f*g$
The one-sided exponential 
$$
g(x)=\begin{cases}
e^{ -ax } & x\geq 0\\0 & x<0
\end{cases}
$$
Has Fourier transform $\frac{1}{ip+a}$, so we can take $g(x)=e^{ -3x }$ for $x\geq 0$ and find that
$$
    y(x)=f*g=\int_{-\infty}^{\infty} f(t)g(x-t) \, dt=\int_{-\infty}^{x} f(t)e^{ -3(x-t) } \, dt=e^{ -3x }\int_{-\infty}^{x} f(t)e^{ 3t } \, dt
$$
This makes sense as if we used the integrating factor method, the integrating factor is $e^{ 3x }$, and we get that
$$
y=\frac{1}{e^{ 3x }}\int_{}^{x} f(t)e^{ 3t } \, dt 
$$
___
another example
## Using Green's method
For some 
$$
\mathcal{L}y=a_{n}y^{(n)}+a_{n-1}y^{(n-1)}+\dots+a_{1}y'(x)+a_{0}y(x)=f(x)
$$
Where $a_{0},a_{1},\dots,a_{n}$ are continuous functions of $x$ and we have boundary conditions on a domain $a<x<b$ (can be unbounded):
$$
B_{1}y=\alpha_{11}y(a)+\alpha_{12}y'(a)+\beta_{11}y'(b)+\beta_{12}y'(b)=\gamma_{1}
$$
$$
 B_{2}y=\alpha_{21}y(a)+\alpha_{22}y'(a)+\beta_{21}y'(b)+\beta _{22}y'(b)=\gamma_{2}
$$
$$
 \vdots
$$
We need $a_{n}\neq 0\forall x$ 
So the general green's method has you solve:
$$
\mathcal{L}g(x,\xi)=\delta(x-\xi)
$$
$$
B_{i}g=0
$$
Solve $\mathcal{L}g(x,\xi)=0$ on $a<x<\xi$ and $\xi<x<b$, so boundary conditions will deal with all but $n$ constants
We need jump and continuity conditions which are:
$$
    \int_{\xi^{-}}^{\xi^{+}}a_{n}g^{(n)}(x,\xi)+\dots+a_{0}g(x,\xi)  \, dx =\int_{\xi^{-}}^{\xi^{+}} \delta(x-\xi) \, dx =1
$$
Using the initial boundary problems:
$$
[a_{n}g^{(n-1)}(x,\xi)]_{\xi^{-}}^{\xi^{+}}+\int_{\xi^{-}}^{\xi^{+}} (a_{n-1}-a_{n})g^{(n-1)}+\dots+a_{0}g(x,\xi) \, dx =1
$$
So enforcing the jump condition
$$
[g^{(n-1)}(x,\xi)]_{\xi^{-}}^{\xi^{+}}=\frac{1}{a_{n}(\xi)}
$$
This jump condition means that $g^{(n-1)}(x,\xi)$ looks like the Heaviside function at $x=\xi$
So for all $g^{(n-i)}$ with $i>1$, we must have continuity at $x=\xi$, therefore the integral bit goes to $\hspace{0pt}0$, so our jump condition is valid
Colinulty
### Example
Solve 
$$
-\nabla^{2} G(\underline{x},\underline{\xi})=\delta(\underline{x}-\underline{\xi})
$$
For $\underline{x},\underline{\xi}\in\mathbb{R}^{3}$ subject to $G(\underline{x},\underline{\xi})\to0$ as $\left| \underline{x} \right|\to \infty$
The laplacian $\frac{ \partial^{2}G }{ \partial x^{2} }+\frac{ \partial^{2}G }{ \partial y^{2} }+\frac{ \partial^{2}G }{ \partial z^{2} }$ which has no coordinate dependence, so it is translationally invariant
Interestingly, $\delta(\underline{x}-\underline{\xi})$ is also translationally invariant (the choice of origin doesn't matter)
And $\delta(\underline{x}-\underline{\xi})$ is also rotationally invariant, so we can expect a solution to only depend on $r=\left| x-\xi \right|$, i.e. $G(x,\xi)=\Phi(r)$
We now solve away from the source, so treat $\underline{\xi}=0$
The radial laplacian is:
$$
\Phi''(r)+\frac{2}{r}\Phi'(r)=0
$$
$$
\implies r^{2}\Phi''(r)+2r\Phi'(r)=0
$$
$$
\implies r^{2}\Phi'(r)=A'
$$
$$
\implies \phi'=\frac{A'}{r^{2}}
$$
$$
\implies \Phi=\frac{-A'}{r}+B
$$
And since $G(\Phi(r))\to 0$ as $r\to \infty$, $B=0$, hence
$$
\Phi(r)=-\frac{A'}{r}=\frac{C}{r}
$$
We need to fix $C$ for the $\delta$ result, so we need to integrate around $r=0$ in a ball of radius $\varepsilon\ll 1$, $B_{\varepsilon}$:
$$
    \int _{B_{\varepsilon}}-\nabla^{2}G \, dV =-\int _{\partial B_{\varepsilon}} \underline{\nabla } G\cdot   \underline{\hat{n}} \, dS
$$
Here $\underline{\hat{n}}$ is $\underline{\hat{r}}$, $\underline{\nabla }G=\frac{ \partial G }{ \partial r } \underline{\hat{r}}=$
$$
= \int _{B_{\varepsilon}}\delta(\underline{x}-\underline{\xi}) \, dV =1 
$$





