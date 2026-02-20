## Definition
Gauss' Law is one of Maxwell's equations describing [[Electric Fields|electric fields]], it is
$$
\underline{\nabla} \cdot \underline{E} =\frac{\rho}{\varepsilon_{0}}
$$
## Integral Form
We also have from Maxwell's equations that
$$
\underline{\nabla} \times \underline{E} =0
$$
We can form an integral from of Gauss' law by considering a closed region $V\subset \mathbb{R}^{3}$ with boundary
$$
S=\partial V
$$
Integrating both sides over $V$:
$$
\int _{V}\underline{\nabla} \cdot \underline{E}  \, d^{3}\underline{x} = \frac{1}{\varepsilon_{0}}\int _{V}\rho \, d^{3}\underline{x}  
$$
We know about the RHS that
$$
\int _{V}\rho \, d^{3}\underline{x}=Q_{V} 
$$
Where $Q_{V}$, the [[electric charge|electric charge]] contained in $V$
We know that the LHS satisfies
$$
\int _{V}\underline{\nabla} \cdot \underline{E}  \, d^{3}\underline{x}=\int _{S}\underline{E} \cdot\, d \underline{S}  
$$
By [[Divergence Theorem|divergence theorem]], hence we get the integral form of Gauss' law:
$$
\int _{\partial V}\underline{E}\cdot \, d\underline{S}= \frac{Q_{V}}{\varepsilon_{0}} 
$$
Which gives a pretty non-trivial things like that $\underline{E}$ flux is independent of surface as long as it encloses the same amount of charge
Also only charges enclosed inside the surface contribute to the $\underline{E}$ [[Surface Integrals|flux]] 
The integral form is useful in simple surfaces with many symmetries, note that we still need to impose that $\underline{\nabla} \times \underline{E}=0$
## Example
Say we want to find the electric field of the infinite charged wire with constant linear charge density $\eta$
A natural coordinate system to suse is cylindrical, we have
$$
\underline{E}(r,\phi,z)=\underline{E}(r)=E_{r}(r)\underline{e}_{r}+E_{\phi}(r)\underline{e}_{\phi}+E_{z}(r)\underline{e}_{z}
$$
Since we can rotate it around the $z$ axis, we must have the field independent of angle $\phi$, so $E_{\phi}=0$, also since we can translate up and down the $z$ axis, $E_{z}=0$
So it only depends on $E(r)$.
$$
\int _{S} \underline{E} \cdot\, d \underline{S} = \frac{Q_{V}}{\varepsilon_{0}}
$$
If we make a cylinder of height $L$ and radius $r$, with top and bottom faces $S_{T},S_{B}$ respectively, then we can say $S=S_{T}u$