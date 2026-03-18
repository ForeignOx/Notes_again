## Equation
In a 3D sense we have Maxwell's equations being (verified by extensive experiment):
$$
\underline{\nabla} \cdot \underline{E} =\frac{\rho}{\varepsilon_{0}}
$$
$$
 \underline{\nabla} \times \underline{B} =\mu_{0}\underline{J}+\mu_{0}\varepsilon_{0} \partial_{t}\underline{B}
$$
$$
 \underline{\nabla} \cdot \underline{B} =0
$$
$$
 \underline{\nabla} \times \underline{ E} =-\partial_{t}\underline{B}
$$
We want to attempt to rewrite these in a relativistic sense,
$$
\frac{1}{c}\underline{\nabla} \cdot \underline{E} =\mu_{0}c\rho 
$$
$$
 \underline{\nabla} \times \underline{B} -\frac{1}{c^{2}}\partial_{t}\underline{E}=\mu_{0}\underline{J} 
$$
$$
 \underline{\nabla} \cdot \underline{B} =0
$$
$$
 \underline{\nabla} \times \underline{E} +\partial_{t}\underline{B}=0
$$
The first two are a scalar and vector equation, and the second two are similarly
Note that for the first two, on the right hand side, we get the components of the space-time current, so we rewrite this:
$$
\partial_{\mu}F^{\mu \nu}=-\mu_{0} J^{\nu} 
$$
$$
 \partial_{\mu}F_{\kappa\lambda}+\partial_{\kappa}F_{\lambda \mu}+\partial_{\lambda}F_{\mu\kappa}=0
$$
Which is the covariant form of Maxwell's equations
As a sanity check, we can see that we have the same number of equations
We see that in the second Maxwell equation, we seem to have a ${0 \choose 3 }$ tensor:
$$
 W_{\mu\kappa\lambda}=\partial_{\mu}F_{\kappa\lambda}+\partial_{\kappa}F_{\lambda \mu}+\partial_{\lambda}F_{\mu\kappa}
$$
Is totally antissymmetric, so for any permutation $\sigma$ of three objects,

$$
W_{\sigma(\kappa)\sigma(\lambda)\sigma(\mu)}=\epsilon(\sigma)W_{\kappa\lambda\mu}
$$
Where
$$
\epsilon(\sigma)=\begin{cases}
1 & \text{for even permutations} \\
-1 & \text{for odd permutations}
\end{cases}
$$