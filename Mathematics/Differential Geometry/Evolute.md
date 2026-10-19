## Definition
Let $\underline{\alpha}:I\to \mathbb{R}^{2}$ be a [[Smooth Functions|smooth]] regular [[Plane Curves|plane]] [[Curves|curve]] with corresponding [[curvature|curvature]] function $\kappa:I\to \mathbb{R}$
Assume that $\underline{\alpha}$ has no [[Vertices of Curves|inflection points]], that is, $\kappa(u)\neq 0$ for all $u\in I$, then the curve $e:I\to \mathbb{R}^{2}$ given by
$$
e(u)=\underline{\alpha}(u)+\frac{1}{\kappa(u)}\underline{n}(u)
$$
Is called the evolute of $\underline{\alpha}$
___
Note that the trace of the evolute does not change under reparametrisations of $\underline{\alpha}$, therefore, we can assume WLOG that our curve $\underline{\alpha}:I\to \mathbb{R}^{2}$ is unit speed
Using the frame equation:
$$
\underline{n}'(s)=-\kappa(s)\underline{t}(s)
$$
we see that the tangent vector of the evolute of the unit speed curve $\underline{\alpha}:I\to \mathbb{R}^{2}$ is given by
$$
e'(s)=\underline{\alpha}'(s)-\frac{\kappa'(s)}{\kappa^{2}(s)} \underline{n}(s)+\frac{1}{\kappa(s)} \underline{n}'(s) 
$$
$$
= \underline{t}(s)-\frac{\kappa'(s)}{\kappa ^{2}(s)} \underline{n}(s)-\frac{1}{\kappa(s)}\kappa(s) \underline{t}(s)=-\frac{\kappa'(s)}{\kappa^{2}(s)} \underline{n}(s)
$$
And therfore
$$
\lvert \lvert e'(s) \rvert \rvert =\frac{\left| \kappa'(s) \right| }{\kappa^{2}(s)}
$$
From this we can dwar the following conclusions:
- $e:I\to \mathbb{R}$ is in general not arclength parametrised
- Since $e'(s)=0$ iff $\kappa'(s)=0$, the evolute is regular iff $\underline{\alpha}$ has no vertices and $e(s)$ is singular iff $\underline{\alpha}(s)$ is a vertex
- If $e$ is regular, then its tangent vector $e'(s)$ is parallel to the unit normal vector $\underline{n}(s)$
