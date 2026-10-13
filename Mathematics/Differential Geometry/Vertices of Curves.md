## Definition
Let $\underline{\alpha}:I\to \mathbb{R}^{2}$ be a [[Smooth Functions|smooth]] regular [[plane curves|plane curve]] with [[curvature|curvature]] $\kappa:I\to\mathbb{R}$
- A point $\underline{\alpha}(u_{0})$ is called an inflection point of $\underline{\alpha}$ if $\kappa(u_{0})=0$
- A point $\underline{\alpha}(u_{0})$ is called a vertex of $\underline{\alpha}$ if $\kappa'(u_{0})=0$
## Examples
Consider a parabola $\underline{\alpha}(u)=(u,u^{2})$, then 
$$
\kappa(u)=\frac{x'y''-x''y'}{((x')^{2}+(y')^{2})^{\frac{3}{2}}}=\frac{2}{(1+4u^{2})^{\frac{3}{2}}}
$$
So 
$$
\kappa'(u)=-\frac{24u}{(1+4u^{2})^{\frac{5}{2}}}
$$
So the only vertex will be when $u=0$
___
Consider a cubic $\underline{\alpha}(u)=(u,u^{3})$, then
$$
\kappa(u)=\frac{6u}{(1+9u^{4})^{\frac{3}{2}}}
$$
$$
\kappa'(u)= \frac{5(1-45u^{4})}{(1+9u^{4})^{\frac{5}{2}}}
$$
So vertices at the points where $u=_\pm \frac{1}{45}^{\frac{1}{4}}$
