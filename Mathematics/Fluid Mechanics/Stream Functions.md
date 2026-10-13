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
