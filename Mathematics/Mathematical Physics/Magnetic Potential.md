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

