A 2D surface embedded in $\mathbb{R}^{3}$ can be defined parametrically as a map $\underline{x}(u,v)$ from $\mathbb{R}^{2}\to \mathbb{R}^{3}$ for $u\in[\upsilon_{0},u_{1}],\upsilon\in[\nu_{0},\nu_{1}]$.
![[Pasted image 20251015162717.png]]
For fixed $v=v_{0}$, position $\underline{x}(u,v_{0})$ is a curve with tangent vector $\frac{ \partial \underline{x} }{ \partial u }$ (and vice versa)
If $\underline{x}(u,v)$ is a well-defined parametrisation, then $\frac{ \partial \underline{x} }{ \partial u },\frac{ \partial \underline{v} }{ \partial v }$ are not collinear, so we define the unit normal to be:
$$
\underline{\hat{n}}=\frac{\frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v } }{\left| \frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v }  \right| }
$$
The sign of $\underline{\hat{n}}$ depends on the ordering of $\frac{ \partial \underline{x} }{ \partial u },\frac{ \partial \underline{x} }{ \partial v }$. A suface together with a specified consistent choice of $\underline{\hat{n}}$ is called oriented
## Smooth Surfaces
A surface is smooth if $\underline{\hat{n}}$ varies [[Continuity|continuously]] over the surface.
A surface is piecewise-smooth if it can be divided into finitely many smooth pieces (such as a cube)
## Open/Closed Surfaces
A surface is open if it is bounded by a [[Curves|curve]] (written $\partial S$), or closed if it has no boundary
## Examples
Find the outward unit normal for the sphere $x^{2}+y^{2}+z^{2}=a^{2}$ 
From spherical coordinates, $\underline{\hat{n}}=\underline{e}_{r}$ which we can derive from:
$$
\frac{ \partial \underline{x} }{ \partial \theta }\times \frac{ \partial \underline{x} }{ \partial \phi }=(h_{\theta}\underline{e}_{\theta})\times(h_{\phi}\underline{e}_{\phi})=h_{\theta}h_{\phi}(\underline{e}_{\theta}\times\underline{e}_{\phi})=h_{\theta}h_{\phi}\underline{e}_{r}
$$
By orthogonality
___
Find the outward unit normal for the torun
$$
\underline{x}(u,r)=(R+\cos v)\cos u \underline{e}_{1}+(R+\cos v)\sin u\underline{e}_{2}+\sin v \underline{e}_{3},u,v\in [0,2\pi]
$$
With $R>1$ constant
The tangent vectors are
$$
\frac{ \partial \underline{x} }{ \partial u } =-(R+\cos v)\sin u \underline{e}_{1}+(R+\cos v)\cos u \underline{e}_{2}
$$
$$
 \frac{ \partial \underline{x} }{ \partial v } =-\sin v\cos u \underline{e}_{1}-\sin v \sin u \underline{e}_{2}+\cos v \underline{e}_{3}
$$
So
$$
\frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v } =(R+\cos v)(\cos u\cos v\underline{e}_{1}+\sin u\cos v \underline{e}_{2}+\sin v \underline{e}_{3})
$$
$$
\left| \frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v } \right| =\left| R+\cos v \right| \sqrt{ \cos ^{2}u\cos ^{2}v +\sin ^{2}u\cos ^{2}v+\sin ^{2}v }=R+\cos v
$$
So the unit normal is
$$
\underline{\hat{n}}=\cos u \cos v \underline{e}_{1}+\sin u\cos v\underline{e}_{2}+\sin v \underline{e}_{3}
$$
If we plug in $u=0,v=0$, then
$$
\underline{\hat{n}}=\underline{e}_{1}
$$
So it is an outward normal
___
Sketch the surface $\underline{x}(r,\theta)=r\cos\theta \underline{e}_{1}+r\sin\theta \underline{e}_{2}+r \underline{e}_{3}$ for $r\in[0,\infty],\theta \in[0,2\pi]$ 
To sketch the surface, note that $x^{2}+y^{2}=z^{2}$, so this is in fact a cone at $\underline{x}=0$
![[Pasted image 20251015175227.png]]
To check smoothness, we compute the normal:
$$
\frac{ \partial \underline{x} }{ \partial r } \times \frac{ \partial \underline{x} }{ \partial \theta } =-r\cos\theta \underline{e}_{1}-r\sin\theta \underline{e}_{2}+r\underline{e}_{3}
$$
Which vanishes at $r=0$, so $\underline{\hat{n}}$ is not defined at $r=0$, so it is not smooth
___
Find the upward unit normal to the surface $z=h(x,y)$. (known as an explicit surface)
This would have parametrisation $\underline{x}(x,y)=x\underline{e}_{1}+y\underline{e}_{2}+h(x,y)\underline{e}_{3}$, so
$$
\frac{ \partial \underline{x} }{ \partial x } \times \frac{ \partial \underline{x} }{ \partial y } = -\frac{ \partial h }{ \partial x } \underline{e}_{1}-\frac{ \partial h }{ \partial y } \underline{e}_{2}+\underline{e}_{3} 
$$
And the unit normal would be
$$
\underline{\hat{n}}= \frac{-\frac{ \partial h }{ \partial x } \underline{e}_{1}-\frac{ \partial h }{ \partial y } \underline{e}_{2}+\underline{e}_{3} }{\sqrt{ 1+\frac{ \partial h }{ \partial x }^{2}+\frac{ \partial h }{ \partial y } ^{2}  }}
$$
