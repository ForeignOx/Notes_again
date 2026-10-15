## Definition
A quasi-linear PDE is a PDE of the form
$$
\sum_{\lvert \lvert \underline{\alpha} \rvert \rvert _{1}=k}a_{\underline{\alpha}}(\underline{x},u(\underline{x}),Du(\underline{x}),\dots,D^{k-1}u(\underline{x}))D^{\underline{\alpha}}u(\underline{x})+a_{0}(\underline{x},u(\underline{x}),Du(\underline{x}),\dots,D^{k-1}u(\underline{x}))=0
$$
## Method of Characteristics for Quasilinear 1st Order PDEs
### Goal
The objective is for $\Omega \subseteq \mathbb{R}^{n}$ open, $a:\Omega \times \mathbb{R}\to \mathbb{R}^{n}$, $b:\Omega \times \mathbb{R}\to \mathbb{R}$ are both given, we want a method to solve
$$
a(x,u(x))\cdot \underline{\nabla } u(x)=b(x,u(x))
$$
For $x\in\Omega$ solving for the unknown $u:\Omega\to \mathbb{R}$
We take a given $n-1$-dimensionsal hypersurface $\Gamma \subset \overline{\Omega}$ where we have $u(x)=u_{0}(x)$ for $x\in \Gamma$ is called the Cauchy condition
$\Gamma$ is called a cauchy surface/curve, $u_{0}$ is called the Cauchy datum, and the PDE together with this cauchy condition is called a Cauchy problem
### Example
Let $\beta:\Omega\to \mathbb{R}^{n}$ is given and consider
$$
\frac{d }{d\tau} X(\tau)=\beta(X(\tau))
$$
$$
X(0)=X_{0}\in  \Omega
$$
