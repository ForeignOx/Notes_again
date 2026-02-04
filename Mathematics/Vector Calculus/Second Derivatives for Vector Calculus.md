![[Pasted image 20251106145119.png]]
We already saw that $\underline{\nabla }\times(\underline{\nabla }g)= \underline{0}$ and $\underline{\nabla }\cdot(\underline{\nabla} \times \underline{f})= \underline{0}$, so there are three nontrivial second derivative operators for a scalar field $g:\mathbb{R}^{3}\to \mathbb{R}$ and a vector field $\underline{f}:\mathbb{R}^{3}\to \mathbb{R}^{3}$:
$$
\underline{\nabla } \cdot(\underline{\nabla } g):\mathbb{R}\to \mathbb{R}
$$
$$
\underline{\nabla } (\underline{\nabla} \cdot \underline{f} ):\mathbb{R}^{3}\to \mathbb{R}^{3}
$$
$$
 \underline{\nabla } \times(\underline{\nabla} \times \underline{f} ):\mathbb{R}^{3}\to \mathbb{R}^{3}
$$
## Laplacian
$$
\underline{\nabla } \cdot(\underline{\nabla } g)=\nabla  ^{2}g=\Delta g
$$
### Example
Compute $\Delta g$ for $g(\underline{x})=x^{3}-3xy^{2}$, in cartesians,
$$
\Delta g= \underline{\nabla } \cdot(\underline{\nabla } g)=\frac{ \partial  }{ \partial x_{j} } [\underline{\nabla } g]_{j}=\frac{ \partial  }{ \partial x_{j} } \left( \frac{ \partial g }{ \partial x_{j} }  \right)=\frac{ \partial^{2}g }{ \partial x^{2} } +\frac{ \partial^{2}g }{ \partial y^{2} } +\frac{ \partial^{2}g }{ \partial z^{2} } 
$$
So
$$
\Delta g = \frac{ \partial  }{ \partial x } (3x^{2}-3y^{2})+\frac{ \partial  }{ \partial y } (-6xy)=6x-6x=0
$$
Note that scalar fields satisfying $\Delta g=0$ are called harmonic functions, and $\Delta g=0$ is [[Laplace's Equation|Laplace's equation]] 
### In [[Curvilinear Coordinates|Curvilinear Coordinates]]
In orthogonal curvilinear coordinates $(u,v,w)$, the laplacian is:
$$
\Delta g \frac{1}{h_{u}h_{v}h_{w}}\left( \frac{ \partial  }{ \partial u } \left(  \frac{h_{v}h_{w}}{h_{u}}\frac{ \partial g }{ \partial u }  \right)+\frac{ \partial  }{ \partial v } \left( \frac{h_{u}h_{w}}{h_{v}}\frac{ \partial g }{ \partial v }  \right)+\frac{ \partial  }{ \partial w } \left( \frac{h_{u}h_{v}}{h_{w}}\frac{ \partial g }{ \partial w }  \right) \right)
$$
#### Proof
Recall that
$$
\underline{\nabla } g=\frac{1}{h_{u}}\frac{ \partial g }{ \partial u } \underline{e}_{u}+\frac{1}{h_{v}}\frac{ \partial g }{ \partial v } \underline{e}_{v}+\frac{1}{h_{w}}\frac{ \partial g }{ \partial w } \underline{e}_{w}
$$
And
$$
\underline{\nabla} \cdot \underline{f} =\frac{1}{h_{u}h_{v}h_{w}}\left( \frac{ \partial  }{ \partial u } (h_{v}h_{w}f_{u})+\frac{ \partial  }{ \partial v } (h_{u}h_{w}f_{v})+\frac{ \partial  }{ \partial w } (h_{u}h_{v}f_{w}) \right)
$$
Combining these, we get the required result
## Gradient of Divergence
$\underline{\nabla } (\underline{\nabla} \cdot \underline{f} )$ has the $i$th component:
$$
[\underline{\nabla } (\underline{\nabla} \cdot \underline{f} )]_{i}=\frac{ \partial  }{ \partial x_{i} } \left( \frac{ \partial f_{j} }{ \partial x_{j} }  \right)
$$
## Curl of Curl
$\underline{\nabla }\times(\underline{\nabla} \times \underline{f})$ has $i$th component
$$
[\underline{\nabla } \times (\underline{\nabla} \times \underline{f} )]_{i}=\epsilon_{ijk}\frac{ \partial  }{ \partial x_{j} } [\underline{\nabla} \times \underline{f} ]_{k}
$$
$$
= \epsilon_{ijk}\frac{ \partial  }{ \partial x_{j} } \left( \epsilon_{klm}\frac{ \partial f_{m} }{ \partial x_{l} }  \right)
$$
$$
= \epsilon_{ijk}\epsilon_{klm}\frac{ \partial  }{ \partial x_{j} } \left( \frac{ \partial f_{m}  }{ \partial x_{l} }  \right)
$$
$$
= (\delta_{il}\delta_{jm}-\delta_{im}\delta_{jl})\frac{ \partial  }{ \partial x_{j} } \left( \frac{ \partial f_{m} }{ \partial x_{l} }  \right)
$$
$$
= \delta_{il}\delta_{jm}\frac{ \partial  }{ \partial x_{j} } \left( \frac{ \partial f_{m} }{ \partial x_{l} }  \right)-\delta_{im}\delta_{jl}\frac{ \partial  }{ \partial x_{j} } \left( \frac{ \partial f_{m} }{ \partial x_{l} }  \right)
$$
$$
= \delta_{il}\frac{ \partial  }{ \partial x_{j} } \left( \frac{ \partial f_{j} }{ \partial x_{l} }  \right)-\delta_{jl}\frac{ \partial  }{ \partial x_{j} } \left( \frac{ \partial f_{i} }{ \partial x_{l} }  \right)
$$
$$
= \frac{ \partial  }{ \partial x_{j} } \left( \frac{ \partial f_{j} }{ \partial x_{i} }  \right)-\frac{ \partial  }{ \partial x_{j} } \left( \frac{ \partial f_{i} }{ \partial x_{j} }  \right)
$$
Assuming continuous second derivatives:
$$
=\frac{ \partial  }{ \partial x_{i} } \left( \frac{ \partial f_{j} }{ \partial x_{j} }  \right)-\frac{ \partial^{2}f_{i} }{ \partial x_{j}\partial x_{j} } 
$$
We define the vector laplacian as the vector field with Cartesian components:
$$
[\underline{\nabla } ^{2}\underline{f}]_{i}=\nabla^{2} f_{i} 
$$
Sooo
$$
\underline{\nabla} \times (\underline{\nabla} \times \underline{f} )= \underline{\nabla } (\underline{\nabla} \cdot \underline{f} )-\underline{\nabla } ^{2} \underline{f} 
$$
Warning!
Be careful when calculating the vector laplacian $\underline{\nabla }^{2}\underline{f}$ in non-cartesian component systems, because:
$$
[\underline{\nabla } ^{2}\underline{f}]\cdot \underline{e}_{u}\neq \nabla^{2}f_{u}
$$
To find the correct expression, calculate $\underline{\nabla }^{2}\underline{f}=\underline{\nabla }(\underline{\nabla} \cdot \underline{f})-\underline{\nabla }\times(\underline{\nabla} \times \underline{f})$, which we know how to do in curvilinear coordinates. 
### Example
Verify this formula for the vector field $\underline{f}(\underline{x})=x\underline{e}_{1}+xy\underline{e}_{2}+y^{3}\underline{e}_{3}$
$$
\underline{\nabla} \cdot \underline{f} =\frac{ \partial  }{ \partial x } (x)+\frac{ \partial  }{ \partial y } (xy)+\frac{ \partial  }{ \partial z } (y^{3})=1+x
$$
$$
\implies \underline{\nabla } (\underline{\nabla} \cdot \underline{f} )=\underline{\nabla } (1+x)=\underline{e}_{1}
$$
$$
\underline{\nabla} \times \underline{f} =\det \begin{pmatrix}
\underline{e}_{1} & \underline{e}_{2} & \underline{e}_{3} \\
\frac{ \partial  }{ \partial x }  & \frac{ \partial  }{ \partial y } & \frac{ \partial  }{ \partial z }  \\
x & xy & y^{3}  
\end{pmatrix}=3y^{2}\underline{e}_{1}+y\underline{e}_{3}
$$
$$
\implies \underline{\nabla } \times(\underline{\nabla} \times \underline{f} )=\det \begin{pmatrix}
\underline{e}_{1} & \underline{e}_{2} & \underline{e}_{3} \\
\frac{ \partial  }{ \partial x }  & \frac{ \partial  }{ \partial y }  & \frac{ \partial  }{ \partial z }  \\
3y^{2} & 0 & y
\end{pmatrix}=\underline{e}_{1}-6y\underline{e}_{3}
$$
In cartesians
$$
\underline{\nabla } ^{2} \underline{f}=(\nabla^{2}f_{1})\underline{e}_{1}+(\nabla^{2}f_{2})\underline{e}_{2}+(\nabla^{2}f_{3})\underline{e}_{3}
$$
$$
= 0+0+6y\underline{e}_{3}
$$
So $\underline{\nabla }\times(\underline{\nabla} \times \underline{f})=\underline{\nabla }(\underline{\nabla} \cdot \underline{f})-\underline{\nabla}^{2}\underline{f}$ as required

