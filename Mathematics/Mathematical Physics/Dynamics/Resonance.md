ergzkovSuppose we have [[Simple Harmonic Motion|simple harmonic motion]], but there is an external forcing term $F(t)$, as well as the motion being [[Damped Oscillations|damped]], now the equation of motion is:
$$
m\ddot{x}+2mb\dot{x}+kx=F(t)
$$
And $x=x_{CF}+x_{PI}$
## Example
First consider a case with no damping, for example

$$
m\ddot{x}+kx=m\sin (pt)
$$
With $p$ being a positive constant, then
$$
x_{CF}=A\cos(\omega t)+B\sin(\omega t)
$$
And 
$$
x_{PI}=\frac{1}{\omega^{2}-p^{2}}\sin(pt)
$$
So $x=x_{CF}+x_{PI}$ is a combination of oscillations with two frequencies. But fails if $p=\omega$
If that is the case, then
$$
x_{PI}=-\frac{t}{2\omega}\cos(\omega t)
$$
So since we have a factor of $t$, $x$ grows without bound, this is resonance
___
Now we can add damping, for example $\ddot{x}+2mb\dot{x}+kx=m\sin(pt)$



___
## Resonance Curves
In a [[Forced Oscillations|forced oscillation]], consider the natural [[Frequency|frequency]] of oscillation $f_{0}$ and $f$ be the frequency of the driving force
- If $f\ll f_{0}$, the amplitude and phase of the oscillations are the same as that of the driving force
- If $f\gg f_{0}$, the amplitude of the oscillations is very small and the phase is $\pi$
- If $f\sim f_{0}$, the amplitude of the oscillations is very large, and the phase is $\frac{\pi}{2}$ behind the driving force
These can be collated into resonance curves:
![[Pasted image 20240302164850.png]]


#Mathematics #Dynamics 
#Physics #Vibrations 