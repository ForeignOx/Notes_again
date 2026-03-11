## Simultaneity
Suppose two inertial observers are related by a [[Lorentz boosts|Lorentz boost]]:
$$
x'=\gamma(x-vt)
$$
$$
 t'=\gamma\left( x-\frac{v}{c^{2}}t \right)
$$
Consider two events $E_{1}$ and $E_{2}$ with coordinates $(t_{1},x_{1})$ and $(t_{2},x_{2})$ for $R$
For observer $R'$ they have $(t_{1}',x_{1}')$ and $(t_{2}',x_{2}')$
$$
x_{i}'=\gamma(x_{i}-vt_{i})
$$
$$
 t_{i}'=\gamma\left( t_{i}- \frac{v}{c^{2}}x_{i} \right)
$$
For observer $R$ there is a spatial distance $\Delta x=x_{2}-x_{1}$ and temporal distance $\Delta t=t_{2}-t_{1}$
For $R'$, they have spatial distance $\Delta x'=x_{2}'-x_{1}'$ and tempporal distance $\Delta t'=t_{2}-t_{1}$
They are related by 
$$
\Delta x'=\gamma(\Delta x-v\Delta t)
$$
$$
 \Delta t'=\gamma\left( \Delta t-\frac{v}{c^{2}}\Delta x \right)
$$
If $E_{1}$ and $E_{2}$ happen simultaneously for $R$, $\Delta t=0$, thus $\Delta t'=\frac{v}{c^{2}}\Delta x\neq 0$ which mean $E_{1}$ and $E$ are not simultaneous for $R'$
## Length Contraction
Suppose that two particles are at rest for $R'$ separated by distance $\ell$
The system moves with velocity $v$ with respect to $R$. What is the spatial distance measured by $R$?
To meausre spatial distance, observers have to look at both particles simultaneously, this is a bit confusing given that they have different understandings of simultaneity
We know that
$$
\Delta x'=\ell
$$
For $R$ who is wanting to measure the distance by looking at both particles at the same time, so $\Delta t=0$, so we want to solve for $\Delta x$:
$$
\ell=\gamma(\Delta x)
$$
$$
 \Delta t'=-\frac{v\gamma}{c^{2}}x
$$
$$
\implies \Delta x=\frac{\ell}{\gamma} 
$$
$$
\implies  \ell'=\frac{\ell}{\gamma}<\ell
$$
So the length seems smaller for the person moving, this is why it's called the length contraction tim
## Time Dilation
Suppose we have two events $E_{1}$ and $E_{2}$ which happen at the same spatial point for $R'$ with time tifference $\Delta \tau$ between them
The observer $R'$ moves with velocity $v$ with respect to $R$
What is the time difference measured by $R$?
We know that we can alays write the Lorentz transformations:
$$
\Delta x'=\gamma(\Delta x-v\Delta t)
$$
$$
 \Delta t'=\gamma\left( \Delta t-\frac{v}{c^{2}}\Delta x \right)
$$
Substituting $\Delta x'=0,\Delta t'=\Delta \tau$, observer $R$ measures $\Delta t$, thus
$$
0=\gamma(\Delta x-v\Delta v)
$$
$$
 \Delta \tau=\gamma\left( \Delta t-\frac{v}{c^{2}}\Delta x \right)
$$
Solving this gives $\Delta t=\gamma\Delta \tau>\Delta \tau$ which means that time seems larger for the person moving, so we say time has dilated
## Example
Consider a detection of muons
Muons are created in the atmosphere at $h\approx 10\pu{km}$
They have high energy moving at $v\approx c$
They have only finite lifetime $\tau \approx 2.2\pu{\mu s}$
If relativity wasn't true, the lifetime from Earth's frame $\tau_{E}=\tau$
They would only be able to travel $v\tau_{E}\approx660\pu{m}$
So they wouldn't reach Earth
So from Earth's frame, due to time dilation,
$$
\Delta \tau_{E}=\gamma \tau \approx 15.8\cdot 2.2 \mu\pu{s} \approx 34.8\mu \pu{s}
$$
So they actually have $d=v\tau_{E}=10.4\pu{d=v\tau_{E}}$ 
But taking spetial relativity 
# The Beauty of 4D Theory
Maxwell's theory is written in very $3D$ language (note the use of cross products) and there is a split between space and time, we use partial time derivatives as opposed to divergence and curl, but the more we look at it, the more we notice that we have to also include time as a dimension
It is complicated because 3D language is pretty unnatural
We need to introduce inherently $3+1$ dimensional technology in $x,y,z,t$
We have the spacetime distance:
$$
\Delta s ^{2}=-c^{2}\Delta t^{2}+\Delta x^{2}+\Delta y^{2}+\Delta z^{2}
$$
It is convenient to introduce the vector
$$
x^{\mu}=\begin{pmatrix}
x^{0} \\
x^{1} \\
x^{2} \\
x^{3}
\end{pmatrix}
$$