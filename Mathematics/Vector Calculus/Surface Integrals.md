## Of [[Scalar Fields|Scalar Fields]]
If $f:\mathbb{R}^{3}\to \mathbb{R}$ is a scalar field and $S$ is a surface with parametrisation $\underline{x}(u,v)$, then we define the surface integral of $f$ over $S$ to be:
$$
\int _{S}f \, dS=\int _{U}f(\underline{x}(u,v))\left| \frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v }  \right|  \, dudv  
$$
Where $U$ is the preimage of $S$ in the $uv$-plane
The idea is that the area element $\left| \frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v }  \right|  \, dudv$ is the ara on $S$ corresponding to an infinitesimal rectangle with sides $du,dv$ in the $uv$-plane:
![[Pasted image 20251015181817.png]]
Note that the value of $\int _{S}f \, dS$ does not depend on the sign of $\frac{ \partial \underline{x} }{ \partial u }\times \frac{ \partial \underline{x} }{ \partial v }$
Note that the surface area of $S$ is $\left| S\right|=\int _{S} \, dS$ i.e. $f(\underline{x})\equiv 1$ (which is the same as for arclength)
## Proposition
The surface integral of a scalar field is independent of the choice of parametrisation
### Proof
Suppose $\underline{x}(u,v)$ and $\underline{x}(\mu,\nu)$ parametrise the same surface:
$$
\frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v } =\left( \frac{ \partial \underline{x} }{ \partial \mu } \frac{ \partial \mu }{ \partial u } +\frac{ \partial \underline{x} }{ \partial \nu } \frac{ \partial \nu }{ \partial u }  \right)\times\left( \frac{ \partial \underline{x} }{ \partial \mu } \frac{ \partial \mu }{ \partial v } +\frac{ \partial \underline{x} }{ \partial \nu } \frac{ \partial \nu }{ \partial v }  \right)
$$
$$
= \frac{ \partial \underline{x} }{ \partial \mu } \frac{ \partial \mu }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial \nu } \frac{ \partial \nu }{ \partial v } +\frac{ \partial \underline{x} }{ \partial \nu } \frac{ \partial \nu }{ \partial u } \times\frac{ \partial \underline{x} }{ \partial \mu } \frac{ \partial \mu }{ \partial v } 
$$
$$
= \left( \frac{ \partial \mu }{ \partial u } \frac{ \partial \nu }{ \partial v }-\frac{ \partial \mu }{ \partial v } \frac{ \partial \nu }{ \partial u }   \right)\frac{ \partial \underline{x} }{ \partial \mu } \times \frac{ \partial \underline{x} }{ \partial \nu } = J\frac{ \partial \underline{x} }{ \partial \mu } \frac{ \partial \underline{x} }{ \partial \nu } 
$$
Where $J$ is the [[Jacobian Transformation|Jacobian]] for going from $(\mu,\nu)\to(u,v)$
$$
\implies \left| \frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v }  \right|=\left| J \right| \left| \frac{ \partial \underline{x} }{ \partial \mu } \times \frac{ \partial \underline{x} }{ \partial v }  \right| 
$$
$$
\implies \int _{U}f(\underline{x}(u,v))\left| \frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v }  \right|  \, dudv=\int _{U}f(\underline{x}(\mu,\nu))\left| J \right| \left| \frac{ \partial \underline{x} }{ \partial \mu } \times \frac{ \partial \underline{x} }{ \partial \nu }  \right| \, \frac{d\mu d\nu}{\left| J \right| }
$$
$$
 =\int _{U}f(\underline{x}(\mu,\nu))\left| \frac{ \partial \underline{x} }{ \partial \mu } \times \frac{ \partial \underline{x} }{ \partial \nu }  \right|  \, d\mu d\nu 
$$
## Remark
If $S\in\mathbb{R}^{2}$ is a flat surface in the $xy$-plane, then our parametrisation $\underline{x}(u,v)$ is just a change of variables and 
$$
\left| \frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v }  \right| =\left| \frac{ \partial x }{ \partial u } \frac{ \partial y }{ \partial v } -\frac{ \partial x }{ \partial v } \frac{ \partial y }{ \partial u }  \right| =\left| J \right| 
$$



### Examples
Find the area element for the plane $z=ax+b$ when parametrised by $(x,y)$
So we have the parametrisation $\underline{x}(x,y)=x\underline{e}_{1}+y\underline{e}_{2}+(ax+b)\underline{e}_{3}$,
$$
\implies \frac{ \partial \underline{x} }{ \partial x } \times \frac{ \partial \underline{x} }{ \partial y } =-\frac{ \partial  }{ \partial x } (ax+b)\underline{e}_{1}-\frac{ \partial  }{ \partial y } (ax+b)\underline{e}_{2}+\underline{e}_{3}=a\underline{e}_{1}+\underline{e}_{3}
$$
So the area element is 
$$
\left| \frac{ \partial \underline{x} }{ \partial x } \times \frac{ \partial \underline{x} }{ \partial y }  \right| dxdy=\sqrt{ 1+a^{2} }dxdy
$$
___
Find the surface area of the sphere $x^{2}+y^{2}+z^{2}=a^{2}$
We shall parametrise with spherical coordinates, since $r=a$ will remain constant
$$
\underline{x}(\theta,\phi)=a\sin\theta \cos \phi \underline{e}_{1}+a\sin\theta \sin \phi \underline{e}_{2}+a\cos\theta \underline{e}_{3},\theta \in [0,\pi],\phi \in [0,2\pi]
$$
Recall that $h_{\theta}=a,h_{\phi}=a\sin\theta$, so we find that $\left| \frac{ \partial \underline{x} }{ \partial \theta }\times \frac{ \partial \underline{x} }{ \partial \phi } \right|=h_{\theta}h_{\phi}=a^{2}\sin\theta$ from this [[Curvilinear Coordinates#Proposition|proposition]], therefore
$$
\left| S \right| =\int _{S} \, dS =\int_{0}^{2\pi} \int_{0}^{\pi} a^{2}\sin\theta \, d\theta  \, d\phi=a^{2}\int_{0}^{2\pi} [-\cos\theta]_{0}^{\pi} \, d\phi=2a^{2}\int_{0}^{2\pi}  \, d\phi=4\pi a^{2}  
$$
___
Find the surface are of the torus from a previous example, we had $\underline{x}(u,v)$ for $u,v\in[0,2\pi]$ and $\left| \frac{ \partial \underline{x} }{ \partial u }\times \frac{ \partial \underline{x} }{ \partial v } \right|=R+\cos v$, so
$$
\left| S \right| =\int_{0}^{2\pi} \int_{0}^{2\pi} R+\cos v \, du  \, dv=2\pi \int_{0}^{2\pi} R+\cos v \, dv =4\pi^{2}R 
$$
## Of [[Vector Fields|Vector Fields]]
If $\underline{f}:\mathbb{R}^{3}\to \mathbb{R}^{3}$ is a vector field and $S$ is an oriented surface with unit normal $\underline{\hat{n}}$ we define the surface integral (or flux) of $\underline{f}$ through $S$ as:
$$
\int _{S} \underline{f}\cdot   \underline{\hat{n}} \, dS =\int _{U} \underline{f}(\underline{x}(u,v))\cdot   \underline{\hat{n}}\left| \frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v }  \right|  \, dudv=\int _{U} \underline{f}(\underline{x}(u,v))\cdot\left( \frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v }  \right) \, dudv  
$$
![[Pasted image 20251020195904.png]]
### Notes
- Sometimes we see the notation $\underline{\hat{n}}=\underline{dS}$ which one might call the vector area element
- Unlike a scalar surface integral, the flux also depends on the sign of $\underline{\hat{n}}$
- A non-zero flux requires a component of $\underline{f}$ "through" the surface
- If the surface is closed, we write $\int _{S} \underline{f} \cdot  \underline{\hat{n}} \, dS=\oint_{S}  \underline{f} \cdot  \underline{\hat{n} }\,dS$ which, unlike circulation, has no special name :(
### Example
Calculate the outward flux of $\underline{f}(\underline{x})=\cos ^{7}\theta \underline{e}_{r}$ (in spherical coordinates) through the hemisphere $r=a$, $z\geq 0$.
![[Pasted image 20251020200141.png]]
We paramerise in spherical coordinates: $\underline{x}(\theta,\phi)$ recall $\underline{\hat{n}}=\underline{e}_{r}$ and $\left| \frac{ \partial \underline{x} }{ \partial \theta }\times \frac{ \partial \underline{x} }{ \partial \phi } \right|=h_{\theta}h_{\phi}=a^{2}\sin\theta$, so
$$
    \int _{S}\underline{f}\cdot   \underline{\hat{n}} \, dS =\int_{0}^{2\pi} \int_{0}^{\frac{\pi}{2}} \underline{f} \cdot   \underline{\hat{n}}\left| \frac{ \partial \underline{x} }{ \partial \theta } \times \frac{ \partial \underline{x} }{ \partial \phi }  \right|  \, d\theta  \, d\phi 
$$
$$
= \int_{0}^{2\pi} \int_{0}^{\frac{\pi}{2}} \cos ^{7}\theta \underline{e}_{r} \cdot \underline{e}_{r}a^{2}\sin\theta \, d\theta  \, d\phi  =a^{2}\int_{0}^{2\pi} \int_{0}^{\frac{\pi}{2}} \cos ^{7}\theta \sin\theta \, d\theta  \, d\phi 
$$
$$
= a^{2}\int_{0}^{2\pi} \left[ -\frac{1}{8} \cos ^{8}\theta \right]^{\frac{\pi}{2}}_{0} \, d\phi=\frac{a^{2}}{8}\int_{0}^{2\pi}  \, d\phi  =\frac{\pi a^{2}}{4}
$$
Consider this time we do the full sphere :o
Now the only difference is $\theta \in[0,\pi]$, but since $\underline{f}=\cos ^{7}\theta \underline{e}_{r}$, this is antisymmetric about the equator $\theta=\frac{\pi}{2}$, so $\oint_{S} \underline{f} \cdot  \underline{\hat{n}}\,dS=0$
___
## Vector-Valued Surface Integrals
One can also have vector-valued surface integrals of the form
$$
\int _{S} \underline{f} \, dS
$$
For some vector field $\underline{f}:\mathbb{R}^{3}\to \mathbb{R}^{3}$
### Example
Evaluate $\int _{S} \underline{e}_{r} \, dS$, where $S$ is the hemisphere $r=a,z\geq 0$ and $\underline{e}_{r}$ is the spherical basis vector. Sadly, since $\underline{e}_{r}$ is not constant over $S$, because its direction varies, we cannot take it out of our integral
Instead we can write it in the Cartesian basis:
$$
\underline{e}_{r} = \sin\theta \cos \phi \underline{e}_{1}+\sin\theta \sin \phi \underline{e}_{2}+\cos\theta \underline{e}_{3}
$$
Sooo
$$
 \int _{S}\underline{e}_{r} \, dS=  \underline{e}_{1}\underbrace{ \int_{S} \sin\theta \cos \phi \, dS }_{ =0 }+\underline{e}_{2}\underbrace{ \int_{S} \sin\theta \sin \phi  \, dS }_{ =0 }+\underline{e}_{3}\int_{S}\cos\theta  \, dS
$$
$$
= \underline{e}_{3}\int _{S} \cos\theta \, dS=\underline{e}_{3}\int_{0}^{2\pi} \int_{0}^{\frac{\pi}{2}} \cos\theta \left| \frac{ \partial \underline{x} }{ \partial \theta } \times \frac{ \partial \underline{x} }{ \partial \phi }  \right|  \, d\theta  \, d\phi 
$$
$$
= a^{2}\underline{e}_{3}\int_{0}^{2\pi} \int_{0}^{\frac{\pi}{2}} \cos\theta \sin\theta \, d\theta \, d\phi=a^{2}\underline{e}_{3}\int_{0}^{2\pi} \left[ \frac{1}{2}\sin ^{2}\theta \right]_{0}^{2\pi} \, d\phi 
$$
$$
= \frac{a^{2}}{2}\underline{e}_{3}\int_{0}^{2\pi}  \, d\phi=\pi a^{2}\underline{e}_{3}   
$$
Note this is not the same as if you took the $\underline{e}_{r}$ out: $\underline{e}_{r}\int _{S} \, dS=\underline{e}_{r} \left| S \right|=2\pi a^{2}\underline{e}_{r}$ which is wrong in both direction and magnitude
We can think of $\frac{1}{\left| S \right|}\int _{S} \underline{e}_{r} \, dS$ as the average of $\underline{e}_{r}$ over $S$:
$$
\frac{1}{\left| S \right| } \int _{S} \underline{e}_{r} \, dS = \frac{1}{2\pi a^{2}}\pi a^{2} \underline{e}_{3}=\frac{1}{2} \underline{e}_{3} 
$$
