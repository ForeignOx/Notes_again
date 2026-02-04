Let $f(x_{1},x_{2},\dots,x_{n})$ be a [[Functions|function]] $f:\mathbb{R}^{n}\to \mathbb{R}$. If all:
$$
\frac{ \partial^{2}f }{ \partial x_{i}\partial x_{j} } 
$$
For $1\leq i,j\leq j$ all exist and are [[Continuity|continuous]] in some neighbourhood, $\vec{x}=\vec{a}$ then
$$
\frac{ \partial^{2}f(\vec{a}) }{ \partial x_{i}\partial x_{j} } =\frac{ \partial^{2}f(\vec{a}) }{ \partial x_{j}\partial x_{i} } 
$$
I.e. the order in which you differentiate them doesn't matter
## Example
$$
f(x,y)=x^{2}+3xy\ln(x+y)
$$
$$
f_{x}=2x+3y\ln(x+y)+\frac{3xy}{x+y}
$$
$$
 f_{y}=3x\ln(x+y)+\frac{3xy}{x+y}
$$
$$
\frac{ \partial f_{x} }{ \partial y } =f_{xy}=3\ln(x+y)+\frac{3y}{x+y}+\frac{3x}{x+y}-\frac{3xy}{(x+y)^{2}}
$$
$$
\frac{ \partial f_{y} }{ \partial x }=f_{yx}=3\ln(x+y)+\frac{3y}{x+y}+\frac{3x}{x+y}-\frac{3xy}{(x+y)^{2}}
$$
Hence $f_{xy}=f_{yx}$

#Mathematics #Calculus #Theorem 