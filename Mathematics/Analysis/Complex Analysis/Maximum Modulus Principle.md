## Theorem: Local Maximum Modulus Principle
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
$$
= \int_{0}^{1} \left| f(\gamma(t)) \right|  \, dt\leq \int_{0}^{1} \left| f(a) \right|  \, dt = \left| f(a) \right|     
$$
Thus all of these inequalities have to be equalities, in particular,
$$
\int_{0}^{1} \left| f(\gamma(t)) \right|  \, dt=\int_{0}^{1} \left| f(a) \right|  \, dt  
$$
This is only possible if $\left| f(\gamma(t)) \right|=\left| f(a) \right|$ for all $t$, in particular, $\left| f(w) \right|=\left| f(a) \right|$
For the second step, we want to show $f$ is constant on $B_{r}(a)$
We know $\left| f(z) \right|=c$ is constant, so
$$
c^{2}=\left| f(z) \right| ^{2}=f(z)\overline{f(z)}
$$
If $c=0$, then $\left| f(z) \right|=0$ for all $z$, so $f=0$
If $c\neq 0$ and $\left| f(z) \right|=c$, then $f(z)\neq 0$ on $B_{r}(a)$
So
$$
\overline{f(z)}=\frac{c^{2}}{f(z)}
$$
is holomorphic on $B_{r}(a)$
If $f,\overline{f}$ are both holomorphic and $f=u+iv$, then by [[Cauchy-Riemann equations|Cauchy-Riemann equations]], $u_{x}=$
## Theorem: Maximum Modulus Principle
Let $f:D\to \mathbb{C}$ be holomorphic on a domain. If therre exists $a\in D$ such that
$$
\left| f(a) \right| \geq \left| f(z) \right| ~\forall z\in  D
$$
Then $f$ is constant on $D$
### Proof
$D$ is a domain, so around $z=a$, pick a ball $B_{r}(a)\subset D$, then $\left| f(a) \right|\geq \left| f(z) \right|~\forall z\in B_{r}(a)$, so by the local maxumum modulus principle, $f$ is constant on $B_{r}(a)$
So by the principle of [[analytic continuation|analytic continuation]], $f$ is constant on $D$
## Corollary: Holomorphic Functions Attain Maxima on Boundaries
If $f: \overline{D}\to C$ is holomorphic on $D$ and [[Continuity|continuous]] on the [[Open Sets|closure]] $\overline{D}$, then in the case that $D$ is [[Boundedness|bounded]] (so $\overline{D}$ is compact), then $\left| f \right|$ attains its maximum on $\partial D$
## Example
Find the max of $\left| z^{2}+2z-3 \right|$ on $\overline{B_{1}(0)}$
By the corollary above, the maximum is attained on $\left| z \right|=1$
Then letting $z=e^{ i t}$ for some $t\in[0,2\pi]$, then
$$
\left| z^{2}+2z-3 \right| ^{2}=(z^{2}+2z-3)\overline{(z^{2}+2z-3)}
$$
$$
= (e^{ 2it }+2e^{ it }-3)(e^{ -2it } +2e^{ -it }-3)=\dots=14-3e^{ -2t }-3e^{ 2t }-4e^{ it }-4e^{ -it }
$$
$$
= 14-6\cos(2t)-8\cos t =-12\cos ^{2}t-8\cos t+20
$$
Which is maximised when $\cos t=-\frac{1}{3}$, so 
$$
\left| f \right| ^{2}=\frac{64}{3}\implies \max_{z\in  \overline{B_{1}(0)}}f=\frac{8}{\sqrt{ 3 }}
$$

