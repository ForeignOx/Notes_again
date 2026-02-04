Given a [[Functions|function]] $f(x,y)$ and a region $R$ in the $xy$-plane, the double [[Integration|integral]]:
$$
\iint_{R}f(x,y)dydx=\iint_{R}f(x,y)dA
$$
Is the signed volume of the region between the $z=f(x,y)$ and the region $R$ in the $z=0$ [[Planes|plane]]
![[Double Integrals 2024-02-21 15.22.15.excalidraw]]
To find a volume you essentially take a sum of areas and take the limit of these areas, which is an integral

$$
A_{i}=\int _{f_{l}(x_{i})}^{f_{u}(x_{i})}f(x,y) \, dy 
$$
$$
V=\lim_{ \Delta x \to 0 } \sum_{ i=1} ^{ n}  A_{i}\Delta x=\lim_{ \Delta x \to 0 } \sum_{ i=1} ^{ n}  \int _{f_{l}(x_{i})}^{f_{u}(x_{i})}f(x,y) \, dy \Delta x
$$
Since $\Delta x=\frac{b-a}{2}$
$$
=\int ^{b}_{a} \int _{f_{l}(x_{i})}^{f_{u}(x_{i})}f(x,y) \, dy  \, dx =\iint_{R}f(x,y)dA
$$

Note that:
$$
\int ^{b}_{a} \int _{c}^{d}f(x,y) \, dy  \, dx =\int _{c}^d \int ^{b}_{a} f(x,y) \, dx  \, dy   
$$

## Examples of Regions
### Rectangular regions
![[Double Integrals 2024-02-21 15.33.49.excalidraw]]
$$
V=\iint_{R}f(x,y)dA , R=\{(x,y)\mid a\leq x\leq b, c\leq y\leq d\}=\int ^{b}_{a} \int _{c}^d f(x,y) \, dy  \, dx
$$
A way of showing this more rigorously is using two [[Riemann Sums|Riemann sums]]:
$$
R=[a,b]\times[c,d]
$$
And construct a [[Subdivisions|subdivision]] $S$ by specifying the points of a 2d lattice with
$$
a=x_{0}<x_{1}<x_{2}<\dots<x_{n}=b
$$
$$
c=y_{0}<y_{1}<y_{2}<\dots<y_{m}=d
$$
The edge lengths of these rectangles in the $xy$-plane are
$$
\Delta x_{i}=x_{i}=x_{i-1},\,i=1,\dots,n
$$
$$
\Delta y_{j}=y_{j}-y_{j-1},\,j=1,\dots,m
$$
The norm $|S|$ is the maximum of the $\Delta x_{i}$ and $\Delta y_{i}$, we can take sample points $(p_{i},q_{j})\in[x_{i-1},x_{i}]\times[y_{j-1},y_{j}]$, the area of this rectangle is $\Delta x_{i}\Delta y_{j}$ and we can associate to each rectangle a cuboid of height $f(p_{i},q_{j})$, so the volume of all the cuboids is the Riemann sum:
$$
V=\sum_{i=1}^{n}\sum_{j=1}^{m}f(p_{i},q_{j})\Delta x_{i}\Delta y_{j}
$$
And the double integral is the limit:
$$
\iint_{R}f(x,y)\,dxdy=\lim_{ |S| \to 0 } V
$$
Note that in the special case $f(x,y)$ is a constant, $f(x,y)=c$, then
$$
\iint_{R}f(x,y)\,dxdy=c\times \text{Area}(R)
$$
For a rectandgular region, a practical way to compute the double integral si as an iterated integral (Fubini's theorem, valid if $f$ is continuous on $R$)
#### Example
$$
V=\iint_{R}2y-3x^{2}y^{2} dA, R= \{(x,y)|0\leq x\leq 1, 0\leq y\leq 2\}
$$
![[Pasted image 20240221173822.png]]
$$
V=\int _{0}^{2}\int _{0}^{1}2y-3x^2y^{2} \, dx  \, dy=\int_{0}^{2} [2yx-y^{2}x^{3}]^{1}_{0} \, dy  
$$
$$
=\int _{0}^{2}2y-y^{2} \, dy= \left[ y^{2}-\frac{y^{3}}{3} \right]_{0}^{2}=4-\frac{8}{3}=\frac{4}{3}
$$
## $y$-simplicity
A region $R$ is $y$-simple if every line parallel to the $y$-axis which intersect $R$ does so in a single line segment or point:
![[Double Integrals 2024-11-15 14.10.28.excalidraw]]
The region $R_{1}$ for example, is $y$-simple and the upper and lower boundaries are given by the functions $y=\phi_{1}(x)$ and $y=\phi_{2}(x)$ respectively, but the region $R_{2}$ is not $y$-simple
The double integral of $f(x,y)$ over $D_{1}$ can be calculated as an iterated integral, integrating over $y$ first:
$$
\iint_{R}f(x,y)\,dxdy=\int ^{b}_{a} \left( \int _{y=\phi_{1}(x)}^{y=\phi_{2}(x)}f(x,y) \, dy  \right) \, dx 
$$
## $x$-simplicity
This is an equivalent definition; a region $R$ is $x$-simple if every line parallel to the $x$-axis which intersects $R$ does so in a simgle line segment (or point
![[Double Integrals 2024-11-15 14.19.08.excalidraw]]
This region is $x$-simple, but not $y$-simple; the boundaries of $R$ are the curves $x=\psi_{1}(y)$ and $x=\psi_{2}(y)$ for $c\leq y\leq d$
The double integral of $f(x,y)$ over this region can be written as an iterated integral by integrating over $x$ first:
$$
\iint_{R}f(x,y)\,dxdy=\int _{c}^{d}\left( \int _{x=\psi_{1}(y)}^{x=\psi_{2}(y)}f(x,y) \, dx  \right) \, dy
$$
If a region is both $x$-simple and $y$-simple, the double integral can be calculated by integrating over $x$ or $y$ first
Sometimes a region may be both $x$-simple and $y$-simple, but the integral is only possible one of the ways
If a region is neither $y$-simple nor $x$-simple, there is always a way to separate it into multiple regions that must be eithe $x$-simple or $y$-simple
### Bounded by 1 function
![[Double Integrals 2024-02-21 17.34.29.excalidraw]]
$$
V=\iint_{R}f(x,y)dA , R=\{(x,y):a\leq x\leq b, c\leq y\leq f(x)\}=\int ^{b}_{a} \int _{c}^{f(x)} f(x,y) \, dy  \, dx
$$
#### Example
$$
V=\iint_{R}4+2x-y^{2}\, dA, R=\left\{ (x,y):1\leq x\leq 3, 0\leq y\leq \left( x-\frac{3}{2}\right)^{2}+2  \right\}=\int _{1}^{3}\int_{0}^{ \left( x-\frac{3}{2}\right)^{2}+2} 4+2x-y^{2} \, dy  \, dx
$$
![[Pasted image 20240221180919.png]]
$$
=\int _{1}^{3}[(4+2x)y-y^{2}]_{0}^{\left( x-\frac{3}{2}\right)^{2}+2} \, dx =\int _{1}^{3}(4+2x)\left(\left( x-\frac{3}{2}\right)^{2}+2\right)-\left( \left( x-\frac{3}{2}\right)^{2}+2\right)^{2} \, dx 
$$
$$
=\frac{1139}{40}
$$

### Bounded by 2 functions
![[Double Integrals 2024-02-21 18.18.20.excalidraw]]
$$
V=\iint_{R}f(x,y)dA, R=\{(x,y):f_{l}(y)\leq x\leq f_{u}(y), a\leq y\leq b\} = \int ^{b}_{a} \int _{f_{l}(y)}^{f_{u}(y)}f(x,y) \, dx  \, dy  
$$
#### Example
$$
V=\iint_{R}e^x+y-x^3+2\,dA, R=\left\{ (x,y):0\leq x\leq 4, \frac{1}{2}x\leq y\leq \frac{3}{2}x \right\}
$$
$$
=\int _{0}^{4}\int _{\frac{1}{2}x}^{\frac{3}{2}x}e^{x}+y-x^{3}+2 \, dy  \, dx 
$$
![[Pasted image 20240221184336.png]]
$$
=\int _{0}^{4}\left[ (e^{ x }-x^{3})y+\frac{y^{2}}{2} \right]_{\frac{1}{2}x}^{3/2x} \, dx 
$$
$$
=\int _{0}^{4} \left( \frac{3}{2}x(e^{ x }-x^{3})+\frac{\left( \frac{3}{2}x \right)^{2}}{2} \right)-\left( \frac{1}{2}x(e^{ x }-x^{3})+\frac{\left( \frac{1}{2}x \right)^{2}}{2} \right) \, dx =3e^{ 4 }-\frac{2737}{15}
$$
### Bounded by 4 functions
![[Double Integrals 2024-02-21 20.00.20.excalidraw]]
This is not possible using the above methods, so you need to re-write the axes so that they are linear, to do this you need to use the [[Jacobian Transformation]]:
$$
\iint_{R}f(x,y) \, dA_{(x,y)}=\iint_{S}f(x(u,v),y(u,v)) |J(u,v)| \, dA_{u,v}
$$
### Example
$$
V=\iint_{R} e^{ xy }dA, R=\text{Bounded by}\begin{cases}
y=\frac{1}{2}x \\ y=x \\y=\frac{1}{x} \\y=\frac{2}{x}
\end{cases}
$$
![[Pasted image 20240221201443.png]]
Let $v=xy$, $u=\frac{y}{x}$, $\therefore y=\sqrt{ uv }$, $x=\sqrt{ \frac{v}{u} }$, $\frac{ \partial x }{ \partial u }=-\frac{v}{2u^{2}\sqrt{ \frac{v}{u} }}$, $\frac{ \partial x }{ \partial v }=\frac{1}{2u\sqrt{ \frac{v}{u} }}$, $\frac{ \partial y }{ \partial u }=\frac{v}{2\sqrt{ uv }}$, $\frac{ \partial y }{ \partial v }=\frac{u}{2\sqrt{ uv }}$
$$
\implies J(u,v)=-\frac{1}{4u}-\frac{1}{4u}=-\frac{1}{2u}
$$
$$
\implies V=\iint_{S}e^{ xy } \, |J(u,v)|\,dA_{u,v}
$$
New bounds, $\frac{1}{2}\leq u\leq 1, 1\leq v\leq 2$
$$
\implies V=\int _{\frac{1}{2}}^{1}\int _{1}^{2} \frac{e^{ v }}{2u} \, dv  \, du =\frac{\ln 2}{2}(e^{2}-e)
$$
 ___
 Let $D$ be a square in the $xy$-plane with vertices $(0,0),(1,1),(2,0),(1,-1)$, calculate:
 $$
\iint_{D}(x+y)\,dxdy
$$
Using a change of variables $x=u+v$, $y=u-v$
![[Double Integrals 2024-11-15 15.40.07.excalidraw]]
First we express $D$ in terms of $u$ and $v$, we have:
$$
\frac{x+y}{2}=u, \frac{x-y}{2}= v
$$
So the vertices of $D$ map to the $[u,v]$ coordinates: $[0,0],[1,0],[1,1],[0,1]$:
![[Double Integrals 2024-11-15 15.45.27.excalidraw]]
The edges of $D$ in the $xy$-plane lie on the lines $y=x$, $y=-x$, $y=x-2$, $y=2-x$, these map to the lines $u=0,v=0,u=1,v=1$ 
So $D$ is a square in the $uv$-plane with vertices as above. The Jacobian is:
$$
J=\frac{ \partial (x,y) }{ \partial (u,v) } =\left| \begin{pmatrix}
\frac{ \partial x }{ \partial u } &\frac{ \partial x }{ \partial v } \\\frac{ \partial y }{ \partial u } &\frac{ \partial y }{ \partial v } 
\end{pmatrix}\right|=\left|  \begin{pmatrix}
1&1\\1&-1
\end{pmatrix}\right|=-2
$$
So $dA=|J|dudv=2dudv$, finally the integrand is $x+y=2u$, so
$$
\iint_{D}(x+y)\,dA=\int _{0}^{1}\int _{0}^{1}2u\times 2 \, du  \, dv=2 
$$
#Mathematics #Calculus