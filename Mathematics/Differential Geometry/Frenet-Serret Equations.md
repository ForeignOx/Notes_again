The local geometry of a [[Spacecurves|spacecurve]] $\underline{x}$ provides an intrinsic set of basis vectors and coordinates called the Frenet frame
## Definition
Let $\underline{\alpha}:I\to \mathbb{R}^{3}$ be a [[Smooth Functions|smooth]] [[Arclength|unit speed]] [[spacecurves|spacecurve]], then we define the principle normal vector 
$$
\underline{n}(s)=\frac{1}{\kappa(s)} \underline{t}'(s)\in \mathbb{R}^{3}
$$
We then define the binormal vector $\underline{b}:I\to \mathbb{R}^{3}$ by $\underline{b}(s)=\underline{t}(s)\times   \underline{n}(s)$, we call the ordered orthonormal basis $(\underline{t}(s), \underline{n}(s), \underline{b}(s))$ the frenet frame of $\underline{\alpha}$ at $\underline{\alpha}(s)$
## Proposition
Let $\underline{\alpha}:I\to \mathbb{R}^{3}$ be a smooth regular unit speed curve, $\kappa :I\to \mathbb{R}_{\geq 0}$ is curvature, $\kappa \neq 0$, $\tau:I\to \mathbb{R}$ be its [[torsion|torsion]], then let $\left\{ \underline{t}, \underline{n},\underline{b} \right\}$ be the tangent, principal normal and binormal vectors, then:
$$
\underline{t}'(s)=\kappa(s)  \underline{n}(s)
$$
$$
 \underline{n}'(s)=-\kappa(s) \underline{t}(s)-\tau(s)\underline{b}(s)
$$
$$
 \underline{b}'(s)=\tau(s) \underline{n}(s)
$$
Or in matrix form:
$$
\begin{pmatrix}
\underline{t}'(s)  \\
\underline{n}'(s) \\
\underline{b}'(s) 
\end{pmatrix}=\begin{pmatrix}
0 & \kappa(s) & 0 \\
-\kappa(s) & 0 & -\tau(s) \\
0 & \tau(s) & 0
\end{pmatrix}\begin{pmatrix}
\underline{t}(s) \\
\underline{n}(s) \\
\underline{b}(s)
\end{pmatrix}
$$
### Proof
The first and third are actually the definition of curvature and torsion, so that's fine, for the second, we have $\underline{b}= \underline{t}\times  \underline{n}$ and $\underline{n}=\underline{b}\times \underline{t}$, so
$$
\underline{n}'(s)=\underline{b}'(s)\times \underline{t}(s)+\underline{b}(s)\times \underline{t}'(s) 
$$
$$
= \tau(s)  \underline{n}(s)\times \underline{t}(s)+\kappa(s) \underline{b}(s)\times  \underline{n}(s)
$$
$$
= -\tau(s)\underline{t}(x)\times    \underline{n}(s)-\kappa(s)   \underline{n}(s)\times \underline{b}(s)
$$
$$
= -\tau(s)  \underline{b}(s)-\kappa(s) \underline{t}(s)
$$
## Issues
If $\kappa=0$, this frame is poorly defined. 
Another issue is as follows, if we have a helix shaped curve defined as
$$
\underline{x}(s)=\left( r\cos\left( \frac{qs}{\sqrt{ 1+(qr)^{2} }} \right),r\sin\left( \frac{qs}{\sqrt{ 1+(qr)^{2} }} \right),\frac{s}{\sqrt{ 1+(qr)^{2} }} \right)
$$
Where $q$ and $r$ are real constants, then the curvature and torsion are constant and given by
$$
\kappa(s)=\frac{q^{2}r}{1+(qr)^{2}}
$$
$$
\tau(s)=\frac{q}{1+(qr)^{2}}
$$
As $r\to 0$, the helix becomes a straight line and the curvature vanishes. The torsion does not however, but a straight line cannot have torsion
Writhe is invariant of choice of framing, further, for $\mathcal{C}^{3}$ differentiable curves, there is always a choice of framing which is non-vanishing