A streakline is a curve made up of all fluid elements that have passed through a given point in the past, it's a snapshot at a given time
Conider smoke from a chimney where the wind initially blows west and later shifts to the east, then the streakline is the trail of the smoke. But the smoke particles emitted at the beginning, middle and end of the story, the particle paths do not always coincide with the streakline:
![[Pasted image 20261006151308.png]]
To determine a streakline at a particular time, we need to find the particles that previously passed through, or were released from, some iven point, $\underline{a}$. That's the same problem as finding [[Particle Paths|particle paths]], but with different initial condition. If we name the release time $\tau$, we have to solve;
$$
\frac{d \underline{x}}{dt} =\underline{u}(\underline{x},t),~\underline{x}(\tau)=\underline{a}
$$
If we have steady flow, so $\frac{ \partial \underline{u} }{ \partial t }=0$, then streaklines are the same as particle paths
## Example
Consider the flow 
$$
\underline{u}=\underline{e}_{1}+t\underline{e}_{2}
$$
Let's find the streakline at time $t_{0}$, of particles that have been released from $\underline{a}=(a,b)$, since $t=0$
We solve the ODEs
$$
\frac{d x}{dt} =1,~x(\tau)=a
$$
$$
\frac{d x}{dt} =t~y(\tau)=b
$$
Integrating, then fixing $t=t_{0}$, gives
$$
\underline{x}(\underline{a},t,\tau)|_{t=t_{0}}=(t_{0}-\tau+a)\underline{e}_{1}+\left( \frac{t_{0}^{2}}{2}-\frac{\tau^{2}}{2}+b \right)\underline{e}_{2}
$$
Once again, to emphasise, $t_{0}$ is fixed and the streaklines are parametried by $\tau$, the time particles in the streakline passed through $\underline{a}$
In some cases we can eliminate $\tau$ to get the explicit streakline equation at $t_{0}$. The $x-$equation says that $x=t_{0}-\tau+a$, so we can expres the $y$-equation as
$$
y=\frac{t_{0}^{2}}{2}+b-\frac{1}{2}(t_{0}+a-x)^{2}
$$
Which we can plot
Finally, note that this is the equation for all particles that pass through $\underline{a}$; we haven't yet used the fact that they are released between $t=0$ and $t_{0}$, i.e. $\tau \in[0,t_{0}]$, which gives us the restriction that $x\in[a,t_{0}+a]$
If we choose the 