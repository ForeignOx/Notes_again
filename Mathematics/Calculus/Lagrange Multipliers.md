If we want to find [[Critical Points|stationary points]] of $f(x,y)$ subject to constraint $g(x,y)=0$, at maxima/minima of $f(x,y)$ along $g=0$, [[Directional Derivatives|$\underline{\nabla f}\cdot  \underline{\hat{n}}=0$]], since the normal will be tangent to the path. But the path is a level set of $g(x,y)=0$, so $\underline{\nabla g}\cdot  \underline{\hat{n}}=0$, so $\underline{\nabla f},\underline{\nabla g}$ are (anti)parallel, or $\underline{\nabla f}=\lambda \underline{\nabla g}$, where $\lambda$ is known as a Lagrange multiplier. If I consider the function $\phi=f-\lambda g$, then at constraned stationary point of $f$, 
$$
\underline{\nabla \phi} =\underline{\nabla f-\lambda g} =\underline{\nabla f} -\lambda \underline{\nabla g} =0
$$
So $\phi$ has an unconstraned stationary point
___
We can generalise to find stationary points of $f(x_{1},x_{2},\dots,x_{n})$ subject to $m<n$ constraints $g_{j}(x_{1},\dots,x_{n})=0$ with $1\leq j\leq m$. At stationary points of $f(x_{1},\dots,x_{n})$ on $n-m$ dimensional constraint surface, we split [[Sums and Intersections of Vectorspaces#Direct Sums|$\mathbb{R}^{n}=V_\text{tangent}\oplus V_\text{normal}$]], where[[Dimension| $\dim(V_\text{tangent})=n-m$]], $\dim(V_\text{normal})=m$#
$\underline{\nabla g_{i}}\in V_\text{normal}$, since normal to level sets $g_{j}=0$, so we assume $\underline{\nabla g_{i}}$ is a [[Basis|basis]] for $V_\text{normal}$
If $f$ is stationary on constrant furvace, then $\underline{\nabla f}\cdot  \underline{\hat{n}}=0$, ie. $\underline{\nabla f}$ is [[Orthogonality|orthogonal]] to $V_\text{tangent}$
Therefore $\underline{\nabla f}\in V_\text{normal}$, since $\underline{\nabla g_{i}}$ are a basis for $V_\text{normal}$ and $\underline{\nabla f}\in V_\text{normal}$, so $\underline{\nabla f}$ can be written as a [[Linear Combinations|linear combination]] of $\underline{\nabla g_{i}}$'s:
$$
\underline{\nabla f} =\sum_{i=1}^{m}\lambda_{i}\underline{\nabla g_{i}} 
$$
Now construct
$$
\phi=f-\sum_{i=1}^{m}\lambda_{i}g_{i}
$$
So $\underline{\nabla \phi}=0$. If I have $n$ equations, $\frac{ \partial \phi }{ \partial x_{i} } =0$ for $1\leq i\leq n$, and 
## Example
What is the maximum area of a rectangle given the constraint the rectangle has perimeter $P=4$, 
We are finding the maximum of 
$$
A=f(x,y)=xy
$$
but we have the constraint that 
$$
P-4=0=g(x,y)=2x+2y-4
$$
So we could solve $g$ for $y$, since it is equal to $0$, and we get
$$
2y=4-2x\implies y=2-x
$$
So area
$$
f(x,y)=xy=x(2-x)=2x-x^{2}
$$
Then we can differentiate to find the maximum:
$$
\frac{d }{dx} (2x-x^{2})\implies 2-2x=0\implies x=1,y=2-x=1
$$
So max area from square of side length 1
We did this by solving the constraint, but Lagrange's method allows solution without first solving the constraint:
$$
\phi=f-\lambda g=xy-\lambda(2x+2y-4)
$$
$$
 \phi_{x}=0=y-2\lambda 
$$
$$
 \phi_{y}=0=x-2\lambda
$$
And we still have that $g=0$, so
$$
2x+2y=4
$$
So we have $\hspace{0pt}3$ equations in $\hspace{0pt}3$ variables, but from the first two equations, $2\lambda=x=y$, so we already know it is a square, then using the third equation, $2x+2y=4x=4\implies x=y=1$

#Mathematics #Calculus 