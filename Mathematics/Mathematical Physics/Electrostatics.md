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
## Energy Stored in Electrostatic Field
How much [[energy|energy]] do we invest to create the electric field $\underline{E}(\underline{x})$?
The same amount of energy it took to assemble the distribution $\rho(\underline{x})$ that creates it
A more elementary question to ask is how much [[work|work]] $U$ do we have to do in order to bring a particle of charge $q$ to the point $\underline{r}$ inside the electric field $\underline{E}(\underline{r})$
$$
U(\underline{r})=-\int _{-\infty}^{\underline{r}}\underline{f}(\underline{r}')\cdot  \, d\underline{r}'=-q\int _{-\infty}^{\underline{r}} \underline{E}(\underline{r}')\cdot \, d\underline{r}' 
$$
$$
= q\int_{-\infty}^{\underline{r}} \underline{\nabla } \varphi(\underline{r}')\cdot \, d\underline{r}'=q(\varphi(\underline{r})-\varphi(\infty))=q\varphi(\underline{r})
$$
### System of $N$-particles
Consider bringing $N$ particles of charges $q_{i}$ with $i \in\overline{N}$ at positions $\underline{x}_{i}$ in empty space
We define
$$
\varphi_{j}(\underline{x}_{i})=\frac{1}{4\pi\varepsilon_{0}} \frac{q_{j}}{\left| \underline{x}_{i}-\underline{x}_{j} \right| }
$$
Which is simply the potential at $\underline{x}_{i}$ due to the particle at $\underline{x}_{j}$
We also define
$$
U_{i,j}=q_{i}\varphi_{j}(\underline{x}_{i})=\frac{1}{4\pi\varepsilon_{0}} \frac{q_{i}q_{j}}{\left| \underline{x}_{j}-\underline{x}_{i} \right| }=q_{j}\varphi_{i}(\underline{x}_{j})=U_{j,i}
$$
Which is the the energy of particle $i$ due to the potential of the $j$th particle, we will take advantage of its symmetry >:)
We warm up with simply considering two particles $U=U_{2,1}$ rather than $U_{1,2}+U_{2,1}$, for three particle, $U=U_{2,1}+U_{3,1}+U_{3,2}$ we don't add all the other nonsense as then we would be double counting, sooo for $N$ particles
$$
U=\sum_{i=1}^{N}\sum_{j>i}U_{i,j}
$$
We take advantage of this, sooo
$$
U=\frac{1}{2}\sum_{i=1}^{N}\sum_{j\neq i}U_{i,j}=\frac{1}{2}\sum_{i=1}^{N}\sum_{j\neq i}q_{i}\varphi_{j}(\underline{x}_{i})=\frac{1}{2}\sum_{i=1}^{N}q_{i}\left( \sum_{j\neq i}\varphi_{j}(\underline{x}_{i}) \right)
$$
$$
= \frac{1}{2}\sum_{i=1}^{N}q_{i}\Phi_{i}(\underline{x}_{i})
$$
Where $\Phi_{j}(\underline{x}_{i})=\sum_{j=i}^{N}\varphi_{j}(\underline{x}_{i})$ is the potential created by all the particles at $\underline{x}_{i}$ except for the $i$th particle
For a smooth distribution,
$$
    U=\frac{1}{2}\int _{\mathbb{R}^{3}}\rho(\underline{r})\varphi(\underline{r}) \, d^{3}\underline{r} = -\frac{\varepsilon_{0}}{2}\int _{\mathbb{R}^{3}} \nabla^{2}\varphi(\underline{r})\cdot \varphi(\underline{r}) \, d^{3}\underline{r}
$$
$$
= \frac{\varepsilon_{0}}{2}\int _{\mathbb{R}^{3}}\underline{\nabla } \varphi(\underline{r})\cdot \underline{\nabla} \varphi(\underline{r}) \, d^{3}\underline{r}   
$$
$$
=\frac{\varepsilon_{0}}{2}\int _{\mathbb{R}^{3}}\left| \underline{E}(\underline{r}) \right| ^{2} \, d^{3}\underline{r}  
$$
$$
\implies U=\frac{\varepsilon}{2}\int _{\mathbb{R}^{3}}\left| \underline{E}(\underline{r}) \right| ^{2} \, d^{3}\underline{r}
$$

