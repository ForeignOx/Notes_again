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