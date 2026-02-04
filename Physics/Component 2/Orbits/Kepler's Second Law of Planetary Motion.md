The line joining the planet to the star sweeps equal areas in equal intervals of time
Note that this can be applied to moons orbiting planets by replacing planet with moon and star with planet
![[Kepler's Second Law of Planetary Motion 2024-03-27 11.52.54.excalidraw]]
This law is a consequence of the fact that gravity is a central force, so the force on a planet is always directed towards the star. Start by considering the case of a planet moving past a star of 0 mass, so the gravitational force is 0:
![[Kepler's Second Law of Planetary Motion 2024-03-27 17.16.36.excalidraw]]
The speed of the planet is a constant $u$ and the closest distance of approach is $d$. The shaded areas represent areas in equal times $\Delta t$. The area of a triangle is $\frac{1}{2}\times \text{base}\times \text{height}$ so all the triangles have an equal area $\frac{1}{2}ud\Delta t$, so the law holds
Next consider that, as the planet passes the star, it receives a 'nudge' from the star, which adds a [[Velocity]] $w$, in the direction of the star, changing its velocity from $u$ to $v$
![[Kepler's Second Law of Planetary Motion 2024-03-27 17.28.30.excalidraw]]
The area swept out per second at position 1 is $\frac{1}{2}uh$
Note that the Law still holds for unbounded orbits
## Proof
If an object follows a path $r=r(\theta)$ and sweeps an are $A(\theta)$ from $\theta=0$to $\theta=\theta$ is:
$$
A(\theta)=\int_{0}^{\theta} \int_{0}^{r(\theta)} r \, dr  \, d\theta  =\int_{0}^{\theta} \frac{1}{2}r(\theta)^{2} \, d\theta 
$$
And 
$$
\frac{d}{dt}A(\theta)=\frac{d A}{d\theta}\frac{d \theta}{dt}=\frac{1}{2}r(\theta )^{2}\dot{\theta}=\frac{L}{2m}
$$
Which is constant
So area in unit time is:
$$
\int_{t_{0}}^{t_{0}+1} \frac{d A}{dt} =\frac{L}{2m} 
$$
Hence proved :)
This is true for any central force and only envolves conservation of angular momentum.




#Physics #Orbits #Law