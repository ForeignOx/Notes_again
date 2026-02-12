Projectiles close to the surface of a planet experience force from weight $mg$. Take $\underline{e}_{3}$ upwards, $\underline{e}_{1},\underline{e}_{2}$ horizontals, so we have force
$$
\underline{F}=-mg\underline{e}_{3}
$$
So by [[Newton's Second Law of Motion|Newton's second law]] we have equation of motion:
$$
m  \underline{\ddot{r}}=-mg\underline{e}_{3}
$$
If $\underline{r}(0)=0$ and $\underline{\dot{r}}(0)=\underline{u}$, then by integrating twice,
$$
\underline{r}(t)=-\frac{1}{2}gt^{2}\underline{e}_{3}+t\underline{u}+ \underline{0}
$$
If we add air resistance, a force proportional to the velocity, acting against it. We write this as a force $-m\mu  \underline{\dot{r}}$, now the equation of motion is
$$
m  \underline{\ddot{r}}=-mg\underline{e}_{3}-m\mu  \underline{\dot{r}}
$$
$$
\iff   \underline{\ddot{r}}=-g\underline{e}_{3}-\mu  \underline{\dot{r}}
$$
$$
 \iff  \underline{\dot{v}}+\mu \underline{v}=-g\underline{e}_{3}
$$
We can use an integrating factor here this still works with an [[First Order Ordinary Differential Equations|integrating factor]], and here it is $I=e^{ \mu t }$, so
$$
\frac{d }{dt} (e^{ \mu t }\underline{v})=e^{ \mu t }(\underline{\dot{v}}+\mu \underline{v})=-ge^{ \mu t }\underline{e}_{3}
$$
$$
\implies e^{ \mu t }\underline{v}=-g\mu ^{-1}e^{ \mu t }\underline{e}_{3}+\underline{c}
$$
where $\underline{c}$ is a vector constant of integration
$$
\implies \underline{v}(t)=-g\mu ^{-1}\underline{e}_{3}+\underline{c}e^{ -\mu t }
$$
And $\underline{v}(0)=\underline{u}$ gives
$$
\underline{u}=-g\mu ^{-1}\underline{e}_{3}+\underline{c}
$$
$$
\implies \underline{c}=\underline{u}+g\mu ^{-1}\underline{e}_{3}
$$
Hence we have $\underline{v}(t)$. We then integrate to get $\underline{r}(t)$.
## Example
Take $\underline{u}=u(\cos \theta)\underline{e}_{1}+u(\sin\theta)\underline{e}_{3}$, no air resistance:
![[Projectiles 2025-02-12 11.31.44.excalidraw]]
Compute range $R$: we have:
$$
x(t)=ut(\cos \theta)
$$
$$
 z(t)=ut(\sin\theta)-\frac{1}{2}gt^{2}
$$
We also have $y(t)=0$, but this is not helpful. It returns to the grount $z=0$ at time
$$
t_{1}=\frac{2u\sin\theta}{g}
$$
So 
$$
R=x(t_{1})=\frac{2u^{2}}{g}\cos\theta \sin\theta=\frac{u^{2}}{g}\sin(2\theta)
$$

_____

A particle is projected from a point $O$ on level horizontal ground with speed of $21$ms$^{-1}$ at an angle $\theta$ to the horizontal with $\tan\theta=\frac{3}{4}$
The particle is moving freely under gravity and lands at a point $A$ on the ground, which is 43.2m away from $O$
- Find the time it takes the particle to travel from $O$ to $A$
- Determine the greatest height above the ground reached by the particle during its flight
- Show that the particle remains at a height of at least 4/5m above ground for exactly $\frac{12}{7}$seconds
($t=\frac{18}{7},h=8.1$)
- A particle is projected from a point $O$ with speed $36$ms$^{-1}$ at an angle of elevation $\beta$. It reaches a point $P$ which is at the same vertical level a $O$ and horizontal distance of $60$m from $O$. The particle is subject to no external forces except its weight. Find the two possible values of $\beta$, and determine the shortest possible flight time for the journey
- The point $O$ lies on a plane which is inclined at an angle of $\frac{\pi}{6}$ to the horizontal. A particle is projected from $O$ up a line of greatest slope of the plane, with speed of $U$ms$^{-1}$ at  an angle $\theta+\frac{\pi}{6}$. The gravitational acceleration $g$ is assumed constant and air resistance is ignored. The particle first hits the plane when it is moving horizontally. Determine the exact value of $\tan\theta$
- A tank that is 200m away is travelling towards you at 15ms$^{-1}$. Determine the initial velocity for a projectile fired at $30^{\circ}$ above the horizontal that will hit the tank
- A cricket ball is struck from a point $A$ which is $1$m above level horizontal ground with speed of $25$ms$^{-1}$ at an angle of $30^\circ$ to above the horizontal. The ball first hits the ground at a point $B$. The ball is modelled as a particle moving through still air without any resistance. Determine the horizontal distance from $A$ to $B$. Calculate, to 3sf the speed of the ball as it reaches $B$
