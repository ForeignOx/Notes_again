An approxiamtion we can make for a large class of fluids is that the density of the fluid element doesn't change as it moves; the flow is incompressible, do $\frac{D\rho}{Dt}=0$
Using this and the [[Mass Conservation|continuity equation]], means
$$
\underline{\nabla} \cdot \underline{u} =0
$$
Or in other words the velocity is divergence free
Note that saying $\frac{D\rho}{Dt}$ doesn't mean $\rho(\underline{x},t)$ is constant in space or time, though the inverse is true. It is possible to have a fluid which has different densities at different points, but as long as they don't change their density as they move, then we are good
___
Returning to the funnel, 
$$
\underline{\nabla} \cdot \underline{u} =0
$$
$$
\implies \int _{V}\underline{\nabla} \cdot \underline{u}  \, dV =0 
$$
$$
\implies \int _{S}\underline{u}\cdot \hat{\underline{n}} \, dS=0 
$$
$$
\implies \sum_{i \in \text{inlet}} u_{i}S_{i}= \sum_{i\in \text{outlet}}u_{i} S_{i}
$$
