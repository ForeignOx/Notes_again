## Definition
A partial [[Differential Equations|differential equation]] or PDE is an equation containing an unknown [[Functions|function]] of two or more variables
The order of a PDE is the highest [[Differentiation|derivative]] it contains
A PDE is [[Linear Partial Differential Equations|linear]]/non-linear if it is [[Linear|Linear]]/non-linear in the dependent variable
## Examples
$$
\frac{ \partial u }{ \partial t } +\frac{ \partial^{3}u }{ \partial x^{3} } -bu\frac{ \partial u }{ \partial x } =0
$$
This has $u$ as the dependent variable, $x$ and $t$ as independents, it is 3rd order and it is non-linear due to the $bu\frac{ \partial u }{ \partial x }$
___
$$
\frac{ \partial^{2}u }{ \partial t^{2} } +\sin (u)\frac{ \partial^{2}u }{ \partial x \partial y} =0 
$$
This is non-linear due to the $\sin(u)$ term and second order
___
$$
\frac{ \partial^{3}u }{ \partial t^{3} } +\sin x\frac{ \partial^{2}u }{ \partial x\partial y } =0
$$
This is 3rd order and linear as $\sin(x)$ is one of the independent variables
## Solutions to PDEs
A solution to a PDE in some region $R$ of the space of independent variables is a function which possesses all the partial derivatives to the PDE in $R$ and satisfies the equation
The solution to a PDE is heavily dependent on boundary conditions which affect the spatial variables
We then also consider the initial conditions, which affect the temporal variable(s)

### Examples
An example of a boundary condition is:
$$
u(0,y,0)  = 
$$
