Electrostatics are determined by setting 
$$
\frac{ \partial \underline{E} }{ \partial t }=\frac{ \partial \underline{B} }{ \partial t }=0
$$
Which, when plugged into Maxwell's Equations, gives
$$
\underline{\nabla} \cdot \underline{E} =\frac{\rho}{\varepsilon_{0}}
$$
$$
 \underline{\nabla} \times \underline{E} =0
$$
These two equations fully determine the field of electrostatics.
Since we have time independence, [[Electric Fields|$\underline{E}$]] and [[Magnetic Fields|$\underline{B}$]] are actualy independent entities
Both of the systems of electrostatics and magnetostatics are of the form
$$
\underline{\nabla} \cdot \underline{F} =D
$$
$$
 \underline{\nabla} \times \underline{F} =\underline{C}
$$
If we take the second and take the divergence of both sides
$$
0=\underline{\nabla} \cdot (\underline{\nabla} \times \underline{F} )=\underline{\nabla} \cdot \underline{ C}  
$$
By definitions of [[Divergence and Curl|divergence and curl]], this is trivial for $\underline{E}$
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
\underline{p}'=\int (\underline{r}+\underline{a})\rho(\underline{r}) \, d^{3}\underline{r}=\underline{a}\int \rho(\underline{r}) \, d^{3}\underline{r}+\int \underline{r}\rho(\underline{r}) \, d^{3}\underline{r}=\underline{a}\cdot 0+\underline{p}   
$$
