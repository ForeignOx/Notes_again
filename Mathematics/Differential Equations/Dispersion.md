Usually, localised waves disperse as they travel, this prevents them from being soliltons.
## Example
Take the advection equation, a linear first order PDE:
$$
\frac{1}{v}u_{t}+u_{x}
$$
Which has solution
$$
u(x,t)=f(x-vt)
$$
For any function $f$
In this case there is no dispersion and all waves travel at the same rate, so not much to worry about
___
Another example is the wave equation,
$$
\frac{1}{v^{2}}u_{tt}-u_{xx}=0
$$
Which has solution
$$
u(x,t)=f(x-vt)+g(x+vt)
$$
Again all waves move at the same speed, so there is no dispersion, but there is no interaction either, so this is also not very interesting
___
Finally, the Klein-Gordon equation
$$
\frac{1}{v^{2}}u_{tt}-u_{x x}+m^{2}u=0
$$
Where we take $v>0$. This is much more interesting
If we try substituting a plane wave, we find:
$$
-\frac{\omega^{2}}{v^{2}}e^{ i(kx-\omega t) }+k^{2}e^{ i(kx-\omega t) }+m^{2}e^{ i(kx-\omega t) }=0 
$$
$$
\implies \frac{\omega^{2}}{v^{2}}+k^{2}+m^{2}=0
$$
So the plane wave is a solution given that $\omega$ satisfies
$$
\omega=\pm v\sqrt{ k^{2}+m^{2} }
$$
We usually ignore the negative sign though...
Here $k$ is wavenumber, $\omega$ is angular frequency, $\lambda=\frac{2\pi}{k}$ is the wavelength which has periodicity in $t$, and $\tau=\frac{2\pi}{\omega}$ which has periodicity in $t$
Any equation relating $\omega$ to $k$ is called a dispersion relation
