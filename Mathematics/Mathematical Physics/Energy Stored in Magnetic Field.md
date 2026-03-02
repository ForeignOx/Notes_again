Why does a [[Magnetic Fields|magnetic field]] store energy?
Why does it take [[energy|energy]] to increase the [[Electric Current|current]] $I(t)$ running in a loop $C$?
![[Pasted image 20260302142022.png]]
We get an induced [[electric fields|electric field]] due to [[Faraday's law|Faraday's law]] which opposes the increasing $I(t)$, we consider a loop of wie $C$ parametrised by $\underline{y}(s)$, the current $I(t)$ increases slowly in time
## Quasi-Static Approximation $\underline{J}(x,t)$
If we take Maxwell' laws, we know
$$
\underline{\nabla} \times \underline{B} =\mu_{0}\left( \underline{J}+\varepsilon_{0}\frac{ \partial \underline{E} }{ \partial t}  \right)
$$
If we are in a quasi-static situation,
$$
\underline{B}\propto \underline{J}(t)\implies \frac{ \partial \underline{B} }{ \partial t } \propto \frac{ \partial \underline{J} }{ \partial t } 
$$
$$
\implies \underline{E}\propto \frac{ \partial \underline{J} }{ \partial t } \implies \frac{ \partial \underline{E} }{ \partial t } \propto \frac{ \partial^{2}\underline{J} }{ \partial t^{2} }   
$$
When $\frac{ \partial^{2}\underline{J} }{ \partial t^{2} }$ is small, we approximate:
$$
\underline{\nabla} \times \underline{B} =\mu_{0}\underline{J}+\cancelto{ 0 }{ \mu\varepsilon_{0} \underbrace{ \frac{ \partial \underline{E} }{ \partial t }  }_{ \propto \frac{ \partial^{2}\underline{J} }{ \partial t^{2} }  } }
$$
Thus we can use the Biot-Savat law:
$$
\underline{B}(t,\underline{x})\approx \int  \frac{\underline{J}(t,\underline{y})\times (\underline{x}-\underline{y})}{\left| \underline{x}-\underline{y} \right| ^{3}} \, d^{3}x 
$$
For a loop with constant current $I(t)$, 
$$
\underline{B}(t,\underline{x})=I(t) \frac{\mu_{0}}{4\pi}    \int _{C} \frac{\dot{y}(s)\times(\underline{x}-\underline{y}(s))}{\left| \underline{x}-\underline{y}(s) \right|^{3} } \, ds\propto I(t)
$$
So the magentic field is proportional to the current
Thus if we have time-dependent flux $\Phi_{S}(t)$, it must be proportional to $I(t)$, since the magnetic field is, and in fact:
$$
\Phi_{S}(t)=LI(t)
$$
And we call $L$ the inductance
Consider a small time interval $\delta t$ where the current increases from $I(t)$ to $I(t+\delta t)$
During $\delta t$, the charge that moves around the loop is
$$
\delta q=I(t)\delta t
$$
The amount of energy the current had to do is precisely,
$$
\delta W(t)=\mathscr{E}_{C}(t)\delta q=\mathscr{E}_{C}(t)I(t)\delta t
$$
Thus from Faraday's law, 
