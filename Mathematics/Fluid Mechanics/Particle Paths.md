## Definition
A particle path is the path $\underline{x}(t)$, of a fluid particle over a given time interval. At any time $t$, the velocity of this particle is given by the velocity field $\underline{u}$ evaluated at the position of the particle, meaning we need to solve the vector ODE:
$$
\frac{d \underline{x}}{dt} (t)=\underline{u}(\underline{x}(t),t)
$$
Subjject to initial conditions (the beginnings to the paths)
## Example
Find the path of a particle in the 2D flow:
$$
\underline{u}(\underline{x},t)=x\underline{e}_{1}-y\underline{e}_{2}
$$
Given $\underline{x}=\underline{a}=(a_{1},a_{2})$ at $t=0$, thismeans that we need to solve:
$$
\frac{d x}{dt} =x,~~x(0)=a
$$
$$
\frac{d y}{dt} =-y  ~ ~ ~y(0)=b
$$
