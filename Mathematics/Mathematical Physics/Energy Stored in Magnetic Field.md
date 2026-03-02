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
Thus from Faraday's law, we have
$$
\delta W=-\frac{d \Phi_{S}(t)}{dt} I(t)\delta t=-L\frac{d I}{dt} I(t)\delta t = -\frac{L}{2}\frac{d }{dt}(I^{2}(t))\delta t 
$$
$$
\implies \frac{d W}{dt} =-\frac{L}{2}\frac{d}{dt} (I^{2}(t))
$$
$$
\implies  W(t)=-\frac{L}{2}(I(t))^{2} 
$$
$$
\implies  W(t)=-\frac{1}{2}\Phi_{S}(t)I(t) 
$$
So the energy we spent is
$$
U(t)=\frac{1}{2}\Phi_{s}(t)I(t)
$$
We know that
$$
\underline{J}(t,\underline{x})=\oint_{C} \delta(\underline{x}-\underline{y}(s))\underline{\dot{y}}(s)I(t)~d s
$$
So
$$
U(t)=\frac{1}{2}I(t)\int _{S}\underline{B}(t,\underline{x})\cdot \, d\underline{S}=\frac{1}{2}I(t)\int _{S}(\underline{\nabla} \times \underline{A} )\cdot \, d\underline{S}  
$$
Which by [[Stokes' Theorem|Stokes' theorem]],
$$
=\frac{1}{2}I(t)\oint_{C}\underline{A}(t,\underline{y})\cdot d\underline{y}=\frac{1}{2}I(t)\oint_{C}\underline{A}(t,y(s))\cdot \underline{y}(s)~ds
$$
$$
=\frac{I(t)}{2}\oint_{C}\left( \int _{\mathbb{R}^{3}}\underline{A}(t,\underline{x})\delta(\underline{x}-\underline{y}(s)) \, d^{3}\underline{x} \right) \cdot \underline{y}(s)~ds 
$$
$$
=\frac{1}{2} \int _{\mathbb{R}^{3}} \underline{A}(t,\underline{x})\cdot\left( \oint_{C} I(t)\delta(\underline{x}-\underline{y}(s))\underline{\dot{y}}(s)~ds \right) \, d^{3}\underline{x}  
$$
$$
= \frac{1}{2}\int _{\mathbb{R}^{3}} \underline{A}(t,\underline{x})\cdot \underline{J}(t,\underline{x}) \, d^{3}\underline{x} 
$$
$$
= \frac{1}{2\mu_{0}}  
$$