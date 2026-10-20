To get a physical picture of fluid motion, it is useful to ask what an arbitrary flow $u(\underline{x},t)$ does to one fluid element. Does it stretch it or spin it or shift it? To answer this, we can compare the velocity at two nearby points $\underline{x}$ and $\underline{x}+\delta \underline{x}$ in the same flulid element $D$:
![[Pasted image 20261020101356.png]]
Expanding about the fixed point $\underline{x}$ using Taylor's theorem gives:
$$
\underline{u}(\underline{x}+\delta \underline{x})=\underline{u}(\underline{x},t)+J\delta(\underline{x})+\mathcal{O}(\left| \delta \underline{x} \right| ^{2})
$$
Where $J$ is the [[Jacobian Transformation|jacobian]]:
$$
J=\nabla_{j}u_{i}=\frac{ \partial u_{i} }{ \partial x_{j} } 
$$
Note that sometimes we denote $J^{\top}=\nabla _{i}u_{j}=\frac{ \partial u_{j} }{ \partial x_{i} }=\underline{\nabla u}$ the velocity gradient tensor
The local structure of the velocity field is determined by the Jacobian. We can decompose it into [[Symmetric and Anti-Symmetric Matrices|symmetric and antisymmetric]] parts:
$$
J=\frac{1}{2}\underbrace{ (J+J^{\top}) }_{ =E }+\frac{1}{2}(J-J^{\top})
$$