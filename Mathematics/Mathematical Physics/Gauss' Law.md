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
If we make a cylinder of height $L$ and radius $r$, with top and bottom faces $S_{T},S_{B}$ and cylindrical part $S_{r}$, then we can say $S=S_{T}\cup S_{B}\cup S_{r}$
We know that $Q_{V}=\eta L$, so we just need to do the integrals now
$$
d\underline{S}_{T}=\underline{e}_{z}\cdot d S_{T},~ d \underline{S}_{B}=-\underline{e}_{z} \cdot dS_{B},~d\underline{S}_{r}=\underline{e}_{r}\cdot dS_{r}
$$
soooo
$$
    \int _{S}\underline{E} \, d \underline{S}=\int _{S_{T}}\underline{E} \cdot\, d\underline{S}_{T}+\int _{S_{B}} \underline{E}\cdot \, d \underline{S}_{B}+\int _{S_{r}}\underline{E} \, d\underline{S}_{r} 
$$
$$
= \cancelto{ 0 }{ \int _{S_{T}} E(r) \underline{e}_{r}\cdot \underline{e}_{z} \, dS_{T} }-\cancelto{ 0 }{ \int _{S_{B}}E(r)\underline{e}_{r}\cdot \underline{e}_{z} \, dS_{B} }+\int _{S_{r}}E(r)\underline{e}_{r}\cdot \underline{e}_{r} \, dS_{r}
$$
$$
= E(r)\int _{S_{r}} \, d S_{r}=E(r)2\pi rL  
$$
So Gauss' law gives
$$
E(r)2\pi rL=\frac{1}{\varepsilon_{0}}\eta L 
$$
$$
\implies E(r)=\frac{\eta}{2\pi\varepsilon_{0}} \frac{1}{r}
$$
And 
$$
\underline{E}= E(r)\underline{e}_{r}=\frac{\eta}{2\pi\varepsilon_{0}} \frac{\underline{e}_{r}}{r}
$$
___
Infinite plane with constant surface charge density $\sigma$, by symmetry we can have translations along $x$ and $y$
We have that $E_{x}=0$ and $E_{y}=0$, so $\underline{E}=E(z)\underline{e}_{z}$
Also that $E(-z)=-E(z)$
So by Gauss' law,
$$
\int _{S}\underline{E} \, d \underline{S}=\frac{Q_{V}}{\varepsilon_{0}} 
$$
We construct a cylinder(?) of same dimensions as previous example
We have total charge equal to $\sigma A$ where $A$ is the area of the end of one of the cylinders
Doing the actual integrals,
$$
\int _{S} \underline{E}\cdot \, d\underline{S}=\int _{S_{B}}\underline{E}\cdot \, d\underline{S}_{B}+\int _{S_{T}}\underline{E}\cdot \, d\underline{S}_{T}   +\int _{S_{r}}\underline{E}\cdot \, d\underline{S}_{r} 
$$
Due to our symmetries, the last integral is zero...
$$
        =-\int _{S_{B}}E(-z)\underline{e}_{z}\cdot \underline{e}_{z} \, dS_{B}+\int _{S_{T}}E(z)\underline{e}_{z}\cdot \underline{e}_{z} \, dS_{T} 
$$
$$
= -E\left( -\frac{L}{2} \right)  \int _{S_{B}} \, dS_{B}+E\left( \frac{L}{2} \right)\int _{S_{T}} \, dS_{T}=A\left( E\left( \frac{L}{2} \right)-E\left( -\frac{L}{2} \right) \right)  
$$
So by Gaus' Law, and since $L$ can be anything, we can call it $z$
$$
E(z)-E(-z)=\frac{\sigma}{\varepsilon_{0}}
$$
$$
\implies E(z)=\frac{\sigma}{2\varepsilon_{0}}
$$
Which is constant
