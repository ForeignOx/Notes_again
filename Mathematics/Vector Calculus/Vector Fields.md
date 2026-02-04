## Definition
A vector field is a [[Functions|function]] $\underline{f}:\mathbb{R}^{n}\to \mathbb{R}^{n}$ that assigns a vector to each point in $\mathbb{R}^{n}$.
A vector field where all vectors point towards the origin is called a sink
## Examples
Sketch the vector field $\underline{f}(\underline{x})=-\underline{x}$ in $\mathbb{R}^{2}$
$$
\underline{f}(\underline{x})=-x\underline{e}_{1}-y\underline{e}_{2}
$$
Consider $y=0\implies \underline{f}(x,0)=-x\underline{e}_{1}$
Consider $x=0\implies \underline{f}(0,y)=-y\underline{e}_{2}$
Consider $y=x\implies \underline{f}(x,x)=-x(\underline{e}_{1}+\underline{e}_{2})$
![[Vector Fields 2025-10-09 14.11.24.excalidraw]]
This is a sink.
___
Sketch the vector field $\underline{g}(\underline{x})=(y-x)\underline{e}_{1}-(x+y)\underline{e}_{2}$ in $\mathbb{R}^{2}$
- When $y=0,g(x,0)=-x(\underline{e}_{1}+\underline{e}_{2})$
- When $x=0,\underline{g}(0,y)=y(\underline{e}_{1}-\underline{e}_{2})$
- When $y=x,\underline{g}(x,x)=-2x\underline{e}_{2}$
- When $y=-x, \underline{g}(x,-x)=-2x\underline{e}_{1}$
![[Vector Fields 2025-10-09 14.21.50.excalidraw]]
This is a clockwise inward spiral
## Conservative Vector Fields
A vector field $\underline{f}: \mathbb{R}^{n}\to \mathbb{R}^{n}$ is conservative if it can be written as $\underline{f}=\underline{\nabla }g$ for some [[Continuity|continuously]] [[Differentiation|differentiable]] $C^{1}$ [[Scalar Fields|scalar field]], $g:\mathbb{R}^{n}\to \mathbb{R}$, called a scalar potential
Note that $\underline{f}=\underline{\nabla }g$ only defines $g$ up to a constant, $c$, because $\underline{\nabla }c=  \underline{0}$
### Example
Show that $\underline{f}(\underline{x})=-\underline{x}$ in $\mathbb{R}^{2}$ is conservative by finding a suitable potential
We need $\frac{ \partial g }{ \partial x }=-x$ and $\frac{ \partial g }{ \partial y }=-y$, integrating with respect to $x$ gives
$$
g(x,y)=-\frac{x^{2}}{2}+h(y)
$$
$$
\implies h'(y)=-y\implies h(y)=-\frac{y^{2}}{2}+c
$$
$$
\therefore  g(x,y)=-\frac{x^{2}+y^{2}}{2}+c
$$
### Proposition 
A vector field is conservative iff it has path independent [[Line Integrals|line integrals]] between each pair of points
#### Proof
$\implies$: Assume $\underline{f}$ is conservative, ie. $\underline{f}=\underline{\nabla }g$
![[Pasted image 20251028113916.png]]
Let $C_{1},C_{2}$ be any two curves sharing both endpoints $\underline{x}_{a},\underline{x}_{b}$, then
$$
\int _{C_{1}}\underline{f} \cdot \underline{\hat{t}} \, d \ell = \int _{C_{1}} \underline{\nabla } g\cdot \underline{\hat{t}} \, d \ell = g(\underline{x}_{b})-g(\underline{x}_{a}) 
$$
By the [[Fundamental Theorem of Line Integrals|fundamental theorem of line integrals]]
$$
\int _{C_{2}}\underline{f} \cdot \underline{\hat{t}} \, d \ell = \int _{C_{2}} \underline{\nabla } g\cdot \underline{\hat{t}} \, d \ell = g(\underline{x}_{b})-g(\underline{x}_{a}) 
$$
$$
\implies \int _{C_{1}} \underline{f} \cdot  \underline{\hat{t}}\, d \ell = \int _{C_{2}}\underline{f}\cdot  \underline{\hat{t}} \, d \ell 
$$
$\impliedby$: Assume $\underline{f}$ has path independent line integrals
We calim that
$$
g(\underline{x})=\int _{C(\underline{x})} \underline{f}\cdot  \underline{\hat{t}} \, d \ell 
$$
Satisfies $\underline{\nabla }g=\underline{f}$, wheree $C(\underline{x})$ is any curve connecting $\underline{0}$ to $\underline{x}$.
We have
$$
\frac{ \partial g }{ \partial x } =\lim_{ \delta \to 0 } \frac{1}{\delta}\left( \int _{C(\underline{x}+\delta \underline{e}_{1})} \underline{f}\cdot  \underline{\hat{t}} \, d \ell- \int _{C(\underline{x})} \underline{f}\cdot  \underline{\hat{t}} \, d \ell   \right)
$$
By the definition of partial derivative
![[Pasted image 20251028114618.png]]
By path independence, this is the same as integrating along $C_{1}$
$$
\therefore  \frac{ \partial g }{ \partial x } =\lim_{ \delta \to 0 } \frac{1}{\delta}\left( \int _{C_{1}}\underline{f}\cdot  \underline{\hat{t}} \, d \ell  \right)
$$
Where $C_{1}$ has $\underline{x}(t)=\underline{x}+t \underline{e}_{1}$ for $t\in[0,\delta]$
$$
    =\lim_{ \delta \to 0 } \frac{1}{\delta}\int_{0}^{\delta} f_{1}(\underline{x}+t \underline{e}_{1}) \, dt 
$$
$$
= \lim_{ \delta \to 0 } \frac{1}{\delta} \delta f_{1}(\underline{x}+t_{*} \underline{e}_{1})
$$
For some $t_{*}\in[0,\delta]$ by the [[Mean Value Theorem#Mean Value Theorem for Integration Integration|mean value theorem for integrals]]
$$
= f_{1}(\underline{x})
$$
By the [[Squeeze Theorem|squeeeze theroem]]
#### Example
Compute $\int _{C} \underline{f}\cdot  \underline{\hat{t}} \, d \ell$, wheere $\underline{f}=-\underline{x}$ and $C$ is the straight line from $(1,0)$ to $(2,0)$.
From above example, $\underline{f}=-\underline{\nabla }\left( \frac{x^{2}+y^{2}}{2} \right)$, so by the fundamental theorem of line integrals,
$$
\int _{C} \underline{f}\cdot  \underline{\hat{t}} \, d \ell=-\left( \frac{x^{2}+y^{2}}{2} \right)|_{(2,0)}+\left( \frac{x^{2}+y^{2}}{2} \right)|_{(1,0)}=-2+\frac{1}{2}=-\frac{3}{2}
$$
### Remark
The name conservative comes from the fact that integrating along a closed path doesn't change $f$:
$$
\oint_{C} \underline{\nabla } f\cdot  \underline{\hat{t}}\,d \ell=f(\underline{x}_{a})-f(\underline{x}_{b})=0
$$
For example gravitational force $\underline{F}(\underline{x})=\underline{\nabla }\left( \frac{GM}{\left| \underline{x} \right|} \right)$, if you move up and come back down to the same height, you will have had no change in energy