The vector product also known as the cross product is particular to $\mathbb{R}^3$ is an operation:
$$
\mathbb{R}^3\times \mathbb{R}^3\to \mathbb{R}^3
$$
$$
(\underline{u},\underline{v})\mapsto \underline{u}\times \underline{v}
$$
## Definition
$$
\underline{x}\times \underline{y}=\begin{pmatrix}
x_{1}\\x_{2}\\x_{3}
\end{pmatrix}\times \begin{pmatrix}
y_{1}\\y_{2}\\y_{3}
\end{pmatrix}:=\begin{pmatrix}
x_{2}y_{3}-x_{3}y_{2}\\x_{3}y_{1}-x_{1}y_{3}\\x_{1}y_{2}-x_{2}y_{1}
\end{pmatrix}
$$
## Properties
- Anti-symmetry
$$
\underline{u}\times \underline{v}=-(\underline{v}\times \underline{u}),\forall \underline{u},\underline{v}\in\mathbb{R}^3
$$
- Linearity 1
$$
(\underline{u}+\underline{v})\times \underline{w}=\underline{u}\times \underline{w}+\underline{v}\times \underline{w}
$$
$$
(\lambda \underline{u})\times \underline{v}=\lambda(\underline{u}\times \underline{v})\,\,\forall\lambda \in \mathbb{R},\underline{u},\underline{v},\underline{w}\in \mathbb{R}^3
$$
- Linearity 2
$$
\underline{u}\times(\underline{v}+\underline{w})=\underline{u}\times \underline{v}+\underline{u}\times \underline{w}
$$
$$
\underline{u}\times(\lambda \underline{v})=\lambda(\underline{u}\times \underline{v})\,\,\forall\lambda \in \mathbb{R},\underline{u},\underline{v},\underline{w}\in \mathbb{R}^3
$$
- Orthogonality to the input, in other words $\underline{u}\times \underline{v}$ is orthogonal to $\underline{u}$ and $\underline{v}$
$$
\underline{u}\cdot(\underline{u}\times \underline{v})=0=\underline{v}\cdot(\underline{u}\times \underline{v}),\,\forall \underline{u},\underline{v}\in \mathbb{R}^3
$$
## Lemma
Suppose that $\underline{x},\underline{y}\in\mathbb{R}^3$ are [[Vectors|vectors]] of [[Magnitude of a Vector|length]] $|\underline{x}|=r>0,|y|=s>0$, then
$$
|\underline{x}\times \underline{y}|=rs\sin\theta
$$
Where $0\leq\theta \leq \pi$ is the [[Angle Between Vectors|angle]] between $\underline{x}$ and $\underline{y}$
### Proof
$$
|\underline{x}\times \underline{y}|^{2}=(\underline{x}\times \underline{y})\cdot(\underline{x}\cdot \underline{y})
$$
$$
= (x_{2}y_{3}-x_{3}y_{2})^{2}+(x_{3}y_{1}-xy_{3})^{2}+(x_{1}y_{2}-x_{2}y_{1})^{2}
$$
$$
= (x_{1}^{2}+x_{2}^{2}+x_{3}^{2})(y_{1}^{2}+y_{2}^{2}+y_{3}^{2})-(x_{1}y_{1}+x_{2}y_{2}+x_{3}y_{3})^{2}
$$
This equals sign is important as the first term shows every combination of $x_{i}^{2}$ with $y_{i}^{2}$ and then subtracts all the terms where $x_{1}$ matches with $y_{1}$ ect. This can be shown rigorously by expanding it out properly
$$
= r^{2}s^{2}-(\underline{x}\cdot \underline{y})^{2}=r^{2}s^{2}-r^{2}s^{2}\cos ^{2}\theta=r^{2}s^{2}(1-\cos ^{2}\theta)
$$
$$
= r^{2}s^{2}\sin ^{2}\theta
$$
$$
\therefore |\underline{x}\times \underline{y}|=rs\sin\theta
$$
As we must take the positive square root

#Mathematics #LinAlg #Definition