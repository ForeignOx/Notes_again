This is a way to extend the concept of an [[Inner Product|inner product]] to [[Complex Numbers|complex numbers]], which still satisfies positivity. The solution to this is called a Hermitian Inner Product, and is defined on a complex vectorspace is a mapping
$$
\left< , \right>:V\times V\to \mathbb{C}
$$
$$
 \underline{u},\underline{v}\mapsto \left< \underline{u},\underline{v} \right> \in \mathbb{C}
$$
For $\underline{u},\underline{v}\in V$ such that:
- $\left< \underline{v},\underline{u} \right>= \overline{\left< \underline{u},\underline{v} \right>}$ (Hermiticity)
- $\left< \underline{u}+\underline{v},\underline{w} \right>=\left< \underline{u},\underline{w} \right> +\left< \underline{v},\underline{w} \right>$ 
- $\left< \lambda \underline{u},\underline{v} \right>=\lambda \left< \underline{u},\underline{v} \right>$ (this and previous, make linear in first argument)
- $\left< \underline{v},\underline{v} \right>\geq 0$ with $\left< \underline{v},\underline{v} \right> =0\iff \underline{v}=\underline{0}$
Why is $\left< \underline{v},\underline{v} \right>\in\mathbb{R}$, it follows from the first point that swapping the vectors gives the conjugate, so they must map to $\mathbb{R}$  
- $\left< \underline{v},\underline{v} \right>\in\mathbb{R}$
Note that $\left< , \right>$ is not quite linear in its second argument, we can use property $\hspace{0pt}1$ to show that $\left< \underline{u},\lambda \underline{v} \right> =\overline{\left< \lambda \underline{v},\underline{u} \right> }$ then by the third property is equal to $\overline{\lambda \left< \underline{v},\underline{u} \right>}=\overline{\lambda}\overline{\left< \underline{v},\underline{u} \right>}$, which by the first property is then equal to $\overline{\lambda}\left< \underline{u},\underline{v} \right>$
- $\left< \underline{u},\lambda \underline{v} \right>=\overline{\lambda}\left< \underline{u},\underline{v} \right>$
The property of linearity in first argument, and complex-conjugate-linearity in second is called sesquilinearity
As for a real inner product, fix a basis $\left\{ \underline{v}_{1},\dots,\underline{v}_{n} \right\}$ of $V$,
$$
\underline{u}=\sum_{ i=1} ^{ n}  x_{i}\underline{v}_{i},\underline{v}=\sum_{ j=1} ^{ n}  y_{j}\underline{v}_{j}
$$
With $x_{i},y_{j}\in\mathbb{C}$, so
$$
\left< \underline{u},\underline{v} \right> =\sum_{ i=1} ^{ n}  \sum_{ j=1} ^{ n}  \overline{y}_{j}\left< \underline{v}_{i},\underline{v}_{j} \right> x_{i}
$$
$$
= \sum_{ i=1} ^{ n}  \sum_{ j=1} ^{ n}  \overline{y}_{j}B_{ji}x_{i}=(\overline{\underline{y}})^{\top}B\underline{x}
$$
$$
= \underline{y}^{*}B\underline{x}
$$
$$
\left< \underline{u},\underline{v} \right> =\begin{pmatrix}
\overline{y}_{1}&\overline{y}_{2}&\dots&\overline{y}_{n}
\end{pmatrix}\begin{pmatrix}
B_{11}
\end{pmatrix}
$$
Where $B_{ji}=\left< \underline{v}_{i},\underline{v}_{j} \right>\in\mathbb{C}$, and $\underline{y}^{*}=(\overline{\underline{y}})^{\top}$, so $B$ is the [[Matrices|matrix]] representation of $\left< , \right>$ in the [[Basis|Basis]] $\left\{ v_{i} \right\}$
$B$ must satisfy $B=(\overline{B})^{\top}=B^{*}$, called the hermitian [[Transpose|transpose]], or the conjugate transpose, or the hermitian conjugate, sometimes written $B^{\dagger}$. Matrices that satisfy $B=B^{*}$ are called Hermitian, likewise $B$ is anti-Hermitian i $B^{*}=-B$
Any complex matrix is the sum of a Hermitian and an anti-Hermitian matrix:
$$
A=\underbrace{ \frac{1}{2}(A+A^{*}) }_{ \text{Hermitian} }+\underbrace{ \frac{1}{2}(A-A^{*}) }_{ \text{Anti-Hermitian} }
$$
Which uses the fact that $(A^{*})^{*}=A$
If $A$ is real and [[Symmetric and Anti-Symmetric Matrices|symmetric]], then it is Hermitian, since $A^{*}=(\overline{A})^{\top}=A^{\top}=A$
## Examples
If $V=\mathbb{C}^{n}$ with a 'standard' hermitian inner product:
$$
\left< \underline{z},\underline{w} \right>  =z_{1}\overline{w}_{1}+\dots+z_{n}\overline{w}_{n}=\begin{pmatrix}
\overline{w}_{1}&\overline{w}_{2}&\dots&\overline{w}_{n}
\end{pmatrix}\begin{pmatrix}
1&0&\dots&0\\0&1&\dots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\dots&1
\end{pmatrix}\begin{pmatrix}
z_{1}\\z_{2}\\\vdots\\z_{n}
\end{pmatrix}
$$
Here $B=I$, now is $\left< \underline{z} ,\underline{z}\right> \geq 0$
$$
\left< \underline{z},\underline{z} \right> = \left| z_{1} \right| ^{2}+\dots+\left| z_{n} \right| ^{2} \geq 0
$$
And
$$
\left< \underline{z},\underline{z} \right> =0\implies z_{i}=0\forall1\leq i\leq n\implies \underline{z}=\underline{0}
$$
___
Does $\left< \underline{z},\underline{w} \right>=z_{1}\overline{w}_{1}+iz_{1}\overline{w}_{2}+iz_{2}\overline{w}_{1}+z_{2}\overline{w}_{2}$ define an inner product on $\mathbb{C}^{2}$?
No as
$$
\left< \underline{w},\underline{z} \right> =w_{1}\overline{z}_{1}+iw_{1}\overline{z}_{2}+iw_{2}\overline{z}_{1}+w_{2}\overline{z}_{2}
$$
While
$$
\overline{\left< \underline{z},\underline{w} \right> }=\overline{z}_{1}-i\overline{z}_{1}w_{2}-i\overline{z}_{2}w_{1}+\overline{z}_{2}w_{2}
$$
These are not equal
We can also show this by saying
$$
\left< \underline{z},\underline{w} \right> =\begin{pmatrix}
\overline{w}_{1}&\overline{w}_{2}
\end{pmatrix}\begin{pmatrix}
1&i\\i&1
\end{pmatrix}\begin{pmatrix}
z_{1}\\z_{2}
\end{pmatrix}
$$
So
$$
B=\begin{pmatrix}
1&i\\i&1
\end{pmatrix}
$$
And 
$$
B^{*}=\begin{pmatrix}
1&-i\\-i&1
\end{pmatrix}\neq B
$$
___
Let $V$ be the infinite [[Dimension|dimensional]] vectorspace 
$$
C([a,b],\mathbb{C})=\left\{ f:[a,b]\to \mathbb{C},\text{continuous complex valued functions} \right\}
$$
Then
$$
\left< f,g \right> =\int ^{b}_{a} f(t)\overline{g(t)} \, dt 
$$
Defines a hermitian inner product
## Change of [[Basis|Basis]] for Hermitian Inner Product
Every inner product has the form
$$
\left< \underline{z},\underline{w} \right> =\underline{q}^{*}B  \underline{p}
$$
Where $\underline{p}$ is the coordinates of $\underline{z}$ in a given basis $\left\{ \underline{w}_{1},..,\underline{w}_{k} \right\}$, and $\underline{q}$ is coordinates of $\underline{w}$ in that basis, so
$$
B_{ij}=\left< \underline{w}_{j},\underline{w}_{i} \right>
$$
Is the matrix representation of $(,)$ in this basis
So there exists $N$ which is [[Matrix Inverses|invertible]] such that
$$
\underline{p}=N\underline{\tilde{p}}
$$
$$
 \underline{q}=M  \underline{\tilde{q}}
$$
Where $\underline{\tilde{p}}$ and $\underline{\tilde{q}}$ are the coordinates of $\underline{z}$ and $\underline{w}$ in the new basis
What is the matrix representation of the same inner product in the new basis?
$$
\left< \underline{z},\underline{w} \right> =\underline{q}^{*}B  \underline{p}=(N  \underline{\tilde{q}})^{*}B(N  \underline{p})=\underline{\tilde{q}}^{*}(N^{*}BN)  \underline{p}
$$
So we can conclude that in our new basis:
$$
b\to \tilde{b}=N^{*}BN
$$
(For the matrix of a linear transformation, we instead found $A= P ^{-1}AP$, this is different)
So a big question for [[Diagonalisation|diagonalisation]], is can we find $M$ such that $N^{*}BN$ is diagonal, and a subquestion, what if $M^{*}=M^{-1}$


#Mathematics #LinAlg #Definition 