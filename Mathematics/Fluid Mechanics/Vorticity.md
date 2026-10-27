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
