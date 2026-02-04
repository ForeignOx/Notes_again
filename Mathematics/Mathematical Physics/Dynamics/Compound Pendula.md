

## Examples
Say we have a [[Light|Light]] rod and two masses:
![[Rigid Bodies 2025-03-10 14.33.56.excalidraw]]
Then the distance $D$ from the axis to the [[Centre of Mass|centre of mass]] is 
$$
D=\frac{1}{2m}\left( m\cdot \frac{L}{2}+m\cdot L \right)=\frac{3}{4}L
$$
And the [[Moment of Inertia|moment of inertia]] is:
$$
I=m\left( \frac{L}{2} \right)^{2}+mL^{2}=\frac{5}{4}mL^{2}
$$
We can comppute $V(\theta)$ by adding the two pendulum equations:
$$
V(\theta)=mgL(1-\cos\theta)+mg\left( \frac{L}{2} \right)(1-\cos\theta)=\frac{3}{2}mgL(1-\cos\theta)
$$
Note that we can also compute $V$ as:
$$
\text{total mass}\times g\times \text{distance from pivot to CoM}\times(1-\cos\theta)
$$
Which for this example gives:
$$
2m\times g \times \frac{3}{4}L(1-\cos\theta)=\frac{3}{2}mgL(1-\cos\theta)
$$
Note that this way of calculating $V(\theta)$ always works because the calculation of centre-of-mass is the same as that of adding up $V(\theta)$ for each bit of the pendulum
___
Say you have a pendulum consisting of a solid [[Rigid Bodies|rigid]] bar of mass $M$, length $L$, pivoted at one end. Compute $E=K+V$
![[Compound Pendula 2025-03-12 11.17.34.excalidraw]]
First, he distance to the centre of mass is $\frac{1}{2}L$, which we can in fact check, but this immediately gives us
$$
V(\theta)=Mg \frac{L}{2}(1-\cos\theta)
$$
However we can consider a more careful calculation of the centre of mass:
![[Compound Pendula 2025-03-12 11.21.58.excalidraw]]
So centre of mass at
$$
\frac{1}{M}\underbrace{ \int_{0}^{L}  }_{ \text{limit of small sums} }\underbrace{ x }_{ \text{location of bit} }\underbrace{ \left( \frac{Mdx}{L} \right) }_{ \text{mass of small bit} }=\frac{1}{L}\int _{0}^{L}x \, dx =\frac{1}{L}\left[ \frac{x^{2}}{2} \right]_{0}^{L}=\frac{L}{2}-0=\frac{L}{2}
$$
We now need the moment of inertia, so we'll need to do a similar process to find it:
$$
I=\int_{0}^{L} x^{2} \left( M \frac{dx}{L}  \right)=\frac{1}{3}ML^{2}
$$
So
$$
K=\frac{1}{6}ML^{2}\dot{\theta}^{2}
$$
Hence
$$
E=\frac{1}{6}ML^{2}\dot{\theta}^{2}+\frac{1}{2}MgL(1-\cos\theta)
$$

What is the equation of motion for $\theta(t)$? What is the [[Period|period]] $P$ of [[Small Oscillations|small oscillations]] about stable equilibrium? Release the bar from rest horizontally, what is the maximum value of $\dot{\theta}$?
For the first part, we use $\frac{d E}{dt}=0$
$$
\frac{1}{3}ML^{2}\dot{\theta} \ddot{\theta}+\frac{1}{2}MgL\sin(\theta)\dot{\theta}=0
$$
$$
\implies \ddot{\theta}+\frac{3}{2} \frac{g}{L}\sin\theta=0
$$
For the second, if $\theta$ is small, then
$$
\ddot{\theta}+\frac{3}{2} \frac{g}{L}\theta=0
$$
$$
\implies P=2\pi \sqrt{ \frac{2L}{3g} }
$$
For the third, we stat at $\theta=\frac{\pi}{2}$, $\dot{\theta}=0$, we finish with $\theta=0$, and $\dot{\theta}$ is maximised. Conservation of energy gives:
$$
\underbrace{ \frac{1}{2}MgL }_{ \text{initial} }=\underbrace{ \frac{1}{6}ML^{2}\dot{\theta}^{2}_\text{max} }_{ \text{finish} }
$$
Giving 
$$
\dot{\theta}_\text{max}=\dots
$$
___
A real pendulum: a rod of mass $M$, with a mass $m$ at the end, rod has length $L$. Find the distance $D$ of the centre of mass from the pivot. Compute the moment of inertia $I$, find an expression for energy $E$
For the first part regard the rod as a particle of mass $M$ at centre $\frac{L}{2}$, then
$$
D=\frac{M\times \frac{L}{2}+mL}{M+m}=\frac{\frac{1}{2}M+m}{M+m}L
$$
For the second part we can simply add:
$$
I=\underbrace{ \frac{1}{3}ML^{2} }_{ \text{rod} }+\underbrace{ mL^{2} }_{ m }=\left( \frac{1}{3}M+m \right)L^{2}
$$
For the third part we simply substitute:
$$
E=\frac{1}{2}I\dot{\theta}^{2}+(M+m)gD(1-\cos\theta)
$$
___
A mass $m$ on string wound around a uniform round pulley of mass $M$ and radius $L$. Pulley is on horizontal axis, gravity acts downwards. Find the acceleration $A$ of the mass as it falls, via the energy $E$
We expect $A=f\left( \frac{M}{m} \right)g$ for some function $f\left( \frac{M}{m} \right)$ independent of $L$. We also expect $f\left( \frac{M}{m} \right)\to1$ as $\frac{M}{m}\to 0$ and $f\left( \frac{M}{m} \right)\to 0$ as $\frac{M}{m}\to \infty$
![[Compound Pendula 2025-03-14 16.28.08.excalidraw]]
The kinetic energy of $m$ is $\frac{1}{2}mv^{2}=\frac{1}{2}m\dot{z}^{2}$. The kinetic energy of the pulley is $\frac{1}{2}I\dot{\theta}^{2}$ and $\dot{z}=L\dot{\theta}$
So we need the moment of inertia $I$, which we can do by looking at the disk in [[Polar Coordinates|polar coordinates]] $(r,\theta)$ and consider a little section
![[Compound Pendula 2025-03-14 16.32.21.excalidraw]]
So the mss of our little piece is
$$
\frac{Mrd\theta dr}{\pi L^{2}}
$$
So
$$
I=\int _{0}^{L}\int_{0}^{2\pi} \frac{Mr}{\pi L^{2}} \, d\theta  \, dr =\int_{0}^{L} \frac{Mr}{\pi L^{2}}2\pi \, dr =\frac{1}{2}ML^{2}
$$
The potential energy of the pulley is constant as its centre of mass is constant
The potential energy of $m$ is $V=-\int mg \, dz=-mgz$ (note that $z$ is acting downwards)
So
$$
E=\frac{1}{2}m\dot{z}^{2}+\frac{1}{4}M\underbrace{ L^{2}\dot{\theta}^{2} }_{ =\dot{z}^{2} }-mgz
$$
And $\frac{d E}{dt}=0$, so
$$
m\dot{z} \ddot{z}+\frac{1}{2}M\dot{z} \ddot{z}-mg\dot{z}=0
$$
$\dot{z}=0$ is a useless solution, so we can divide
$$
\ddot{z}  \left( 1+\frac{1}{2}\frac{M}{m} \right)=g
$$
And $\ddot{z}=A$, so
$$
A=\frac{g}{\left( 1+\frac{1}{2} \frac{M}{m} \right)}
$$
Note that this is what we expected with 
$$
f\left( \frac{M}{m} \right)=\frac{1}{1+\frac{1}{2} \frac{M}{m}}
$$
And as $\frac{M}{m}\to0,f\left( \frac{M}{m} \right)\to1$, and as $\frac{M}{m}\to \infty,f\left( \frac{M}{m} \right)\to 0$ 
