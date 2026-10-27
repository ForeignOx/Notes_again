If a fluid has no [[Vorticity|vorticity]] anywhere, then it can be called irrotational. This doesn't mean there is no rotation in the flow, but it turns out to be a special case which is useful, it means:
$$
\underline{\nabla} \times \underline{u} = \underline{0}
$$
When using [[Stream Functions|stream functions]],  means that $\underline{u}$ is a conservative vector field. [[Vector Fields|Conservative vector field]] can be written as the [[Gradient of Scalar Fields|gradient]] of a [[scalar fields|scalar field]], so there exists $\phi(\underline{x},t)$ such that
$$
\underline{u}=\underline{\nabla}\phi
$$
This scalar $\phi$ can encode our velocity and is known as the velocity potential
The difference between this and the stream function is that stream functions are for incompressible fluids and only in 2D, whereas velocity potential is for irrotational fields and works in both 2D and 3D
If $\underline{u}$ is also incompressible, then
$$
\underline{\nabla} \cdot \underline{u} =\underline{\nabla} \cdot (\underline{\nabla} \phi)=\Delta \phi=0 
$$
Which is [[Laplace's Equation|Laplace's equation]], which is very easy (but note only for irrotational and incompressible)
Note that constant $\psi$ lines are streamlines, constant $\phi$ lines are equipotential line
Since Laplace's equation is linear, we can combine 2 valid solutions to get another by the [[Principle of Superposition|principle of superposition]], so we can build more complex flows from elementary ones
___
Note that in 2D, $\underline{u}=(u,v)$ satisfies:
$$
u=\frac{ \partial \phi }{ \partial x } =\frac{ \partial \psi }{ \partial y } ,v=\frac{ \partial \phi }{ \partial y } =-\frac{ \partial \psi }{ \partial x } 
$$
So $\phi$ and $\psi$ satisfy the [[Cauchy-Riemann equations|Cauchy-Riemann equations]], so we can analyse the flow by considering
$$
\omega=\phi+i\psi
$$
