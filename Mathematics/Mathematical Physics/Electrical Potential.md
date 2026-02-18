For a static electric field, by Maxwell's equations, we have
$$
\underline{\nabla} \cdot \underline{ E} =\frac{\rho}{\varepsilon_{0}}
$$
$$
 \underline{\nabla} \times \underline{E} =0
$$
And we consider travelling on a contour $C$ around a surface $S$, i.e. $C=\partial $
Consider the [[Line Integrals|contour integral]] of the [[electric fields|electric field]], so by [[Stokes' Theorem|stokes' theorem]]:
$$
\oint_{C}\underline{E}\cdot ~d \underline{\ell}=0 =\int _{S}\underline{\nabla} \times \underline{E}  \, d\underline{S}
$$
Since $\oint_{C}\underline{E}~d \underline{\ell}=0$, then
$$
\oint_{C}\underline{E}\cdot~d \underline{\ell}=\oint_{C_{1}}\underline{E}\cdot~d \underline{\ell}+\oint_{C_{2}}\underline{E}\cdot ~d \underline{\ell}
$$
$$
\implies \oint_{C_{1}}\underline{E}\cdot~d \underline{\ell}=- \oint_{C_{2}} \underline{E}\cdot~d \underline{\ell}
$$
Taking $C_{2}'$ to be the opposite direction to $C_{2}$, then
$$
\oint_{C_{1}}\underline{E}\cdot~d \underline{\ell}=\oint_{C_{2}} \underline{E}\cdot ~d \underline{\ell}
$$
So we get the following properties:
- $\oint_{C}\underline{E}\cdot d \underline{\ell}=0$ for any closed loop $C$
- $\int _{\underline{a}}^{\underline{b}}\underline{E}\cdot \, d \underline{\ell}$ is independent of path taken
- $\underline{E}=-\underline{\nabla }\phi$, the electric potential (also known as $V$), then the second Maxwell equation is trivially satisfied:
$$
\underline{\nabla} \times \underline{E} =-\underline{\nabla} \times \underline{\nabla }\phi=0  
$$
    Which is known a Hodge de Rham decomposition, or Helmoltz decomposition. Also [[Gauss' Law|Gauss' law]] becomes:
$$
\nabla^{2}\phi=-\frac{\rho}{\varepsilon_{0}}
$$
One physically relevant quantity is $\underline{E}$
$\phi(\underline{x})\to \phi(\underline{x})+C$ give the same $\underline{E}$, this is a baby example of gauge invariance. We can fix $C$ by demanding that $\phi(\underline{x})\to 0$ as $\left| \underline{x} \right|\to 0$
## For the Point Particle
For a point $\rho(\underline{r})=Q\delta(\underline{r}-\underline{r}_{0})$, with $\delta$ the [[Dirac Delta Function|Dirac-delta]], we need to solve
$$
\nabla^{2}\phi(\underline{r})=\frac{Q}{\varepsilon_{0}}\delta(\underline{r}-\underline{r}_{0})
$$
So for the point particle,
$$
\underline{E}(\underline{r})=\frac{Q}{4\pi\varepsilon_{0}} \frac{\underline{r}-\underline{r}_{0}}{\left| \underline{r}-\underline{r}_{0} \right| ^{3}}=-\underline{\nabla } \phi
$$
Sooo
$$
\phi(\underline{r})=\frac{Q}{4\pi\varepsilon_{0}} \frac{1}{\left| \underline{r}-\underline{r}_{0} \right| }+C
$$
Fixing $C=0$ so that $\phi(\left| \underline{r} \right|\to \infty)=0$, then
$$
\phi(\underline{r})= \frac{Q}{4\pi\varepsilon_{0}} \frac{1}{\left| \underline{r}-\underline{r}_{0} \right| }
$$



## Definition
The potential, $V$, at a point $P$ in an [[Electric Fields|electric field]] is the [[Work]] done by the field per unit [[Electric Charge|charge]] on a test charge as it goes from $P$ to infinity. The potential due to a point charge, $Q$ at distance $r$ from $Q$ is:
$$
V=\frac{Q}{4\pi\epsilon_{0}r}
$$
## Derivation
Recall that work is force multiplied by distance in direction of force. The force on $q$ is $qE$, radially outwards from $Q$. But $E$ decreases as we go from $P$ to infinity, this is because:
$$
E=\frac{Q}{4\pi \epsilon_{0}r^{2}}
$$
 We can therefore calculate the work done in small steps at a time, with distance $\delta r$, and we can see that that the work done on $q$ as $q$ moves a distance $\delta r$ from $Q$ is equal to:
 $$
W=\int_{r_{P}}^{\infty} qE \, dr =\frac{qQ}{4\pi\epsilon_{0}}\int _{r_{P}}^{\infty} \frac{1}{r^{2}} \, dr 
$$
$$
=\frac{qQ}{4\pi\epsilon_{0}}\left[ -\frac{1}{r} \right]_{r_{P}}^{\infty}=\frac{qQ}{4\pi\epsilon_{0}}\left( 0-\left( -\frac{1}{r_{P}} \right) \right)
$$
The limits in the above integration have been ignored
$$
=\frac{qQ}{4\pi\epsilon_{0}r_{P}}
$$
Which can be generalised to
$$
W=\frac{qQ}{4\pi\epsilon_{0}r}
$$
And since the potential is the work done per unit charge,
$$
V=\frac{Q}{4\pi\epsilon_{0}r}
$$
___
## More than one charge
In principle we can calculate the electric potential due to any spatial distribution of charges by viewing the charge distribution as a collection of point charges, calculating $V$ at $P$ due to each point charge and adding them as scalars

#Physics #Fields #Equation #Definition