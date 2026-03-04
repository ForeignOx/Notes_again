## General Solution
A plane wave on an [[electric fields|electric field]] $\underline{E}(x,t)=f_{R}(x-ct)\underline{e}_{y}$ then Maxwell's equations will be satisfied by [[magnetic fields|magnetic field]] $\underline{B}(x,t)=\frac{1}{c}f_{R}(x-ct)\underline{e}_{z}$ so the direction of propagation, $x$ is orthogonal to the electric field and the magnetic field, which are orthogonal to each other
If we choose $f_{R}(s)=E_{0}\sin(ks)$, then the electric field takes the form:
$$
\underline{E}(x,t)=E_{0}\sin(kx-kct)\underline{e}_{y}=E_{0}\sin(kx-\omega t)\underline{e}_{y}
$$
$$
\implies \underline{B}(x,t)=\frac{E_{0}}{c}\sin(kx-\omega t)\underline{e}_{z}
$$
Where we have defined $\omega=kc$
This is an example of a monochromatic wave propagating through space
Since it is monochromatic, it will be a single colour, and $T=\frac{2\pi}{\omega}$ is its [[period|period]] in time which gives [[frequency|frequency]] $\nu = \frac{1}{T}$ ad the [[wavelength|wavelength]] is $\lambda=\frac{2\pi}{k}$ which we can think of as the period in space
We can also write 
$$
\underline{E}(x,t)=E_{0} e^{ i(kx-\omega(k)) } \underline{e}_{y}
$$
$$
\underline{B}(x,t)=\frac{E_{0}}{c}e^{ i(kx-\omega(k)) }\underline{e}_{z}
$$
With $E_{0}$ complex with the understanding that the real and imaginary parts are solutions to Maxwell's equations separately

For a monochromatic plane wave propakating in some random direction $\underline{\hat{k}}$, we can write:
$$
\underline{E}(t,\underline{x})=\underline{E}_{0}e^{ i(\underline{k}\cdot \underline{x}-\omega t) }
$$
$$
 \underline{B}(t,\underline{x})=\underline{B}_{0}e^{ i(\underline{k}\cdot \underline{x}-\omega t) }
$$
Where $\left| \underline{k} \right|$ is the analogue to the $k$ above, and $\underline{k}=\left| \underline{k} \right| \underline{\hat{k}}$. $\underline{k}$ is called the wave vector and $\left| \underline{k} \right|$ is called the wavenumber
$\underline{E}_{0}$ and $\underline{B}_{0}$ are constant complex vectors, and
$$
\underline{\nabla} \cdot \underline{E} =i\underline{k}\cdot \underline{E}_{0}e^{ i(\underline{k}\cdot \underline{x}-\omega t) }
$$
$$
 \underline{\nabla} \cdot \underline{B} =i\underline{k}\cdot \underline{B}_{0}e^{ i(\underline{k}\cdot \underline{x}-\omega t) }
$$
$$
 \underline{\nabla} \times \underline{E} =i(\underline{k}\times \underline{E}_{0})e^{ i(\underline{k}\cdot \underline{x}-\omega t) }
$$
$$
 \underline{\nabla} \times \underline{B} =i(\underline{k}\times \underline{B}_{0})e^{ i(\underline{k}\cdot \underline{x}-\omega t) }
$$
We need these to satisfy Maxwell's equations:
$$
\underline{\nabla} \cdot \underline{E} =0,\underline{\nabla} \cdot \underline{B} =0
$$
$$
 \underline{\nabla} \times \underline{E} =-\frac{ \partial \underline{B} }{ \partial t},\underline{\nabla} \times \underline{B} =\varepsilon_{0}\mu_{0} \frac{ \partial \underline{E} }{ \partial t } 
$$
Thus
$$
i\underline{k}\cdot \underline{E}_{0}=0
$$
$$
 i\underline{k}\cdot \underline{B}_{0}=0
$$
$$
 i\underline{k}\times \underline{B}=-i\varepsilon_{0}\mu_{0}\omega \underline{E}_{0}
$$
$$
 i\underline{k}\times \underline{E}_{0}=i\omega \underline{B}_{0}
$$
Which tells us that both $\underline{E}_{0}$ and $\underline{B}_{0}$ will be orthogonal to the direction of motion $\underline{k}$
It also tells us that $\underline{E}_{0}$ and $\underline{B}_{0}$ are orthogonal
Conbining the last two euations:
$$
\frac{1}{\omega}\underline{k}\times(\underline{k}\times \underline{E}_{0})=-\varepsilon_{0}\mu_{0}\omega \underline{E}_{0}
$$
$$
\implies \underline{k}\times(\underline{k}\times \underline{E}_{0})=-\varepsilon_{0}\mu_{0}\omega^{2}\underline{E}_{0} 
$$
$$
\implies \cancelto{ 0 }{ (\underline{k}\cdot \underline{E}_{0}) }\underline{k}-(\underline{k}\cdot \underline{k})\underline{E}_{0}=-\varepsilon_{0}\mu_{0}\omega^{2}\underline{E}_{0 } 
$$
$$
\implies \left| \underline{k} \right| ^{2}\underline{E}_{0}=\varepsilon_{0}\mu_{0}\omega^{2}\underline{E}_{0}
$$
Since we want $\underline{E}_{0}$ to be nontrivial, we need
$$
\omega^{2}=c^{2}\left| \underline{k} \right| ^{2}
$$
Which then gives
$$
c^{2}=\frac{1}{\varepsilon_{0}\mu_{0}}
$$
:)
The bottom line is that $\underline{k}\cdot \underline{E}_{0}=0$, and $\underline{B}_{0}=\frac{1}{\omega}(\underline{x}\times \underline{E}_{0})$ and also $\omega^{2}=c^{2}\left| \underline{k} \right|^{2}$ then we have a solution
In general any combination of monochromatic waves will in fact solve this, soo
$$
\underline{E}(t,\underline{x})=\int _{\mathbb{R}^{3}} \underline{E}_{0}(\underline{k})e^{ i(\underline{k}\cdot \underline{x}-\omega(k)t) } \, d^{3}\underline{x} 
$$
Where we make sure $\underline{k}\cdot \underline{E}_{0}(\underline{k})=0$ which is the most general solution for $\underline{E}(t,\underline{x})$
By writing the electric field, we fix the magnetic field to be
$$
    \underline{B}(t,\underline{x})=\int _{\mathbb{R}^{3}} \underline{B}_{0}(\underline{k})e^{ i(\underline{k}\cdot \underline{x}-\omega(\underline{k})t) } \, d^{3}\underline{x}
$$
So
$$
\underline{B}_{0}(\underline{k})= \frac{\underline{k}\times \underline{E}_{0}}{\omega(\underline{k})}
$$
## Transport of Energy
For the electromagnetic field we concluded that the energy in a region $V$ is given by
$$
        U_{V}=\int _{V} \frac{\varepsilon_{0}}{/2}\left| \underline{E}(t,\underline{x}) \right| ^{2}+\frac{1}{2\mu_{0}} \left| \underline{B}(t,\underline{x}) \right| ^{2} \, d^{3}\underline{x} 
$$

We can think of 
$$
\mathcal{E}(t,\underline{x})=\frac{\varepsilon_{0}}{2}\underline{E}^{2}(t,\underline{x})+\frac{1}{2\mu_{0}}\underline{B}^{2}(t,\underline{x})
$$
As the energy density
How does this change in time? We take derivatives:
$$
\frac{ \partial \mathcal{E} }{ \partial t }=\varepsilon_{0}\underline{E}\cdot \frac{ \partial \underline{E} }{ \partial t } +\frac{1}{\mu_{0}} \underline{B}\cdot \frac{ \partial \underline{B} }{ \partial t }  
$$
We have time derivatives, so we want to consider equations of motion, returning to Maxwell's, we know
$$
\underline{\nabla} \times \underline{B} =\mu_{0}\varepsilon_{0} \frac{ \partial \underline{E} }{ \partial t } +\mu_{0}\underline{J}
$$
$$
 \underline{\nabla} \times \underline{E} =-\frac{ \partial \underline{B} }{ \partial t } 
$$
So substituting these in:
$$
\frac{ \partial \mathcal{E} }{ \partial t } =\frac{1}{\mu_{0}} \underline{E}\cdot(\underline{\nabla} \times \underline{B} -\mu_{0}\underline{J})-\frac{1}{\mu_{0}}\underline{B}\cdot(\underline{\nabla} \times \underline{E} ) 
$$
$$
= -\underline{E}\cdot \underline{J}+\frac{1}{\mu_{0}}(\underline{E}\cdot(\underline{\nabla} \times \underline{B} )-\underline{B}\cdot(\underline{\nabla} \times \underline{E} )) 
$$
$$
= -\underline{E}\cdot \underline{J}-\frac{1}{\mu_{0}}\underline{\nabla} \cdot (\underline{E}\times \underline{B}) 
$$
We define the Poynting vector to be
$$
\mathcal{\underline{S}}=\frac{1}{\mu_{0}} \underline{E}\times \underline{B}
$$
So
$$
\frac{ \partial \mathcal{E} }{ \partial t }+\underline{\nabla} \cdot \underline{\mathcal{S}}  =-\underline{E}\cdot \underline{J}
$$
Which has the form of a continuity equation:
$$
\frac{ \partial \rho }{ \partial t } +\underline{\nabla} \cdot \underline{J} =0
$$
Where $\rho$ is the density of the conserved quantity and $\underline{J}$ is the current describing the flow of the conserved density
So the Poynting vector describes the flow of energy carried by the electromagnetic field, but we note that the RHS is not actually $\hspace{0pt}0$, it is $-\underline{E}\cdot \underline{J}$
This occurs becuase the electromagnetic field is not isolated, it exchanges energy with the charges
More precisely, this is the energy transferred to particles through the Lorentz force
The $-\underline{E}\cdot \underline{J}$ is the rate of energy lost from the electromagnetic field to move charged particles
Taking a volume of charge $\delta q=\rho\delta V$ which has fluid velocity $\underline{v}$. In time $\delta t$, the electromagnetic field does work 
$$
\delta W=\delta F_{L}\cdot\delta \underline{\ell}=\delta F_{L}\cdot \underline{v}\delta t
$$
Where $F_{L}$ is the [[Lorentz force|Lorentz force]] on $\delta q$
We know
$$
\delta F_{L}=f_{L}\delta V=(\rho \underline{E}+\underline{J}\times \underline{B})\delta V
$$
So
$$
\delta W=\rho(\underline{E}+\cancelto{ 0 }{ \underline{v}\times \underline{B} })\cdot \underline{v}\delta t\delta V 
$$
$$
= \rho \underline{E}\cdot \underline{v}\delta t\delta V
$$
$$
=\underline{J}\cdot \underline{E}\delta t\delta V
$$
Which tells us that the electromagnetic field loses energy $\underline{J}\cdot \underline{E}$ per unit time and unit volume which is exactly what our conservation law above was trying to tell us