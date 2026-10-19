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
____
We have seen that the curvature of the ellipse $\underline{\alpha}(u)=(a\cos u,b\sin u)$ with $a,b>0$ is given by:
$$
\kappa(u)=\frac{ab}{(a^{2}\sin ^{2}u+b^{2}\cos ^{2}u)^{\frac{3}{2}}}>0
$$
```desmos-graph
a=3
b=2
y=(a*b)/(a^2*(\sin(x))^2+b^2*(\cos(x))^2)|0<x<2*\pi
```
The ellipse has no inflection points since
$$
\kappa'(u)=-\frac{3ab(a^{2}-b^{2})\sin(2u)}{2(a\sin ^{2}u+b^{2}\cos ^{2}u)^{\frac{5}{2}}}
$$
We conclude in the case that $a\neq b$, that the ellipse has its vertices at $u=\frac{k\pi}{2}$ for $k\in \mathbb{Z}$
Restricting $\underline{\alpha}:I\to \mathbb{R}^{2}$ to the interval $I=[0,2\pi]$ and using the fact that the ellipse is a closed curve, we see that the ellipse has precisely four vertices at $(\pm a,0)\in\mathbb{R}^{2}$ and $(0,\pm b)\in\mathbb{R}^{2}$
The curvature at these vertices is:
$$
\kappa(0)=\kappa(\pi)=\frac{a}{b^{2}}
$$
$$
 \kappa\left( \frac{\pi}{2} \right)=\kappa\left( \frac{3\pi}{2} \right)=\frac{b}{a^{2}}
$$
The fact that an ellipse has at leat 4 vertices is a special case of a general result for simple smooth closed plane curves


