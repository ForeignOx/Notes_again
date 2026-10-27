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
___
Next consider $\underline{u}=\frac{k}{r}\underline{e}_{\theta}$ which has a singularity at the origin, things rotating near the origin go faster whereas the further from the origin, the slower they rotate
$$
\underline{\omega}(\underline{x})=\underline{\nabla} \times \underline{u} =\underline{0}
$$
So the vorticity is $0$ away from $r=0$, so the vorticity must just be generated at $r=0$, the fluid is rotating, but not the fluid particles this is curious
This is apparently a decent model for tornadoes
Let's calculate the circulation