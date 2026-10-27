## Definition
We define vorticity $\underline{\omega}$:
$$
\underline{\omega}=\underline{\nabla} \times \underline{u} 
$$
And it is equal to twice the angular velocity $\frac{1}{2}\underline{\omega}$
We say the angular velocity is a global measure of rotation, and the vorrticity a local measure of rotation or swirling
Flows are called irrotational if they have no vorticity, $\underline{\omega}=\underline{\nabla} \times \underline{u}= \underline{0}$
## Example
Let's calculate the vorticity for 
$$
\underline{u}(\underline{x})=-ky\underline{e}_{x}+kx\underline{e}_{y}=kr\underline{e}_{\theta}
$$
The vorticity is
$$
\underline{\omega}(\underline{x})=\underline{\nabla} \times \underline{u} =2k\underline{e}_{z}
$$
So we have a rotating flow and we have vorticity, but these could be coincidental, we have to be careful not to judge vorticity (local rotation at every point) based on overall rotation
___
Let's find the vorticity for $\underline{u}(\underline{x})=y\underline{e}_{x}$, here,
$$
\underline{\omega}=\underline{\nabla} \times \underline{u}=-\underline{e}_{z}
$$
so the fluid particles are rotating but the fluid is actually translating
## Line Vortex
Next consider $\underline{u}=\frac{k}{r}\underline{e}_{\theta}$ which has a singularity at the origin, things rotating near the origin go faster whereas the further from the origin, the slower they rotate
$$
\underline{\omega}(\underline{x})=\underline{\nabla} \times \underline{u} =\underline{0}
$$
So the vorticity is $0$ away from $r=0$, so the vorticity must just be generated at $r=0$, the fluid is rotating, but not the fluid particles this is curious
This is apparently a decent model for tornadoes
Let's calculate the circulation using the line integral. Suppose $C$ is the circle $r=R$, in polar coordinates, $d\underline{x}=dr \underline{e}_{r}+rd\theta \underline{e}_{\theta}+dz \underline{e}_{z}$, so
$$
\Gamma=\oint_{C}\underline{u}\cdot d\underline{x}=\oint_{C} \frac{k}{r}\underline{e}_{\theta}\cdot(dr \underline{e}_{r}+r d\theta \underline{e}_{\theta}+dz \underline{e}_{z})
$$
For our circle, this is:
$$
=\int_{0}^{2\pi} \frac{k}{R}R \, d\theta=2\pi k 
$$
This is independent of $R$, suggesting that all the circulation is generated at the origin. We call $\Gamma$ the strength of the line vortex
Notice how there is a non-zero circulation around $C$, even though $\underline{\omega}= \underline{0}$ at every point on $C$ and inide $C$, except from the origin, so $\underline{\omega}$ must be a [[Dirac Delta Function|delta function]]
We found that the circulation is independent of radius, taking $R\to \infty$, we can calculate the circulation in the whole plane. For the line vortex, we have:
$$
\Gamma=\int _{S}\underline{\omega}\cdot \, d \underline{S}=\int _{S}\underline{\omega}\cdot \hat{\underline{n}} \, dS 
$$
$$
= \int_{0}^{\infty} \int_{0}^{2\pi} \omega_{z}(r,\theta)r \, dr  \, d\theta  =2\pi k 
$$
From earliler, so we can write the vorticity of the line vortex as:
$$
\underline{\omega}=2\pi k\delta(r)\underline{e}_{z}
$$
## Vortex Tubes
The line vortex is pretty good, but let's consider a vortex with thickness, is circulation conserved in some way?
Conider a rigid body flow with lines parallel to $\underline{\omega}$ at each point on the curve, just lilke how we can define streamlines to be parallel to velocity, but this time parallel to vorticity instead. If we consider our rigid body planar flow from before, for example, where $\underline{\omega}(\underline{x})=2k \underline{e}_{z}$, it would look like:
![[Pasted image 20261027103206.png]]
We can make these s long as we like, exactly like streamlines but for vorticity.
These are called vortex lines or filaments, not to be confused with the line vortex
Taking the bundle of lines going through $C$, we end up with a wall of lines called a vortex tube
### Example
Consider the rigid body planar flow, bur scaled by $z$, $\underline{u}(\underline{x})=zr\underline{e}_{\theta}$, the further from $z=0$ you go, the faster you spin. The vorticity is:
$$
\underline{\omega}=\frac{1}{r}\left| \begin{pmatrix}
\underline{e}_{r} & r\underline{e}_{\theta} & \underline{e}_{z} \\
\frac{ \partial  }{ \partial r }  & \frac{ \partial  }{ \partial \theta }  & \frac{ \partial  }{ \partial z }  \\
0 & zr^{2} & 0
\end{pmatrix} \right| =-r\underline{e}_{r}+2z\underline{e}_{z}
$$
Drawing a curve $C$ at the bottom and following the vortex lines, our vortex tube is:
![[Pasted image 20261027104204.png]]
An upside-down tornado!
___
The circulation around the original $C$ is actually the same for all closed $C$ around the tube, allowing us to define the vortex tube's strength by this circulation $\Gamma$
To confirm this, picking two closed curves $C_{1}$ and $C_{2}$ around the same vortex tube:
![[Pasted image 20261027104334.png]]
Labelling the surface at the ends of the tube $S_{1}$ and $S_{2}$ and the tubular surface $S_{3}$, we can consider the difference between the two circulations:
$$
\Gamma_{2}-\Gamma_{1}=\int _{S_{2}}\underline{\omega}\cdot \, d\underline{S}-\int _{S_{1}}\underline{\omega} \cdot\, d\underline{S}  
$$
$$
        = \int _{S_{2}} \underline{\omega}\cdot \hat{\underline{n}} \, dS+\int _{S_{1}}\underline{\omega} \cdot \hat{\underline{n}} \, dS  
$$
$$
    = \int _{S_{2}} \omega\cdot \hat{\underline{n}} \, dS+\int _{S_{1}}\underline{\omega}\cdot \hat{\underline{n}} \, dS+\int _{S_{3}}\underbrace{ \underline{\omega}\cdot \hat{\underline{n}}  }_{ =0 }\, dS   
$$
$$
= \int _{S_{1}\cup S_{2}\cup S_{3}}\underline{\omega}\cdot \hat{\underline{n}} \, dS=\int _{V}\underline{\nabla} \cdot \underline{\omega}  \, dV  
$$
By the divergence theorem