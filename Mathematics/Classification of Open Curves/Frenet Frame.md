The local geometry of a [[Spacecurves|spacecurve]] $\underline{x}$ provides an intrinsic set of basis vectors and coordinates called the Frenet frame
## Definition
Let
$$
\kappa\equiv \left| \frac{d \underline{\hat{T}}(s)}{ds}  \right| 
$$
Be the curvature of $\underline{x}$ at $s$. The principal normal bector is defined (where $\kappa \neq 0$) as
$$
\underline{\hat{H}}=\frac{1}{\kappa}\frac{d \underline{\hat{T}}(s)}{ds} 
$$
As $\underline{\hat{T}}(s)$ is always a unit vector, $\underline{\hat{N}}\cdot \underline{\hat{T}}=0$. We define a third vector, the binormal as
$$
\underline{\hat{B}}=\underline{\hat{T}}\times \underline{\hat{N}}
$$
The three vectors $\underline{\hat{T}},\underline{\hat{N}},\underline{\hat{B}}$ forma right-handed orthonormal basis, and satisfy the Frenet-Serret equations:
$$
\frac{d \underline{\hat{T}}(s)}{ds} =\kappa \underline{\hat{N}}
$$
$$
 \frac{d \underline{\hat{N}}(s)}{ds} =\tau \underline{\hat{B}}-\kappa \underline{\hat{T}} 
$$
$$
 \frac{d \underline{\hat{B}}(s)}{ds} =-\tau \underline{\hat{N}}
$$
Where $\tau$ is known as the torsion, which is equal to:
$$
\tau(s)=\frac{\left( \underline{\hat{T}}(s)\times \frac{d \underline{\hat{T}(s)}}{ds}  \right)\cdot \frac{d ^{2}\underline{\hat{T}}(s)}{ds^{2}} }{\left| \underline{\hat{T}}(s)\times \frac{d \underline{\hat{T}(s)}}{ds} \right|^{2} }
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