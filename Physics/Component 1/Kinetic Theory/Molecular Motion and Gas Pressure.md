### Assumptions
- Gases will be treated as [[Ideal Gas Equation|ideal gases]]
- The volume of the molecules themselves is a negligible fraction of the volume occupied by the gas
- The molecules exert negligible forces on one another except during [[Molecular Collisions|collisions]]
- The effect of gravity is negligible
- Molecules have negligible volume
## Pressure and Molecular Motion
Imagine a single molecule of mass $m$ in a box, we ask the question, what pressure does it exert on face A?
![[Molecular Motion and Gas Pressure 2024-03-02 19.03.58.excalidraw]]
At the instant of the diagram, let the velocity $c$ have [[Components of vectors|components]]  $c_{x}, c_{y}, c_z$. Eventually, one molecule will hit face A. Because we are assuming [[Elastic Collisions]], it will bounce off with velocity $(-c_{x}, c_{y}, c_{z})$, so the change in [[Momentum]] of the molecule at A$=-2mc_{x}$
After bouncing off a few more walls it will reach A again after a time $\Delta t$ given by:
$$
\Delta t=\frac{2l_{x}}{c_{x}}
$$
at which the momentum will change by $-2mc_{x}$ again. So its rate of change of momentum at A is $-2mc_{x}\times \frac{c_{x}}{2l_{x}}=-\frac{mc_{x}^{2}}{l_{x}}$, and from [[Newton's Second Law of Motion]], we know that rate of change of momentum is equal to force, so the mean force exerted by A on the molecule is also equal to $-\frac{mc_{x}^{2}}{l_{x}}$ and by [[Newton's Third Law of Motion]], the mean force exerted by the molecule on A$=-\frac{mc_{x}^{2}}{l_{x}}$ and the mean pressure, $p$, exerted on A by the molecule is given by:
$$
p=\frac{F}{A}=\frac{mc_{x}^{2}}{l_{x}(l_{y}l_{z})}=\frac{mc_{x}^{2}}{V}
$$
Where $V$ is the volume of the box.
We now introduce a lot more molecules, so there are $N$ molecules in total and we'll call their $x$-velocity components $c_{1x}, c_{2x}, \dots, c_{Nx}$. Their pressures on face A add to give:
$$
p=\frac{mc_{1x}^{2}}{V}+\frac{mc_{2x}^{2}}{V}+\dots+\frac{mc_{Nx}^{2}}{V}=\frac{Nm \bar{c_{x}^{2}}}{V}
$$
Where $\bar{c_{x}^{2}}$ is the mean of the $c_{x}^{2}$ values. Applying Pythagoras' theorem for each molecule:
$$
\bar{c^{2}}=\bar{c_{x}^{2}}+\bar{c_{y}^{2}}+\bar{c_{z}^{2}}
$$
Given the assumption that gravity is negligible, there is no special direction, and after multiple collisions, the distribution of components of velocity in all directions would be the same, even if they started out different. This must mean that $\bar{c_{x}^{2}}=\bar{c_{y}^{2}}=\bar{c_{z}^{2}}$ which therefore means that $\bar{c_x^{2}}=\frac{1}{3}\bar{c^{2}}$, substituting into the earlier equation, we can see that:
$$
p=\frac{1}{3} \frac{Nm \bar{c^{2}}}{V}\implies pV=\frac{1}{3}Nm \bar{c^{2}}
$$
Since $Nm$ is the mass of the gas, we can divide by $V$ to get:
$$
p=\frac{1}{3}\rho \bar{c^{2}}
$$

#Physics #Kinetic_theory #Equation