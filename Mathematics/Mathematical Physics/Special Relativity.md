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
\end{pmatrix}=\begin{pmatrix}
ct \\
x \\
y \\
z
\end{pmatrix}
$$
For $\mu \in \left\{ 0,1,2,3 \right\}$
Sol rewriting the spacetime distance,
$$
\Delta s^{2}=-(\Delta x^{0})^{2}+(\Delta x^{1})^{2}+(\Delta x^{2})^{2}+(\Delta x^{3})^{3}
$$
And if we use Einstein's summation convention, we write this:
$$
\Delta s^{2} = \Delta x^{\mu}\eta_{\mu \nu}\Delta x^{\nu}
$$
Where we define the Minkowski metric,
$$
\eta_{\mu \nu}=\mathrm{diag}(-1,1,1,1)
$$
So we say the space $\mathbb{R}^{4}$ equipped with the distance $\Delta s^{2}$ is called the Minkowski space $\mathbb{R}^{1,3}$
The inverse of the Minkowski is
$$
\eta^{-1}_{\mu \nu}=\eta^{\mu \nu}=\mathrm{diag}(-1,1,1,1)
$$
And note that
$$
\eta^{\alpha \mu}\eta_{\mu\beta}=\delta^{\alpha}_{\beta}
$$
Note that while $\eta$ and $\eta ^{-1}$ are technically the same matrix, they are different mathematical objects
$$
\eta^{\alpha\beta}\neq \eta_{\alpha\beta}
$$
A homogeneous [[Lorentz boosts|Lorentz transformation]] acting on coordinate can be written as:
$$
x^{\mu'}=\Lambda^{\mu}_{\nu}x^{\nu}
$$
By definition, it preserves the spacetime ditance:
$$
\Delta s^{2}=x^{\mu'}\eta_{\mu \nu}x^{\nu'}=x^{\rho}\eta_{\rho\sigma}x^{\sigma}  
$$
$$
\implies (\Lambda^{\mu}_{\rho}x^{\rho})\eta_{\mu \nu}(\Lambda^{\nu}_{\sigma}x^{\sigma})x^{\sigma}=x^{\rho}\eta_{\rho\sigma}x^{\sigma} 
$$
$$
\implies x^{\rho}\underbrace{ (\Lambda^{\mu}_{\rho} \eta_{\mu \nu}\Lambda^{\nu}_{\sigma}-\eta_{\rho\sigma}) }_{ =C_{\rho\sigma} }x^{\sigma}=0
$$
$$
\implies \Lambda^{\mu}_{\rho}\eta_{\mu \nu}\Lambda^{\nu}_{\sigma}=\eta_{\rho\sigma}
$$
Which is the defining feature of the Lorentz transformation
Note that we have used the fact that if $C_{ab}$ is [[Symmetric and Anti-Symmetric Matrices|symmetric]] and $x^{a}C_{ab}x^{b}=0$ means that $C_{ab}=0$
We can prove this:
$$
\frac{ \partial^{2} }{ \partial x ^{m}\partial x^{n} } (x^{a}C_{ab}x^{b})=0 
$$
$$
\implies 2(C_{mn}+C_{nm})=0 
$$
$$
\implies 4C_{mn}=0\implies C_{mn}=0
$$
As $C_{nm}=C_{mn}^{\top}=C_{mn}$
In matrix notation, we write the defining feature as:
$$
\Lambda ^{\top}\eta\Lambda= \eta
$$
This is an aanlogue of $R^{\top}IR=I$ in $\mathbb{R}^{3}$
