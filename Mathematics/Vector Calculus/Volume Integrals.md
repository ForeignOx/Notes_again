## Of [[Scalar Fields|Scalar Fields]]
The volume integral of a scalar field $f:\mathbb{R}^{3}\to \mathbb{R}^{3}$ over a 3D subregion $V\subset \mathbb{R}^{3}$ is
$$
\int _{V}f \, dV=\int _{U} f(\underline{x}(u,v,w))\left| \frac{ \partial \underline{x} }{ \partial u }  \cdot\left( \frac{ \partial \underline{x} }{ \partial v } \times \frac{ \partial \underline{x} }{ \partial w }  \right) \right|  \, dudvdw
$$
Where $U$ is the preimage of $V$ in $uvw$-space
![[Pasted image 20251020205228.png]]
The "volume element" $\left| \frac{ \partial \underline{x} }{ \partial u }\cdot\left( \frac{ \partial \underline{x} }{ \partial v }\times \frac{ \partial \underline{x} }{ \partial w } \right) \right|dudvdw$ is the volume of an infinitesimal parallelepiped, which we get from the [[Scalar Triple Product|scalar triple product]], as it is the [[Determinants|determinant]] of the [[Matrices|matrix]]:
$$
\begin{pmatrix}
\frac{ \partial x  }{ \partial u } & \frac{ \partial x }{ \partial v }  & \frac{ \partial x }{ \partial w }  \\
\frac{ \partial y }{ \partial u }  & \frac{ \partial y }{ \partial v }  & \frac{ \partial y }{ \partial w }  \\
\frac{ \partial z }{ \partial u }  & \frac{ \partial z }{ \partial v }  & \frac{ \partial z }{ \partial w }  
\end{pmatrix}
$$
Which is the [[Jacobian Transformation|Jacobian determinant]] 
### Proposition
If $(u,v,w)$ are [[Orthogonality|orthogonal]] [[Curvilinear Coordinates|curvilinear coordinates]], then $\left| \frac{ \partial \underline{x} }{ \partial u } \cdot\left( \frac{ \partial \underline{x} }{ \partial v }\times \frac{ \partial \underline{x} }{ \partial w } \right) \right|=h_{u}h_{v}h_{w}$
#### Proof
Recall $\left| \frac{ \partial \underline{x} }{ \partial u }=h_{u} \right|,\frac{ \partial \underline{x} }{ \partial u }=h_{u}\underline{e}_{u}$, similarly $\frac{ \partial \underline{x} }{ \partial v }=h_{v}\underline{e}_{v},\frac{ \partial \underline{x} }{ \partial w }=h_{w}\underline{e}_{w}$ 
### Volume
The volume of $V$ is $\left|V \right|=\int _{V} \, dV$, i.e. $f(\underline{x})\equiv1$
#### Example
Find the volume of the ball enclosed by the sphere $x^{2}+y^{2}+z^{2}=a^{2}$
First recall spherical coordinates: $\underline{x}(r,\theta,\phi)=r\sin\theta \cos \phi \underline{e}_{1}+r\sin\theta \sin \phi \underline{e}_{2}+r\cos\theta \underline{e}_{3}$
$$
\left| \frac{ \partial \underline{x} }{ \partial u } \cdot \left( \frac{ \partial \underline{x} }{ \partial v } \times \frac{ \partial \underline{x} }{ \partial w }  \right) \right| =h_{r}h_{\theta}h_{\phi}=1\cdot r\cdot r\sin\theta=r^{2}\sin\theta
$$
$$
    \left| V \right| =\int_{0}^{2\pi} \int_{0}^{\pi} \int_{0}^{a} r^{2}\sin\theta \, dr  \, d\theta  \, d\phi=\int_{0}^{2\pi} \int_{0}^{\pi} \left[ \frac{r^{3}}{3}\sin\theta \right]_{0}^{a} \, d\theta  \, d\phi 
$$
$$
= \frac{a^{3}}{3}\int_{0}^{2\pi}[-\cos\theta]_{0}^{\pi} \, d\phi =\frac{2a^{3}}{3} \int_{0}^{2\pi}  \, d\phi= \frac{4\pi a^{3}}{3} 
$$
### Remark
Finding the correct limits can be tricky which is why one should always draw diagrams
### Proposition
The volume integral of a scalar field is independent of the choice of parametrisation/coordinates
#### Proof
Same as the 2D case, so extremely tedious :/
### Example
Let $V$ be the region bounded by the planes $x=0,y=0,z=2$ and the surface $z=x^{2}+y^{2}$ for $x,y\geq 0$. Calculate $\int _{V} x \, dV$, first we make a sketch
![[Pasted image 20251021100846.png]]
Due to the rotational symmetrhy, it makes sense to use cylindrical coordinates: $\underline{x}(r,\theta,z)=r\cos\theta \underline{e}_{1}+r\sin\theta \underline{e}_{2}+z\underline{e}_{3}$
We know they are orthogonal, so
$$
\left| \frac{ \partial \underline{x} }{ \partial r } \cdot \left( \frac{ \partial \underline{x} }{ \partial \theta } \times \frac{ \partial \underline{x} }{ \partial z }  \right) \right| =h_{r}h_{\theta}h_{z}=r
$$
Our limits are $y=0 \iff \theta=0$, $x=0 \iff \theta=\frac{\pi}{2}$, $r^{2}=x^{2}+y^{2}=z\implies r=\sqrt{ z }$
Soo
$$
\int _{V}x \, dV = \int_{0}^{2} \int_{0}^{\frac{\pi}{2}} \int_{0}^{\sqrt{ z }} xr \, dr  \, d\theta  \, dz  =\int_{0}^{2} \int_{0}^{\frac{\pi}{2}} \int_{0}^{\sqrt{ z }} r^{2}\cos\theta \, dr  \, d\theta  \, dz 
$$
$$
= \int_{0}^{2} \int_{0}^{\frac{\pi}{2}} \left[ \frac{r^{3}}{3} \right]_{0}^{\sqrt{ z }}\cos\theta \, d\theta \, dz=\int_{0}^{2} \int_{0}^{\frac{\pi}{2}} \frac{z^{\frac{3}{2}}}{3}\cos\theta \, d\theta  \, dz 
$$
$$
= \frac{1}{3}\int_{0}^{2} z^{\frac{3}{2}}[\sin\theta]_{0}^{\frac{\pi}{2}} \, dz =\frac{1}{3}\int_{0}^{2} z^{\frac{3}{2}} \, dz=\frac{1}{3}\left[ \frac{2}{5}z^{\frac{5}{2}} \right]_{0}^{2}=\frac{8\sqrt{ 2 }}{15} 
$$
## Vector Valued Volume Integrals
One can also have a vector-valued volume integral $\int _{V} \underline{f} \, dV$, which is the same as with surface integrals; evaluate by changing to cartesians:
$$
\int _{V} \underline{f} \, dV=\underline{e}_{1} \int _{V} f_{1} \, dV +\underline{e}_{2} \int _{V}f_{2} \, dV+\underline{e}_{3}\int _{V} f_{3} \, dV   
$$
An example of when one might use this is to calculate a centre of mass:
$$
\underline{x}= \frac{\int _{V} \rho(\underline{x})\underline{x} \, dV }{\int _{V}\rho(\underline{x}) \, dV }
$$
