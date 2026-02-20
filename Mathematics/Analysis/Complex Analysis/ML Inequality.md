## Theorem
Let [[Complex Functions|$f:U\to \mathbb{C}$]] be [[Continuity|continuous]] on an [[open sets|open set]] $U$ and let $\gamma:[a,b]\to U$ be a [[Contour Integration|contour]]. Then
$$
\left| \int _{\gamma}f(z) \, dz  \right| \leq ML=M(\gamma,f)L(\gamma)
$$
Where
$$
L(\gamma)=\int _{\gamma} \, d\left| z \right| =\int ^{b}_{a} \left| \gamma'(t) \right|  \, dt  
$$
Is the length of the contour and 
$$
M=\sup_{z\in  \gamma}\left| f(z) \right| 
$$
Where we are using the notation $z\in \gamma$ to mean $z\in\left\{ \gamma(t):\middle|: t\in[a,b] \right\}$
### Proof
$$
\left| f(z) \right| \leq\sup_{z\in \gamma}\left| f(z) \right| 
$$
So by the [[Estimate Lemma|Estimate Lemma]],
$$
\left| \int _{\gamma}f(z) \, dz  \right| \leq \int _{\gamma}\left| f(z) \right|  \, d\left| z \right| \leq M\int _{\gamma} \, d\left| z \right| =ML  
$$
## Example
Let $\gamma:\left[ 0,\frac{\pi}{2} \right]\to \mathbb{C}$ be $\gamma(\theta)=2e^{ i\theta }$, then
$$
L(\gamma)=\int_{0}^{\frac{\pi}{2}} \left| \gamma'(\theta) \right|  \, d\theta = \int_{0}^{\frac{\pi}{2}} \left| 2e^{ i\theta } \right|  \, d\theta=\pi  
$$
So
$$
\left| \int _{\gamma} \frac{z+4}{z^{3}-1} \, dz  \right| \leq \pi \sup_{z\in \gamma}\left|  \frac{z+4}{z^{3}-1} \right| \leq \frac{6\pi}{7}
$$
