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
Our velocity just away from the reference point $\underline{x}$ and therefore representing the deformation to $D$ is:
$$
\underline{u}(\underline{x}+\delta \underline{x},t)\approx \underline{u}(\underline{x},t)+[\underline{\underline{E}}(\underline{x},t)+\underline{\underline{\Omega}}(\underline{x},t)]\delta \underline{x}
$$
So there are three components:
- bodily translation of the whole $D$ with velocity $\underline{u}(\underline{x},t)$
- stretching or compression of $D$, since $\underline{\underline{E}}$ is a symmetric matrix, the [[Euler's Principle Axis Theorem|principle axes theorem]] says we can diagonalise it, $\underline{\underline{E}}=\underline{\underline{P}}\underline{\underline{D}}\underline{\underline{P}}^{-1}$, wher $\underline{\underline{D}}=\mathrm{diag}(\lambda_{1},\lambda_{2},\lambda_{3})$ contain the [[eigenvalues|eigenvalues]] of $\underline{\underline{E}}$ and additionally $\underline{\underline{P}}$ is formed of the [[Orthogonality|orthogonal]] [[Eigenvectors|eigenvectors]] of $\underline{\underline{E}}$, which means that the effect of $\underline{\underline{E}}$ is just to stretch or compress the element along the eigenvectors. The normalised eigenvectors are called the principle axes, and the eigenvalues are the corresponding principal rates of strain
- Finally we consider the rotation of $D$ given by the vorticity $\underline{\omega}=\underline{\nabla} \times \underline{u}$, which gives $\underline{\underline{\Omega}}$ by:
$$
\underline{\underline{\Omega}}=\frac{1}{2}\begin{pmatrix}
0 & -\omega_{3} & \omega_{2} \\
\omega_{3} & 0 & -\omega_{1} \\
-\omega_{2} & \omega_{1} & 0
\end{pmatrix}
$$
    We can also write $\underline{\underline{\Omega}}\delta \underline{x}=\frac{1}{2}\underline{\omega}\times\delta \underline{x}$ showing that the fluid element is rotating with angular velocity $\frac{1}{2}\underline{\omega}$
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
So how does a fluid particle at $\underline{x}_{0}$ deform? 
- $\underline{u}(\underline{x}_{0},t_{0})=\begin{pmatrix}y_{0} \\ 0\end{pmatrix}$ translates in the $x$-direction with a $y_{0}$ rate,
- $\underline{\underline{E}}(\underline{x}_{0},t)\cdot\delta \underline{x}=\frac{1}{2}\begin{pmatrix}\delta y  \\ \delta x\end{pmatrix}$
- $\underline{\underline{\Omega}}(\underline{x}_{0},t)\cdot\delta \underline{x}=\frac{1}{2}\begin{pmatrix}\delta y \\ -\delta x\end{pmatrix}$
We can plot these:
![[Pasted image 20261020103906.png]]Where does this rotation come from?
Let's find these eigenvalues and eigenvectors:
$$
\det(\underline{\underline{E}}-\lambda \mathbb{1})=0 \implies \left| \begin{pmatrix}
-\lambda &\frac{1}{2} \\
\frac{1}{2} & -\lambda
\end{pmatrix} \right|=0 
$$
$$
\implies \lambda_{1,2}=\pm \frac{1}{2}
$$
So the normalised eigenvectors are:
$$
\underline{v}_{1}=\frac{1}{\sqrt{ 2 }}\begin{pmatrix}
 1 \\
1
\end{pmatrix},\underline{v}_{2}=\frac{1}{\sqrt{ 2 }}\begin{pmatrix}
1 \\
-1
\end{pmatrix}
$$
Which are the principle axes we thought of. Positive eigenvalues stretch, negative eigenvalues compress
The angular velocity, 
$$
\frac{1}{2}\underline{\omega}=\frac{1}{2}\underline{\nabla} \times \underline{u}=-\frac{1}{2} \underline{e}_{z}
$$
The place that the rotation comes from is actually the vorticity, 