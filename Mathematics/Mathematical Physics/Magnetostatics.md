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