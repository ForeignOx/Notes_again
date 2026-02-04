A directional [[Differentiation|derivative]] tells me the slope of [[Functions|$f$]] when I move in direction of unit [[Vectors|vector]] $\hat{\underline{n}}=(n_{1},n_{2})$ 
This is the same as the derivative with respect to $t$ along the curve
$$
(x(t),y(t))=(x_{0}+n_{1}t,y_{0}+n_{2}t)
$$
By [[Chain Rule#Situation $ hspace{0pt}2$ $f(x,y(x))$|Situation 1]], of the chain rule, we get
$$
\frac{d f}{dt} =\frac{ \partial f }{ \partial x } \frac{d x}{dt} +\frac{ \partial f }{ \partial y } \frac{d y}{dt} =\frac{ \partial f }{ \partial x } n_{1}+\frac{ \partial f }{ \partial y } n_{2}=\begin{pmatrix}
\frac{ \partial f }{ \partial x } \\\frac{ \partial f }{ \partial y } 
\end{pmatrix}\cdot \begin{pmatrix}
n_{1}\\n_{2}
\end{pmatrix}=\underline{\nabla f} \cdot \hat{ \underline{n}} 
$$
Note here $\underline{\nabla f}=\left( \frac{ \partial f }{ \partial x },\frac{ \partial f }{ \partial y } \right)$ is calld the gradient of $f$ 'grad $f$'
## Example
Calcuolate the slpe of function $f(x,y)=e^{ -x^{2}-y^{2} }$ at the point $(1,0)$ in direction $(1,1)$
## $n$ Variables
If $f$ is a function of $n$ variables $f(x_{1},..,x_{n})$,
$$
\underline{\nabla f} =\begin{pmatrix}
\frac{ \partial f }{ \partial x_{1} } \\\frac{ \partial f }{ \partial x_{2} } \\ \vdots\\\frac{ \partial f }{ \partial x_{n} } 
\end{pmatrix}
$$
If I want the slope in direction of $\underline{v}$, I use:
$$
\underline{\nabla f} \cdot \frac{\underline{v}}{\left| \underline{v} \right| }
$$
## Geometric Interpretation of [[Dot Product|Dot Product]]
![[Directional Derivatives 2025-01-24 15.41.56.excalidraw]]
We can write
$$
\underline{\nabla f} \cdot \hat{\underline{n}}=\left| \underline{\nabla f}  \right| \left| \hat{\underline{n}} \right| \cos\theta=\left| \underline{\nabla f}  \right| \cos\theta
$$
So since $-1\leq \cos\theta \leq 1$,
$$
- \left| \underline{\nabla f} \right|  \leq \underline{\nabla f} \cdot \hat{\underline{n}}\leq \left| \underline{\nabla f} \right| 
$$
The Directional derivative is a maximum when $\underline{\nabla f}$ and $\hat{\underline{n}}$ point in the same direction, i.e. $\underline{\nabla f}$ points in direction you move in $(x,y)$ plane to experience max slope
___
Contours
![[Directional Derivatives 2025-01-24 15.47.13.excalidraw]]
If $\hat{\underline{n}}$ is tangent to level set $f=c$, then $\underline{\nabla f}\cdot  \hat{\underline{n}}=0$ (as slope vanishes on level set), therefore $\underline{\nabla f}$ is normal to level set $f=c$
## Example
Find the tangent plane to the 2D surface
$$
f(x,y,z)=x^{4}+y^{2}x^{2}+yz+z^{2}=13
$$
At the point $(1,2,2)$
![[Directional Derivatives 2025-01-24 15.51.08.excalidraw]]
$\underline{\nabla f}$ is normal to the surface $f=13$ at $(1,2,2)$, so
$$
\underline{\nabla f} =\begin{pmatrix}
\frac{ \partial f }{ \partial x } \\\frac{ \partial f }{ \partial y } \\\frac{ \partial f }{ \partial z } 
\end{pmatrix}=\begin{pmatrix}
4x^{3}+2xy^{2}\\2yx^{2}+z\\y+2z
\end{pmatrix}=\begin{pmatrix}
12\\6\\6
\end{pmatrix}
$$
But $\underline{\nabla f}$ is also normal to tangent plane
$$
12x+6y+6z=c
$$
And we know
$$
\begin{pmatrix}
x\\y\\z
\end{pmatrix}=\begin{pmatrix}
1\\2\\2
\end{pmatrix}
$$
Lies on the tangent plane, so
$$
\begin{pmatrix}
12\\6\\6
\end{pmatrix}\cdot \begin{pmatrix}
1\\2\\2
\end{pmatrix}=12+12+12=36=c
$$
Therefore
$$
12x+6y+6z=36
$$
$$
 2x+y+z=6
$$


#Mathematics #Calculus #Definition 