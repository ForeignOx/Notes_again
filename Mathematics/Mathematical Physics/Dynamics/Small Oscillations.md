Consider motion of a particle in a potential such as:
![[Small Oscillations 2025-01-27 14.14.54.excalidraw]]
Motion in this sort of potiential is always periodic, but the period is unknown except for the simplest case where $V(x)=\frac{1}{2}kx^{2}$ (the [[Simple Harmonic Motion|simple harmonic oscillator]]) where the period is $p=\frac{2\pi}{\sqrt{ \frac{k}{m} }}=2\pi \sqrt{ \frac{m}{k} }$  
The way to get any information about a general case is to approximate with the simple shape, so we want to simply fit a parabola to a local minimum:
![[Stuff 2025-01-27 14.08.54.excalidraw]]
If $V'(x_{0})=0$, then $x_{0}$ is an equilibrium, where $F(x_{0})=0$. This will identify [[Critical Points|local minima and maxima]]. We call this point a stable equilirium if the point is a local minimum; if you push it slightly, it would oscillate around that point, $V''(x_{0})>0$. Otherwise, it is usually unstable, $V''(x_{0})<0$, it is a local maximum, a slight push would send it far away from $x_{0}$. If $V''(x_{0})=0$, we simply have to check what is occurring
The period of small oscillations about a stable equilibrium is the period of the "best fitting" simple harmonic oscillator
## Computing $P$
Let $x_{0}$ be a local minimum of $V(x)$. Write $x(t)=x_{0}+\varepsilon(t)$ where $\varepsilon(t)$ is a small [[Functions|function]]. Substitute into the equation of motion obtained using [[Newton's Second Law of Motion|Newton's second law]]:
$$
m\ddot{x}=F(x)=-V'(x)\implies m \ddot{\varepsilon}=F(x_{0}+\varepsilon)
$$
Which we can approximate using the [[Taylor Series|Taylor expansion]]:
$$
=F(x_{0})+\varepsilon F'(x_{0})+\dots
$$
We can do this approximation since $\varepsilon$ is small and so higher powers are similarly. We also have $F(x_{0})=0$ since it is an equilibrium point
$$
\implies m\ddot{\varepsilon}=\varepsilon F'(x_{0})=-V''(x_{0})\varepsilon
$$
Which is the equation for simple harmonic motion in $\varepsilon$, where $V''(x_{0})$ is the 'spring constant' $k$, so the period of small oscillations is $P=2\pi \sqrt{ \frac{m}{V''(x_{0})} }$ This makes sense for a local minimum where $V''(x_{0}))>0$. If we have $V''(x_{0})<0$, the $\varepsilon$ would get exponentially far away

## Example
$m=3$, $V(x)=\frac{1}{4}x^{4}-\frac{1}{3}x^{3}-x^{2}$, then $V'(x)=x(x+1)(x-2)$, so there are $\hspace{0pt}3$ equilibria, $\hspace{0pt}2$ stable, $\hspace{0pt}1$ stable
We then look for period $P$ about $x=-1$, so we want to find $V''(x)=\frac{d }{dx}(x(x+1)(x-2))$, which will have three terms, and we can do a shorcut, since we will substitute $x=-1$, two of the terms will be $\hspace{0pt}0$, so only the middle term will not be $0$. In fact 
$$
V''(-1)=\left[ x(x-1)\frac{d }{dx}(x-1) \right]_{x=-1}=[x(x-2)]_{x=-1}=3
$$
Hence
$$
P=2\pi \sqrt{ \frac{m}{V''(x_{0})} }=2\pi \sqrt{ \frac{3}{3} }=2\pi
$$
This is an approximation, but is a good one for small oscillations

#Mathematics #Dynamics 