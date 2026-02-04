There are two standard ways to [[Differentiation|differentiate]] a [[Vector Fields|vector field]] $\underline{f}:\mathbb{R}^{3}\to \mathbb{R}^{3}$ (where we assume that $\underline{f}$ is [[Continuity|continuously]] differentiable, $C^{1}$):
- Divergence
$$
\underline{\nabla } \cdot \underline{f}\mid_{\underline{x}}=\lim_{ d(S) \to 0 } \frac{1}{\left| V \right| }\oint_{S}  \underline{\hat{n}}\cdot \underline{f}\,dS
$$
- Curl
$$
\underline{\nabla } \times \underline{f} \mid_{\underline{x}}=\lim_{ d(S) \to 0 } \frac{1}{\left| V \right| } \oint_{S}   \underline{\hat{n}}\times \underline{f}\,dS
$$
Where $S$ is a closed surface around $\underline{x}$ with outward normal $\underline{\hat{n}}$, enclosed volume $\left| V \right|$ and diameter $d(S)$
Note that the divergence is a [[Scalar Fields|scalar field]] and the curl is a [[Vector Fields|vector field]]
Intuition for divergence is the measure of how much $\underline{f}$ points outward or inward:
![[Pasted image 20251021121331.png]]
Intuition for curl is the measure of how much $\underline{f}$ rotates around each axis:
![[Pasted image 20251021121412.png]]
## Lemma 
If $\underline{a}\in\mathbb{R}^{3}$ is a constant vector and $f:\mathbb{R}^{3}\to \mathbb{R}$ is a $C^{1}$ scalar field, then:
- $\underline{\nabla} \cdot (f \underline{a})=(\underline{\nabla}f )\cdot \underline{a}$
- $\underline{\nabla} \times (f\underline{a})=(\underline{\nabla}f) \times \underline{a}$
### Proof
For the first part:
$$
\underline{\nabla } \cdot(f\underline{a})=\lim_{ d(S) \to 0 } \frac{1}{\left| V \right| }\oint_{S}  \underline{\hat{n}}\cdot (f\underline{a})\,dS=\left( \lim_{ d(S) \to 0 } \frac{1}{\left| V \right| }\oint_{S} \underline{\hat{n}}f\,dS \right)\cdot \underline{a}=(\underline{\nabla } f)\cdot \underline{a}
$$
For the second part:
$$
\underline{\nabla } \times(f\underline{a})=\lim_{ d(S) \to 0 } \frac{1}{\left| V \right| }\oint_{S}  \underline{\hat{n}}\times (f\underline{a})\,dS=\left( \lim_{ d(S) \to 0 } \frac{1}{\left| V \right| }\oint_{S} \underline{\hat{n}}f\,dS \right)\times \underline{a}=(\underline{\nabla } f)\times \underline{a}
$$
## Proposition
In Cartesian [[Coordinates|coordinates]],
$$
\underline{\nabla} \cdot \underline{f}=\frac{ \partial f_{1} }{ \partial x }+\frac{ \partial f_{2} }{ \partial y }+\frac{ \partial f_{3} }{ \partial z }
$$
$$
\underline{\nabla} \times \underline{f}=\det \begin{pmatrix} \underline{e}_{1} & \underline{e}_{2} & \underline{e}_{3} \\
\frac{ \partial  }{ \partial x }  & \frac{ \partial  }{ \partial y }  & \frac{ \partial  }{ \partial z }  \\
f_{1} & f_{2} & f_{3}\end{pmatrix}
$$
$$
= \left( \frac{ \partial f_{3} }{ \partial y } -\frac{ \partial f_{2} }{ \partial z }  \right)\underline{e}_{1}+\left( \frac{ \partial f_{1} }{ \partial z } -\frac{ \partial f_{3} }{ \partial x }  \right)\underline{e}_{2}+\left( \frac{ \partial f_{2} }{ \partial x } -\frac{ \partial f_{1} }{ \partial y }  \right)\underline{e}_{3}
$$
Note that this shows that divergence and curl are really [[Linear Differential Operators|differential operators]], and this justifies the dot and cross notation, if we think of $\underline{\nabla } = \underline{e}_{1}\frac{ \partial  }{ \partial x }+\underline{e}_{2}\frac{ \partial  }{ \partial y }+\underline{e}_{3}\frac{ \partial  }{ \partial z }$ (which is not entirely true! or helpful for curvilinear coordinates)
In [[Index Notation|index notation]]:
$$
\underline{\nabla} \cdot \underline{f} =\frac{ \partial f_{j} }{ \partial x_{j} } 
$$
$$
[\underline{\nabla} \times \underline{f}]_{i} = \epsilon_{ijk} \frac{ \partial f_{k}  }{ \partial x_{j} } 
$$
### Proof
For the divergence:
$$
\underline{\nabla} \cdot \underline{f} =\underline{\nabla } \cdot(f_{1}\underline{e}_{1}+f_{2}\underline{e}_{2}+f_{3}\underline{e}_{3})
$$
$$
= \underline{\nabla } \cdot(f_{1} \underline{e}_{1})+\underline{\nabla } \cdot(f_{2}\underline{e}_{2})+\underline{\nabla } \cdot(f_{3}\underline{e}_{3})
$$
$$
= (\underline{\nabla } f_{1})\cdot \underline{e}_{1}+(\underline{\nabla } f_{2})\cdot \underline{e}_{2}+(\underline{\nabla } f_{3})\cdot \underline{e}_{3}
$$
$$
= \frac{ \partial f_{1} }{ \partial x } +\frac{ \partial f_{2} }{ \partial y } +\frac{ \partial f_{3} }{ \partial z \ } 
$$
For the curl we shall do only one coordinate, and the others follow by symmetry:
$$
\underline{\nabla } \times(f_{1}\underline{e}_{1})=(\underline{\nabla } f_{1})\times \underline{e}_{1}
$$
$$
= \left( \frac{ \partial f_{1} }{ \partial x } \underline{e}_{1}+\frac{ \partial f_{1} }{ \partial y } \underline{e}_{2}+\frac{ \partial f_{1} }{ \partial z } \underline{e}_{3} \right)\times \underline{e}_{1}
$$
$$
= \frac{ \partial f_{1} }{ \partial x } \underline{e}_{1}\times \underline{e}_{1}+\frac{ \partial f_{1} }{ \partial y } \underline{e}_{2}\times \underline{e}_{1}+\frac{ \partial f_{1} }{ \partial z } \underline{e}_{3}\times \underline{e}_{1}=-\frac{ \partial f_{1} }{ \partial y } \underline{e}_{3}+\frac{ \partial f_{1} }{ \partial z } \underline{e}_{2}
$$
## Corollary
If $f:\mathbb{R}^{3}\to \mathbb{R}$ is a scalar field and $\underline{f}:\mathbb{R}^{3}\to \mathbb{R}^{3}$ is a vector field, both with continuous second partial derivatives, then
- $\underline{\nabla }\cdot(\underline{\nabla} \times \underline{f})=0$
- $\underline{\nabla }\times(\underline{\nabla }f)= \underline{0}$
### Proof
For the first part:
$$
\underline{\nabla } \cdot(\underline{\nabla} \times \underline{f} )=\frac{ \partial  }{ \partial x } \left( \frac{ \partial f_{3} }{ \partial y } -\frac{ \partial f_{2} }{ \partial z }  \right)+\frac{ \partial  }{ \partial y }\left( \frac{ \partial f_{1} }{ \partial z } -\frac{ \partial f_{3} }{ \partial x }  \right)+\frac{ \partial  }{ \partial z } \left( \frac{ \partial f_{2} }{ \partial x } -\frac{ \partial f_{1} }{ \partial y }  \right)
$$
$$
= \frac{ \partial^{2} f_{3} }{ \partial x \partial y }-\frac{ \partial^{2}f_{2} }{ \partial x \partial z }+\frac{ \partial^{2}f_{1} }{ \partial y\partial z }-\frac{ \partial^{2}f_{3} }{ \partial y\partial x }+\frac{ \partial^{2}f_{2} }{ \partial z\partial x }-\frac{ \partial^{2}f_{1} }{ \partial z\partial y }=0       
$$
Which is assuming that partials commute by continuity ([[Clairaut's Theorem|Clairaut's theorem]]) 
For the second part:
$$
\underline{\nabla } \times(\underline{\nabla } f)=\left( \frac{ \partial^{2}f }{ \partial y\partial z }-\frac{ \partial^{2}f }{ \partial z\partial y }   \right)\underline{e}_{1}+\left( \frac{ \partial^{2}f }{ \partial z\partial x }-\frac{ \partial^{2}f }{ \partial z\partial x }   \right)\underline{e}_{2}+\left( \frac{ \partial^{2}f }{ \partial x\partial y }-\frac{ \partial^{2}f }{ \partial y\partial x }   \right)\underline{e}_{3}= \underline{0}
$$
Again by Clairaut's theorem
___
Using index notation
$$
\underline{\nabla } \cdot(\underline{\nabla} \times \underline{f} )= \frac{ \partial  }{ \partial x_{j} } [\underline{\nabla} \times \underline{f} ]_{j}
$$
$$
= \frac{ \partial  }{ \partial x_{j} } \left( \epsilon_{jkl}\frac{ \partial f_{l} }{ \partial x_{k} }  \right)
$$
$$
= \epsilon_{jkl}  \frac{ \partial  }{ \partial x_{k} } \left( \frac{ \partial f_{l} }{ \partial x_{j} }  \right)
$$
Assuming second derivatives are all continuous, relableling $j\leftrightarrow j$:
$$
\epsilon_{kjl}\frac{ \partial  }{ \partial x_{j} } \left( \frac{ \partial f_{l} }{ \partial x_{k} }  \right)
$$
$$
= -\epsilon_{jkl} \frac{ \partial  }{ \partial x_{j} } \left( \frac{ \partial f_{l} }{ \partial x_{k} }  \right)=-\frac{ \partial  }{ \partial x_{j} } \left( \epsilon_{jkl}\frac{ \partial f_{l} }{ \partial x_{k} }  \right)
$$
Since this expression equals the negative of itself, it must be zero

## Example
Compute the divergence and curl of the vector field $\underline{f}(\underline{x})=-\underline{x}$ and $\underline{g}(\underline{x})=(y-x)\underline{e}_{1}-(x+y)\underline{e}_{2}$
Using the proposition:
$$
\underline{\nabla} \cdot \underline{f} =\frac{ \partial }{ \partial x } (-x)+\frac{ \partial  }{ \partial y } (-y)+\frac{ \partial  }{ \partial z } (-z)=-3
$$
$$
 \underline{\nabla} \cdot \underline{g} =\frac{ \partial  }{ \partial x } (y-x)+\frac{ \partial  }{ \partial y } (-x-y)+\frac{ \partial  }{ \partial z } (0)=-2
$$
Both of which are negative, so we know both are inward pointing
$$
\underline{\nabla} \times \underline{f} =\left( \frac{ \partial  }{ \partial y } (-z)-\frac{ \partial  }{ \partial z } (-y) \right)\underline{e}_{1}+\left( \frac{ \partial  }{ \partial z } (-x)-\frac{ \partial  }{ \partial x } (-z) \right)\underline{e}_{2}+\left( \frac{ \partial  }{ \partial x } (-y)-\frac{ \partial  }{ \partial y } (-x) \right)\underline{e}_{3}
$$
$$
= \underline{0}
$$
Which makes sense as there is no spinny
$$
\underline{\nabla} \times \underline{g} =\left( \frac{ \partial  }{ \partial y } (0)-\frac{ \partial  }{ \partial z } (-x-y) \right)\underline{e}_{1}+\left( \frac{ \partial  }{ \partial z } (y-x)-\frac{ \partial  }{ \partial x } (0) \right)\underline{e}_{2}+\left( \frac{ \partial  }{ \partial x } (-x-y)-\frac{ \partial  }{ \partial y } (y-x) \right)\underline{e}_{3}
$$
$$
= -2\underline{e}_{3}
$$
Which tells us we have a clockwise rotation around the $\underline{e}_{3}$ axis
Note that if we have a vector field that is 2D, then it never has components of curl in those dimensions
In general, for nonlinear vector fields, the divergence and curl will not be constant in space
## In [[Curvilinear Coordinates|Curvilinear Coordinates]]
Recall, if we have curvilinear coordinates $(u,v,w),\underline{e}_{u}=\frac{1}{h_{u}}\frac{ \partial \underline{x} }{ \partial u }$ with $h_{u}=\left| \frac{ \partial \underline{x} }{ \partial u } \right|$, they are orthogonal if $\underline{e}_{u}\cdot \underline{e}_{v}=\underline{e}_{u}\cdot \underline{e}_{w}=\underline{e}_{v}\cdot \underline{e}_{w}=0$
In orthogonal curvilinear coordinates $(u,v,w)$, we have the following:
$$
\underline{\nabla} \cdot \underline{f}=\frac{1}{h_{u}h_{v}h_{w}}\left( \frac{ \partial  }{ \partial u }(h_{v}h_{w}f_{u})+\frac{ \partial  }{ \partial v } (h_{u}h_{w}f_{v})+\frac{ \partial  }{ \partial w } (h_{u}h_{v}f_{w}) \right)
$$
$$
\underline{\nabla} \times \underline{f} =\frac{1}{h_{u}h_{v}h_{w}}\det \begin{pmatrix}
h_{u}\underline{e}_{u} & h_{v}\underline{e}_{v} & h_{w}\underline{e}_{w} \\
\frac{ \partial  }{ \partial u }  & \frac{ \partial  }{ \partial v }  & \frac{ \partial  }{ \partial w }  \\
h_{u}f_{u} & h_{v}f_{v} & h_{w}f_{w}
\end{pmatrix}
$$
Warning - one might be tempted to think
$$
\underline{\nabla} \cdot \underline{f} =\frac{1}{h_{u}}\frac{ \partial f_{u} }{ \partial u } +\frac{1}{h_{v}}\frac{ \partial f_{v} }{ \partial v } +\frac{1}{h_{w}}\frac{ \partial f_{w} }{ \partial w } 
$$
But this is not true and doesn't work because $\underline{e}_{u},\underline{e}_{v},\underline{e}_{w}$ are not constant vectors (a their direction varies)
### Proof
Recall from [[Gradient of Scalar Fields|gradient]] with curvilinear coordinates that
$$
\underline{\nabla } f=\frac{1}{h_{u}}\frac{ \partial f }{ \partial u } +\frac{1}{h_{v}}\frac{ \partial f }{ \partial v } +\frac{1}{h_{w}}\frac{ \partial f }{ \partial w } 
$$
$$
\implies \underline{\nabla } u=\frac{1}{h_{u}}\frac{ \partial u }{ \partial u } \underline{e}_{u}+\frac{1}{h_{v}}\frac{ \partial u }{ \partial v } \underline{e}_{v}+\frac{1}{h_{w}}\frac{ \partial u }{ \partial w } \underline{e}_{w}=\frac{1}{h_{u}}
$$
$$
\implies \underline{e}_{u}=h_{u}\underline{\nabla } u
$$
So for the first part, consider the first component:
$$
\underline{\nabla } \cdot(f_{u}\underline{e}_{u})=\underline{\nabla }\cdot(f_{u}\underline{e}_{v}\times \underline{e}_{w})
$$
$$
= \underline{\nabla }\cdot(f_{u}(h_{v}\underline{\nabla } v)\times(h_{w}\underline{\nabla } w))
$$
$$
= \underline{\nabla }\cdot(f_{u}h_{v}h_{w}(\underline{\nabla } v)\times(\underline{\nabla } w))
$$
$$
= \underline{\nabla } (f_{u}h_{v}h_{w})\cdot((\underline{\nabla } v)\times(\underline{\nabla } w))+\underbrace{ f_{u}h_{v}h_{w}\underline{\nabla }\cdot(\underline{\nabla } v\times \underline{\nabla } w) }_{ =\underline{\nabla }\cdot(\underline{\nabla } \times(v\underline{\nabla } w))=0 }
$$
$$
= \underline{\nabla } (f_{u}h_{v}h_{w})\cdot \frac{\underline{e}_{v}\times \underline{e}_{w}}{h_{v}h_{w}}
$$
$$
= \frac{1}{h_{v}h_{w}}\underline{e}_{u}\cdot \underline{\nabla } (f_{u}h_{v}h_{w})=\frac{1}{h_{u}h_{v}h_{w}}\frac{ \partial  }{ \partial u } (f_{u}h_{v}h_{w})
$$
And other components are analogous
For the second part, consideer again the first component:
$$
\underline{\nabla} \times (f_{u}\underline{e}_{u})=\underline{\nabla } \times(f_{u}h_{u}\underline{\nabla } u)
$$
$$
= f_{u}h_{u}\underbrace{ \underline{\nabla } \times(\underline{\nabla } u)  }_{ =0 }+\underline{\nabla } (f_{u}h_{u})\times(\underline{\nabla } u)
$$
$$
= \underline{\nabla } (f_{u}h_{u})\times\left( \frac{1}{h_{u}}\underline{e}_{u} \right)
$$
$$
= \frac{1}{h_{u}} \underline{\nabla } (f_{u}h_{u})\times(\underline{e}_{v}\times \underline{e}_{w})
$$
Which is a vector triple product !! which we can use the bac of the cab identity:
$$
\underline{a}\times(\underline{b}\times \underline{c})=\underline{b}(\underline{a}\cdot \underline{c})-\underline{c}(\underline{a}\cdot \underline{b})
$$
$$
= \frac{1}{h_{u}}\underline{e}_{v}(\underline{e}_{w}\cdot \underline{\nabla } (f_{u}h_{u}))-\frac{1}{h_{u}}\underline{e}_{w}(\underline{e}_{v}\cdot \underline{\nabla } (f_{u}h_{u}))
$$
$$
= \frac{1}{h_{u}h_{w}}\frac{ \partial  }{ \partial w } (f_{u}h_{u})\underline{e}_{v}-\frac{1}{h_{u}h_{v}}\frac{ \partial  }{ \partial v } (f_{u}h_{u})\underline{e}_{w}
$$
Which matches what we would get if we expanded the determinant

### Example
Calculate $\underline{\nabla} \times \underline{f}$ for $\underline{f}(\underline{x})=r\sin\theta \underline{e}_{\phi}$ in spherical coordinates:
$$
\underline{\nabla} \times \underline{f} =\frac{1}{h_{r}h_{\theta}h_{\phi}}\det \begin{pmatrix}
h_{r}\underline{e}_{r} & h_{\theta}\underline{e}_{\theta} & h_{\phi}\underline{e}_{\phi} \\
\frac{ \partial  }{ \partial r }  & \frac{ \partial  }{ \partial \theta }  & \frac{ \partial  }{ \partial \phi }  \\
0 & 0 & h_{\phi}f_{\phi}
\end{pmatrix}
$$
$$
= \frac{1}{r^{2}\sin\theta}\det \begin{pmatrix}
\underline{e}_{r} & r \underline{e}_{\theta} & r\sin\theta \underline{e}_{\phi} \\
\frac{ \partial  }{ \partial r }  & \frac{ \partial  }{ \partial \theta }  & \frac{ \partial  }{ \partial \phi }  \\
0 & 0 & r^{2}\sin ^{2}\theta
\end{pmatrix}
$$
$$
= \frac{1}{r^{2}\sin\theta}\frac{ \partial  }{ \partial \theta } (r^{2}\sin ^{2}\theta)\underline{e}_{r}-\frac{r}{r^{2}\sin\theta}\frac{ \partial  }{ \partial r } (r^{2}\sin\theta)\underline{e}_{\theta}
$$
$$
= 2\cos\theta \underline{e}_{r}-2\sin\theta \underline{e}_{\theta}
$$
Alternatively, you could convert $\underline{f}$ to cartesian components first:
$$
\underline{f}(\underline{x})=r\sin\theta \underline{e}_{\phi}=r\sin\theta(-\sin \phi \underline{e}_{1}+\cos \phi \underline{e}_{2})=-y\underline{e}_{1}+x\underline{e}_{2}
$$
Then
$$
\underline{\nabla} \times \underline{f}=\det \begin{pmatrix}
\underline{e}_{1} & \underline{e}_{2} & \underline{e}_{3} \\
\frac{ \partial  }{ \partial x }  & \frac{ \partial  }{ \partial y }  & \frac{ \partial  }{ \partial z }  \\
-y & x & 0 
\end{pmatrix} 
$$
$$
= \left( \frac{ \partial x }{ \partial x } +\frac{ \partial y }{ \partial y }  \right)\underline{e}_{3}=2\underline{e}_{3}=2(\cos\theta \underline{e}_{r}-\sin\theta \underline{e}_{\theta})
$$
### Alternate Definition for Curl
Let $C$ be a planar curve in a plane with unit normal $\underline{\hat{n}}$, with diameter $d(C)$, enclosed area $\left| A\right|$ and containing the point $\underline{x}$
![[Pasted image 20251030151112.png]]
For any vector field $\underline{f}:\mathbb{R}^{3}\to \mathbb{R}^{3}$,
$$
\underline{\hat{n}}\cdot(\underline{\nabla} \times \underline{f} )|_{\underline{x}} = \lim_{ d(C) \to 0 } \frac{1}{\left| A \right| } \oint_{C}  \underline{f}\cdot  \underline{\hat{t}}\,d \ell
$$
Where $C$ is oriented with $\underline{\hat{t}}=\underline{\hat{n}}\times  \underline{\hat{n}}_{C}$, where $\underline{\hat{n}}_{C}$ is the outward normal to the curve
I.e. projecting $\underline{\nabla} \times \underline{f}$ in some fixed direction $\underline{\hat{n}}$ gives "circulation per unit area" around that axis. Some authors take this to be the definition of the curl
#### Proof
Extrude $C$ by a small distance $h$ in the $\underline{\hat{n}}$ direction to form a thin "pill" surface $S$, with normal $\underline{\hat{n}}_{S}$
![[Pasted image 20251030151714.png]]
By the definition of curl, 
$$
\underline{\hat{n}}\cdot  (\underline{\nabla} \times \underline{f} )|_{\underline{x}}= \underline{\hat{n}}\cdot\left( \lim_{ d(S) \to 0 } \frac{1}{\left| V \right| }\oint_{S} \underline{\hat{n}}_{S}\times \underline{f}\, dS \right)
$$
$$
= \lim_{ d(S) \to 0 } \frac{1}{\left| V \right| }\oint_{S}\underline{\hat{n}}\cdot (\underline{\hat{n}}_{S}\times \underline{f})\,dS 
$$
$$
= \lim_{ d(S) \to 0 }  \frac{1}{\left| A \right| h} \oint_{S} \underline{f}\cdot (\underline{\hat{n}}\times  \underline{\hat{n}}_{S})\,dS
$$
And $\underline{\hat{n}}\times  \underline{\hat{n}}_{S}$ vanishes at the top and the bottom since $\underline{\hat{n}}_{S}=\pm  \underline{\hat{n}}$
$$
 = \lim_{ \left| A \right| ,h \to 0 } \frac{1}{\left| A \right| h}\int _{\tilde{S}} \underline{f}\cdot (\underline{\hat{n}}\times  \underline{\hat{n}}_{C}) \, dS
$$
We can parametrise $\tilde{S}$ by $\underline{\tilde{x}}(t,v)=\underline{x}_{C}(t)+v  \underline{\hat{n}}$ for $v\in[0,h]$, $t\in [t_{0},t_{1}]$ and $\underline{x}_{C}$ is the parametrisation of $C$
$$
\implies \left|  \frac{ \partial  \underline{\tilde{x}} }{ \partial t } \times \frac{ \partial  \underline{\tilde{x}} }{ \partial r }  \right|=\left| \frac{d \underline{x}_{C}}{dt} \times  \underline{\hat{n}} \right| =\left| \frac{d \underline{x}_{C}}{dt}  \right| \left|   \underline{\hat{n}} \right| =\left| \frac{d \underline{x}_{C}}{dt}  \right|  
$$
Sooo
$$
\int _{\tilde{S}} \underline{f}\cdot(\underline{\hat{n}}\times  \underline{\hat{n}}_{C}) \, dS = \int_{t_{0}}^{t_{1}}\int_{0}^{h}   \underline{f}\cdot\underbrace{ (  \underline{\hat{n}}\times  \underline{\hat{n}}_{C})\left| \frac{d \underline{x}_{C}}{dt}  \right|  }_{ \text{independent of }v } \, dv\,dt  
$$
$$
    = \int_{t_{0}}^{t_{1}} (\underline{\hat{n}}\times  \underline{\hat{n}}_{C})\cdot\left( \int_{0}^{h} \underline{f} \, dv  \right)\left| \frac{d \underline{x}_{C}}{dt}  \right|  \, dt 
$$
And by the [[Mean Value Theorem#Mean Value Theorem for Integration Integration|mean value theorem for integrals]], $\int_{0}^{h} \underline{f} \, dv= h\underline{f}(t,v_{*}(t))$ for some $v_{*}(t)\in[0,h]$
$$
=h\int_{t_{0}}^{t_{1}} (\underline{\hat{n}}\times  \underline{\hat{n}}_{C})\cdot \underline{f}(t,v_{*}(t))\left| \frac{d \underline{x}_{C}}{dt}  \right|  \, dt
$$
In the limit $h\to 0$, we have that $v_{*}(t)=0$ for all $t$ by the [[Squeeze Theorem|squeeze thoerem]], so
$$
\underline{\hat{n}}\cdot(\underline{\nabla} \times \underline{f} )|_{\underline{x}} = \lim_{ \left| A \right|  \to 0 }  \frac{1}{\left| A \right| }\int_{t_{0}}^{t_{1}} \underbrace{ (\underline{\hat{n}}\times  \underline{\hat{n}}_{C}) }_{ =\underline{\hat{t}} }\cdot \underline{f}(t,0)\left| \frac{d \underline{x}_{C}}{dt}  \right|  \, dt 
$$
$$
= \lim_{ \left| A \right|  \to 0 }  \frac{1}{\left| A \right| } \oint_{C} \underline{f}\cdot  \underline{\hat{t}}\, d \ell
$$