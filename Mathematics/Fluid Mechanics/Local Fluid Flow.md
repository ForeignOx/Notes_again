To get a physical picture of fluid motion, it is useful to ask what an arbitrary flow $u(\underline{x},t)$ does to one fluid element. Does it stretch it or spin it or shift it? To answer this, we can compare the velocity at two nearby points $\underline{x}$ and $\underline{x}+\delta \underline{x}$ in the same flulid element $D$:
![[Pasted image 20261020101356.png]]
Expanding about the fixed point $\underline{x}$ using Taylor's theorem gives:
$$
\underline{u}(\underline{x}+\delta \underline{x})=\underline{u}(\underline{x},t)+\underline{\underline{J}}\delta(\underline{x})+\mathcal{O}(\left| \delta \underline{x} \right| ^{2})
$$
Where $\underline{\underline{J}}$ is the [[\underline{\underline{J}}acobian Transformation|jacobian]]:
$$
\underline{\underline{J}}=\nabla_{j}u_{i}=\frac{ \partial u_{i} }{ \partial x_{j} } 
$$
Note that sometimes we denote $\underline{\underline{J}}^{\top}=\nabla _{i}u_{j}=\frac{ \partial u_{j} }{ \partial x_{i} }=\underline{\nabla u}$ the velocity gradient tensor
The local structure of the velocity field is determined by the \underline{\underline{J}}acobian. We can decompose it into [[Symmetric and Anti-Symmetric Matrices|symmetric and antisymmetric]] parts:
$$
\underline{\underline{J}}=\frac{1}{2}\underbrace{ (\underline{\underline{J}}+\underline{\underline{J}}^{\top}) }_{ =E }+\frac{1}{2}\underbrace{ (\underline{\underline{J}}-\underline{\underline{J}}^{\top}) }_{ =\Omega }
$$
Where $\underline{\underline{E}}$ is a symmetric tensor (called the rate of strane tensor), and $\underline{\underline{\Omega}}$ is antisymmetric
## Example
Tke a planar shear flow $\underline{u}(\underline{x},t)=i\begin{pmatrix}y \\ 0\end{pmatrix}$,
$$
\underline{\underline{J}}=\begin{pmatrix}
\frac{ \partial u }{ \partial x }  & \frac{ \partial u }{ \partial y }  \\
\frac{ \partial v }{ \partial x }  & \frac{ \partial v }{ \partial y } 
\end{pmatrix}=\begin{pmatrix}
0 & 1  \\
0 & 0
\end{pmatrix}
$$
Then
$$
\underline{\underline{E}}=\frac{1}{2}(\underline{\underline{J}}+\underline{\underline{J}}^{\top})=\frac{1}{2}\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}
$$
$$
\underline{\underline{\Omega}}=\frac{1}{2}(\underline{\underline{J}}-\underline{\underline{J}}^{\top})=\frac{1}{2}\begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix}
$$
___
Going back to the Taylor expansion, our velocity just away from the reference point $\underline{x}$ and therefore representing the deformation to $D$ is:
$$
\underline{u}(\underline{x}+\delta \underline{x},t)\approx \underline{u}(\underline{x},t)+[\underline{\underline{E}}(\underline{x},t)+\underline{\underline{\Omega}}(\underline{x},t)]\delta \underline{x}
$$
So there are three components:
- bodily translation of the whole $D$ with velocity $\underline{u}(\underline{x},t)$
- stretching or compression of $D$, since $\underline{\underline{E}}$ is a symmetric matrix, the [[Euler's Principle Axis Theorem|principle axes theorem]] says we can diagonalise it