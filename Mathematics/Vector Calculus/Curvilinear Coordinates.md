## In $\mathbb{R}^{3}$
A system of curvilinear [[Coordinates|coordinates]] $(u,v,w)$ for $\mathbb{R}^{3}$ has coordinate lines 
$$
\underline{x}(u,v_{0},w_{0}),\underline{x}(u_{0},v,w_{0}),\underline{x}(u_{0},v_{0},w)
$$ 
which are curves with tangent vectors
$$
\frac{ \partial \underline{x} }{ \partial u } ,\frac{ \partial \underline{x} }{ \partial v } ,\frac{ \partial \underline{x} }{ \partial w } 
$$
![[Curvilinear Coordinates 2025-10-09 15.12.14.excalidraw]]
The coordinate system is [[Orthogonality|orthogonal]] if the three tangent [[Vectors|vectors]] are mutually orthogonal everywhere. Then we get an [[Orthonormal Vectors|orthonormal]] [[Basis|Basis]]:
$$
\underline{e}_{u}=\frac{\frac{ \partial \underline{x} }{ \partial u } }{\left| \frac{ \partial \underline{x} }{ \partial u }  \right| },\underline{e}_{v}=\frac{\frac{ \partial \underline{x} }{ \partial v} }{\left| \frac{ \partial \underline{x} }{ \partial v }  \right| },\underline{e}_{w}=\frac{\frac{ \partial \underline{x} }{ \partial w } }{\left| \frac{ \partial \underline{x} }{ \partial w } \right|  }
$$
Where $\left| \frac{ \partial \underline{x} }{ \partial u_{i} } \right|$ are called the scale factors, $h_{u},h_{v},h_{w}$.
Geometrically, the scale factors tell us how much an infinitesimal region in $(u,v,w)$-space is stretched at different points in $\mathbb{R}^{3}$.
## Proposition
If $(u,v)$ are two of a set of orthogonal curvilinear coordinates, then $\left| \frac{ \partial \underline{x} }{ \partial u }\times \frac{ \partial \underline{x} }{ \partial v } \right|=h_{u}h_{v}$
### Proof
Recall that $\frac{ \partial \underline{x} }{ \partial u }=h_{u}\underline{e}_{u}$ and $\frac{ \partial \underline{x} }{ \partial v }=h_{v}\underline{e}_{v}$, so
$$
\left| \frac{ \partial \underline{x} }{ \partial u } \times \frac{ \partial \underline{x} }{ \partial v }  \right| =\left| h_{u}h_{v}\underline{e}_{u}\times \underline{e}_{v} \right| =h_{u}h_{v}\left| \underline{e}_{u}\times \underline{e}_{v} \right| =h_{u}h_{v}
$$
## Examples
FInd the unit basis vectors for plane [[Polar Coordinates|polar coordinates]] $\underline{x}(r,\theta)=r\cos\theta \underline{e}_{1}+r\sin\theta \underline{e}_{2}$.
Differentiate to find coordinate tangent vectors:
$$
\frac{ \partial \underline{x} }{ \partial r } =\cos\theta \underline{e}_{1}+\sin\theta \underline{e}_{2},\frac{ \partial \underline{x} }{ \partial \theta } =-r\sin\theta \underline{e}_{1}+r\cos\theta \underline{e}_{2}
$$
So the scale factors are:
$$
h_{r}=\left| \frac{ \partial \underline{x} }{ \partial r }  \right| =\sqrt{ \cos ^{2}\theta+\sin ^{2}\theta }=1,h_{\theta}=\left| \frac{ \partial \underline{x} }{ \partial \theta }  \right| =\sqrt{ r^{2}\cos ^{2}\theta+r^{2}\sin ^{2}\theta }=r
$$
So the basis vectors are:
$$
\underline{e}_{r}=\frac{1}{h_{r}}\frac{ \partial \underline{x} }{ \partial r }=\cos\theta \underline{e}_{1}+\sin\theta \underline{e}_{2}
$$
$$
 \underline{e}_{\theta}=\frac{1}{h_{\theta}}\frac{ \partial \underline{x} }{ \partial \theta } =-\sin\theta \underline{e}_{1}+\cos\theta \underline{e}_{2}
$$
These are normal to r being constant and $\theta$ being constant respectively
![[Curvilinear Coordinates 2025-10-09 15.28.59.excalidraw]]
### Cylindrical Coordinates
$$
\underline{x}(r,\theta,z)=\underbrace{ r\cos\theta \underline{e}_{1}+r\sin\theta \underline{e}_{2} }_{ \text{usual polar coordinates} }+z\underline{e}_{3}
$$
![[Curvilinear Coordinates 2025-10-09 15.34.35.excalidraw]]
They have scale factors: $h_{r}=1,h_{\theta}=r,h_{z}=1$ and they are orthogonal.
#### Example
Write the [[Vector Fields|vector field]] $\underline{g}(\underline{x})=(y-x)\underline{e}_{1}-(x+y)\underline{e}_{2}$ in the cylindrical basis $\left\{ \underline{e}_{r},\underline{e}_{\theta}, \underline{e}_{z} \right\}$
We find
$$
\underline{e}_{r}=\cos\theta \underline{e}_{1}+\sin\theta \underline{e}_{2}
$$
$$
 \underline{e}_{\theta}=-\sin\theta \underline{e}_{1}+\cos\theta \underline{e}_{2}
$$
$$
 \underline{e}_{z}=\underline{e}_{3}
$$
Which we can solve simultaneously to get
$$
\underline{e}_{1}=\cos\theta \underline{e}_{r}-\sin\theta \underline{e}_{\theta}
$$
$$
 \underline{e}_{2}=\sin\theta \underline{e}_{r}+\cos\theta \underline{e}_{\theta}
$$
$$
 \underline{e}_{3}=\underline{e}_{z}
$$
So
$$
\underline{g}(\underline{x})=(r\sin\theta-r\cos\theta)(\cos\theta \underline{e}_{r}-\sin\theta \underline{e}_{\theta})-(r\cos\theta+r\sin\theta)(\sin\theta \underline{e}_{r}+\cos\theta \underline{e}_{\theta})
$$
$$
= -r(\underline{e}_{r}+\underline{e}_{\theta})
$$
Which is a nice short expression which makes sense because $\underline{g}$ has axial symmetry
### Spherical Coordinates
Here $r>0,\theta \in [0,\pi],\phi \in[0,2\pi]$
$$
\underline{x}(r,\theta,\phi)=r\sin\theta \cos \phi \underline{e}_{1}+r\sin\theta \sin \phi \underline{e}_{2}+r\cos\theta \underline{e}_{3}
$$
![[Curvilinear Coordinates 2025-10-09 15.42.04.excalidraw]]
They have scale factors $h_{r}=1,h_{\theta}=r,h_{\phi}=r\sin\theta$
To derive the parametrisation, we firstly imagine taking a side view of the sphere:
![[Curvilinear Coordinates 2025-10-09 15.44.56.excalidraw]]