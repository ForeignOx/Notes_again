There are three main ways of representing planes in [[Vectorspace Rn|$\mathbb{R}^3$]]
## Parametric Form
![[Planes in R3 2024-10-14 11.41.53.excalidraw]]
Pick a point $\underline{a}\in\Pi$ on the plane and two [[Vectors|vectors]] $\underline{d_{1}},\underline{d_{2}}\in\mathbb{R}^3$ parallel to $\Pi$ but not parallel to each other and such that $\underline{d_{1}}\neq \underline{0}$,$\underline{d_{2}}\neq \underline{0}$
To get to a general point on the plane $\underline{p}\in\Pi$, you first travel from the origin to the point $\underline{a}$ on the plane and then some multiples of $\underline{d_{1}}$ and some multiples of $\underline{d_{2}}$, so:
$$
\Pi=\{ \underline{a}+\lambda_{1}d_{1}+\lambda_{2}d_{2}|\lambda_{1},\lambda_{2}\in \mathbb{R} \}
$$
Here $\lambda_{1},\lambda_{2}$ are called "free variables” and the fact that there are two of them links to the fact that planes are two-dimensional
## Using the Normal Vector
![[Planes in R3 2024-10-14 11.52.40.excalidraw]]
Consider a point $\underline{a}\in\Pi$, $\underline{n}$ is a normal to $\Pi$ ($n\neq 0$) and a general point $\underline{x}\in\Pi$ must satisfy:
$$
\underline{x}\in \Pi \iff(\underline{x}-\underline{a})\text{ orthogonal to } \underline{n}\iff(\underline{x}-\underline{a})\cdot \underline{n}=0
$$
$$
\iff \underline{x}\cdot \underline{n}-\underline{a}\cdot \underline{n}=0\iff \underline{x}\cdot \underline{n}=\underline{a}\cdot \underline{n}=l
$$
So we can describe a plane as:
$$
\Pi=\{ \underline{x}\in \mathbb{R}^3|\underline{x}\cdot \underline{n}=\underline{a}.\underline{n} \}=\{ \underline{x}\in \mathbb{R}^3|\underline{x}\cdot \underline{n}=l \}
$$
You can find the normal vector by taking the [[Cross Product|cross product]] of $\underline{d_{1}}$ and $\underline{d_{2}}$ from the method above
___
The fact that $\mathbb{R}^{n}$ has the natural [[Inner Product|inner product]] $(\underline{x},\underline{y})$ is of course extremely important, both algebraically and geometrically. However, most vectorspaces do not have natural scalar products. This leads us to seek a different interpretation of the equation $\underline{x}\cdot \underline{n}=\underline{a}\cdot  \underline{n}$. We know that the most general [[Linear Functionals|linear functional]] $f$ on $\mathbb{R}^{3}$ is $\underline{x}\mapsto \sum_{i}a_{i}x_{i}$
Therefore, given any plaine $M\in \mathbb{E}^{3}$, there is a nonzero linear functional $f$ on $\mathbb{R}^{3}$ and a number $l$ such that the equation of $M$ is $f(\underline{x})=l$
Conversely, given any non-zero linear functional $f:\mathbb{R}^{3}\to \mathbb{R}$ and any $l\in \mathbb{R}$, the locus of $f(\underline{x})=l$ is a plane $M\in \mathbb{E}^{3}$. We see this by recalling that we can obtain the coefficient triple $\underline{a}$ from $f$ by $a_{i}=f(\delta^{i})$, since then 
$$
f(\underline{x})=f\left( \sum_{i=1}^{3}x_{i}\delta^{i} \right)=\sum_{i=1}^{3}x_{i}f(\delta^{i})=\sum_{i=1}^{3}x_{i}a_{i}
$$
___
Consider the plane $M$ with equation $f(\underline{x})=l$, conider what happens to $M$ under the [[Parallel Translations|translation]] $\underline{x}\mapsto \underline{y}=\underline{x}+\underline{b}$
Since $\underline{x}=\underline{y}-\underline{b}$, we can see that a point $\underline{x}$ is on $M$ iff its translate $\underline{y}$ satisfies the equation $f(\underline{y}-\underline{b})=l$, or, since $f$ is linear, the equation $f(\underline{y})=l'$, where $l'=l+f(\underline{b})$
But this is the equation of a plane $N$. Thus the translate of $M$ is the plane $N$
___
It is natural to transfer this geometic terminology fron sets in $\mathbb{E}^{3}$ to the corresponding sets in $\mathbb{R}^{3}$ and therefore to speak of the set of ordered tuples satisfying $f(\underline{x})=l$ as a set of points in $\mathbb{R}^{3}$ forming a plane in $\mathbb{R}^{3}$, and to call the mapping $\underline{x}\mapsto \underline{x}+\underline{b}$ the parallel translation of $\mathbb{R}^{3}$ through $\underline{b}$
Moreover, since $\mathbb{R}^{3}$ is a [[Vectorspaces|vectorspace]], we would expect these geometric ideas to interplay with [[Vectors|vector]] notions. For instance, translation through $\underline{b}$ is simply the operation of adding the constant vector $\underline{b}$ such that $\underline{x}\mapsto \underline{x}+\underline{b}$
Thus if $M$ is a plane, then the palne $N$ obtained by translating $M$ through $\underline{b}$ is just the vector set sum $M+\underline{b}$. If the equation of $M$ is $f(\underline{x})=l$, then the plane $M$ goes through $0$ iff $l=0$, in which case $M$ is a vector [[Subspaces|subspace]] of $\mathbb{R}^{3}$ (the [[Kernel|nullspace]] of $f$) 
It is easy to see that any plane $M$ is a translate of a plane through $\hspace{0pt}0$. Similarly, the line $\left\{ \lambda \underline{a}+\underline{b}\mid\lambda \in\mathbb{R} \right\}$ is the translate through $\underline{b}$ of the line $\left\{ \lambda \underline{a}\mid\lambda \in\mathbb{R} \right\}$, and this second line is a subspace, the [[Linear Span|linear span]] of $\underline{a}$. Thus planes and linear are translates of subspaces
## Cartesian Form
This is essentially the same as the method using the normal vector above, but using coordinates
If we write:
$$
\underline{n}=\begin{pmatrix}
a\\b\\c
\end{pmatrix},\underline{x}=\begin{pmatrix}
x\\y\\z
\end{pmatrix}
$$
So $\underline{n}\cdot \underline{x}=l$ can be written:
$$
ax+by+cz=l
$$
So:
$$
\Pi=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3|ax+by+cz=l  \right\}
$$
## Parametric Description from Normal/Cartesian
Suppose:
$$
\Pi=\left\{ \underline{x}\in \mathbb{R}^3 \middle| \underline{n}\cdot \underline{x}=l \right\}=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3\middle|ax+by+cz=l \right\}
$$
$$
\underline{n}=\begin{pmatrix}
a\\b\\c
\end{pmatrix}
$$
If $c\neq 0$ then:
$$
ax+by+cz=l\iff z=\frac{l}{c}-\left( \frac{a}{c} \right)x-\left( \frac{b}{c} \right)y
$$
Since we can use $z$ to be any point, $x$ and $y$ become our free parameters essentially; so:
$$
\Pi=\left\{  \begin{pmatrix}
0\\0\\ \frac{l}{c}
\end{pmatrix} +x\begin{pmatrix}
1\\0\\-\frac{a}{c}
\end{pmatrix}+y\begin{pmatrix}
0\\1\\ -\frac{b}{c}
\end{pmatrix}\middle|x,y\in \mathbb{R} \right\}
$$
If $c=0$, then you can do the same process using $b$ or $c$
## Hyperplanes
We can think of planes loosely as a translate of a subspace, whatever its dimension. More properly, this is the definition of an [[Affine Subspace|affine subspace]]
If some [[Vectorspaces|vectorspace]] $V$ is finite-[[Dimension|dimensional]] with dimension $n$, then the [[Kernel|nullspace]] of a nonzero [[Linear Functionals|linear functional]] $f$ is always $(n-1)$-dimensional, and therefore it cannot be a Euclidean-like 2D plane that we're used to unless $n=3$
We use the term hyperplane for such a nullspace or one of its translates
Thus, in general, a hyperplane is a [[Sets|set]] with hte equation $f(\underline{x})=l$, where $f$ is a nonzero linear functional
It is a proper affine subspace (plane) which is maximal in the sense that the only affine subspace properly including it is the whole of $V$
In $\mathbb{R}^{3}$ hyperplanes are thus planes, but in $\mathbb{R}^{2}$, hyperplanes are just lines
## Examples
### Find Plane using Point and Normal
Find the cartesian description of the plane $\Pi$ that passes through:
$$
\begin{pmatrix}
1\\-1\\3
\end{pmatrix}=\underline{a}\in \Pi
$$
and is normal to the direction:
$$
\begin{pmatrix}
5\\2\\1
\end{pmatrix}=\underline{n}
$$
So:
$$
\Pi=\left\{  \underline{x}=\begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3|\begin{pmatrix}
x\\y\\z
\end{pmatrix}\cdot \begin{pmatrix}
5\\2\\1
\end{pmatrix}= \begin{pmatrix}
1\\-1\\3
\end{pmatrix}\cdot \begin{pmatrix}
5\\2\\1
\end{pmatrix} \right\}
$$
$$
\implies \Pi=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3|5x+2y+z=6  \right\}
$$
### Find Normal Vector and Point on the Plane
Find a normal vector and a point on the plane $6x-5y+3z=30$, using what we know about the cartesian equation for a plane we can clearly see:
$$
\underline{n}=\begin{pmatrix}
6\\-5\\3
\end{pmatrix}
$$
and $\underline{a}$ can be any point on the plane, an easy way of finding one is to let $z,y=0$ and solve $6x=30\implies x=5$, so:
$$
\underline{a}=\begin{pmatrix}
5\\0\\0
\end{pmatrix}
$$
Using the same method we could obtain
$$
\underline{a}=\begin{pmatrix}
0\\-6\\0
\end{pmatrix}\text{ or }\underline{a}=\begin{pmatrix}
0\\0\\10
\end{pmatrix}
$$
### FInding Parametric and Cartesian Descriptions of the Plane $\Pi$ based on Points
Where $\Pi \subseteq\mathbb{R}^3$ that passes through:
$$
\underline{a}=\begin{pmatrix}
1\\0\\1
\end{pmatrix},\underline{b}=\begin{pmatrix}
2\\-1\\3
\end{pmatrix},\underline{c}=\begin{pmatrix}
5\\1\\1
\end{pmatrix}
$$
![[Planes in R3 2024-10-15 11.45.09.excalidraw]]

This method works assuming $\underline{a},\underline{b}$ and $\underline{c}$ are not colinnear
Set:
$$
\underline{d_{1}}=\underline{b}-\underline{a}=\begin{pmatrix}
1\\-1\\2
\end{pmatrix}
$$
$$
\underline{d_{2}}=\underline{c}=\underline{a}=\begin{pmatrix}
4\\1\\0
\end{pmatrix}
$$
So 
$$
\Pi=\{ \underline{a}+\lambda_{1}  \underline{d_{1}}+ \lambda_{2} \underline{d_{2}}|\lambda_{1},\lambda_{2}\in \mathbb{R}\}
$$
Now to find a cartesian description, we can use the fact that $\underline{n}$ will be orthogonal to $\underline{d_{1}}$ and $\underline{d_{2}}$ so:
$$
\underline{n}:=\underline{d_{1}}\times \underline{d_{2}}
$$
$$
\therefore \underline{n}=\begin{pmatrix}
1\\-1\\2
\end{pmatrix}\times \begin{pmatrix}
4\\1\\0
\end{pmatrix}=\begin{pmatrix}
-2\\8\\5
\end{pmatrix}
$$
Then we know $l=\underline{n}\cdot \underline{a}$, so $l=-2+5=3$, so we have:
$$
\Pi=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3\middle|-2x+8y+5z=3  \right\}
$$

#Mathematics #LinAlg 