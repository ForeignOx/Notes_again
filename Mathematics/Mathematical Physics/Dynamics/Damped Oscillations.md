An oscillatory system is damped if the its [[Free Oscillations|free oscillations]] die away due to resistive forces. For example if a car drives over a small obstacle, the compression in suspension springs is increased. The springs then expand, releasing the excess elastic energy and, in the absence of damping forces the car, would continue oscillating
There are three categories of damping, under damping, over damping and critical damping, the last of which is the aim in designing many structures
## Derivation
A force that damps it will oppose velocity and no longer conserve [[Energy|energy]]. It will have the form $-c\dot{x}$ where $c$ is some constant. Forr convenience, we will call it $c=2mb$. Hence by [[Newton's Second Law of Motion|Newton's second law]], the equation of motion is:
$$
m\ddot{x}=-kx-2mb\dot{x}
$$
With $b>0$. This is a [[Second Order Ordinary Differential Equations|second order ODE]], and has auxiliary equation:
$$
m\lambda^{2}+2mb\lambda+k=0
$$
$$
\implies \lambda_{\pm}=-b\pm \sqrt{ b^{2}-\omega^{2} }
$$
Where $\omega=\sqrt{ \frac{k}{m} }$, so
$$
x(t)=Ae^{ \lambda_{+}t }+Be^{ \lambda_{-}t }
$$
## Overdamping
In the case where $b>\omega$, both $\lambda$ are real, both are negative, and the graph will look simply like:
![[Damped Oscillations 2025-01-22 11.47.30.excalidraw]]
So the initial $x$ dies out exponentially fast. This is called overdamping
## Underdamping
In the case $0\leq b<\omega$, we have underdamping, and $\lambda_{\pm}=-b\pm iq$, where $q=\sqrt{ \omega^{2}-b^{2} }$ so 
$$
x(t)=e^{ -bt }(\alpha \cos(qt)+\beta \sin(qt))
$$
![[output-onlinepngtools.png]]
Notice that the [[Period]] of the oscillation is constant - the time for oscillations does not get shorter as the amplitude decays. Also the amplitude goes down by the same fraction in each cycle
The greater the value of $\lambda$, the more rapidly the amplitude of the oscillations decreases
## Critical Damping
In the case $b=\omega$ known as critical damping and $\lambda_{\pm}=-b$, so 
$$
x(t)=e^{ -bt }(At+B)
$$
No oscillation
## Real Life
As the degree of damping increases, the system initially returns to equilibrium more quickly
![[Pasted image 20240302163350.png]]
For many purposes, engineers attempt to design systems which are critically damped, as critically damped oscillations converge most rapidly

#Mathematics #Dynamics
#Physics #Vibrations 