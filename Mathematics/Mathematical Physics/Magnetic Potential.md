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
Attempting to solve this leads us to the pretty non-trivial problem that $\underline{A}$ is not unique, so we need to consider Gauge transformations
We see this since we can always make the transformation on $\underline{A}$:
$$
\underline{A}'=\underline{A}
$$