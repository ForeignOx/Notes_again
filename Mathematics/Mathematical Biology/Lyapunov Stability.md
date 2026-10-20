## Definition
Given an equilibrium solution $x_{0}$ to an [[Autonomous ODEs|autonomous]] ODE,
$$
F\left( x(t),\frac{d x}{dt} ,\dots,\frac{d x^{n}}{dt^{n}}  \right)=0
$$
The solution is Lyapunov stable if
$$
\forall\varepsilon>0,\exists\delta>0: \left| x(0)-x_{0} \right| <\delta\implies \left| x(t)-x_{0} \right| <\varepsilon
$$
