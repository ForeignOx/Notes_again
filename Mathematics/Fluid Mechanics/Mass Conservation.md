One of the key principles of physics is that mass cannot be created nor destroye in the classical limit
We also know that water pumped through a funnel speeds up, so there must be a law that places a restriction on the velocity of the fluid.
Consider a mass $m$ of fluid inside a fixed fluid volume $V$ with surface $S$. The mass is the integral of density:
$$
m=\int _{V}\rho \, dV 
$$
Although our volume is fixed, the mass can change as fluid particles enter and leave the volume
![[Pasted image 20261013102826.png]]
The mass which leaves $V$ through $S$ per unit time, is the integral of all the mass leaving $V$, outward through the pieces of surface $dS$:
We get that change of mass is equal to the density on travelling through the surface, so
$$
-\frac{d m}{dt} =-\frac{d }{dt} \int _{V}\rho \, dV =\int _{S}\rho \underline{u}\cdot \hat{\underline{n}} \, dS=\int \rho \underline{u}\cdot \, d\underline{S}  
$$
As the volume is fixed, differentiating under the integral and using the [[divergence theorem|divergence theorem]] gives us, 
$$
\int _{V}\frac{ \partial \rho }{ \partial t } +\underline{\nabla} \cdot \rho\underline{u}  \, dV=0 
$$
Since this is true for any volume, we need the inside of the integral to be zero. Using the [[Leibniz Rule|product rule]] for [[Divergence and Curl|divergence]],
$$
\underline{\nabla} \cdot \rho\underline{u} =\underline{u}\cdot \underline{\nabla } \rho +\rho \underline{\nabla} \cdot \underline{u} 
$$
We can write the continuity equation:
$$
\frac{ \partial \rho }{ \partial t } +\rho \underline{\nabla} \cdot \underline{u} +\underline{u}\cdot \underline{\nabla } \rho=\frac{D\rho}{Dt}+\rho \underline{\nabla} \cdot \underline{u} =0
$$
This whole derivation was done in the Eulerian perspective. In the Lagrangian perspective we follow a fluid particle and fix the mass, so the surface can deform with the flow. Differentiating under the integral needs different handling using the Reynolds transport theorem
