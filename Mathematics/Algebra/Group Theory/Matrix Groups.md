Consider [[Vectorspace Rn|$\mathbb{R}^{n}$]] with [[Dot Product|standard]] [[Inner Product|inner product]]:
$$
(\underline{u},\underline{v})=\underline{v}^{\top}\underline{u}
$$
## Rotations and Reflections
Are a [[Linear Maps|linear transformations]] which are:
- rigid (preserve lengths and angles):
$$
\underline{v}^{\top}\underline{u}=(\underline{u},\underline{v})\to (M\underline{u},M\underline{v})=\underline{v}^{\top}M^{\top}M\underline{u}
$$
- preserve orientation
So if [[Orthogonal Group|$M\in O(n)$]], $\det(M)=\pm 1$. When $\det(M)=1$, $M$ is a "pure" reflection, if $\det(M)=-1$, then $M$ also contains a reflection
### Rotations
Rotations have $\det(M)=1$, so correspond to the [[Special Orthogonal Group|$SO(n)$]]
- $SO(2)$ is [[Abelian Groups|abelian]] and infinite-dimenstional
- $SO(3)$ is non-abelian
We find that [[Cyclic Groups|cyclic groups]] are actually finite subgroups of $SO(2)$. They are the clockwise rotation by $\frac{2\pi}{n}j$ for $j=0,1,\dots,n-1$, so
$$
M_{j}=\begin{pmatrix}
\cos\left( \frac{2\pi}{n}j \right) & \sin\left( \frac{2\pi}{n}j \right)\\ -\sin\left( \frac{2\pi}{n}j \right) & \cos\left( \frac{2\pi}{n}j \right)
\end{pmatrix}
$$
And this is [[Isomorphisms|isomorphic]] to $\mathbb{Z}_{n}$
We hence can also understand the property
$$
M_{j}M_{k}=M_{j+k}
$$
With $j+k$ being modulo $n$
___
### $SO(3)\&SU(2)$
These are of course continuous groups, with some differentiability conditions, these are Lie groups
These are in general more complicated than [[Vectorspaces|vectorspaces]], for example if $M\in SO(n)$, then $2M\not\in SO(n)$
What kind of spaces are they then?
$$
O(3)=\left\{ M\in GL(3,\mathbb{R}):\middle|:M^{\top}M=MM^{\top}=I \right\}
$$
$$
SO(3)=\left\{ M\in O(3):\middle|:\det M=1 \right\}
$$
These are rotation sin $\mathbb{R}^{3}$