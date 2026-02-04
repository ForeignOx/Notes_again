Projectiles close to the surface of a planet experience force from weight $mg$. Take $\underline{e}_{3}$ upwards, $\underline{e}_{1},\underline{e}_{2}$ horizontas, so we have force
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

