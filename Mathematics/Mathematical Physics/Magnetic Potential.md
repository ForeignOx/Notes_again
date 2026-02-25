## Build Up
For a [[Magnetostatics|static]] [[Magnetic Fields|magnetic field]] we are solving the modified Maxwell's equations:
$$
\underline{\nabla} \times \underline{B} =\mu_{0} \underline{J}
$$
$$
 \underline{\nabla} \cdot \underline{B} =0
$$
From the second, we know that the [[Magnetic Flux|magnetic flux]] satisfies
$$
\Phi_{S}=\int _{S}\underline{B}\cdot \, d\underline{S}=\Phi_{\partial S} 
$$
Which only depends on the boundary $\partial S$, not $S$
We also know that $\underline{B}=\underline{\nabla} \times \underline{A}$ automatically solves the second equation. We call $\underline{A}$ the vector potential. In $\mathbb{R}^{3}$ you can always write this equation given $\underline{\nabla} \cdot \underline{B}=0$
Substituting this into the curl equation:
$$
\underline{\nabla} \times (\underline{\nabla} \times \underline{A} )=\mu_{0} \underline{J} 
$$
We know from facts from [[Divergence and Curl|vector calculus]]:
$$
-\nabla^{2} \underline{A}+\underline{\nabla } (\underline{\nabla} \cdot \underline{A} )=\mu_{0} \underline{J}
$$
## Gauge Transformations
Attempting to solve this leads us to the pretty non-trivial problem that $\underline{A}$ is not unique, so we need to consider Gauge transformations
We see this since we can always make the transformation on $\underline{A}$:
$$
\underline{A}'=\underline{A}+\underline{\nabla } \chi
$$
Where $\chi$ is a scalar function, soo
$$
\underline{B}=\underline{\nabla} \times \underline{A}  
$$
$$
\implies \underline{B}'=\underline{\nabla} \times \underline{A} '=\underline{\nabla} \times (\underline{A}+\underline{\nabla } \chi)=\underline{\nabla} \times \underline{A} +\cancelto{ 0 }{ \underline{\nabla} \times \underline{\nabla } \chi  } =\underline{B}
$$
So the vector potential actually defines an [[Equivalence Relation|equivalence class]] $\underline{A}'\sim \underline{A}+\underline{\nabla }\chi$
So we need to impose additional Gauge fixing condition:
$$
G(\underline{A})=0
$$
To uniquely fix $\underline{A}$ in addition to solving our equation
### Coulomb Gauge
We can always choose $\underline{A}$ so that it satisfies the Coulomb gauge condition:
$$
G_{c}(\underline{A})=\underline{\nabla} \cdot \underline{A} =0
$$
Which we can impose
#### Proof
Fill this in later
## Biot-Suvart Law
In Coulomb's Gauge, the equation becomes:
$$
\nabla^{2} \underline{A}=-\mu_{0} \underline{J}
$$
The vector version of the [[electrical potential|electrostatic potential]]
This equation takes simple form in Cartesian coordinates:
$$
\nabla^{2} A_{i}(\underline{x})=-\mu_{0} J_{i}(\underline{x})
$$
One general solution is:
$$
A_{i}(\underline{x})=\frac{\mu_{0}}{4\pi} \int_{\mathbb{R}^{3}}  \frac{J_{i}(\underline{x}_{0})}{\left| \underline{x}-\underline{x}_{0} \right| } \, d^{3} \underline{x}_{0}
$$
Where $A_{i}\leftrightarrow \phi$, $\mu_{0}\leftrightarrow \frac{1}{\varepsilon_{0}}$ and $J_{i}\leftrightarrow \rho$ are our equivalents of the electrostatic potential
We can check that $\underline{\nabla} \cdot \underline{ A}(\underline{x})$ is satisfied
For the magnetic field we can write:
$$
\underline{B}(\underline{x})=\underline{\nabla} \times \underline{A} (\underline{x})= \frac{\mu_{0}}{4\pi} \int _{\mathbb{R^{3}}} \underline{\nabla} \times \left(  \frac{\underline{J}(\underline{x}_{0})}{\left| \underline{x}-\underline{x}_{0} \right| } \right)  \, d^{3} \underline{x}_{0}
$$
$$
=\frac{\mu_{0}}{4\pi}\int _{\mathbb{R}^{3}}\underline{\nabla } \left( \frac{1}{\left| \underline{x}-\underline{x}_{0} \right| } \right)\times \underline{J}(\underline{x})+\frac{1}{\left| \underline{x}-\underline{x}_{0} \right| }\cancelto{ 0 }{ \underline{\nabla} \times \underline{J} (\underline{x}_{0}) } \, d^{3}\underline{x}_{0} 
$$
Where we have used $\underline{\nabla} \times (f \underline{A})=\underline{\nabla }f\times \underline{A}+f \underline{\nabla} \times \underline{A}$
$$
=-\frac{\mu_{0}}{4\pi}\int _{\mathbb{R}^{3}} \frac{\underline{x}-\underline{x}_{0}}{\left| \underline{x}-\underline{x}_{0} \right| }\times \underline{J}(\underline{x}_{0}) \, d^{3}\underline{x}_{0} 
$$
$$
\implies \underline{B}(\underline{x})=\frac{\mu_{0}}{4\pi} \int _{\mathbb{R}^{3}} \frac{\underline{J}(\underline{x}_{0}) \times (\underline{x}-\underline{x}_{0}) }{\left| \underline{x}-\underline{x}_{0} \right| ^{3}} \, d^{3}\underline{x}_{0}
$$
Which is the Biot-Savart law!
Which is true for a three dimensional current density
We can also introduce surface and linear currents:
For a wire $C$ with constant current $I$, the Biot Savart law becomes:
$$
\underline{B}(\underline{x})=-\frac{\mu_{0}I}{4\pi}\int _{C} \frac{1}{\left| \underline{x}-\underline{y}(s) \right| ^{3}} (\underline{x}-\underline{y}(s))\times \, d\underline{y}(s)
$$
$$
 =-\frac{\mu_{0}I}{4\pi} \int _{C}\frac{1}{\left| \underline{x}-\underline{y}(s) \right| ^{3}} ((\underline{x}-\underline{y}(s))\times \underline{\dot{y}}(s))\cdot \, ds

$$
Which our lecturer writes in cursed notation
$$
\underline{B}(\underline{x})=\frac{\mu_{0}I}{4\pi}\int _{C} \frac{d\underline{y}(s)\times (\underline{x}-\underline{y}(s))}{\left| \underline{x}-\underline{y}(s) \right| ^{3}}  
$$
### Example
For the infinitely long straight wire, we use cylindrical coordinates. The parametrisation of $C$ is
$$
\underline{y}(z)=z\cdot \underline{e}_{z}\implies d\underline{y}(z)=\underline{e}_{z} dz 
$$
$$
 \underline{x}=r\cdot \underline{e}_{r}
$$
Now computing the cross product,
$$
d\underline{y} \times(\underline{x}-\underline{y})=(\underline{e}_{z} dz)\times(r\underline{e}_{r}-z\underline{e}_{z}) 
$$
$$
= (\underline{e}_{z}\times (r \underline{e}_{r}-z\underline{e}_{z}))dz 
$$
$$
= r(\underline{e}_{z}\times \underline{e}_{r})dz=r\underline{e}_{\phi}dz
$$
Next,
$$
\left| x-\underline{y}(z) \right| =(r^{2}+z^{2})^{\frac{1}{2}}
$$
Sooo
$$
    \underline{B}(\underline{x})=\frac{\mu_{0}I}{4\pi} \int_{-\infty}^{\infty} \frac{\underline{e}_{\phi}r}{(r^{2}+z^{2})^{\frac{3}{2}}} \, dz
$$
Since $\underline{e}_{\phi}$ stays constant as we move along the $z$-axis, we can take it out of the integral:
$$
=\frac{\mu_{0}Ir}{4\pi}\underline{e}_{\phi}\int_{-\infty}^{\infty} \frac{1}{(r^{2}+z^{2})^{\frac{3}{2}}} \, dz 
$$
We now make the substitution $z=\tan\theta r$
$$
=\frac{\mu_{0}I}{4\pi r}\underline{e}_{\phi}\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} \cos\theta \, d\theta 
$$
$$
= \frac{\mu_{0}I}{2\pi r}\underline{e}_{\phi}
$$
# Long Distance Behaviour
Imagine a localised current density $\underline{J}(\underline{x})$, in Coulomb gauge
$$
A_{i}(\underline{x})=\frac{\mu_{0}}{4\pi}\int _{\mathbb{R}^{3}} \frac{J_{i}(\underline{y})}{\left| \underline{x}-\underline{y} \right| } \, d^{3}\underline{y} 
$$
At long distances, $\left| \underline{x} \right|\gg \left| \underline{y} \right|$ we can expand
$$
\frac{1}{\left| \underline{x}-\underline{y} \right| }=\frac{1}{\left| \underline{x} \right| }+ \frac{\underline{x}\cdot \underline{y}}{\left| \underline{x} \right| ^{3}}+\dots
$$
(as physicists we don't case about higher order terms) plugging this in,
$$
A_{i}(\underline{x})=\frac{\mu_{0}}{4\pi} \left( \frac{1 }{\left| \underline{x} \right| }\int J_{i}(\underline{y}) \, d^{3}\underline{y}+\frac{1}{\left| \underline{x} \right|^{3} }\int J_{i}(\underline{y})\underbrace{ x_{j}y_{j}  }_{ \underline{x}\cdot \underline{y} }\, d^{3}\underline{y}+\dots\right)
$$
The first integral is the total current, so we would imagine that as we are going over loops, that it will be zero, indeed
$$
\frac{ \partial (J_{j}(\underline{y})y_{i}) }{ \partial y_{j} } =y_{i}\frac{ \partial J_{j} }{ \partial y_{j} } +J_{j}\frac{ \partial y_{i} }{ \partial y_{j} } 
$$
Since $\frac{ \partial J_{j} }{ \partial y_{j} }=\underline{\nabla} \cdot \underline{J}=0$,
$$
=J_{i}(\underline{y})\delta_{ii}=I_{i}(\underline{y})
$$
Thus
$$
\int J_{i}(\underline{y}) \, d^{3}\underline{y}=\int_{\mathbb{R}^{3}}  \frac{ \partial (J_{j}(\underline{y})\underline{y}_{i}) }{ \partial y_{j} }  \, d^{3}\underline{y} = 0
$$
As by the [[Divergence Theorem|divergence theorem]], this evaluates to the current on the surface, which is the current at infinity which we define to be 0
This is different to the electrostatic case
The second term iss
$$
x_{j}\int_{\mathbb{R}^{3}} J_{i}(\underline{y})y_{j} \, d^{3}\underline{y}=(\underline{m}\times \underline{x})_{i} 
$$
Where
$$
\underline{m}=\frac{1}{2}\int _{\mathbb{R}^{3}} \underline{y}\times \underline{J}(\underline{y}) \, d^{3}\underline{y} 
$$
Which is defined to be the magnetic dipole moment $\underline{m}$
Thus,
$$
\underline{A}(\underline{x})=\frac{\mu_{0}}{4\pi} \frac{\underline{m}\times \underline{x}}{\left| \underline{x} \right| ^{3}}+\dots
$$
We use the identity,
$$
\underline{\nabla} \times (\underline{A}\times \underline{B})=\underline{A}\cdot (\underline{\nabla } \cdot\underline{B}) -(\underline{A}\cdot \underline{\nabla } )\underline{B}-\underline{B}(\underline{\nabla} \cdot \underline{A} )+(\underline{B}\cdot \underline{\nabla } )\underline{A}
$$

The absence of magnetic monopoles make the dipole contribution to be leading
In nature, elementary point particles come with intrinsic spin which gives rise to magnetic dipole moment
## Example
Dipole moment of planar loop with constant current $I$
For a 3D current density, we know
$$
\underline{m}-\frac{1}{2}\int _{\mathbb{R}} \underline{y}\times \underline{J}(\underline{y}) \, d^{3}\underline{y} 
$$
We can parametrise a loop by $\underline{x}(s)$