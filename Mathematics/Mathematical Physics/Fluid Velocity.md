## Definition
Consider an infinitesimally small volume element $\delta V$ centred at some position $\underline{x}$ small enough for $\underline{v}(t,\underline{x})$ to be approximately constant throughout the volume
We can think  that $\underline{v}(t,\underline{x})$ gives the average velocity of constituent particles inside $\delta V$ at time $t$
## Example
If we have a charged fluid with [[Electric Charge|charge]] density $\rho(t,\underline{x})$ and fluid velocity $\underline{v}(t,\underline{x})$, then the [[Electric Current|current]] density $\underline{J}(t,\underline{x})=\rho(t,\underline{x})\underline{v}(t,\underline{x})$
Imagine that $\delta Q(t)$ passes through $\delta S$ in time $\delta t$, we know that $\delta Q=\underline{J}\cdot\delta \underline{S} \delta t$ and $\delta \underline{S}=\hat{\underline{n}}\delta S$
In the time $\delta t$, the fluid travels a distace $\delta l =\left| \underline{v} \right|\delta t$
$$
\delta Q=\rho \delta V=\rho \delta l\delta S\cos\theta=\rho \left| \underline{v} \right| \delta t\delta S\cos\theta 
$$
$$
= \rho(\left| \underline{v} \right| \cos\theta)\delta S\delta t=\rho \underline{v}\cdot \hat{\underline{n}}\delta S\delta t 
$$
$$
= \rho \underline{v}\cdot \delta \underline{S} \delta t
$$
Which tells us that $\rho \underline{v}=\underline{J}$ :)
___
The electromagnetic field exerts force density 
$$
\underline{f}_{L}=\rho \underline{E}+\underline{J} \times \underline{B}
$$
On a distribution $\rho,\underline{J}$
Consider a small volume element at $\underline{x}$ with volume $\delta V$ and fluid velocity $\underline{v}(t,\underline{x})$
The element contains $\delta q=\rho(t,\underline{x})\delta V$
The Lorentz force is 
$$
\delta F_{L}= \delta q (\underline{E}(t,\underline{x})+\underline{v}(t,\underline{x})\times \underline{B}(t,\underline{x}))
$$
$$
=\rho(t,\underline{x})(\underline{E}(t,\underline{x})+\underline{v}(t,\underline{x})\times \underline{B}(t,\underline{x}))\delta V 
$$
$$
= (\rho(t,\underline{x} )\underline{E}(t,\underline{x})+\rho(t,\underline{x})\underline{v}(t,\underline{x})\times \underline{B}(t,\underline{x}))\delta V
$$
$$
=(\rho(t,\underline{x})\underline{E}(t,\underline{x})+\underline{J}(t,\underline{x})\times \underline{B}(t,\underline{x}))\delta V
$$
This means that this first term must be the force density:
$$
\underline{f}_{L}=\rho \underline{E}+\underline{J}\times \underline{B}
$$
As we wanted
___
Finding $\rho$ and $\underline{J}$ for a point particle $q$
Suppose particle is at $\underline{y}(t)$ and its density is $\rho_{\underline{y}(t)}(t,\underline{x})$:
$$
\int _{V}\rho_{\underline{y}(t)}(t,\underline{x}) \, d^{3} \underline{x}=\begin{cases}
0 & \underline{y}(t)\not\in  V \\
q & \underline{y}(t)\in  V
\end{cases} 
$$
This means that
$$
\rho_{\underline{y}(t)}(t,\underline{x})=\begin{cases}
0 & \underline{x}\neq \underline{y}(t) \\
\infty & \underline{x}=\underline{y}(t)
\end{cases}
$$

This means that all the charge comes from a single point, so strictly speaking this is not a function, it is a distribution
For this reason we can define it to be the [[Dirac Delta Function|Dirac delta function]]
