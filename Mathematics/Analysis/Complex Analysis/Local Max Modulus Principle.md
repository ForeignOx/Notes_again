## Theorem
Let [[Complex Functions|$f$]] be [[Holomorphicity|holomorphic]] on some ball $B_{r}(a)$. If $\left| f(a) \right|\geq \left| f(z) \right|$ $\forall z\in B_{r}(a)$, then $f$ is constant
### Proof
We start by showing the modulus $\left| f \right|$ is constant.
We do this by showing $\left| f(w) \right|=\left| f(a) \right|$ $\forall w\in B_{r}(a)$
Picking $w\in B_{r}(a)$ and letting $\rho=\left| w-a \right|$, so $\gamma(t)=a+\rho e^{ 2\pi it }$ for $t\in[0,1]$, then by [[Cauchy's Integral Formula|Cauchy's Integral Formula]], 
$$
\left| f(a) \right| =\frac{1}{2\pi}\left| \oint _{\gamma} \frac{f(z)}{z-a} \, dz  \right| 
$$
Then we use the [[estimate lemma|estimate lemma]],
$$
\leq \frac{1}{2\pi}\int_{0}^{1} \left| \frac{f(\gamma(t))}{\gamma(t)-a} \right| \left| \gamma'(t) \right|  \, dt = \frac{1}{2\pi} \int_{0}^{1}  \frac{\left| f(\gamma(t)) \right| }{\rho} 2\pi \rho \, dt  
$$