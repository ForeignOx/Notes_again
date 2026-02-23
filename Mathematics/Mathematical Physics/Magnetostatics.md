Magnetostatics are determined by setting 
$$
\frac{ \partial \underline{E} }{ \partial t }=\frac{ \partial \underline{B} }{ \partial t }=0
$$
Which, when plugged into Maxwell's Equations, gives
$$
\underline{\nabla} \cdot \underline{B} =0
$$
$$
\underline{\nabla} \times \underline{E} =\mu \underline{J}
$$
These two equations fully determine the field of magnetostatics.
Since we have time independence, [[Electric Fields|$\underline{E}$]] and [[Magnetic Fields|$\underline{B}$]] are actualy independent entities
Both of the systems of [[Electrostatics|electrostatics]] and magnetostatics are of the form
$$
\underline{\nabla} \cdot \underline{F} =D
$$
$$
 \underline{\nabla} \times \underline{F} =\underline{C}
$$
If we take the second and take the divergence of both sides
$$
0=\underline{\nabla} \cdot (\underline{\nabla} \times \underline{F} )=\underline{\nabla} \cdot \underline{ E}  
$$
By definitions of [[Divergence and Curl|divergence and curl]], so the divergence of $\underline{J}$ must be zero
## Helmoltz Theorem
One question we are interested is whether these equations are enough to completely fix $\underline{F}$?
Given a solution to $\underline{F}_{0}$, then
$$
\underline{F}=\underline{F}_{0}+\underline{W}
$$
Is also a solution if
$$
\underline{\nabla} \cdot \underline{W} =0,\underline{\nabla} \times \underline{W} =0
$$
For example if 
$$
\underline{W}(x,y,z)=gz\underline{e}_{1}+zx\underline{e}_{2}+xy\underline{e}_{3}
$$
So we need to supply boundary conditions that uniquely fix $\underline{F}$, (such as vanishing at $\infty$), then we can determine the solutions provided that $\underline{D}(\underline{r})$ and $\underline{C}(\underline{r})$ vanish faster than $\frac{1}{\left| \underline{r} \right|^{2}}$  as $\left| \underline{r} \right|\to \infty$
This is known as Helmoltz theorem
## Remark
By [[linear|linearity]],
$$
\underline{\nabla} \cdot \underline{E} _{1}=\frac{1}{\varepsilon_{0}}\rho_{1},~\underline{\nabla} \cdot \underline{E}_{2}=\frac{1}{\varepsilon_{0}}\rho_{2}
$$
$$
 \underline{\nabla} \times \underline{E} _{1}= \underline{\nabla} \times \underline{E} _{2}=0 
$$
Then
$$
\underline{\nabla} \cdot \underline{E} _{1}+\underline{\nabla} \cdot \underline{E} _{2}= \frac{1}{\varepsilon_{0}}(\rho_{1}+\rho_{2})=\underline{\nabla} \cdot (\underline{E}_{1}+\underline{E}_{2})
$$
$$
\underline{\nabla} \times \underline{E}_{1}+\underline{\nabla} \times \underline{E}_{2}=\underline{\nabla} \times (\underline{E}_{1}+\underline{E}_{2})=0   
$$
So our solutions are linear
The total $\rho_{T}=\rho_{1}+\rho_{2}$ has $\underline{E}_{T}=\underline{E}_{1}+\underline{E}_{2}$
So if we find several solutions, we can simply add them up
___
In magnetostatics, there is an absence of electric charge, so $\rho=0$
We study the electric current density $\underline{J}(\underline{x})$, which obeys the continuity equation
$$
\underline{\nabla} \cdot \underline{J} =0
$$
Which is already satisfied by Maxwell's equations
$$
\frac{ \partial \rho }{ \partial t } +\underline{\nabla } \underline{J}=0
$$
Note that there can be no analogue of magnetic charge
It is natural to consider integrating $\underline{\nabla} \times \underline{B}=\mu\underline{J}$ on surface $S$ and use [[Stokes' Theorem|Stokes' theorem]]
$$
\int _{S}(\underline{\nabla} \times \underline{A} )\cdot \, d \underline{S}=\int _{C=\partial S}\underline{A} \cdot\, d \underline{\ell}  
$$
Note that this introduces a key feature of directionality
Using Ampere's law $\underline{\nabla} \cdot \underline{ B}=0$,
$$
\int _{C-\partial S}\underline{B}\cdot \, d\underline{\ell}=\mu_{0}\int _{S}\underline{J}\cdot \, d\underline{S}=\mu_{0}I_{S} 
$$
This is the integral form of Ampere's law
So electric currents generate magnetic fields in a right-handed rule manner
Ampere's law gives some intuition, but the full answer is only given in symmetric cases
### Remark
Ampere's law seems a lil ambiguoso iykwim
If we have  boundary $\partial S=C$, this could be like the circle cutting a sphere into two hemispheres $S_{1}$ and $S_{2}$, should we calculate $I_{S_{1}}$ or $I_{S_{2}}$??
They end up being in fact the same, this is because $\underline{\nabla }\underline{J}=0$ which implies that
$$
\int _{V}\underline{\nabla } \underline{J} \, d V=0 
$$
Therefore, by Gauss' theorem
$$
\int _{S_{1}}\underline{J}\cdot \, d\underline{S}=-\int _{S_{2}}\underline{J} \, d\underline{S}
$$
$$
\implies I_{S_{1}}=I_{S_{2}}  
$$
Also it means $\underline{\nabla} \cdot \underline{B}=0$
## Examples
It is meaningful to define flux out of $\underline{B}$ through a loop
Consider the infinitely long straight wire.
It is natural to gue $\underline{B}(\underline{r})=B(\underline{\rho})\underline{\hat{e}}_{\varphi}$ (using cylinrical coords)
Henc we define $I_{S_{R}}=I$, and
$$
\int _{C_{R}}\underline{B}\cdot \, d \underline{\ell}=\int_{0}^{2\pi} B(R)R \, d\varphi=2  
$$

