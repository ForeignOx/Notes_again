The gravitational force affects all matter and has infinite range. It is negligible for subatomic particles. It is the weakest force out of [[Strong Force|strong]], [[Electromagnetic Force|e-m]], [[Weak Force|weak]] and gravitational. It doesn't have a force carrier
___
## Gravitational Trajectory Example
Take the force of gravity to a be a [[Central Forces|central force]], $f(r)=-\frac{k}{r^{2}}$. Take $m=1$, $f(r)=-\frac{1}{r^{2}}$, start at $r=1$ with speed $v_{0}$, show that the particle is bounded if $v_{0}<\sqrt{ 2 }$, if $f_{0}<\sqrt{ 2 }$ and the initial velocity is perpendicular to $\underline{r}$, find $r_\text{min}$ and $r_\text{max}$
We do this by considering [[Energy|energy]]. The pootential energy is 
$$
V(r)=-\int f(r) \, dr =-\frac{1}{r}
$$
$$
\implies E=\frac{1}{2}v^{2}-\frac{1}{r}
$$
Which at $t=0$ is $\frac{1}{2}v_{0}^{2}-1$, so
$$
\frac{1}{2}v^{2}-\frac{1}{r}=\frac{1}{2}v_{0}^{2}-1
$$
$$
\implies v^{2}=v_{0}^{2}-2+\frac{2}{r}\geq 0
$$
Since $v^{2}\geq 0$
$$
\implies \frac{2}{r}\geq 2-v_{0}^{2}
$$
If $2-v_{0}^{2}>0$:
$$
\implies r \leq \frac{2}{2-v_{0}^{2}}
$$
So if $v_{0}<\sqrt{ 2 }$, then $r\leq \frac{2}{2-v_{0}^{2}}$
![[Gravitational Force 2025-02-24 14.20.29.excalidraw]]
From the initial conditions:
$$
\underline{r}(0)=\underline{e}_{r},\underline{v}(0)=v_{0}\underline{e}_{\theta}
$$
Then the [[Angular Momentum|angular momentum]] is 
$$
\underline{L}=\underline{r}\times \underline{v}=v_{0}\underline{e}_{r}\times \underline{e}_{\theta}=v_{0}\underline{e}_{3}
$$
Hence $L=v_{0}$, now 
$$
E=\frac{1}{2}(\dot{r}^{2}+r^{2}\dot{\theta}^{2})-\frac{1}{r}=\frac{1}{2}v_{0}^{2}-1
$$
Note $L=r^{2}\dot{\theta}$, so $r^{2}\dot{\theta}^{2}=\frac{v_{0}^{2}}{r^{2}}$, so
$$
\dot{r}^{2}+\frac{v_{0}^{2}}{r^{2}}-\frac{2}{r}+(2-v_{0}^{2})=0
$$
$$
=\frac{1}{r^{2}}(Q(r))
$$
Where $Q(r)=(2-v_{0}^{2})r^{2}-2r+v_{0}^{2}$. Since $\dot{r}^{2}\geq 0$, we need $Q(r)\leq 0$
If $v_{0}=1$, then $Q(r)=r^{2}-2r+1=(r-1)^{2}$, so $r=1\forall t$, and $\dot{r}=0\forall t$, so we have a circular orbit
If $v_{0}=\sqrt{ 2 }$, then $Q(r)=-2r+2=2(1-r)$, so $r\geq 1$
If $v_{0}>\sqrt{ 2 }$, then $Q$ will be a negative parabola and again, $r\geq 1$
If $v_{0}<\sqrt{ 2 }$, then $Q$ will have two roots, $r=1$, and $r=\frac{v_{0}^{2}}{2-v_{0}^{2}}$, and this is a bounded orbit (it will in fact be periodic and elliptical)
### Example
For shooting a projectile from the surface of Earth, we have
$$
f(r)=-\frac{GMm}{r^{2}}
$$
Where $M$ is mass of Earth, $m$ is mass of projectile and $G$ is Newton's constant
Start at $r=R$ the radius of Earth, then
$$
E=\frac{1}{2}mv^{2}-\frac{GMm}{r}=\frac{1}{2}mv_{0}^{2}-\frac{GMm}{R}
$$
So escape speed requires $\frac{GMm}{r}\to0$, and has
$$
\frac{1}{2}mv_{0}^{2}\geq \frac{GMm}{R}
$$
$$
\implies v_{0}\geq \sqrt{ \frac{2GM}{R} }
$$




#Physics #Particles 