## Definition
A plane curve is a subset of Euclidean space, they can be parametrised and are then described via maps from the interval into the Euclidean plane, in which case they have a direction.
Their tangent vectors provide information about the speed in which a curve is traced
## Definition: Unit Normal Vector
![[Plane Curves 2026-10-12 13.20.27.excalidraw]]
We want to find a normal vector to the tangent vector
Let $\underline{\alpha}:I\to \mathbb{R}^{2}$ be a smooth regular curve in the plane, then the unit normal vector to $\underline{\alpha}$ at $\underline{\alpha}(u)$ is obtained by the anticlockwise rotation of the unit tangent vector $\underline{t}(u)$ of $\underline{\alpha}$ at $u$ by $\frac{\pi}{2}$
If $\underline{t}(u)=(x,y)$, then
$$
\underline{n}(u)=\underline{t}(u)\begin{pmatrix}
\cos \frac{\pi}{2} & \sin \frac{\pi}{2} \\
-\sin \frac{\pi}{2} & \cos \frac{\pi}{2} 
\end{pmatrix}=(x,y)\begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix}=(-y,x)
$$
And in general if $\underline{t}(u)=(x(u),y(u))$, then for the same reason, $\underline{n}(u)=(-y(u),x(u))$
## Lemma
Let $\underline{\alpha}:I\to \mathbb{R}^{2}$ be a smooth unit speed plane curve. Then the vector $\underline{t}'(s)$ is parallel to $\underline{n}(s)$
### Proof
In the case of a unit spee curve, we have $\underline{t}(s)=\underline{\alpha}'(s)$. The statement of the lemma is then an immediate consequence of the fact that
$$
\underline{\alpha}'(s)\cdot\underline{\alpha}'(s)=\lvert \lvert \underline{\alpha}'(s) \rvert \rvert ^{2}=1
$$
Namely, differentiating this gives:
$$
0=\underline{\alpha}''(s)\cdot\underline{\alpha}'(s)+\underline{\alpha}'(s)\cdot\underline{\alpha}''(s)=2\underline{\alpha}''(s)\cdot\underline{\alpha}'(s)=2\underline{t}'(s)\cdot \underline{t}(s)
$$
This shows that $\underline{t}'(s)$ is perpendicular to $\underline{t}(s)$ and must be, therefore parallel to the unit normal vector $\underline{n}(s)$
## Fundamental Theorem of Local Theory of Plane Curves
Given an open interval $I\subset \mathbb{R}$ and a smooth function $\kappa:I\to \mathbb{R}$, $s_{0}\in I,a\in\mathbb{R}^{2},v_{0}\in \mathbb{R}^{2}$ with $\lvert \lvert v_{0} \rvert \rvert=1$, then there exists a unique smooth unit unit speed plane curve $\underline{\alpha}:I\to \mathbb{R}^{2}$ with curvature function $\kappa$ and satisfying 
$$
\underline{\alpha}(s_{0})=a,~\underline{\alpha}'(s_{0})=v_{0}
$$
In other words, the curvature function determines the curve uniquely up to orientation presserving isometries, that is, up to a map of the form $f_{A,\underline{b}}(\underline{x})=\underline{x}A+\underline{b}$ with $\underline{x}\in\mathbb{R}^{2}$ a row vector, $A\in SO(2)$ (a rotation), and a row vector $\underline{b}\in\mathbb{R}^{2}$ (a translation)
Again, in other words, two unit speed plane curves $\underline{\alpha}:I\to \mathbb{R}^{2}$, $\underline{\beta}:I\to \mathbb{R}^{2}$ with the same curvature function $\kappa:I\to \mathbb{R}$ agree up to a map $f_{A,\underline{b}}$, that is $\underline{\beta}$
