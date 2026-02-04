## Classical Mechanics
We start with an overview of classical mechanics:
Say we have a particle in 1D $x(t)$, that follows [[Newton's Second Law of Motion|Newton's second law]]:
$$
m\frac{d x^{2}}{dt^{2}}=F=-\frac{d V}{dx}  
$$
Which is a [[Second Order Ordinary Differential Equations|second order]] [[Linear Ordinary Differential Equations|ODE]], so we need to know two things about the system at $t=0$, the [[Position|position]] $x(0)$ and $\frac{d x}{dt}(0)$, the [[Velocity|velocity]].
## Quantum Mechanics
If we have a particle in 1D, and it is denoted by the wave function $\psi(x,t)$, a function of position and time, which follows Schrodinger's Equation
$$
i\hbar \frac{ \partial \psi }{ \partial t } =-\frac{\hbar^{2}}{2m}\frac{ \partial^{2}\psi }{ \partial x^{2} } +V(x)\psi(x,t)
$$
Where $\hbar$ is Plank's constant, $V(x)$ is the [[Energy|potential]]. It is a [[Linear Partial Differential Equations|parabolic]] PDE. 
$\left| \psi(x,t) \right|^{2}$ tells you the probability of a particle being measured at $x$:
![[Quantum Mechanics 2025-03-20 14.12.43.excalidraw]]
It is first order in time, so its state is specified by the value of $\psi(x,0)=\psi(x)$.
We can then take the [[Fourier Transform|Fourier transform]] of this to find the probability of measuting the particle's [[Momentum|momentum]] as $p$ is:
$$
\frac{1}{2\pi}\left| \tilde{\psi}(p) \right| ^{2}
$$
![[Heisenberg's Uncertainty Principle 2025-03-20 14.17.31.excalidraw]]
Note that $\left| \psi \right|^{2}$ is a [[Probabilities|probability]] distribution, so
$$
\int_{-\infty}^{\infty} \left| \psi \right| ^{2} \, dx =1
$$
And so we can find the [[Standard Deviation|standard deviation]] by saying that the [[Expectation|expectation]], $E(x)=0$ and finding
$$
E(x^{2})=\int_{-\infty}^{\infty} x^{2}\left| \psi \right| ^{2} \, dx 
$$
And so
$$
\Delta x=\sqrt{ E(x^{2}) }
$$
Similarly $\frac{1}{2\pi}\left| \psi(p) \right|^{2}$ isis a probability density function:
$$
\frac{1}{2\pi}\int_{-\infty}^{\infty} \left| \psi(p) \right| ^{2} \, dp =1
$$
So we can find the standard deviation of the momentum
$$
\Delta p^{2}=E(p^{2})=\frac{1}{2\pi}\int_{-\infty}^{\infty} p^{2}\left| \tilde{\psi}(p) \right| ^{2} \, dp 
$$
Which leaves us with the uncertainty relation:
$$
\Delta x\Delta p\geq \frac{\hbar}{2}
$$

## Example
Take $\psi(x)=\left( \frac{b}{\pi} \right)^{\frac{1}{4}}e^{ -\frac{bx^{2}}{2} }$, such that
$$
\int_{-\infty}^{\infty} \left| \psi \right| ^{2} \, dx =1
$$
So we can take the fourier transform:
$$
\tilde{\psi}(p)=\sqrt{ 2\pi }\left( \frac{1}{\pi b} \right)^{\frac{1}{4}}e^{ -\frac{p^{2}}{2b} }
$$
So
$$
(\Delta x)^{2}=\frac{1}{2b}
$$
$$
 (\Delta p)^{2}=\frac{b}{2}
$$
Then
$$
(\Delta x)^{2}(\Delta p)^{2}=\frac{1}{4}
$$
Which is the minimum that we can get, since $\Delta x\Delta p\geq \frac{1}{2}$. So the most accurate way having $\psi$, is if it is a Gaussian.
![[Heisenberg's Uncertainty Principle 2025-03-20 14.32.10.excalidraw]]
If we let
$$
F(x)=\frac{d \psi(x)}{dx} 
$$
By the derivative theorem,
$$
\tilde{F}(p)=ip\tilde{\psi}(p)
$$
So by by [[Plancherel's Theorem|Plancherel's theorem]] on $F$,
$$
\int_{-\infty}^{\infty} \left| F(x) \right| ^{2} \, dx =\int_{-\infty}^{\infty} \left| \frac{d \psi}{dx}  \right| ^{2} \, dx =\frac{1}{2\pi}\int_{-\infty}^{\infty} \left| \tilde{F}(p) \right| ^{2} \, dp
$$
$$
= \frac{1}{2\pi}\int_{-\infty}^{\infty} \left| ip\tilde{\psi}(p) \right| ^{2} \, dp =\frac{1}{2\pi}\int_{-\infty}^{\infty} p^{2}\left| \tilde{\psi}(p) \right| ^{2} \, dp=E(p^{2})=(\Delta p)^{2}  
$$
Now we start on the proof of the Heisenberg uncertainty principle, we consider the integral:
$$
0\leq \int_{-\infty}^{\infty} \left| \frac{d \psi}{dx} -\lambda x\psi \right| ^{2} \, dx =\int_{-\infty}^{\infty} (\psi'-\lambda x\psi)(\overline{\psi'}-\lambda x  \overline{\psi}) \, dx 
$$
$$
= \int_{-\infty}^{\infty} \left| \psi' \right| ^{2} \, dx +\lambda^{2}\int_{-\infty}^{\infty} x^{2}\left| \psi \right| ^{2} \, dx -\lambda \int_{-\infty}^{\infty} x\left( \psi  \overline{\frac{d \psi}{dx} }+\overline{\psi}\frac{d \psi}{dx}  \right) \, dx 
$$
$$
= \Delta p^{2}+\lambda^{2}\Delta x^{2}-\lambda \int_{-\infty}^{\infty} x\frac{d }{dx} (\psi \overline{\psi}) \, dx 
$$
We [[Integration|integrate]] by [[Integration by Parts|parts]]:
$$
=\Delta p^{2}+\lambda^{2}\Delta x^{2}-\lambda\cancel{ [x\left| \psi \right| ^{2}]_{\infty}^{\infty} }+\lambda \underbrace{ \int_{-\infty}^{\infty} \left| \psi \right| ^{2} \, dx  }_{ =1 } 
$$
SInce $\left| \psi \right|^{2}\to0$ as $\left| x \right|\to \infty$, sooo
$$
0\leq\Delta p^{2}+\lambda^{2}\Delta x^{2}+\lambda
$$
Which is a quadratic in $\lambda$, which cannot be negative, so it cannot have two real roots, so the discriminant gives:
$$
b^{2}-4ac\leq 0
$$
$$
\implies 1-4(\Delta x)^{2}(\Delta p)^{2}\leq 0
$$
$$
 \therefore (\Delta x)(\Delta p)\geq \frac{1}{2}
$$

