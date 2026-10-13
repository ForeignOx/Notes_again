A stream function is a scalar field that can encode $\underline{u}$ and streamlines inside a single scalar function
## Assumptions
Assume the fluid flow is [[Incompressibility|incompressible]] and 2D, so
$$
\underline{u}=\begin{pmatrix}
u \\
v
\end{pmatrix}
$$
We take an ansatz $\underline{F}=\begin{pmatrix}-u \\ v\end{pmatrix}$ which is conservative which we can see by showing that its integral over a closed curve is 0, so
$$
\oint_{C}\underline{F}\cdot d\underline{x}=\oint-vdx+udy 
$$
$$
= \iint_{R}\frac{ \partial u }{ \partial x } +\frac{ \partial v }{ \partial y } ~dx~dy
$$
By Green's theorem
$$
=\iint_{R}\underline{\nabla} \cdot \underline{u} ~dx~dy=0
$$
As $\underline{u}$ is divergence free (as it's incompressible)
Now recall that conservative vector fields can always be written as the gradient of a scalar field, so $\exists \psi: \underline{F}=\underline{\nabla }\psi$, so
$$
\frac{ \partial \psi }{ \partial x } =-v,\frac{ \partial \psi }{ \partial y } =u
$$
We call $\psi$ the streamfunction, and
$$
\underline{u}=\underline{\nabla} \times \psi\underline{e}_{z} 
$$
In [[Curvilinear Coordinates|cylindrical coordinates]], 
$$
\underline{u}=\frac{1}{r}\det \begin{pmatrix}
\underline{e}_{r} & r\underline{e}_{\theta} & \underline{e}_{z} \\
\frac{ \partial  }{ \partial r }  & \frac{ \partial  }{ \partial \theta }  & \frac{ \partial  }{ \partial z }  \\
0 & 0 & \psi 
\end{pmatrix} =\frac{1}{r}\frac{ \partial \psi }{ \partial \theta } \underline{e}_{r}-\frac{ \partial \psi }{ \partial r } \underline{e}_{\theta}
$$
So our equivalent equations to the ones above where $\underline{u}=u_{r}\underline{e}_{r}+u_{\theta}\underline{e}_{\theta}$,
$$
u_{r}=\frac{1}{r}\frac{ \partial \psi }{ \partial \theta } ,~u_{\theta}=-\frac{ \partial \psi }{ \partial r } 
$$
Another bonus function of the stream function is that
$$
\underline{u}\cdot \underline{\nabla } \psi=-uv+uv=0
$$
So $\underline{u}$ is perpendicular to $\underline{\nabla }\psi$, which means that lines of $\psi=c$ for $c$ constant are [[streamlines|streamlines]]
## Stream Functions to Measure Flux
The stream function has an additional physical interpretation. Take two points on the same streamline and draw a curve $C$ between them. What is the total flux through this curve?
![[Pasted image 20261013153322.png]]
Flux is eaual to $\int _{C}\underline{u}\cdot \hat{\underline{n}} \, ds$ but no flow can pass through the streamline, because, as we've seen, the streamline is parallel to the velocity. So there's only one way in and out of the region enclosed by the streamline and $C$, so by [[Mass Conservation|mass conservation]], the total flow in through $C$ must equal the total flow out through $C$, soo 
$$
\int _{C}\underline{u}\cdot \hat{\underline{n}} \, ds=0
$$
If $C$ passes instead between points on two different streamlines, what's the flux now? We can again calculate $\oint\underline{u}\cdot \hat{\underline{n}}~ds$ but we should first observe that flux can go in either direction through $C$; whichever way we pick $\hat{\underline{n}}$ will represent positive flux
![[Pasted image 20261013153835.png]]
Let $C$ be any simple curve connecting $\underline{x}_{1}$ to $\underline{x}_{2}$ with tangent vector $\underline{t}(s)$,
$$
\underline{t}=\begin{pmatrix}
t_{x} \\
t_{y}
\end{pmatrix}
$$
The unit normal to $C$ can therefore be written as:
$$
\hat{\underline{n}}=\frac{1}{\left| \underline{t} \right| }\begin{pmatrix}
t_{y} \\
-t_{x}
\end{pmatrix}
$$
Which points clockwise relative to $\underline{x}_{1}$, the flux through $C$ in this direction is
$$
\int _{C} \underline{u}\cdot \hat{\underline{n}} \, ds=\int _{C}\begin{pmatrix}
\frac{ \partial \psi }{ \partial y }  \\
-\frac{ \partial \psi }{ \partial x } 
\end{pmatrix} \cdot \frac{1}{\left| \underline{t} \right| }\begin{pmatrix}
t_{y} \\
-t_{x} 
\end{pmatrix} \, ds 
$$
$$
= \int _{C} \frac{\underline{\nabla } \psi\cdot \underline{t}}{\left| \underline{t} \right| } \, ds=\int _{C}\underline{\nabla } \psi \cdot d\underline{x} =\psi(\underline{x}_{2})-\psi(\underline{x}_{1})
$$
Which is path independent