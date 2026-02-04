## Numbers
If $x,y\in \mathbb{R}$ then $\left| x+y \right|\leq \left| x \right|+\left| y \right|$
### Proof
Given $x,y\in\mathbb{R}$, then $xy=0$ or $xy>0$ or $xy<0$
If $xy=0$ then either $x=0$ or $y=0$
    If $x=0$, $\left| x+y \right|=\left| y \right|=\left| x \right|+\left| y \right|$
    Similarly, if $y=0$, by symmetry, $\left| x+y \right|=\left| x \right|+\left| y \right|$
If $xy>0$ either $x>0$, $y>0$ or $x<0$, $y<0$
    If $x>0$, $y>0$ then $x+y>0$, so $\left| x+y \right|=x+y=\left| x \right|+\left| y \right|$
    If $x<0$, $y<0$ then $x+y<0$ so $\left| x+y \right|=-(x+y)=-x+-y=\left| x \right|+\left| y \right|$
If $xy<0$, either $x>0$,$y<0$ or $x<0$, $y>0$
    Without loss of generalisation, $x>0$, $y<0$
        If $\left| x \right|>\left| y \right|$ then $x+y>0$ so $\left| x+y \right|=\left| x \right|-\left| y \right|<\left| x \right|<\left| x \right|+\left| y \right|$
        If $\left| x \right|<\left| y \right|$, then $\left| x+y \right|=\left| y \right|-\left| x \right|<\left| y \right|<\left| x \right|+\left| y \right|$
        If $\left| x \right|=\left| y \right|$, then $\left| x+y \right|=0=\left| x \right|+\left| y \right|$
### Alternate Version
We can also say:
$$
||a|-|b| |\leq|a-b|
$$
#### Proof
$$
|a|=|a-b+b|\leq|a-b|+|b|
$$
$$
\implies |a|-|b|\leq|a-b|
$$
$$
|b-a+a|\leq |b-a| +| a|=|a-b|+|a|
$$
$$
\implies |b|-|a|\leq|a-b|
$$
$$
\implies -|a-b|\leq|a|-|b|
$$
$$
\therefore | |a|-|b| |\leq|a-b|
$$
## [[Vectors|Vectors]] in $\mathbb{R}^n$
The triangle inequality is as follows:
$$
|\underline{u}+\underline{v}|\leq|\underline{u}|+|\underline{v}|
$$
Intuitively it can be thought of by considering the triangle formed with side lengths $|\underline{u}|,|\underline{v}|,|\underline{u}+\underline{v}|$:
![[Triangle Inequality 2024-10-15 22.09.42.excalidraw]]
We can see that clearly one side can't be greater than the sum of the lengths of the other two sides, and that equality holds when $\underline{v}$ and $\underline{u}$ are parallel
### Proof
Let $\underline{u},\underline{v}\in\mathbb{R}^n$, let:
$$
\underline{u}=\begin{pmatrix}
u_{1}\\u_{2}\\\vdots\\u_{n}
\end{pmatrix},\underline{v}=\begin{pmatrix}
v_{1}\\v_{2}\\\vdots\\v_{n}
\end{pmatrix}
$$
We can now express the [[Dot Product|dot product]] in terms of $|\underline{u}|,|\underline{v}|,|\underline{u}+\underline{v}|$ by first noting:
$$
\underline{u}\cdot \underline{v}=u_{1}v_{1}+u_{2}v_{2}+\dots+u_{n}v_{n}
$$
$$
|\underline{u}|^{2}=u_{1}^{2}+u_{2}^{2}+\dots+u_{n}s^{2}
$$
$$
|\underline{v}|^{2}=v_{1}^{2}+v_{2}^{2}+\dots+v_{n}^{2}
$$
So:
$$
|\underline{u}+\underline{v}|^{2}=(u_{1}+v_{1})^{2}+(u_{2}+v_{2})^{2}+\dots+(u_{n}+v_{n})^{2}
$$
$$
= u_{1}^{2}+2u_{1}v_{1}+v_{1}^{2}+u_{2}^{2}+2u_{2}v_{2}+v_{2}^{2}+\dots+u_{n}^{2}+2u_{n}v_{n}+v_{n}^{2}=|\underline{u}|^{2}+|\underline{v}|^{2}+2(\underline{u}\cdot \underline{v})
$$
$$
\implies \underline{u}\cdot \underline{v}=\frac{|\underline{u}+\underline{v}|^{2}-|\underline{u}|^{2}-|\underline{v}|^{2}}{2}
$$
Using the [[Cauchy-Schwarz Inequality|Cauchy-Schwarz inequality]] we have:
$$
\underline{u}\cdot \underline{v}\leq|\underline{u}| | \underline{v}|
$$
Combining these, we get:
$$
|\underline{u}| |\underline{v}|\geq \frac{|\underline{u}+\underline{v}|^{2}-|\underline{u}|^{2}-|\underline{v}|^{2}}{2}
$$
$$
\implies |\underline{u}+\underline{v}|^{2}\leq|\underline{u}|^{2}+2|\underline{u}| |\underline{v}|+|\underline{v}|^{2}
$$
$$
\implies |\underline{u}+\underline{v}|^{2}\leq (|\underline{u}|+|\underline{v}|)^{2}
$$
$$
\implies |\underline{u}+\underline{v}|\leq|\underline{u}|+|\underline{v}|
$$
Since $|\underline{u}+\underline{v}|^{2}$ is the square of a magnitude (and so is positive) and $|\underline{u}|+|\underline{v}|$ is the sum of two magnitudes (and so is also positive)
## Real [[Norms|Norms]]
Suppose we have a [[Vectorspaces|vectorspace]] $V$, with real [[Inner Product|inner product]] $(,)$; a real [[Inner Product Spaces|inner product space]], then $\forall \underline{u},\underline{v}\in V$,
next board, we want
$$
(\lvert \lvert \underline{u} \rvert \rvert +\lvert \lvert \underline{v} \rvert \rvert )^{2}-\lvert \lvert \underline{u}+\underline{v} \rvert \rvert ^{2}\geq 0
$$
$$
(\lvert \lvert \underline{u} \rvert \rvert +\lvert \lvert \underline{v} \rvert \rvert )^{2}-\lvert \lvert \underline{u}+\underline{v} \rvert \rvert ^{2}=\lvert \lvert \underline{u} \rvert \rvert ^{2}+2\lvert \lvert \underline{u} \rvert \rvert \lvert \lvert \underline{v} \rvert \rvert +\lvert \lvert \underline{v} \rvert \rvert^{2}-(\underline{u}+\underline{v},\underline{u}+\underline{v})
$$
$$
= \lvert \lvert \underline{u} \rvert \rvert ^{2}+2\lvert \lvert \underline{u} \rvert \rvert \lvert \lvert \underline{v} \rvert \rvert +\lvert \lvert \underline{v} \rvert \rvert ^{2}-\lvert \lvert \underline{u} \rvert \rvert ^{2}-2(\underline{u},\underline{v})-\lvert \lvert \underline{v} \rvert \rvert ^{2}
$$
$$
= 2(\lvert \lvert \underline{u} \rvert \rvert \lvert \lvert \underline{v} \rvert \rvert -(\underline{u},\underline{v})) 
$$
Which is positive by [[Cauchy-Schwarz Inequality|Cauchy-Schwarz]]
## Complex Norms
Suppose we have a complex vectorspace $V$, with [[Hermitian Inner Product|hermitian inner product]] $\left< , \right>$, then $\forall \underline{u},\underline{v}\in V$, we want
$$
\lvert \lvert \underline{u}+\underline{v} \rvert \rvert \leq \lvert \lvert \underline{u} \rvert \rvert +\lvert \lvert \underline{v} \rvert \rvert 
$$
### Proof
$$
(\lvert \lvert \underline{u} \rvert \rvert +\lvert \lvert \underline{v} \rvert \rvert )^{2}-\lvert \lvert \underline{u}+\underline{v} \rvert \rvert ^{2}=\lvert \lvert \underline{u} \rvert \rvert ^{2}+2\lvert \lvert \underline{u} \rvert \rvert \lvert \lvert \underline{v} \rvert \rvert +\lvert \lvert \underline{v} \rvert \rvert ^{2}-\left< \underline{u}+\underline{v},\underline{u}+\underline{v} \right> 
$$
$$
= \lvert \lvert \underline{u} \rvert \rvert ^{2}+2\lvert \lvert \underline{u} \rvert \rvert \lvert \lvert \underline{v} \rvert \rvert +\lvert \lvert \underline{v} \rvert \rvert ^{2}-\lvert \lvert \underline{u} \rvert \rvert -\left< \underline{u},\underline{v} \right> -\left< \underline{v},\underline{u} \right> -\lvert \lvert \underline{v} \rvert \rvert ^{2}
$$
$$
= 2(\lvert \lvert \underline{u} \rvert \rvert \lvert \lvert \underline{v} \rvert \rvert -\mathrm{Re}\left< \underline{u},\underline{v} \right> )\geq 2(\lvert \lvert \underline{u} \rvert \rvert \lvert \lvert \underline{v} \rvert \rvert -\left| \left< \underline{u},\underline{v} \right>  \right| )\geq 0
$$
By Caucy-Schwarz


#Mathematics #LinAlg #Theorem