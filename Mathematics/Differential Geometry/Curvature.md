## Motivation
We want a quantitative characterisation of the shape of a curve at every point. This goal leads to the notion of curvature $~\kappa$. Desired properties of $\kappa$ are:
- $\kappa=0$ for all points on a straight line,
- $\kappa$ at a point of the curve should be independent of the parametrisation
- $\kappa\to0$ for points on increasing circles
- $\kappa=\pm \frac{1}{r}$ for points on circles of radius $r$
It happens that curvature is related to the change of unit vector
## [[Plane Curves|Plane Curves]]
Since for a unit speed plane curve $\underline{\alpha}$, $\underline{t}'(s)$ is a multiple of $\underline{n}(s)$, we define the curvature of $\underline{\alpha}$ at $s$ as the proportionality factor.
### Definition
The (signed) curvature $\kappa(s)$ of a unit speed plane curve $\underline{\alpha}:I\to \mathbb{R}^{2}$ at $s \in I$ is defined by
$$
\underline{t}'(s)=\kappa(s)  \underline{n}(s)
$$
### Remark
For a given unit speed plane curve $\underline{\alpha}:I\to \mathbb{R}^{2}$, we can compute $\kappa(s)$ for $\sin n I$ via
$$
\underline{t}'(s)\cdot  \underline{n}(s)=\kappa(s)  \underline{n}(s)\cdot  \underline{n}(s)=\kappa(s)\lvert \lvert  \underline{n}(s) \rvert \rvert ^{2}=\kappa(s)
$$
So if $\underline{t}(s)=(x(s),y(s))$, then $\underline{n}'(s)=(-y(s),x(s))$ and $\underline{t}'(s=(x'(s),y'(s)))$$, soo
$$
\kappa(s)=\underline{t}'(s)  \underline{n}(s)=(x'(s),y'(s))\cdot(-y(s),x(s))=-x'(s)y(s)+y'(s)x(s)
$$
## Proposition
Let $\underline{\alpha}:I\to \mathbb{R}^{2}$ be a smooth regular plane curve with $\underline{\alpha}(u)=(x(u),y(u))$ (not necessarily parametrised by arclength), we have
$$
\kappa=\frac{x'y''-x''y'}{((x')^{2}+(y')^{2})^{\frac{3}{2}}}
$$
### Proof
The idea is that curv ature does not depend on parametrisation, so we need to do a change of variable. Let $u_{0}\in I$,
$$
S=\ell(u)=\int _{u_{0}}^{u}\lvert \lvert \underline{\alpha}'(t) \rvert \rvert  \, dt 
$$
Write $\underline{\beta}=\underline{\alpha}$