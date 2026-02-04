## 1D
We say that a [[Functions|function]] $f$ has a local minimum at a point $x=a$ if:
$$
\exists h>0:f(a)\geq f(x)\forall x\in (a-h,a+h)
$$
Or a local maximum at a point $x=a$ if:
$$
\exists h>0:f(a)\leq f(x)\forall x\in (a-h,a+h)
$$
A local extremum is either a local maximum or a local minimum
If $f(x)$ has a local maximum (or minimum) at $x=a$, and if it is [[Differentiation|differentiable]] at $x=a$, then $f'(a)=0$
We say $f(x)$ has a stationary point at $x=a$, if it is differentiable at $x=a$ and $f'(a)=0$
An interior point $x=a$ of the domain of $f(x)$ is a critical point if either $f'(a)=0$ or doesn't exist, hence all stationary points are critical, but not the other way
If $f(x)$ is twice differentiable in an open interval around $x=a$ with $f''(a)=0$ and changes sign at $x=a$, then we say that $x=a$ is a point of inflection
If $c\in \text{Dom}f$ and if $\exists h>0$ such that $f(x)$ is defined on $[c,c+h)$, but not $(c-h,c]$ (or vice-versa), then $x=c$ is an endpoint of $f(x)$
If $x=c$ is an endpoint of $f(x)$, then $f(x)$ has an endpoint maximum (or minimum) at $x=c$ if $f(x)\leq f(c)$ (or $f(x)\geq f(c)$) for $x$ close to $c$
If $f(x)$ is continuous on $[a,b]$, then all cloval extrema in this interval are attained either at critical points or endpoints
### Proof
Since $f(x)$ is differentiable at $x=a$:
$$
\lim_{ x \to a^- } \frac{f(x)-f(a)}{x-a}=\lim_{ x \to a^+ } \frac{f(x)-f(a)}{x-a}=f'(a)
$$
If $f(x)$ has a local maximum at $x=a$, then $\frac{f(x)-f(a)}{x-a}\leq 0$ for $x\in(a,a+h)$, as the numerator is negative, and the denominator is positive, and if the expression is always negative, the limit is also:
$$
 \lim_{ x \to a^+ } \frac{f(x)-f(a)}{x-a}=f'(a)\leq 0
$$
But also $\frac{f(x)-f(a)}{x-a}\geq 0$, for $x\in(a-h,a)$, then the numerator and denominators are both negative, so is positive, and if an expression is always positive, the limit is also:
$$
\lim_{ x \to a^- } \frac{f(x)-f(a)}{x-a}=f'(a)\geq 0
$$
So:
$$
0\leq f'(a)\leq 0\implies f'(a)=0
$$
### Example
$f(x)=x^{3}$ has $f'(0)=0$, so $x=a$ is a stationary point (& critical point), but not a local extremum, since $f(x)>f(0)\forall x\in(0,h)$, but $f(x)<f(0)\forall x\in(-h,0)$, but $f''(x)=6x$, so $f''(0)=0$ and since $f''(x)<0$ for $x<0$ and $f''(x)>0$ for $x>0$, then $x=0$ is a point of inflection
### First Derivative Test
Suppose $f(x)$ is [[Continuity|continuous]] at a critical point $x=a$
- If $\exists h>0:f'(x)<0\forall x\in(a-h,a),f'(x)>0\forall x\in(a,a+h)$, then $x=a$ is a local minimum
- If $\exists h>0:f'(x)>0\forall x\in(a-h,a),f'(x)<0\forall x\in(a,a+h)$, then $x=a$ is a local maximum
- If $\exists h>0:f'(x)$ has constant sign $\forall x\neq a$ in $(a-h,a+h)$, then $x=a$ is not a local extremum
- If $f(x)$ is continuous and differentiable close to an endpoint, then the sign of the deribative can determine the natrue of the endpoint
#### Example
$f(x)=|x|$ is a continuous function, but $f'(x)\neq 0$, so $\not\exists$ stationary point. $x=a$ is a critical point (as the first derivative doesn't exist here)
$$
f(x)<0\forall x\in (-1,0)\,\&\,f'(x)>0\forall x\in (0,1)
$$
So $x=0$ is a local minimum
___
Find the global extrema of $f(x)=x^{2}-2|x|=2$ for $x\in\left[ -\frac{1}{2},2 \right]$, first note:
$$
f(x)=\begin{cases}
x^{2}-2x+2&\text{for }x\in [0,2]\\x^{2}+2x+2&\text{for }x\in \left[ -\frac{1}{2},0 \right]
\end{cases}
$$
On $(0,2),f'(x)=2x-2$, so critical point at $x=1$, $f(1)=1$, so $(1,1)$ in cartesian coordinates
On $\left( -\frac{1}{2},0 \right),f'(x)=2x+2$, so no critical point in this interval
Note:
$$
\lim_{ x \to 0^+ } f'(x)=-2\neq 2=\lim_{ x \to 0^- } 
$$
So $x=0$ is a critical point with $f(0)=0$
The endpoit values are $f\left( -\frac{1}{2} \right)$ and $f(2)=2$, so global min is $1$ (at $x=1$) and global max is $2$
so $f'(x)$ doesn't exist at $x=0$
### Second Derivative Test
Suppose $f(x)$ is twice differentiable at $x=a$, with $f'(a)=0$
- If $f''(a)>0$ then $x=a$ is a local minimum
- If $f''(a)<0$ then $x=a$ is a local maximum
- If $f''(a)=0$, then the second derivative test doesn't say anything :(
### [[Taylor Series|Taylor Series]]
We can decide between maxima and minima as follows using the Taylor Series. Suppose $f(x)$ has a stationary point at $x=x_{0}$, i.e. $f'(x_{0})=0$
$$
f(x_{0}+\delta x)=f(x_{0})+\delta x\underbrace{ f'(x_{0}) }_{ =0 }+\frac{(\delta x)^{2}}{2}f''(x_{0})+\dots
$$
So for small enough $\delta x$, the quadratic term dominates the rest of the expansion, so
$$
\delta f=f(x_{0}+\delta x)-f(x_{0})\approx \frac{(\delta x)^{2}}{2}f''(x_{0})
$$
This is $>0$ if $f''(x_{0})>0$, thus we have a minimum
This is $<0$ if $f''(x_{0})<0$, thus we have a maximum
If $f''(x_{0})=0$, the quadratic term doesn't dominate and the stationary point is called degenerate
___
## 2D
For $f(x,y)$, stationary points come in $\hspace{0pt}3$ basic categories, mimima, maxima and saddle points
![[Pasted image 20240311125832.png]]
At a stationary point, the slope vanished in all directions, so if we consider the [[Directional Derivatives|directional derivative]], we must have
$$
\underline{\nabla f} \cdot \underline{\hat{n}}=0\forall\underline{\hat{n}}\implies \underline{\nabla f} =0
$$
The point $\underline{a}=(a_{1},\dots,a_{n})$ is a stationary point of $f$ iff $f$ is differentiable at $\underline{a}$ and
$$
\underline{\nabla f}(\underline{a})=\begin{pmatrix}
\frac{ \partial f }{ \partial x_{1} } \\\frac{ \partial f }{ \partial x_{2} } \\\vdots\\\frac{ \partial f }{ \partial x_{n} } 
\end{pmatrix}=\begin{pmatrix}
0\\0\\\vdots\\0
\end{pmatrix} 
$$
I.e.
$$
\frac{ \partial f }{ \partial x_{i} } =0\forall1\leq i\leq n
$$
___
We have a few methods to determine the nature of stationary points for functions of more than one variable
### Method 1
This is easy to use, but only works for functions of $\hspace{0pt}2$ variables
Suppose $f(x,y)$ has a stationary point at $(x_{0},y_{0})$, then
$$
\frac{ \partial f }{ \partial x } (x_{0},y_{0})=\frac{ \partial f }{ \partial y } (x_{0},y_{0})=0
$$
Near the stationary point, by Taylor series we have:
$$
f(x_{0}+\delta x,y_{0}+\delta y)=f(x_{0},y_{0})+\underbrace{ f_{x}(x_{0},y_{0})\delta x+f_{y}(x_{0},y_{0})\delta y }_{ =0 }
$$
$$
 +\frac{1}{2}(f_{xx}(x_{0},y_{0})(\delta x)^{2}+2f_{xy}(x_{0},y_{0})\delta x\delta y+f_{yy}(x_{0},y_{0})(\delta y)^{2})+\dots
$$
$$
\implies \delta f=f(x_{0}+\delta x,y_{0}+\delta y)-f(x_{0},y_{0})\approx \frac{1}{2}Q(\delta x,\delta y)
$$
Where
$$
Q(x,y)=f_{x x}x^{2}+2f_{xy}xy+f_{yy}y^{2}
$$
Where $Q$ is an example of a quadratic form $Ax^{2}+Bxy+Cy^{2}$. And $Q$ can be written as a [[Matrices|matrix]] equation with the [[Hessian Matrix|Hessian]]:
$$
=\begin{pmatrix}
x&y
\end{pmatrix}\begin{pmatrix}
f_{xx}&f_{xy}\\f_{xy}&f_{yy}
\end{pmatrix}\begin{pmatrix}
x\\y
\end{pmatrix}=\underline{x}^{\top}H\underline{x}
$$
Note that
$$
Q(\lambda x,\lambda y)=(\lambda x)^{2}f_{x x}+2(\lambda x)(\lambda y)f_{xy}+(\lambda y)^{2}f_{yy}=\lambda^{2}Q(x,y)
$$
For a saddle point, since we know there are regions where $Q>0$ and regions where $Q<0$, we must have (at least) two lines where $Q=0$. If $Q=0$, then
$$
f_{x x}x^{2}+2f_{xy}xy+f_{yy}y^{2}=0
$$
Since it is trivial if $x=0$, we can divide:
$$
f_{xx}+2 f_{yx}\left( \frac{x}{y} \right)+f_{yy}\left( \frac{y}{x} \right)^{2}
$$
Which is a [[Quadratic Equations|quadratic]], so has solutions
$$
\frac{y}{x}= \frac{-2f_{xy}\pm \sqrt{ (2f_{xy})^{2}-4f_{x x}f_{yy} }}{2f_{yy}}
$$
Need the discriminant to be greater than $\hspace{0pt}0$, so
$$
(f_{xy})^{2}-f_{x x }f_{yy}>0
$$
Or using the Hessian:
$$
\det(H)<0
$$
If $\det(H)>0$, then there are no lines for which $Q=0$ which implies either $Q>0\forall(x,y)\neq(0,0)$, giving a minimum, or $Q<0\forall(x,y)\neq(0,0)$, giving a maximum
Now consider $Q(x,0)=f_{xx}x^{2}$, then 
$$
Q>0\forall(x,y)\neq(0,0)
$$
if $f_{x x}>0$ or 
$$
Q<0\forall(x,y)\neq(0,0)
$$
if $f_{x x}<0$
So to summarise, classification of stationary points using method 1: 
1. $\det(H)>0$ and $f_{x x}>0$, then minimum point
2. $\det(H)>0$ and $f_{x x}<0$ then maximum
3. $\det(H)<0$ then saddle point
4. $\det(H)=0$ then degenerate case
Note that you can equivalently use $f_{yy}$
### Method 2
This method works for functions of $\hspace{0pt}2$ or more variables. This method relies on [[Diagonalisation|diagonalising]] $H$

We can then prove that if $x$ lies along axis of symmetry of an ellipse, it is an eigenvector of $H$
We can prove that axes of symmetry are orthogonal
#### Proof
Consider
$$
\underline{e}_{1}\cdot(H\underline{e}_{2})=\underline{e}_{1}^{\top}(H\underline{e}_{2})=\begin{pmatrix}
*&*
\end{pmatrix}\begin{pmatrix}
*&*\\ *&*
\end{pmatrix}\begin{pmatrix}
*\\ *
\end{pmatrix}
$$
Which is just a number, and by properties of the [[Transpose|transpose]], 
$$
=(\underline{e}_{1}^{\top}H\underline{e}_{2})^{\top}=\underline{e}_{2}^{\top}H\underline{e}_{1}
$$
And since $H$ is a [[Symmetric and Anti-Symmetric Matrices|symmetric]] matrix,
$$
\therefore \underline{e}_{1}\cdot(H\underline{e}_{2})=\underline{e}_{2}\cdot(H\underline{e}_{1})
$$
So
$$
\underline{e}_{1}\cdot H\underline{e}_{2}=\underline{e}_{1}\cdot\lambda_{2}\underline{e}_{2}=\underline{e}_{2}\cdot H\underline{e}_{1}=\underline{e}_{2}\cdot\lambda_{1}\underline{e}_{1}
$$
$$
\implies (\lambda_{2}-\lambda_{1})\underline{e}_{1}\cdot \underline{e}_{2}=0
$$
If $\lambda_{1}\neq\lambda_{2}$, then $\underline{e}_{1}\cdot \underline{e}_{2}=0$; they are orthogonal
If $\lambda_{1}=\lambda_{2}$, then the ellipse becomes a circle which means all directions are axes of symmetry, all vectors are eigenvectors of $H$; so we can pick them to be orthogonal.
___
Let's work in a basis of eigenvectors $\underline{e}_{1},\underline{e}_{2}$, we know $\underline{e}_{1}\cdot \underline{e}_{2}=0$, we will want unit vectors; $\underline{e}_{1}\cdot \underline{e}_{1}=\underline{e}_{2}\cdot \underline{e}_{2}=1$
$$
Q=\underline{x}\cdot H\underline{x}
$$
Let $\underline{x}=x_{1}\underline{e}_{1}+x_{2}\underline{e}_{2}$
Then
$$
Q=(x_{1}\underline{e}_{1}+x_{2}\underline{e}_{2})\cdot H(x_{1}\underline{e}_{1}+x_{2}\underline{e}_{2})
$$
$$
= (x_{1}\underline{e}_{1}+x_{2}\underline{e}_{2})\cdot(x_{1}H\underline{e}_{1}+x_{2}H\underline{e}_{2})
$$
$$
= (x_{1}\underline{e}_{1}+x_{2}\underline{e}_{2})\cdot(x_{2}\lambda_{1}\underline{e}_{1}+x_{2}\lambda_{2}\underline{e}_{2})=\lambda_{1}x_{1}^{2}+\lambda_{2}x_{2}^{2}
$$
$$
= \begin{pmatrix}
x_{1}&x_{2}
\end{pmatrix}\begin{pmatrix}
\lambda_{1}&0\\0&\lambda_{2}
\end{pmatrix}\begin{pmatrix}
x_{1}\\x_{2}
\end{pmatrix}
$$
So $Q>0\forall(x_{1},x_{2})\neq(0,0)$ if $\lambda_{1},\lambda_{2}>0$ (minimum point)
$Q<0\forall(x_{1},x_{2})\neq(0,0)$ if $\lambda_{1},\lambda_{2}<0$ (maximum point)
So if $\lambda_{1},\lambda_{2}\neq 0$ and different signs, then you have a saddle point
___
This can be generalised to more than two variables... For functions of $n$ variables $f(x_{1},x_{2},\dots,x_{n})$, we will find (when we work in a basis of eigenvectors) $\underline{x}=x_{1}\underline{e}_{1}+x_{2}\underline{e}_{2}+\dots+x_{n}\underline{e}_{n}$, where $\underline{e}_{1},\dots,\underline{e}_{n}$ are eigenvectors of $H$; $H\underline{e}_{i}=\lambda_{i}\underline{e}_{i}$, then
$$
Q=\lambda_{1}x_{1}^{2}+\lambda_{2}x_{2}^{2}+\dots+\lambda_{n}x_{n}^{2}
$$
If I move away from the stationary point int the direction of $\underline{e}_{i}$th eigenvector; $\underline{x}=(0,0,\dots,0,\delta x_{i},0,\dots,0)$ with $\delta x_{i}$ as the $i$th entry, then $Q=\lambda_{i}(\delta x_{i})^{2}$ will be a parabola
![[Critical Points 2025-02-04 14.30.52.excalidraw]]
Then we can classify them
#### Rules for this Method
Suppose $f(x_{1},\dots,x_{n})$ has a stationary point at $\underline{x}=\underline{a}$, then we can evaluate the Hessian $H$ at $\underline{x}=\underline{a}$ and find its $n$ eigenvalues $\lambda_{1},\dots,\lambda_{n}$ (guaranteed real by symmetry of $H$), then
- If $\lambda_{i}>0\forall 1\leq i\leq n$ and $Q>0\forall \underline{x}\neq  \underline{0}$ then it is a minimum point
- If $\lambda_{i}<0\forall_{1}\leq i\leq n$ and $Q<0\forall \underline{x}\neq  \underline{0}$ then it is a maximum point
- If $\lambda_{i}\neq 0\forall 1\leq i\leq n$ and have different signs, then it is a saddle point
- If $\lambda_{i}=0$ for some $i$, then $\det(H)=\prod_{i=1}^{n}\lambda_{i}=0$, so it is a degenerate
This method is kinda overkill, since we don't want the exact values of $\lambda$, we just want their signs (if they're positive or not)
### Method 3
This solves the issue of method $\hspace{0pt}2$ taking ages, and is the best of both worlds; it is a generalisation of Method $\hspace{0pt}1$, and involves [[Sylvester's Criterion|Sylvester's Criterion]]
- If $H$ has all positive eigenvalues, the $H$ will correspond to a minimum. If $H$ has all negative eigenvalues, then $-H$ must have all positive eigenvalues and satisfy Sylversers criterion
- For matrices of even size $2n\times 2n$, the negative of them will have the same determinant, so for a maximum, we need an alternating pattern of determinants with alternating signs, starting with a minus; $\det(H^{(i)})(-1)^{i}>0$
- If $H$ corresponds to a degenerate stationary point, then $\lambda_{i}=0$ for some $i$, then $\det(H)=0$
- All other cases give saddle points
Note that for $n=2$, we are considering $\det(H)$, and $H^{(1)}=f_{xx}$
### Example
Find the stationary points of $f(x,y)=xye^{ -x^{2}-y^{2} }$,
$$
\frac{ \partial f }{ \partial x } =0=ye^{ -x^{2}-y^{2} }+x(-2x)ye^{ -x^{2}-y^{2} }=y(1-2x^{2})e^{ -x^{2}-y^{2} }
$$
$$
 \frac{ \partial f }{ \partial y } =0=x(1-2y^{2})e^{ -x^{2}-y^{2} }
$$
The first equation means that either $y=0$ or $2x^{2}=1$. If $y=0$, then the second equation means $x=0$
If $x^{2}=\frac{1}{2}$, then the second equation gives $2y^{2}=1$, so $y^{2}=\frac{1}{2}$. This has $\hspace{0pt}5$ solutions, and the stationary points are $(0,0),\left( \pm \frac{1}{\sqrt{ 2 }},\pm \frac{1}{\sqrt{ 2 }} \right)$ 
This looks like
![[Pasted image 20250130144120.png]]
So $(0,0)$ is a saddle point, $\left( \frac{1}{\sqrt{ 2 }}, \frac{1}{\sqrt{ 2 }} \right),\left(- \frac{1}{\sqrt{ 2 }}, -\frac{1}{\sqrt{ 2 }} \right)$ are maxima, and $\left( -\frac{1}{\sqrt{ 2 }}, \frac{1}{\sqrt{ 2 }} \right),\left( \frac{1}{\sqrt{ 2 }}, -\frac{1}{\sqrt{ 2 }} \right)$
___
Find and classigy the stationary points of $f(x,y)=-\frac{x^{2}}{2}(y-1)+\frac{y^{2}}{2}+y$
For a stationary point $0=f_{x}=f_{y}$
$$
f_{x}=-x(y-1)=0
$$
$$
 f_{y}=\frac{x^{2}}{2}+y+1
$$
The first implies either $x=0$ or $y=1$, if $x=0$, then the second gives $y=-1$, if $y=1$ then the second gives $x=\pm2$, so three stationary points at $(0,-1),(2,1),(-2,1)$, now we classify them. The Hessian matrix is:
$$
H=\begin{pmatrix}
f_{x x}&f_{xy}\\f_{xy}&f_{yy}
\end{pmatrix}=\begin{pmatrix}
-y+1&-x\\-x&1
\end{pmatrix}
$$
Then
$$
\det(H)=1-y-x^{2}
$$
Now we see what this is at each stationary point, at $(0,-1),\det(H)=2>0$ and $f_{x x }=2>0$, so it's a minimum. At $(\pm2,1)$, $\det(H)=-4<0$, so saddle points
___
Consider if $Q(x,y)=2x^{2}+2xy+y^{2}$, then
$$
Q(x,y)=\begin{pmatrix}
x&y
\end{pmatrix}\begin{pmatrix}
2&1\\1&1
\end{pmatrix}\begin{pmatrix}
x\\y
\end{pmatrix}
$$
If we plot a contour of $Q$, it looks like:
![[Pasted image 20250131154543.png]]
So has two [[Eigenvectors|eigenvectors]] going in the axes of symmetry. Since along axes of symmetry we can take the [[Directional Derivatives|directional derivative]] $\underline{\nabla Q}$ which is normal to the level set and parallel to the eigenvector $\underline{x}$, so $\underline{\nabla Q}=2\lambda \underline{x}$, (the two for convenience), so
$$
\underline{\nabla Q} =\begin{pmatrix}
\frac{ \partial Q }{ \partial x } \\\frac{ \partial Q }{ \partial y } 
\end{pmatrix}=\begin{pmatrix}
2f_{x x}x+2f_{xy}y\\2f_{xy}+2f_{yy}y
\end{pmatrix}=2\begin{pmatrix}
f_{x x}&f_{xy}\\f_{xy}&f_{yy}
\end{pmatrix}\begin{pmatrix}
x\\y
\end{pmatrix}=2H\underline{x}
$$
So along axes of symmetry $2H\underline{x}=2\lambda \underline{x}\implies H\underline{x}=\lambda \underline{x}$ showing they're eigenvectors as expected. 
___
Using Method $\hspace{0pt}2$, $f(x,y,z)=xy+xz+yz$, we want to find and classify stationary points, so we need
$$
f_{x}=y+z=0
$$
$$
 f_{y}=x+z=0
$$
$$
 f_{z}=y+x=0
$$
So only stationary point at $(x,y,z)=(0,0,0)$, so let's find what type it is, so we consider the Hessian matrix:
$$
H=\begin{pmatrix}
f_{xx}&f_{xy}&f_{xz}\\f_{xy}&f_{yy}&f_{yz}\\f_{zx}&f_{yz}&f_{zz}
\end{pmatrix}=\begin{pmatrix}
0&1&1\\1&0&1\\1&1&0
\end{pmatrix}
$$
Then eigenvalues are given by $\det(H-\lambda t)=0$;
$$
\det\begin{pmatrix}
-\lambda&1&1\\1&-\lambda&1\\1&1&-\lambda
\end{pmatrix}=-\lambda^{3}+3\lambda+2=-(\lambda-2)(\lambda+1)^{2}
$$
So $\lambda=-1,-1,2$ so the $\lambda$'s are not $\hspace{0pt}0$ and have different signs, so it is a saddle point
___
$f(x,y,z)=-\frac{3x^{2}}{2}-\frac{3y^{2}}{2}-\frac{z^{2}}{2}+xy+yz-xz$, has a stationary point at $(0,0,0)$, where $f_{x}=f_{y}=f_{z}=0$, we have the Hessian:
$$
H=\begin{pmatrix}
f_{x x}&f_{xy}&f_{xz}\\f_{xy}&f_{yy}&f_{yz}\\f_{xz}&f_{yz}&f_{zz}
\end{pmatrix}=\begin{pmatrix}
-3&1&-1\\1&-3&1\\-1&1&-1
\end{pmatrix}
$$
$$
\det(H^{(1)})=-3<0
$$
$$
 \det(H^{(2)})=\det \begin{pmatrix}
-3&1\\1&-3
\end{pmatrix}=8>0
$$
$$
 \det(H^{(3)})=-4<0
$$
So we have a pattern of negative-positive-negative, so we have a maximum!

#Mathematics #Calculus #Definition 