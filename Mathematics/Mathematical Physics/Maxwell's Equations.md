## Equation
In a 3D sense we have Maxwell's equations being (verified by extensive experiment):
$$
\underline{\nabla} \cdot \underline{E} =\frac{\rho}{\varepsilon_{0}}
$$
$$
 \underline{\nabla} \times \underline{B} =\mu_{0}\underline{J}+\mu_{0}\varepsilon_{0} \partial_{t}\underline{E}
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
So $W_{\kappa\lambda\mu}=0$ whenever any two indices coincide
Given that we have $\hspace{0pt}4$ choices for $\kappa,\lambda,\mu$, we have ${4 \choose 3 }=4$ independent equations
Now we want to do a detailed check that this gives us back what we want
For the first Maxwell equation, if $\nu=0$,
$$
\cancelto{ 0 }{ \partial_{0}F^{0 0} }+\partial_{i}F^{i0}=-\mu_{0}J^{0} 
$$
$$
\implies -\frac{1}{c}\partial_{i} E_{i}=-\mu_{0}c\rho 
$$
$$
\implies \underline{\nabla} \cdot \underline{ E} =\frac{\rho}{\varepsilon_{0}}
$$
Which gives us Gauss' law
If $\nu=i$,
$$
\partial_{0}F^{0i}+\partial_{j}F^{ji}=-\mu_{0} J^{i}
$$
Which if we do the faffing tells us that
$$
\underline{\nabla} \times \underline{ B} =\mu_{0}\underline{J}+\mu_{0}\varepsilon_{0}\partial_{t}\underline{E}
$$
Yay
Doing the same for Maxwell's second equation, if $\mu=0,\kappa=i,\lambda=j$, then the we get
$$
\partial_{0}F_{ij}+\partial_{i}F_{j{0}}+\partial_{j}F_{0i}=0 
$$
$$
\implies \epsilon_{ijk}\partial_{t}B_{k}+\partial_{i}E_{j}-\partial_{j}E_{i}=0 
$$
$$
\implies \epsilon_{lij}\epsilon_{ijk}\partial_{t}B_{k}+\epsilon_{ijk}(\partial_{i}E_{j}-\partial_{j}E_{i})=0 
$$
$$
\implies  \partial_{t}B_{l}+\epsilon_{lij}E_{j}=0 
$$
$$
\implies  \underline{\nabla} \times \underline{ E} =-\partial_{t}\underline{B}
$$
And if we let $\mu=i,\kappa=j,\lambda=k$, then
$$
\partial_{i}F_{jk}+\partial_{j}F_{ki}+\partial_{k}F_{ij}=0 
$$
$$
\implies \underline{\nabla} \cdot \underline{B} =0
$$
