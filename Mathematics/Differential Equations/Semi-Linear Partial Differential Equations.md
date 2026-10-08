## Definition
A semi-linear [[Partial Differential Equations|partial differential equation]] of order $k\in\mathbb{N}$ has highest order derivatives appearing in a linear way and at least one lower order derivative not. They have general form
$$
\sum_{\lvert \lvert \underline{\alpha} \rvert \rvert }a_{\underline{\alpha}}(x)D^{\underline{\alpha}}u(x)+a_{0}(x,u(x),\dots,D^{k-1}u(x))=0
$$
## Example
The Navier-Stokes equation:
$$
\partial_{t}v-\beta\Delta v+(Dv)v+\nabla p=0
$$
With $\nabla\cdot v=0$ in $n$ dimensions, $\beta>0$
## Remark
We can write a ge eral first order semi-linear operator as:
$$
\underline{a}(\underline{x})\cdot \underline{\nabla } u+a_{0}(\underline{x},u(\underline{x}))=0
$$
Where $\underline{a}:\Omega\to \mathbb{R}^{n}$, $a_{0}:\Omega \times \mathbb{R}\to \mathbb{R}$ must be nonlinear in $u(\underline{x})$ (or the last variable) 