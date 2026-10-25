## Definition
A streamline is a line parallel to the velocity vector $\underline{u}(\underline{x},t)$ at fixed time $t=t_{0}$. It is often used as a way to visualise a snapshot of the velocity field everywhere, because you can draw a streamline through any point $\underline{x}_{0}$. A streamline is a curve $\underline{x}(s)$ satisfying
$$
\frac{d \underline{x}}{ds} =\underline{u}(\underline{x}(s),t_{0})
$$
So the main difference is that $\underline{x}$ is a function of $s$ and not $t$ with initial condition $\underline{x}(0)=\underline{x}_{0}$
## Example
Find the streamlines at $t=t_{0}$ of the velocity field:
$$
\underline{u}=\underline{e}_{1}+t \underline{e}_{2}
$$
We have to solve two simulataneous ODEs,
$$
\frac{d x}{ds} =1, ~x(0)=x_{0}
$$
$$

\frac{d y}{ds} =t_{0}~y(0)=y_{0}
$$
When we want the streamline that passes through some given $(x_{0},y_{0})$. Integrating the first equation, $x=s+x_{0}$, whicle the second gives $y=t_{0}s+y_{0}$ Eliminating $s$ hows that the streamilnes are line with slope $t_{0}$
## Streamlines as Boundaries
Streamlines are defined as being parallel to the velocity which means there is no flow normal to the streamline. This condition $\underline{u}\cdot \hat{\underline{n}}=0$ is known as the ==🔵no normal flow condition==
Now we can think about a solid boundary (a wall) which is impermeable to fluid flow. Well, along the boundary we must also have the no normal flow condition, so boundaries themselves are streamlines
In an inviscid fluid, where there is no friction between the fluid and any wall, we can replace streamlines in 2D with ssolid boundaries and the fluid will not know
Note that streamlines are snapshots and can move in time, so associated walls will also have to move
