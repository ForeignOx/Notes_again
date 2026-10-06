## Definition
A partial [[Differential Equations|differential equation]] or PDE is an equation containing an unknown [[Functions|function]] of two or more variables
The order of a PDE is the highest [[Differentiation|derivative]] it contains
A PDE is [[Linear Partial Differential Equations|linear]]/non-linear if it is [[Linear|Linear]]/non-linear in the dependent variable
## Order
Let $k\in\mathbb{N}$ and let $\Omega \subseteq \mathbb{R}^{n}$ be open. A $k$th order PDE has the form
$$
F(\underline{x},u(\underline{x}),Du(\underline{x}),\dots,D^{k}u(\underline{x}))=0, ~\underline{x}\in \Omega
$$
Where $F:\Omega \times \mathbb{R}\times \mathbb{R}^{n}\times \dots \times \mathbb{R}^{n^{k}}\to \mathbb{R}$
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
u(0,y,0)  = 0
$$
## Multi-index Notation
Let $\underline{\alpha}=(\alpha_{1},\dots,\alpha_{n})$ be a vector of nonnegative integers and let $\lvert \lvert \underline{\alpha} \rvert \rvert_{1}=\alpha_{1}+\dots+\alpha_{n}$ be the $\ell^{1}$-[[norms|norm]] of $\underline{\alpha}$. If $u:\mathbb{R}^{n}\to \mathbb{R}$, we define $D^{\underline{\alpha}}u$ to be the partial derivative
$$
D^{\underline{\alpha}}u=\frac{\partial^{\lvert \lvert \underline{\alpha} \rvert \rvert _{1}}u}{\partial x_{1}^{\alpha_{1}}\dots \partial x_{n}^{\alpha_{n}}}=\partial_{x_{1}}^{\alpha_{1}}\dots \partial_{x_{n}}^{\alpha_{n}}u
$$
For example if $u:\mathbb{R}^{2}\to \mathbb{R}$, then
$$
D^{(0,0)}u=u,~D^{(1,0)}u=u_{x},~D^{(0,1)}u=u_{y},~ D^{(2,0)}u=u_{xx},~D^{(1,1)}u=u_{xy},~ D^{(0,2)}u_{yy}
$$
Let $k\in\mathbb{N}_{0}$. We define $D^{k}u(\underline{x})$ to be the set of values of all partial derivatives of $u$ of order $k$ at point $\underline{x}$:
$$
D^{k}u(\underline{x})=\left\{ D^{\underline{\alpha}}u(\underline{x}):\middle|:\lvert \lvert \underline{\alpha} \rvert \rvert _{1}=k \right\}
$$
For the special case $k=1$, we write $Du=D^{1}u$ and regard the elements of $Du$ as being arranged in a row vector:
$$
Du=(u_{x_{1}},\dots,u_{x_{n}})
$$
Which is simply $(\underline{\nabla }u)^{\top}$
For the case $k=2$, we write this as the [[Hessian Matrix|hessian matrix]]:
$$
D^{2}u=\begin{pmatrix}
u_{x_{1}x_{1}} & \dots & u_{x_{1}x_{n}} \\
\vdots & \ddots & \vdots \\
u_{x_{n}x_{1} } & \dots & u_{x_{n}x_{n}}
\end{pmatrix}
$$
And observe that $[D^{2}u]_{ij}=\frac{\partial^{2}u}{\partial x_{i}\partial x_{j}}$ 
And in general, $Df$ is the Jacobian of $f$ for $f:\Omega \to \mathbb{R}^{m}$ with $\Omega \subseteq \mathbb{R}^{n}$
