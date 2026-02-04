A link to [[Eigenfunction Method|eigenfunction method]]:
We are looking for a solution to $\mathcal{L}y=f$
$$
y(x)=\sum_{k=1}^{\infty}  \frac{\left< f,w_{k} \right> }{\lambda_{k}\left< y_{k},w_{k} \right> }y_{k}(x)
$$
By assuming $\mathcal{L}y_{k}=-\lambda_{k}y_{k}$
We rewrite $n_{k}=\left< y_{k},w_{k} \right>$
$$
y(x)=\sum_{k=1}^{\infty} \frac{1}{\lambda_{k}n_{k}}\left( \int ^{b}_{a} f(t)w_{k}(t) \, dt  \right)y_{k}(x)
$$
$$
= \int ^{b}_{a} \sum_{k=1}^{\infty}\left( \frac{1}{\lambda_{k}n_{k}}w_{k}(t)y_{k}(x) \right) f(t) \, dt 
$$
$$
= \int ^{b}_{a} g(x,t)f(t) \, dt 
$$
Is our solution to $\mathcal{L}y=f$ and $g(x,t)$ is an example of a Green's function
## Example
If we have $\mathcal{L}y=-y''=f(x)$ for $0<x<1$, $y(0)=y(1)=0$
Here we find that the Green's function can be written quite simply:
$$
g(x,\xi)=\begin{cases}
(1-\xi)x & 0<x<\xi \\
(1-x)\xi & \xi<x<1
\end{cases}
$$
We want to show
$$
y(x)=\int ^{b}_{a} g(x,\xi)f(\xi) \, d\xi  
$$
Solves our problem. To do this, we need the Leibniz rule:
$$
\frac{d }{dx} \int_{a(x)}^{b(x)} f(x,\xi) \, d\xi=\int_{a(x)}^{b(x)} \frac{ \partial f(x,\xi) }{ \partial x }  \, d\xi+\frac{db(x)}{dx}f(x,b(x))-\frac{d a(x)}{dx} f(x,a(x))   
$$
Which is a generalisation of the antiderivative:
$$
y(x)=\int_{0}^{1} g(x,\xi)f(\xi) \, d\xi =\int_{0}^{x} (1-x)\xi f(\xi) \, d\xi+\int_{x}^{1} (1-\xi)xf(\xi) \, d\xi  
$$
$$
\frac{d y}{dx} =-\int_{0}^{x} \xi f(\xi) \, d\xi+(1-x)xf(x)+\int_{x}^{1} (1-\xi)f(\xi) \, d\xi- (1-x)xf(x)  
$$
$$
= \int_{x}^{1}(1-\xi) f(\xi) \, d\xi-\int_{0}^{x} \xi f(\xi) \, d\xi 
$$
$$
\frac{d^{2}y}{dx^{2}} =-xf(x)-(1-x)f(x)=-f(x)
$$
$W^{5}$ :)
___
This Green's function has the following properties; 
- for $x\neq \xi$, it satisfies $\mathcal{L}g=0$
- $g(x,\xi)$ satisfies the boundary conditions of the full problem
- $g(x,\xi)$ is continuous on the whole inteval
- $g(x,\xi)$ is differentiable everywhere (in the interval) except $x=\xi$
- When we differentiate $y=\int_{0}^{1} g(x,\xi)f(\xi) \, d\xi$ it was the boundary terms which gave $f(x)$
What would be nice is if we could do the following:
$$
y(x)=\int_{0}^{1} g(x,\xi)f(\xi) \, d\xi 
$$
$$
 \frac{d y}{dx} =\int_{0}^{1} \frac{ \partial g(x,\xi) }{ \partial x } f(\xi) \, d\xi 
$$
$$
 \frac{d ^{2}y}{dx^{2}} =\int_{0}^{1} \frac{ \partial^{2}g(x,\xi) }{ \partial x^{2} } f(\xi) \, d\xi=-f(x)   
$$
We would need that
$$
\frac{ \partial^{2}g(x,\xi) }{ \partial x^{2} }=-\delta(x,\xi) 
$$
Where $\int_{0}^{1} \delta(x,\xi)f(\xi) \, d\xi=f(x)$
This $\delta(x,\xi)$ is the [[Dirac Delta Function|delta function]] :)
## Example of Using the Green Function
Consider the point source at $x=\frac{1}{2}$, under the [[Heat Equation|heat equation]]:
$$
-y''(x)=\delta\left( x-\frac{1}{2} \right)
$$
(technically this doesn't mean anything until you integrate, but we can pretend it's ok)
We can use the fact that $\delta\left( x-\frac{1}{2} \right)=0\forall x\neq \frac{1}{2}$
So on $x\in\left[ 0,\frac{1}{2} \right]$ and $x\in\left( \frac{1}{2},0 \right)$, we solve $y''(x)=0$, which gets
$$
y(x)=\begin{cases}
Ax+B & z<\frac{1}{2} \\
Cx+D & x>\frac{1}{2}
\end{cases}
$$
Applying boundary conditions, 
$$
y(0)=0\implies B=0,y(1)=0\implies D=-C
$$
$$
\implies y(x)-\begin{cases}
Ax & x<\frac{1}{2} \\
C(x-1) & x>\frac{1}{2}
\end{cases}
$$
So we need two more conditions, which we obtain from the $\delta$
$$
\int_{\frac{1}{2}^{-}}^{\frac{1}{2}^{+}} -y''(x)  \, dx =\int_{\frac{1}{2}^{-}}^{\frac{1}{2}^{+}} \delta\left( x-\frac{1}{2} \right) \, dx 
$$
$$
\implies [-y']_{\frac{1}{2}^{-}}^{\frac{1}{2}^{+}}=1
$$
$$
\implies y'\left( \frac{1}{2}^{+} \right)-y'\left( \frac{1}{2}^{-} \right)=-1
$$
$$
\implies C-A=-1
$$
$$
\implies y(x)=\begin{cases}
Ax & x<\frac{1}{2} \\
(A-1)(x-1) & x>\frac{1}{2}
\end{cases}
$$
Finally, we ask that $y(x)$ is continuous, so 
$$
[y]_{\frac{1}{2}^{-}}^{\frac{1}{2}^{+}}=0
$$
$$
\implies \frac{A}{2}=-\frac{A-1}{2}
$$
$$
\implies A=\frac{1}{2}
$$
Yayyyyyyyyyyyyyyyyyyyyyyyyy we have solved
## General Function (?)

We want to consider a Green's function construction for a BVP
$$
-y''x=f(x),0<x<1,y(0)=y(1)=0
$$
We solve the Green's problem first:
$$
-g''(x,\xi)=\delta(x-\xi),0<x<1,g(0,\xi)=g(1,\xi)=0
$$
Which is essentially just solving
$$
g''(x,\xi)=0,0\leq x<\xi 
$$
$$
 g''(x,\xi)=0,\xi<x\leq 1
$$
Sooo using the above problem, since we have the same boundary conditions, we get
$$
g(x,\xi)=\begin{cases}
Ax & x<\xi \\
C(x-1) & x>\xi
\end{cases}

$$
From our jump condition, we require
$$
[-g']_{\xi^{-}}^{\xi^{+}}=1
$$
$$
\implies g'(\xi^{+})-g'(\xi^{-})=-1
$$
$$
\implies g(x,\xi)=\begin{cases}
Ax & x<\xi \\
(A-1)(x-1) & x>\xi
\end{cases}
$$
By continuity, we require
$$
[g]_{\xi^{-}}^{\xi^{+}}=0
$$
$$
\implies A\xi=-(A-1)(\xi-1)\implies A=1-\xi 
$$
$$
\implies g(x,\xi)=\begin{cases}
(1-\xi)x & 0<x<\xi \\
(1-x)\xi & \xi<x<1
\end{cases}
$$
So we know our overall solution is hence
$$
y=\int_{0}^{1} g(x,\xi)f(\xi) \, d\xi
$$
## Examples
Solving $\mathcal{L}y=f(x)$ where $\mathcal{L}=\frac{d ^{2}}{dx^{2}}-1$, $y(0)=y(1)=0$, so
$$
\frac{d ^{2}y}{dx^{2}} -y=f(x)
$$
So we solve the Green's problem
$$
\frac{d ^{2}G(x,\xi)}{dx^{2}} -G(x,\xi)=\delta(x-\xi)
$$
So we solve $G''-G=0$ on $0<x<\xi$ and $\xi<x<1$ separately:
$$
G=Ae^{ x }+Be^{ -x }
$$
$$
\implies G=\begin{cases}
Ae^{ x }+Be^{ -x } & 0<x<\xi \\
Ce^{ x }+De^{ -x } & \xi<x<1
\end{cases}
$$
Applying boundary conditions, we get
$$
G(0,\xi)=0\implies A+B=0\implies A=-B
$$
$$
 G(1,\xi)=0\implies Ce+De^{-1}=0\implies D=-Ce^{2}
$$
$$
\implies G=\begin{cases}
A(e^{ x }-e^{ -x }) & 0<x<\xi \\
C(e^{ x }-e^{ 2-x }) & \xi<x<1
\end{cases}
$$
So for continuity we want
$$
G(\xi^{+},\xi)=G(\xi^{-},\xi)
$$
$$
\implies A(e^{ \xi }-e^{ -\xi })=C(e^{ \xi }-e^{ 2-\xi })
$$
And for our jump condition:
$$
\int_{\xi^{-}}^{\xi^{+}} G''-G \, d\xi= \int_{\xi^{-}}^{\xi^{+}} \delta(x-\xi) \, d\xi=1 
$$
Where continuity is telling us that the $G$ in $G''-G$ vanishes
$$
\implies [G']_{\xi^{-}}^{\xi^{+}}=1
$$
$$
\implies G'(\xi^{+},\xi)-G'(\xi^{-},\xi)=1
$$
$$
\implies C(e^{ x }+e^{ 2-x })-A(e^{ x }+e^{ -x })=1
$$
Evaluating at $\xi$, we get
$$
C(e^{ \xi }+e^{ 2-\xi })-A(e^{ \xi }+e^{ -\xi })=1
$$
$$
\implies A=\frac{e^{ -\xi }(e^{ -2 }+e^{ 2\xi })}{2(e^{2}-1)},C=\frac{e^{ -\xi }(e^{ 2\xi }-1)}{2(e^{2}-1)}
$$
So we have $G$ :>
And then our solution is
$$
y=\int_{0}^{1} G(x,\xi)f(\xi) \, dx 
$$
___
Solve 
$$
\mathcal{L}y=y''-\mu^{2}y'=f(x),-\infty<x<0
$$
Subject to $y\to0$ as $x\to -\infty$, $y(0)=1$ inhomogeneous
Green's problem:
$$
\frac{d ^{2}G}{dx^{2}} -\mu^{2}\frac{d G}{dx} =\delta(x-\xi)
$$
With boundary conditions $G(x\to-\infty,\xi)=0,G(0,\xi)=0$
Solve on $-\infty<x<\xi$ and $\xi<x<0$:
$$
G''-\mu^{2}G=0
$$
$$
\implies G'-\mu^{2}G=B
$$
$$
\implies G=-\frac{B}{\mu^{2}}+Ae^{ \mu^{2}x }
$$
With $-\frac{B}{\mu^{2}}$ as our particular solution and $Ae^{ \mu^{2}x }$ our homogeneous solution, hence:
$$
G=\begin{cases}
-\frac{B_{1}}{\mu^{2}}+A_{1}e^{ \mu^{2}x } & -\infty<x<\xi \\
-\frac{B_{2}}{\mu^{2}}+A_{2}e^{ \mu^{2}x } & \xi<x<0
\end{cases}
$$
Then $G(-\infty,\xi)=0\implies B_{1}=0,G(0,\xi)=0$, so
$$
-\frac{B_{2}}{\mu^{2}}+A_{2}=0\implies A_{2}=\frac{B_{2}}{\mu^{2}}
$$
So
$$
G=\begin{cases}
A_{1}e^{ \mu^{2} x}  & -\infty<x<\xi \\
\frac{B_{2}}{\mu^{2}}(e^{ \mu^{2}x }-1) & \xi<x<0

\end{cases}

$$
So by continuity, 
$$
A_{1}e^{ \mu^{2}\xi }=\frac{B_{2}}{\mu^{2}}(e^{ \mu^{2} \xi}-1)
$$
And from our jump condition:
$$
[G']_{\xi^{-}}^{\xi^{+}}-\mu^{2}[G]_{\xi^{-}}^{\xi^{+}}=1
$$
With again $G=0$, so
$$
B_{2}e^{ \mu^{2}\xi }-A_{1}\mu^{2}e^{ \mu^{2}\xi }=1
$$
So solving simultaneously, we get
$$
B_{2}=1,A_{1}= \frac{e^{ -\mu^{2}\xi }(e^{ \mu^{2}\xi }-1)}{\mu^{2}}
$$
$$
\implies G(x,\xi)=\begin{cases}
\frac{e^{ \mu^{2}x }}{\mu^{2}}(1-e^{ -\mu^{2}\xi }) & -\infty<x<\xi \\
\frac{1}{\mu^{2}}(e^{ \mu^{2}x }-1) & \xi<x<0
\end{cases}
$$
So now we have
$$
y_{h}=\int_{-\infty}^{0} G(x,\xi)f(\xi) \, d\xi 
$$
Which solves $y''-\mu^{2}y'=f,y\to0$ as $x\to-\infty$ and $y(0)=0$
So we need a particular solutipn $y_{p}$ which solves the differential equation, and we can combine $y_{h}$ and $y_{p}$ to get the final solution :)
Note that eigenfunction method doesn't work on infinite domains, it turns into fourier series nonsense, so this is better

