## Definition
The gradient of a [[Scalar Fields|scalar field]] $f:\mathbb{R}^{3}\to \mathbb{R}$ is the operator
$$
\underline{\nabla } f|_{x}=\lim_{ d(S) \to 0 }  \frac{1}{\left| V \right| }\oint_{S} f \underline{\hat{n}}\,dS
$$
Where $S$ is a closed surface around $\underline{x}$ with outward normal $\underline{\hat{n}}$, enclosed volume $\left| V \right|$ and diameter $d(S)=\sup\left| \underline{x}-\underline{y} \right|$ for $\underline{x},\underline{y}\in S$
## Notes
- $\underline{\nabla }f$ is a [[Vector Fields|vector field]] $\mathbb{R}^{3}\to \mathbb{R}^{3}$
- $\underline{\nabla }f$ points in the direction of the fastest increase of $f$, and $\left| \underline{\nabla }f \right|$ tells you the maximum rate of increase
- To ensure the limit exists, usually $f$ is [[Continuity|continuously]] [[Differentiation|differentiable]], $C^{1}$, meaning $\frac{ \partial f }{ \partial x },\frac{ \partial f }{ \partial y },\frac{ \partial f }{ \partial z }$ all exist and are continuous
- $\underline{\nabla }f$ extends to scalar fields on any $\mathbb{R}^{n}$, always giving a vector in $\mathbb{R}^{n}$
![[Pasted image 20251021111310.png]]
## Proposition
In cartesian [[Coordinates|coordinates]], 
$$
\underline{\nabla } f=\frac{ \partial f }{ \partial x } \underline{e}_{1}+\frac{ \partial f }{ \partial y } \underline{e}_{2}+\frac{ \partial f }{ \partial z } \underline{e}_{3}
$$
In [[Index Notation|index notation]] this can be written:
$$
[\underline{\nabla } g]_{i}= \frac{ \partial g }{ \partial x_{i} } 
$$
### Proof
We derive the $\underline{e}_{1}$ component, and the others follow by symmetry
Let $S$ be a small cylinder of radius $\varepsilon$, length $h$, with axis $\underline{e}_{1}$. We know the vlume $\left| V \right|=\pi\varepsilon^{2}h$
![[Pasted image 20251021113720.png]]
$$
\underline{e}_{1} \cdot \underline{\nabla } f=\lim_{ d(S) \to 0 } \frac{1}{\left| V \right| }\oint_{S}f\underline{e}_{1} \cdot   \underline{\hat{n}}\, dS
$$
$$
= \lim_{ \varepsilon,h \to 0 } \frac{1}{\pi\varepsilon^{2}h}\left( \int _{S_{1}}f \, dS +\int _{S_{0}} f\cdot(-1) \, dS  \right)
$$
(note there is no contribution on the curved surface as $\underline{e}_{1}\cdot  \underline{\hat{n}}=0$ in that region)
$$
= \lim_{ \varepsilon,h \to 0 } \frac{1}{\pi\varepsilon^{2}h}(\pi\varepsilon^{2}f(\underline{x}_{1})-\pi\varepsilon^{2}f(\underline{x}_{0}))
$$
By the [[Mean Value Theorem#Mean Value Theorem for Double Integrals Double Integrals|mean value therorem]]. Taking limit $\varepsilon\to 0$, we find $\underline{x}_{0}\to \underline{x}$ and $\underline{x}_{1}\to \underline{x}+\underline{h}_{1}$, so
$$
\underline{e}_{1}\cdot \underline{\nabla } f=\lim_{ h \to 0 } \frac{1}{h}(f(\underline{x}+h\underline{e}_{1})-f(\underline{x}))=\frac{ \partial f }{ \partial x }  |_{\underline{x}}
$$
## Proposition
In [[Curvilinear Coordinates|curvilinear]] coordinates $(u,v,w)$, 
$$
\underline{\nabla } f= \frac{1}{h_{u}}\frac{ \partial f }{ \partial u } \underline{e}_{u}+\frac{1}{h_{v} }\frac{ \partial f }{ \partial v }\underline{e}_{v}+\frac{1}{h_{w}}\frac{ \partial f }{ \partial w } \underline{e}_{w}
$$
### Proof
Again we only do one coordinate as the others are identical
$$
\underline{e}_{u}\cdot \underline{\nabla } f=\frac{1}{h_{u}}\left( \frac{ \partial x }{ \partial u }\underline{e}_{1}+\frac{ \partial y }{ \partial u } \underline{e}_{2}+\frac{ \partial z }{ \partial u } \underline{_{3}}  \right)\cdot \left( \frac{ \partial f }{ \partial x }\underline{e}_{1}+\frac{ \partial f }{ \partial y } \underline{e}_{2}+\frac{ \partial f }{ \partial z } \underline{e}_{3}  \right)
$$
$$
= \frac{1}{h_{u}}\left( \frac{ \partial x }{ \partial u } \frac{ \partial f }{ \partial x } +\frac{ \partial y }{ \partial u } \frac{ \partial f }{ \partial y } +\frac{ \partial z }{ \partial f } \frac{ \partial f }{ \partial z }  \right)=\frac{1}{h_{u}}\frac{ \partial f }{ \partial u } 
$$
## Example
Calculate the gradient of $f(\underline{x})=y+x^{2}$
$$
\underline{\nabla } f=2x\underline{e}_{1}+\underline{e}_{2}
$$
___
Compute $\underline{\nabla }z$ in both cartesian and spherical coordinates:
$$
\underline{\nabla } z-\frac{ \partial z }{ \partial x } \underline{e}_{1}+\frac{ \partial z }{ \partial y } \underline{e}_{2}+\frac{ \partial z }{ \partial z } \underline{e}_{3}=\underline{e}_{3}
$$
In spherical: recall $z=r\cos\theta$, so
$$
\underline{\nabla } (r\cos\theta)=\frac{1}{h_{r}}\frac{ \partial  }{ \partial r } (rco\theta)\underline{e}_{r}+\frac{1}{h_{\theta}}\frac{ \partial  }{ \partial \theta } (r\cos\theta)\underline{e}_{\theta}+\frac{1}{h_{\phi}}\frac{ \partial  }{ \partial \phi } (r\cos\theta)\underline{e}_{\phi}
$$
$$
= \cos\theta \underline{e}_{r}-\sin\theta \underline{e}_{\theta}(=\underline{e}_{3})
$$

