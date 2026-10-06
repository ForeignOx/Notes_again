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