![[Simple Pendula 2024-02-27 22.38.32.excalidraw]]
A mass $m$ on a light inextensible string of length $l$ (measured to the [[Centre of Mass|centre of mass]]) executes [[Simple Harmonic Motion]] as long as the amplitude of the oscillations is small (maximum angle of $\theta =5^{\circ}$) 
Ignoring air resistance, there are two forces on the pendulum, the weight $mg$ and the tension $T$ in the string. The mass is constrained to travel along the arc of a circle of radius $l$, the displacement from the centre along this arc, is $x$. Considering the tangential components:
	Component of $T$ along the arc = 0 (radius and tangent are perpendicular)
	Component of $mg$ along the arc $=-mg\sin\theta$
Hence:
$$
ma=-mg\sin\theta
$$
$$
\implies a=-g\sin\theta
$$
By small angle approximations, for small $\theta, \sin\theta=\theta$, and since $\sin\theta=\frac{\text{opp}}{\text{hyp}}=\frac{x}{l}$
$$
a=-\frac{g}{l}x=-\omega^{2}x
$$
Hence
$$
\omega=\sqrt{ \frac{g}{l} }
$$
$$
\implies T=2\pi \sqrt{ \frac{l}{g} }
$$
We can therefore write
$$
x=A\cos(\omega t+\epsilon)
$$
Or
$$
\theta=\theta_{\text{max}}\cos(\omega t+\epsilon)
$$
if the oscillation starts from its maximum positive position, then $\epsilon=0$
___
A rigid rod of length $L$ and negligivle mass. Pivot at one end, so swings in vertical plane. Attach mass $m$ to other end. Position is given by angle $\theta$. Set up $x$ and $z$ axes, $z$ upwards, $x$ side-to-side. Gravity acts downwards, so we have force $-mg$ in $z$ direction, so potential energy $V(\theta)=-\int F \, dz$, and $L-L\cos\theta=L(1-\cos\theta)$, thus
$$
V(\theta)=mgL(1-\cos\theta)
$$
The kinetic energy is 
$$
\frac{1}{2}mv^{2}=\frac{1}{2}m\underline{v}\cdot \underline{v}=\frac{1}{2}m(\dot{x}^{2}+\dot{z}^{2})
$$
$$
 \underline{v}= \underline{\dot{r}}=\frac{d }{dt} (x\underline{e}_{1}+z\underline{e}_{2})=\dot{x}\underline{e}_{1}+\dot{z}\underline{e}_{2}
$$
And $x=L\sin\theta$, so 
$$
\dot{x}=L\cos(\theta)\dot{\theta},\dot{z}=L\sin(\theta)\dot{\theta}
$$
So
$$
\frac{1}{2}mv^{2}=\frac{1}{2}mL^{2}\dot{\theta}^{2}
$$
Thus the energy is conserved:
$$
E=\frac{1}{2}mL^{2}\dot{\theta}^{2}+mgL(1-\cos\theta)
$$
Here $\dot{\theta}$ is the angular vlocity and $v=L\left| \dot{\theta} \right|$. 
We can consider this situation as identical to if a ball was rolling in a potential graph of $1-\cos\theta$
![[Simple Pendula 2025-02-10 14.30.09.excalidraw]]
We clearly have equilibria if $\theta=0$, stable as the pendulum hangs down, or $\theta=\pm \pi$ which is unstable
We can get the equation of motion from 
$$
\frac{d E}{dt} =0
$$
$$
\implies mL^{2}\dot{\theta}\ddot{\theta}+mg\sin(\theta)\dot{\theta}=0
$$
Whence either $\dot{\theta}=0$, or
$$
mL^{2} \ddot{\theta}+mgL\sin\theta=0
$$
$$
\implies  \ddot{\theta}+\frac{g}{L}\sin\theta=0
$$
This is non-linear so we can't do much properly, but we can do physics things yayy
We can approximate the period by staying close to $\theta=0$, we can use $\sin\theta   \underline{\overline{\equiv}} \theta$ , so this is shmmm and $\omega=\sqrt{ \frac{g}{L} }$ ect ect
If we release the pendulum from rest horizontally, what is the speed $u$ of the mass when it passes $\theta=0$?
We do this by conservation of energy:
$$
E=\frac{1}{2}mL^{2}\dot{\theta}^{2}+mgL(1-\cos\theta)
$$
$$
 \underbrace{ mgL }_{ \text{initial} }=\underbrace{ \frac{1}{2}mu^{2} }_{ \text{final} }
$$
$$
\implies u=\sqrt{ 2gL }
$$
Or we could do it 


#Mathematics #Dynamics #Physics #Vibrations 