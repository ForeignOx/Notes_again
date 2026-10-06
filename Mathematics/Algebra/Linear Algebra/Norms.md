Given a [[Vectorspaces|vectorspace]] over $\mathbb{R}$, (or $\mathbb{C}$), a norm on $V$ is a [[Functions|functions]] 
$$
\lvert \lvert \cdot \rvert \rvert:V\to \mathbb{R}
$$
$$
 \underline{v}\mapsto \lvert \lvert \underline{v} \rvert  \rvert 
$$
Such that it satisifes the following properties:
- $\lvert \lvert a\underline{v} \rvert \rvert =\left| a \right| \lvert \lvert \underline{v} \rvert \rvert$ (absolute homogeneity)
- $\lvert \lvert \underline{u}+\underline{v} \rvert \rvert\leq \lvert \lvert \underline{u} \rvert \rvert+\lvert \lvert \underline{v} \rvert \rvert$ ([[Triangle Inequality|triangle inequality]])
- $\lvert \lvert \underline{v} \rvert \rvert=0\iff \underline{v}=\underline{0}$ (separation of points)
Note from property $\hspace{0pt}1$, we have $\lvert \lvert -\underline{v} \rvert \rvert=\lvert \lvert \underline{v} \rvert \rvert$, and also $\lvert \lvert \underline{0} \rvert \rvert=0$, so by the triangle inequality,
$$
0=\lvert \lvert \underline{0} \rvert \rvert =\lvert \lvert \underline{v}+-\underline{v} \rvert \rvert\leq \lvert \lvert \underline{v} \rvert \rvert +\lvert \lvert -\underline{v} \rvert \rvert =2\lvert \lvert \underline{v} \rvert \rvert 
$$
So
$$
\lvert \lvert \underline{v} \rvert \rvert \geq 0\forall \underline{v}\in V
$$
So this can be used a s definition of a length
## Real Case
If $\left\{ V,(,) \right\}$ is an [[Inner Product Spaces|inner product space]], then the norm induced by the [[Inner Product|inner product]] $(,)$ is
$$
\lvert \lvert \underline{v} \rvert \rvert _{(,)}=\lvert \lvert \underline{v} \rvert \rvert =\sqrt{ (\underline{v},\underline{v}) }\in \mathbb{R}
$$
Which is well defined since $(\underline{v},\underline{v})\geq 0\forall \underline{v}\in V$
We must check that this really is a norm, so do the properties hold?
$$
\lvert \lvert a\underline{v} \rvert \rvert =\sqrt{ (a\underline{v},a\underline{v}) }=\sqrt{ a^{2}(\underline{v},\underline{v}) }=\left| a \right| \lvert \lvert \underline{v} \rvert \rvert 
$$
$$
\lvert \lvert \underline{v} \rvert \rvert =0\iff(\underline{v},\underline{v})=0\iff \underline{v}=\underline{0}
$$
By positive definitivity
The second one is proved with triangle inequality
## Complex Version
Let $\left\{ V,\left< , \right> \right\}$ be a complex inner product space with [[Hermitian Inner Product|hermitian inner product]] $\left< , \right>$.
Then the norm induced by $\left< , \right>$ is 
$$
\lvert \lvert \underline{v} \rvert \rvert =\sqrt{ \left< \underline{v},\underline{v} \right>  }
$$
(the same as the real case) $\forall \underline{v}\in V$
This is ok by the positive definite property of $\left< \underline{v},\underline{v} \right>$
### Properties
$$
\lvert \lvert a\underline{v} \rvert \rvert =\sqrt{ \left< a\underline{v},a\underline{v} \right>  }=\sqrt{ \left| a \right| ^{2}\lvert \lvert \underline{v},\underline{v} \rvert \rvert  }
$$
Since $\left| a \right|^{2}=a \overline{a}$ for any $a\in\mathbb{C}$
$$
\implies \lvert \lvert a\underline{v} \rvert \rvert =\left|  a\right| \sqrt{ \left< \underline{v},\underline{v} \right>  }=\left| a \right| \lvert \lvert \underline{v},\underline{v} \rvert \rvert 
$$

## Unit Vectors
$\underline{v}$ is a unit vector s $\lvert \lvert \underline{v} \rvert \rvert=1$
## Examples
For $(x_{1},\dots,x_{n})\in\mathbb{R}^{n}$ define the $\ell_{p}$ norm:
$$
\lvert \lvert x \rvert \rvert _{p}=\left( \sum_{i=1}^{n} x_{i}^{p}\right)^{\frac{1}{p}}
$$
Key ones include the Euclidean norm $\lvert \lvert x \rvert \rvert_{2}$, the manhattan norm, $\lvert \lvert x \rvert \rvert_{1}$ and the $\ell_{\infty}$ norm:
$$
\lvert \lvert x \rvert \rvert _{\infty}=\max\left\{ \left| x_{i} \right| \in \mathbb{R}:\middle|: i=1,\dots,n \right\}
$$
The three norm properties are easily checked for these functions, with the exception of the [[Triangle Inequality|triangle inequality]] for the Euclidean norm
Because of [[Pythagoras' Theorem|pythagoras' theorem]], we think of $\lvert \lvert \cdot \rvert \rvert_{2}$ as the most reasonable choice of distance. The euclidean norm is the norm induced by the standard [[Dot Product|dot product]] on $\mathbb{R}^{n}$, so
$$
\lvert \lvert x \rvert \rvert _{2}=\sqrt{ \left< x,x \right>  }
$$
Where
$$
\left< x,y \right> =\sum_{i=1}^{n}x_{i}y_{i}
$$



#Mathematics #LinAlg #Definition 