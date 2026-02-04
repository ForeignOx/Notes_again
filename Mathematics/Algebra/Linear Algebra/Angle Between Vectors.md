Suppose we have a [[Vectorspaces|vectorspace]] $V$, with real [[Inner Product|inner product]] $(,)$; a real [[Inner Product Spaces|inner product space]], then $\forall \underline{u},\underline{v}\in V$, then by the [[Cauchy-Schwarz Inequality|Cauchy-Schwarz inequality]],
$$
-\lvert \lvert \underline{u} \rvert \rvert \lvert \lvert \underline{v} \rvert \rvert \leq(\underline{u},\underline{v})\leq \lvert \lvert \underline{u} \rvert \rvert \lvert \lvert \underline{v} \rvert \rvert 
$$
Where $\lvert \lvert . \rvert \rvert$ is the induced [[Norms|norm]]
We can say that 
$$
(\underline{u},\underline{v})=\lvert \lvert \underline{u} \rvert \rvert \lvert \lvert \underline{v} \rvert \rvert \cos\theta
$$
With $\theta \in[0,\pi]$, we call $\theta$ the angle between $\underline{u}$ and $\underline{v}$.
Special cases:
- $\theta=0\iff(\underline{u},\underline{v})=\lvert \lvert \underline{u} \rvert \rvert\lvert \lvert \underline{v} \rvert \rvert\iff$ $\underline{u},\underline{v}$ are parallel
- $\theta=\frac{\pi}{2}\iff (\underline{u},\underline{v})=0\iff \underline{u}\bot\underline{v}$ ($\underline{u},\underline{v}$ are [[Orthogonality|orthogonal]])
- $\theta=\pi \iff(\underline{u},\underline{v})=-\lvert \lvert \underline{u} \rvert \rvert\lvert \lvert \underline{v} \rvert \rvert\iff \underline{u},\underline{v}$ are antiparallel
Note we can't define a real angle with a [[Hermitian Inner Product|hermitian inner product]], since $\left< \underline{u},\underline{v} \right>$ might be complex (but orthogonality still makes sense)
## Example
FInd all unit vectors $\underline{w}\in\mathbb{R}^3$ that make an angle of $\frac{\pi}{4}$ with both:
$$
\underline{u}=\begin{pmatrix}
1\\-1\\0
\end{pmatrix},\underline{v}=\begin{pmatrix}
1\\0\\1
\end{pmatrix}
$$
![[Angle Between Vectors 2024-10-10 10.45.34.excalidraw]]
Each vector will have a 'circle' of vectors around them in a cone that are $\frac{\pi}{4}$ around them, so to find the intersection of two sets of vectors, we sort of want to find the intersection of two circles, so we expect to find $\hspace{0pt}1$ vector, $\hspace{0pt}2$ vectors or no vectors (unless both vectors are the same in which case all vectors in the cone satisfy)

Suppose a solution takes the form:
$$
\underline{w}=\begin{pmatrix}
w_{1}\\w_{2}\\w_{3}
\end{pmatrix}
$$
First note:
$$
|\underline{u}|=\sqrt{ 1^{2}+(-1)^{2} }=\sqrt{ 2 },|\underline{v}|=\sqrt{ 1^{2}+1^{2} }=\sqrt{ 2 }
$$
Now
$$
\underline{u}\cdot \underline{w}=|\underline{u}| |\underline{w}|\cos\left( \frac{\pi}{4} \right)=\sqrt{ 2 }\times 1\times \frac{1}{\sqrt{ 2 }}=1
$$
$$
\underline{v}\cdot \underline{w}=|\underline{v}| |\underline{w}|\cos\left( \frac{\pi}{4} \right)=1
$$
So $w_{1}-w_{2}=1$ and $w_{1}+w_{3}=1$, $w_{1}^{2}+w_{2}^{2}+w_{3}^{2}=1$
Hence
$$
w_{1}^{2}+(w_{1}-1)^{2}+(1-w_{1})^{2}=1
$$
Solve for $w_{1}$ (it's a quadratic), then we can get $w_{2}$ and $w_{3}$

#Mathematics #LinAlg 