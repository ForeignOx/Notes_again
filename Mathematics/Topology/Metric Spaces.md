A metric space motivates the notion of a metric
## Definition
A metric space is a set $X$ together with a function $d:X\times X\to \mathbb{R}_{\geq 0}$, such that #
- We have $d(x,y)\geq 0$ for all $x,y\in X$ and $d(x,y)=0$ iff $x=y$
- We have $d(x,y)=d(y,x)$ for all $x,y\in X$
- For all $x,y,z\in X$, we have $d(x,y)\leq d(x,y)+d(z,y)$
## Remark
The function $d$ is called a metric. If no confusion can arise, we omit $d$ from the notation and simply say $X$ is a metric space. $d$ stands for distance, and we think of it as measuring distances on $X$
The first condition ensures that the distance between different points is positive, while the second reflects the symmetry in the distance between points is positive, while the second reflects the symmetry in the distance between two points, the final condition is the [[Triangle Inequality|triangle inequality]]
## Example
 A norm on a [[Vectorspaces|vectorspace]] $V$ defines a metric
 $$
d_{\lvert \lvert \cdot \rvert \rvert }(x,y)=\lvert \lvert x-y \rvert \rvert 
$$
Which satisfies all the conditions by definition of metric
___
Let $M$ be a set, define a metric $d:M\times M\to \mathbb{R}$ by
$$
d(x,y)=1-\delta_{xy}
$$
Which can indeed be seen as a metric by checking the things. This is called the discrete metric
___
Let $(M,d)$ be a metric space and $A\subseteq M$, then $A$ is also a metric space; define $d_{A}:A\times A\to \mathbb{R}$  by restricting $d$ to $A\times A$, then $d_{A}$ is also a metric, the condition satisfaction is inherited from the superset
