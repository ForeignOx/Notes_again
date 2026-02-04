We define the scalar or dot product:
$$
\mathbb{R}^n\times \mathbb{R}^n\to \mathbb{R}
$$
$$
(\underline{u},\underline{v})\mapsto \underline{u}\cdot \underline{v}
$$
$$
\underline{u}\cdot \underline{v}=\begin{pmatrix}
u_{1}\\u_{2}\\\vdots\\v_{n}
\end{pmatrix}\cdot \begin{pmatrix}
v_{1}\\v_{2}\\\vdots\\v_{n}
\end{pmatrix}=u_{1}v_{1}+u_{2}v_{2}+\dots+u_{n}v_{n}=\sum_{ i=1} ^{ n}  u_{i}v_{i} \in \mathbb{R}
$$
## Properties of the dot product
- Symmetry: 
$$
\underline{u}\cdot \underline{v}=\underline{v}\cdot \underline{u},\forall \underline{u},\underline{v}\in\mathbb{R}^n
$$
- Linearity 1:
$$
(\underline{u}+\underline{v})\cdot \underline{w}=\underline{u}\cdot \underline{w}+\underline{v}\cdot \underline{w}
$$
$$
(\lambda \underline{u})\cdot \underline{w}=\lambda(\underline{u}\cdot \underline{w}),\,\forall\lambda \in \mathbb{R},\underline{u},\underline{v},\underline{w}\in \mathbb{R}^n
$$
- Linearity 2
$$
\underline{u}\cdot(\underline{v}+\underline{w})=\underline{u}\cdot \underline{v}+\underline{u}\cdot \underline{w}
$$
$$
\underline{u}\cdot(\lambda \underline{w})=\lambda(\underline{u}\cdot \underline{w}),\,\forall\lambda \in \mathbb{R},\underline{u},\underline{v},\underline{w}\in \mathbb{R}^n
$$
- Positivity
$$
\underline{v}\cdot \underline{v}\geq 0\,\forall \underline{v}\in \mathbb{R}^n
$$
$$
\underline{v}\cdot \underline{v}=\underline{0}\iff \underline{v}=\underline{0}
$$
## Consider $\mathbb{R}^2$
Suppose $\underline{v},\underline{w}\in\mathbb{R}^2$, where $|\underline{v}|=r$, $|\underline{w}|=s$, suppose that $\underline{v},\underline{w}$ make an angle of $\alpha$ with each other where $0\leq\alpha \leq \pi$
![[Polar Coordinates 2024-10-10 10.12.27.excalidraw]]
Then using the [[Dot Product|dot product]], we want to show $\underline{v}\cdot \underline{w}=rs\cos\alpha$
### Proof
Suppose polar coordinates of $\underline{v}$ are $(r,\theta)$ and of $\underline{w}$ are $(s,\phi)$, then
$$
\underline{v}=\begin{pmatrix}
r\cos\theta\\r\sin\theta
\end{pmatrix}
$$
$$
\underline{w}=\begin{pmatrix}
s\cos \phi\\s\sin \phi
\end{pmatrix}
$$
$$
\implies \underline{v}\cdot \underline{w}=\begin{pmatrix}
r\cos\theta\\r\sin\theta
\end{pmatrix}\cdot
\begin{pmatrix}
s\cos \phi\\s\sin \phi
\end{pmatrix}=rs\cos\theta \cos \phi+rs\sin\theta \sin \phi=rs(\cos\theta \cos \phi+\sin\theta \sin \phi)
$$
$$
= rs\cos(\theta-\phi)=rs\cos(\pm\alpha)=rs\cos\alpha
$$
as $\cos$ is an [[Even Functions|even function]]
### Corollary
If $\underline{v}\neq 0$ and $\underline{w}\neq 0$, $\underline{v}$ and $\underline{w}$ are orthogonal iff $\underline{v}\cdot \underline{w}=0$
#### Proof
$$
\underline{v}\cdot \underline{w}=0\iff \cos\alpha=0\iff\alpha=\frac{\pi}{2}
$$





#Mathematics #LinAlg #Definition