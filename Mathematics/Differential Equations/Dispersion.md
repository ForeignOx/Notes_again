Usually, localised waves disperse as they travel, this prevents them from being soliltons, dispersion is characterised by having waves that travel at different speeds
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
The maxima of a real plane wave such as $\mathfrak{R}(e^{ ikx-\omega(k)t })$ or $\mathfrak{I}(e^{ ikx-\omega(k)t })$ are called wave crests. By a slight abuse of terminology, we always call the real or imaginary parts of the complex wave as wave crests

By rewriting the complex plane solution of the Klein-Gordon equation as $e^{ ik(x-c(k)t) }$
We see that its wave crests move at velocity (called the phase velocity)
$$
c(k)=\frac{\omega(k)}{k}=v\sqrt{ 1+\frac{m^{2}}{k^{2}} }\mathrm{sign}(k)
$$
So plane waves with different wavenumbers move at different velocities, so if we try to make a lump of Klein-Gordon field by superimposing plane waves:
$$
u(x,t)=\mathfrak{R}\left( \int_{-\infty}^{\infty} f(k)e^{ i(kx)-\omega(k)t } \, dk  \right)
$$
It will disperse
There is another form of velocity than phase velocity called group velocity for lumps of field
$$
c_{g}(k)=\frac{d \omega(k)}{dk} 
$$
Which is the velocity of the lump while it disperses
## Remark
The energy and information carried by a wave travels at the group velocity and not the phase velocity. For a relativisting wave equation with speed of light $v$, no signals can be transmitted vaster than that, so it should be the case that $\left| c_{g}(k) \right|\leq v$ for all wavenumbers $k$, but there is no analogous bound on the phase velocity
