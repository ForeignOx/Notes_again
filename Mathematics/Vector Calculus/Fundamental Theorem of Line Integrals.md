## Theorem
If $f:\mathbb{R}^{n}\to \mathbb{R}$ is a $C^{1}$ ([[Continuity|continuously]] [[Differentiation|differentiable]]) [[Scalar Fields|scalar field]] and $C$ is an oriented [[Curves|curve]] with parametrisation $\underline{x}(t)$ for $t\in[t_{0},t_{1}]$, then
$$
\int _{C}\underline{\nabla } f\cdot  \underline{\hat{t}} \, d\ell =f(\underline{x}(t_{1}))-f(\underline{x}(t_{0}))
$$
This is a generalisation of the [[Fundamental Theorem of Calculus|fundamental theorem of calculus]] applied to [[Line Integrals|line integrals]].
Note if $n=1$, then $C$ is just $[t_{0},t_{1}]$, and $\underline{\nabla }f=f'\underline{e}_{1}$, $\underline{\hat{t}}=\underline{e}_{1}$ which reduces to the fundamental theorem of calculus as expected
### Proof
$$
\int _{C} \underline{\nabla } f\cdot  \underline{\hat{t}} \, d \ell=\int _{t_{0}}^{t_{1}} \underline{\nabla } f \cdot \frac{d \underline{x}}{dt}  \, dt 
$$
$$
= \int_{t_{0}}^{t_{1}} \frac{ \partial f }{ \partial x_{1} } \frac{d x_{1}}{dt} +\frac{ \partial f }{ \partial x_{2} } \frac{d x_{2}}{dt} +\dots+\frac{ \partial f }{ \partial x_{n} } \frac{d x_{n}}{dt}  \, dt 
$$
$$
= \int_{t_{0}}^{t_{1}} \frac{d f}{dt}  \, dt= f(\underline{x}(t_{1}))-f(\underline{x}(t_{0}))    
$$
By the fundamental theorem of calculus and the [[Chain Rule|chain rule]].

