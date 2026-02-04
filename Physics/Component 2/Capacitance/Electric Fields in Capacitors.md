Consider the [[Electric Fields|electric field]] due to the [[Electric Charge|charges]] on a charged parallel plate [[Capacitor]]
![[Electric Fields in Capacitors 2024-03-24 21.16.11.excalidraw]]
If the gap between the plates is small compared to the length of side of the plates (if they are square) or their diameter (if they are discs), the field in the gap is [[Uniform Electric Field|uniform]]
If we apply a [[Potential Difference]], $V$ between plates a distance $d$ apart, the magnitude of the [[Electric Field Strength|field strength]] $|E|$ in the gap is:
$$
|E|=\frac{V}{d}
$$
Between the plates of a parallel plate capacitor, the electric field strength can be shown to be proportional to the 'charge density'. That is:
$$
E \propto \frac{Q}{A}
$$
But $E=\frac{V}{d}$, so $\frac{Q}{A}\propto \frac{V}{d}$, so $\frac{Q}{V}\propto \frac{A}{d}$. Hence, the [[Capacitance]] is $C=\frac{\epsilon_{0}A}{d}$ 
## [[Motion of Charged Particle in Uniform Electric Field|Motion of a particle]]
### In a straight path
Suppose a particle of mass $m$ and (positive) charge $q$ is released from rest near the positive plate of a capacitor, we can calculate the time to reach the other plate, and the speed it will do so using [[Uniform Acceleration Equations]]:
$$
x=ut+\frac{1}{2}at^{2}
$$
With $x=d$, $u=0$, $a=\frac{qE}{m}=\frac{qV}{md}$, making these substitutions, and re-arranging, we get
$$
t=\sqrt{ 2d\times \frac{md}{qV} }=d\sqrt{ \frac{2m}{qV} }
$$
For the final speed, we can use
$$
v^{2}=u^{2}+2ax
$$
Substituting as before, we get
$$
v=\sqrt{ 2d \frac{qV}{md} }=\sqrt{ \frac{2qV}{m} }
$$
Note that for a given particle then, the final speed depends only on $V$, not $d$. In fact it doens't even depend on the field being [[Uniform Electric Field|uniform]], since the [[Kinetic Energy]] gained by the particle must be equal to the [[Electrical Potential Energy]] lost by the particle, hence (assuming the particle starts at rest):
$$
\frac{1}{2}mv^{2}=qV
$$
$$
\implies v = \sqrt{ \frac{2qV}{m} }
$$
In which $v$ is the speed acquired due to moving through a potential difference of $V$
### In a parabolic path
Consider an electron enters a transverse (crosswise) electric field between parallel plates with a potential difference, $V_{y}$. We shall assume that the field is uniform and doesn't extend beyond the edges of the plates. The electrons' $x$-wise velocity component, $v_{x}(=v)$ remains unchanged, and equal to the speed $v$ at which they entered the field. So their $x$-wise [[Displacement]] component at time $t$ after entering will be:
$$
x=v_{x}t=vt
$$
The $y$-direction acceleration is:
$$
\frac{-e}{m}E_{y}=\frac{-e}{m}\left( -\frac{V_{y}}{d} \right)=\frac{eV_{y}}{md}
$$
In which $d$ is the distance between plates. Applying $s=ut+\frac{1}{2}at^{2}$ to the $y$ component, we get
$$
y=\frac{eV_{y}}{2md}t^{2}
$$
As the initial $y$-[[Velocity]] is 0. Eliminating $t$ from both equations, we get:
$$
y=\frac{eV_{y}}{2md}\left( \frac{x}{v} \right)^{2}
$$
Hence $y\propto x^{2}$ and the path is parabolic

#Physics #Capacitance #Equation