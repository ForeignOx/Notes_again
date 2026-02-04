## Theorem
If $\underline{f}:\mathbb{R}^{3}\to \mathbb{R}^{3}$ is a [[Continuity|continuously]] [[Differentiation|differentiable]] [[Vector Fields|vector field]] and $C$ is an oriented closed [[Curves|curve]] bounding a surface $S$, then
$$
    \oint_{C}\underline{f}\cdot  \underline{\hat{t}}\,d \ell = \int _{S}(\underline{\nabla} \times \underline{f} )\cdot  \underline{\hat{n}} \, dS
$$
Where $\underline{\hat{n}}$ is chosen such that $\underline{\hat{t}}\times  \underline{\hat{n}}$ is outward
![[Pasted image 20251030141329.png]]
### Notes
$S$ is sometimes called a capping surface for $C$
This tells us that the [[Surface Integrals|flux]] of [[Divergence and Curl|$\underline{\nabla} \times \underline{f}$]] is the same for every possible $S$ sharing the boundary $C$
![[Pasted image 20251030141656.png]]
You can remember the correct orientation by the "right hand grip rule"
There is a much more generalised version of Stokes' theorem in differential geometry:
$$
\int _{\Omega} \, d\omega = \int _{\partial \Omega}\omega
$$
Where $\Omega$ is a manifold, $d$ is the exterior derivative, which is a generalisation of divergence, curl and gradient, $\omega$ is a differential form and $\partial \Omega$ is the boundary of $\Omega$, then the divergence theorem is a special case of this
### Proof
Similar to the proof of the [[Divergence Theorem|divergence theorem]]. Subdivide $S$ into a disjoint union of smaller regions $S_{i}$ for $i=1,\dots ,m$ whose boundary curves have unit tangent vectors $\underline{\hat{t}}_{i}$
![[Pasted image 20251030153814.png]]
Observe that each boundary segment is shared by two neighbourfing regions with eqwual and opposite tangents, so
$$
\oint_{C}\underline{f}\cdot  \underline{\hat{t}}\, d \ell = \sum_{i=1}^{m} \oint_{C_{i}}  \underline{f}\cdot  \underline{\hat{t}}_{i}\, d \ell 
$$
$$
= \sum_{i=1}^{m}\left( \frac{1}{\left| A_{i} \right| } \oint_{C_{i}} \underline{f}\cdot  \underline{\hat{t}}_{i}\, d \ell \right)\left| Ai \right| 
$$
$$
= \lim_{ m \to \infty } \sum_{i=1}^{m}\left( \frac{1}{\left| A_{i} \right| }\oint_{C_{i}} \underline{f}\cdot  \underline{\hat{t}}_{i}\,d \ell \right)\left| A_{i} \right| 
$$
$$
= \int _{S} (\underline{\nabla} \times \underline{f} )\cdot  \underline{\hat{n}} \, dS 
$$
By [[Divergence and Curl#Alternate Definition for Curl|this alternate definition of curl]]
### Example
Verify Stokes' theorem by computing both sides for $\underline{f}(\underline{x})=z\underline{e}_{1}+x\underline{e}_{2}-x\underline{e}_{3}$ with $S$ the unit disk $\left\{ x^{2}+y^{2}\leq 1,z=0 \right\}$
For the left hand side (the [[Line Integrals|circulation]]), we parametrixe as $\underline{x}(t)=\cos t \underline{e}_{1}+\sin t \underline{e}_{2}$ for $t\in[0,2\pi]$, so
$$
\oint_{C}\underline{f}\cdot  \underline{\hat{t}}\,d \ell=\int_{0}^{2\pi} \underline{f}\cdot \frac{d \underline{x}}{dt}  \, dt 
$$
$$
= \int_{0}^{2\pi} (\cos t \underline{e}_{2}-\cos t \underline{e}_{3})\cdot (-\sin t \underline{e}_{1}+\cos t \underline{e}_{2}) \, dt 
$$
$$
= \int_{0}^{2\pi} \cos ^{2}t \, dt =\pi
$$
For the right hand side,
$$
\underline{\nabla} \times \underline{f} =\det \begin{pmatrix}
\underline{e}_{1} & \underline{e}_{2} & \underline{e}_{3} \\
\frac{ \partial  }{ \partial x }  & \frac{ \partial }{ \partial y }  & \frac{ \partial  }{ \partial z }  \\
z & x & -x 
\end{pmatrix}=2\underline{e}_{2}+\underline{e}_{3}
$$
The unit normal is $\underline{\hat{n}}=\underline{e}_{3}$, so
$$
    \int _{S} (\underline{\nabla} \times \underline{f} )\cdot  \underline{\hat{n}} \, dS=\int _{S}(2\underline{e}_{2}+\underline{e}_{3})\cdot \underline{e}_{3} \, dS = \int _{S} \, dS  
$$
Which is the area of the disk which is $\pi(1)^{2}=\pi=LHS$ :)
___
Repeat the surface integral, but with $S$ in this case the hemisphere $\left\{ x^{2}+y^{2}+z^{2}=1,z\geq 0 \right\}$, now $\underline{\hat{n}}= \underline{e}_{r}$ since we are using spherical coordinates, so
$$
    \int _{S}(\underline{\nabla} \times \underline{f} )\cdot  \underline{\hat{n}} \, dS=\int _{S}(2 \underline{e}_{2}+\underline{e}_{3})\cdot \underline{e}_{r} \, dS  
$$
Now $\underline{e}_{r}=\frac{\underline{x}}{r}=\frac{x\underline{e}_{1}+y\underline{e}_{2}+z\underline{e}_{3}}{r}$
$$
= \int _{S} \frac{2y}{r}+\frac{z}{r} \, dS = \int _{S} 2\sin\theta \sin \phi+\cos\theta \, dS 
$$
$$
= \int_{0}^{2\pi} \int_{0}^{\frac{\pi}{2}} (2\sin\theta \sin \phi+\cos\theta)\sin\theta \, d\theta  \, d\phi 
$$
$$
= \int_{0}^{2\pi} \int_{0}^{\frac{\pi}{2}}  2\sin ^{2}\theta \sin \phi +\cos\theta \sin\theta \, d\theta \, d\phi 
$$
$$
= \int_{0}^{2\pi} \left[ -\frac{\cos ^{2}\theta}{2} \right]_{0}^{\frac{\pi}{2}} \, d\phi=\frac{1}{2}\int_{0}^{2\pi}  \, d\phi=\pi   
$$
Which is what we wanted :)))
## Corollary
If $\underline{f}:\mathbb{R}^{3}\to \mathbb{R}^{3}$ is a $C^{1}$ vector field with $\underline{\nabla} \times \underline{f}\equiv 0$ throughout some simply-connected region $V\subset \mathbb{R}^{3}$, then $\underline{f}$ is conservative in $V$; i.e. $\underline{f}=\underline{\nabla }g$ with $g\in C^{1}$
A domain is simply-connected if any curve in the domain can be shrunk toa  point within the domain;
### Proof
Recall that $\underline{f}=\underline{\nabla }g$ iff $\underline{f}$ has path indepent line integrals.So we wen consif orient two arbitrary curves $C_{1},C_{2}$, between $\underline{x}_{a},\underline{x}_{b}\in V$
Devine $C=C_{1}x_{3}-C_{2}$
![[Pasted image 20251030145216.png]]
Since $V$ is simply connected, theere exists a capping surface $S\subset V$ for $C$, so stokes theorem gives:
$$
\oint_{C}\underline{f}\cdot  \underline{\hat{t}}\, d \ell =\int _{S}(\underline{\nabla} \times \underline{f} )\cdot   \underline{\hat{n}} \, dS 3
$$
$$
= \int _{C_{1}} \underline{f}\cdot   \underline{\hat{t}} \, d \ell = \int _{C_{2}} \underline{f}\cdot  \underline{\hat{t}} \, dS = 0
$$
$$
\implies \int _{C_{1}}\underline{f}\cdot \underline{\hat{t}} \, d \ell = \int _{C_{2}}\underline{f}\cdot  \underline{\hat{t}} \, d \ell 
$$
So path independence holds, so $\underline{f}$ is conservative.
