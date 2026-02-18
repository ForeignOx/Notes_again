An electric field is a [[Vectors|vector]] $\underline{E}$ (in general a function of $x,y,z,t$, but we will take it as constant)
There is an electric field at any point, $P$, where a charged body (at rest) experiences a force proportional to its [[Electric Charge|charge]]
We shall call a charged body used to test for the presence of an electric field a test charge. Ideally it would have a tiny charge (so as to not displace the very charges that are giving rise to the field), and would occupy very little space, so as to respond to the field at a point
Not only do charges respond to electric fields, they also create electric fields around them
## General Solution
In general we have to solve
$$
\nabla^{2}\phi(\underline{r})=-\frac{1}{\varepsilon_{0}}\rho(\underline{r})
$$
We know that $\nabla^{2} G(\underline{r},\underline{r}_{0})=\delta(\underline{r}-\underline{r}_{0})$ for the Green's function
$$
G(\underline{r},\underline{r}_{0})=-\frac{1}{4\pi \left| \underline{r}-\underline{r}_{0} \right| }
$$
So one solution is thus
$$
\phi(\underline{r})=-\frac{1}{\varepsilon_{0}}\int _{\mathbb{R}^{3}}G(\underline{r},\underline{r}_{0})\rho(\underline{r}_{0}) \, d^{3} \underline{x}_{0} 
$$
$$
\implies \nabla^{2}\phi(\underline{r})=-\frac{1}{\varepsilon_{0}}\nabla^{2}\left( \int _{\mathbb{R}^{3}} G(\underline{r},\underline{r}_{0})\rho(\underline{r}_{0}) \, d^{3} \underline{x}_{0}  \right) 
$$
$$
=-\frac{1}{\varepsilon_{0}}\int _{\mathbb{R}^{3}}\nabla^{2}G(\underline{r},\underline{r}_{0})\rho(\underline{r}_{0}) \, d^{3}\underline{x}_{0}
$$
$$
= -\frac{1}{\varepsilon_{0}} \int _{\mathbb{R}^{3}} \delta(\underline{r}-\underline{r}_{0}) \rho(\underline{r}_{0}) \, d^{3}\underline{x}_{0}  
$$
$$
= -\frac{1}{\varepsilon_{0}} \rho(\underline{r})
$$
One general solution is then
$$
\phi(\underline{r})=\frac{1}{4\pi\varepsilon_{0}}\int _{\mathbb{R}^{3}} \frac{\rho(\underline{r}_{0})}{\left| \underline{r}-\underline{r}_{0} \right| } \, d^{3} \underline{r}_{0} 
$$
The electric field for the general solution is then
$$
\underline{E}=-\underline{\nabla } \phi=-\frac{1}{4\pi\varepsilon_{0}} \underline{\nabla } \int _{\mathbb{R}^{3}} \frac{\rho(\underline{r}_{0})}{\left| \underline{r}-\underline{r}_{0} \right| } \, d^{3} \underline{r}_{0} 
$$
$$
= -\frac{1}{4\pi\varepsilon_{0}}\int _{\mathbb{R}^{3}}\rho(\underline{r}_{0}) \underline{\nabla } \left( \frac{1}{\left| \underline{r}-\underline{r}_{0} \right| } \right) \, d^{3}\underline{r}_{0} 
$$
$$
= \frac{1}{4\pi\varepsilon_{0}}\int _{\mathbb{R}^{3}}\rho(\underline{r}_{0}) \frac{\underline{r}-\underline{r}_{0}}{\left| \underline{r}-\underline{r}_{0} \right|^{3} } \, d^{3}\underline{r}_{0}  
$$
Which is the general solution of the electric field!!
We note that this is in fact just Coulomb's Law but with an integral, which we can think of a summing many many point charges, since the law is linear
## Example
System of $N$ charged particles with charges $q_{i},i\in \overline{N}$ at locations $\underline{r}_{i}$,
$$
\rho(\underline{r}_{0})=\sum_{i=1}^{N}q_{i}\delta(\underline{r}-\underline{r}_{i})
$$
The scalar potential is
$$
\phi(\underline{r})=\frac{1}{4\pi\varepsilon_{0}}\int \frac{\rho(\underline{r})}{\left| \underline{r}-\underline{r}_{0} \right| } \, d^{3}\underline{r}_{0} 
$$
$$
= \frac{1}{4\pi\varepsilon_{0}} \int \frac{1}{\left| \underline{r}-\underline{r}_{0} \right| }\left( \sum_{i=1}^{N} q_{i}\delta(\underline{r}_{0}-\underline{r}_{{i}}) \right) \, d^{3} \underline{r}_{0} 
$$
$$
= \frac{1}{4\pi\varepsilon_{0}} \sum_{i=1}^{N}\int \frac{1}{\left| \underline{r}-\underline{r}_{0} \right| }q_{i}\delta(\underline{r}-\underline{r}_{i}) \, d^{3}\underline{r}_{0} 
$$
$$
= \frac{1}{4\pi\varepsilon_{0}} \sum_{i=1}^{N}q_{i}\int \frac{\delta(\underline{r}_{0}-\underline{r}_{i})}{\left| \underline{r}-\underline{r}_{0} \right| } \, d^{3} \underline{r}_{0}   
$$
$$
= \frac{1}{4\pi\varepsilon_{0}}\sum_{i=1}^{N} \frac{q_{i}}{\left| \underline{r}-\underline{r}_{i} \right| }
$$
Yayy
___
Surface charge densidy
C




#Mathematics #Dynamics #Physics #Fields #Definition