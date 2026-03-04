# Time Independent Form
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
## Long Distance Behaviour
In this section we consider scalar potential and electric field far from their sources, we assume that a charge density $\rho(\underline{x})$ is localised inside a bounded region $V\subset \mathbb{R}^{3}$, so $\rho(\underline{x})=0$ outside $V$
![[Pasted image 20260223141933.png]]
In the integral expression of Gauss' law, the integration variable $\underline{x}'$ only ranges over $V$. We are interested in the behaviour of the potential at observation points satisfying $\left| \underline{x} \right|\gg \left| \underline{x}' \right|$ for all $\underline{x}'\in V$
The key ingredient is the asymtotic expansion of the Green's function kernel,
$$
\frac{1}{\left| \underline{x}-\underline{x}' \right| }=\frac{1}{\left| \underline{x} \right| }-\underline{x}'\cdot \underline{\nabla } \frac{1}{\left| \underline{x} \right| }+\frac{1}{2}(\underline{x}'\cdot \nabla^{2}) \frac{1}{\left| \underline{x} \right| }+\dots 
$$
$$
= \frac{1}{\left| \underline{x} \right| }+ \frac{\underline{x}\cdot \underline{x}'}{\left| \underline{x} \right| ^{3}}+\dots
$$
Which is simply the [[Taylor Series|Taylor expansion]] in $\underline{x}'$ with derivatives acting on $\underline{x}$
Keeping only the first few terms and substituting into the general solution gives
$$
\varphi(\underline{x})=\frac{1}{4\pi\varepsilon_{0}} \frac{1}{\left| \underline{x} \right| }\int _{V}\rho(\underline{x}') \, d^{3}\underline{x}' +\frac{1}{4\pi\varepsilon_{0}\left| \underline{x} \right| ^{3}}\underline{x} \cdot \int _{V}\rho(\underline{x}')\underline{x}' \, d^{3}\underline{x}'+\dots 
$$
$$
= \frac{1}{4\pi\varepsilon_{0}} \frac{Q}{\left| \underline{x} \right| }+\frac{1}{4\pi\varepsilon_{0}} \frac{\underline{x}\cdot \underline{p}}{\left| \underline{x} \right| ^{3}} 
$$
Where we define 
$$
Q=\int _{V}\rho(\underline{x}') \, d^{3}\underline{x}' 
$$
$$
 \underline{p}=\int _{V}\rho(\underline{x}')\underline{x}' \, d^{3}\underline{x}'  
$$
As the total charge or monopole moment and the dipole moment of the charge distribution
Keeping higher order terms would similarly define higher multipole moments
The general patterns is that higher moments contribute terms that fall off more rapidly far from the sources. The monopole potential scales as $\frac{1}{\left| \underline{x} \right|}$, while the dipole correction scales as $\frac{1}{\left| \underline{x} \right|^{2}}$
### Remark
The dipole moment is the first shape-sensitive moment of the distribution
For discrete particles, $\rho(\underline{x}')=\sum_{i}q_{i}\delta(\underline{x}-\underline{x}_{i})$ gives
$$
\underline{p}=\int \underline{x}'\rho(\underline{x}') \, d^{3}\underline{x}'\to \sum_{i}q_{i}\underline{x}_{i}
$$
Which are points from negative to positive charges
They are a measure of how polarised the distribution is
For spherically symmetric particles,
$$
\rho(\underline{r})=\rho(\left| \underline{r} \right| )\implies \underline{p}=0
$$
Shifting the origin by $\underline{a}$ give
$$
\underline{p}'=\int (\underline{r}+\underline{a})\rho(\underline{r}) \, d^{3}\underline{r}=\underline{a}\int \rho(\underline{r}) \, d^{3}\underline{r}+\int \underline{r}\rho(\underline{r}) \, d^{3}\underline{r}=\underline{a}\cdot Q+\underline{p}   
$$
So $\underline{p}$ is origin independent when $Q=0$, but dependent in general
This means we get the following field lines 
![[Pasted image 20260223143423.png]]
For different cases, soo
$$
\varphi(\underline{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{Q}{\left| \underline{r} \right| }+0+\dots
$$
For the left and
$$
\varphi(\underline{r})=0+\frac{1}{4\pi\varepsilon_{0}} \frac{\underline{p}\cdot \underline{r}}{\left| \underline{r} \right| ^{3}}+\dots
$$
For the right.
### Example
Two point particles of charges $q_{i}$ located at $\underline{r}_{i}$ for $i\in\left\{ 1,2 \right\}$
The charge density for the system is 
$$
\rho(\underline{r})=q_{1}\delta(\underline{r}-\underline{r}_{1})+q_{2}\delta(\underline{r}-\underline{r}_{2})
$$
Soo
$$
Q=\int _{\mathbb{R}^{3}} \rho(\underline{r}) \, d^{3}\underline{r}=q_{1}\int _{\mathbb{R}^{3}} \delta(\underline{r}-\underline{r}_{1}) \, d^{3}\underline{r}+q_{2}\int _{\mathbb{R}^{3}} \delta(\underline{r}-\underline{r}_{2}) \, d^{3}\underline{r} =q_{1}+q_{2}  
$$
And
$$
\underline{p}=\int _{\mathbb{R}^{3}}\underline{r}\rho(\underline{r}) \, d^{3}\underline{r} =q_{1}\int \underline{r}\delta(\underline{r}-\underline{r}_{1}) \, d^{3}\underline{r}+q_{2}\int \underline{r}\delta(\underline{r}-\underline{r}_{2}) \, d^{3}\underline{r}=q_{1}\underline{r}_{1}+q_{2}\underline{r}_{2} 
$$
Shifting both: $\underline{r}_{i}\to \underline{r}_{i}+\underline{a}$, then
$$
\underline{p}'=(q_{1}+q_{2})\cdot \underline{a}+q_{1}\underline{r}_{1}+q_{2}\underline{r}_{2}=Q\underline{a}+\underline{p}
$$
If $q_{1}=-q_{2}=q$so that $Q=0$,
$$
\underline{p}=q(\underline{r}_{1}-\underline{r}_{2})=q\underline{d}
$$
With $\underline{d}$ being the distance between the two charges
# Time Dependent
Here we have the full Maxwell equations:
$$
\underline{\nabla} \cdot \underline{E} =\frac{\rho}{\varepsilon_{0}}
$$
$$
 \underline{\nabla} \times \underline{E} =-\frac{ \partial \underline{B} }{ \partial t } 
$$




















#Physics #Fields #Equation #Definition