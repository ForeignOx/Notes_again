## Definition
A streamline is a line parallel to the velocity vector $\underline{u}(\underline{x},t)$ at fixed time $t=t_{0}$. It is often used as a way to visualise a snapshot of the velocity field everywhere, because you can draw a streamline through any point $\underline{x}_{0}$. A streamline is a curve $\underline{x}(s)$ satisfying
$$
\frac{d \underline{x}}{ds} =\underline{u}(\underline{x}(s),t_{0})
$$
So the main difference is that $\underline{x}$ is a function oof $s$ and not $t$ with initial condition $\underline{x}(0)=\underline{x}_{0}$
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