![[Oscillating Masses on Springs 2024-02-27 21.50.13.excalidraw]]
Consider a spring with spring constant $k$, the spring applies force $F_{0}$ to the mass
The mass $m$ in the first part is in equilibrium, so we can write:
$$
F_{0}=mg
$$
Then consider pulling down on the mass and then releasing it. It will oscillate vertically. Consider when the mass is at a displacement $x$ below its equilibrium position. The extension of the spring is increased by $x$, so the force $F(x)$ exerted by the spring on the mass is now given by
$$
F(x)=F_{0}+kx
$$
The resultant downward force is:
$$
F_{r es}=mg-F(x)=mg-F_{0}-kx=mg-mg-kx=-kx
$$
Hence we have [[Simple Harmonic Motion]], and thus we know $a=-\omega^{2}x$
Consider the force on the spring in equilibrium:
$$
F=-kx=-m\omega^{2}x
$$
$$
\implies k=m\omega^{2}
$$
$$
\implies \omega = \sqrt{ \frac{k}{m} }
$$
And since $T=\frac{2\pi}{\omega}$:
$$
T=2\pi \sqrt{ \frac{m}{k} }
$$
And since $f=\frac{1}{T}$
$$
f=\frac{1}{2\pi}\sqrt{ \frac{k}{m} }
$$
The same principle holds for a two-spring system
![[Oscillating Masses on Springs 2024-02-27 22.29.33.excalidraw]]
The same principle holds and the stiffness coefficient is simply the sum of the spring constants and there will again be SHM if friction is negligible
## Lagrangian Form
If the spring has mas $m$ and natural length $l$, which we can take to be $0$
We have $L=T-V$, with $T=\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2})$ and $V=\frac{1}{2}\kappa( \sqrt{ x^{2}-y^{2} }-l)^{2}=\frac{1}{2}\kappa(x^{2}+y^{2})$ 
$$
L=\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2})-\frac{1}{2}\kappa (x^{2}+y^{2})
$$
Which gives the Euler-Lagrange equations
$$
0=\frac{d }{dt} \left( \frac{ \partial L }{ \partial \dot{x} }  \right)-\frac{ \partial L }{ \partial x } =m\ddot{x}+\kappa x 
$$
$$
\implies x(t)=a_{x}\sin(\omega t)+b_{x}\cos(\omega t)
$$
And similarly for $y$
We can also do this in polar coortinates $r$ and $\theta$, this time $V=\frac{1}{2}\kappa r^{2}$, and
$$
T=\frac{1}{2}m(\dot{r}^{2}+r^{2}\dot{\theta}^{2})
$$
So 
$$
L=\frac{1}{2}m( \dot{r}^{2}+r^{2}\dot{\theta}^{2})-\frac{1}{2}\kappa r^{2}
$$
So we get equations
$$
\frac{d }{dt} (m\dot{r})-m\dot{\theta}^{2} r+\kappa r =0
$$
$$
 \frac{d }{dt} (mr^{2}\dot{\theta})=0
$$
With the latter telling us that $mr^{2}\dot{\theta}$ is conserved which tells us about the the rotational symmetry


#Physics #Vibrations 