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
= \frac{1}{\left| \underline{x} \right| }+ \frac{\underline{x}\cdot xun}{}
$$