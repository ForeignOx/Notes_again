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