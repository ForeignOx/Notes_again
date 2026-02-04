## Construction
A useful [[Vectorspaces|space]] is the $n$-[[Dimension|dimensional]] euclidean space $\mathbb{E}^{n}$. We want to set up a coordinate correspondence between $\mathbb{E}^{n}$ and the Cartesian vectorspace [[Vectorspace Rn|$\mathbb{R}^{n}$]] 
We first choose arbitrarily a zero point $O$ and $n$ unit points $Q_{1},Q_{2},\dots,Q_{n}$ in such a way that a maximum of $\hspace{0pt}3$ of them lie on a 2D plane.
Each of the unit points $Q_{i}$ determines a [[Lines|line]] $L_{i}$ through $O$ and a coordinate correspondence on this line. The $n$ lines $L_{i}$ are called the coordinate axes
Consider any point $X$ in $\mathbb{E}^{3}$, the plane through $X$ parallel to all $L_{i}$ except $L_{k}$ for some $k\in \overline{n}$ intersects $L_{k}$ at a point $X_{k}$, and theefore determines a number $x_{k}$, the coordinate of $X_{k}$ on $L_{k}$. Doing this for all $k$, we get an $n$-tuple
$$
\underline{x}=(x_{1},x_{2},\dots,x_{n})
$$
In $\mathbb{R}^{n}$ and have thus defined a mapping $\theta:X\mapsto x$ from $\mathbb{E}^{n}$ to $\mathbb{R}^{n}$
We call $\theta$ the coordinate correspondence defined by the axis system
The convention implicit in our notation above is that $\theta(Y)$ is $\underline{y}$, $\theta(A)$ is $\underline{a}$ etc.
Note that the unit point $Q_{i}$ on $L_{i}$ has the coordinate tuple [[Coordinates|$\delta^{i}$]] 
___
There are certian basic facts about the correspondence that have to be proved a theorems of geometry before the correspondence an be used to treat geometric questions algebraically. These geometric theorems are tricky, so we assume them:
- $\theta$ is a [[Bijective Functions|bijection]] from $\mathbb{E}^{n}$ to $\mathbb{R}^{n}$
- Two line segments $AB$ and $XY$ are equal in length and parallel, and the direction from $A$ to $B$ is the same as that from $X$ to $Y$ iff $\underline{b}-\underline{a}=\underline{y}-\underline{x}$ (in $\mathbb{R}^{3}$). A directed line segment is a geometric line segment, together with a choice of one of the two directions along it. If we interpret $AB$ as the directed line segment from $A$ to $B$, and if we define an [[Equivalence Relation|equivalence relation]] with some other line segment $XY$ if they are equal in length, parallel and similarly directed, then we say:
$$
AB\sim XY\iff \underline{b}-\underline{a}=\underline{y}-\underline{x}
$$
- If $X\neq 0$, then $Y$ is on the line through $O$ and $X$ in $\mathbb{E}^{n}$ iff $\underline{y}=t \underline{x}$ for some $t\in\mathbb{R}$. Moreover, this $t$ is the coordinate of $Y$ with respect to $X$ as a unit point on the line through $O$ and $X$
- If the axis system in $\mathbb{E}^{n}$ is cartesian, that is, if the axes are mutually [[Orthogonality|orthogonal]] and a common unit of disttance is used, then the length $\left| OX \right|$ of the line segment $OX$ is given by the euclidean [[Norms|norm]] $\left| OX \right|=\sqrt{ \sum_{i}x_{i}^{2} }$. This follows directly from [[Pythagoras' Theorem|Pythagoras]]. Then this formula and further application of pythagoras to a triangle $OXY$ imply that the segments $OX$ and $OY$ are perpendicular iff the [[Dot Product|scalar product]] $(\underline{x},\underline{y})=\sum_{i}x_{i}y_{i}$ has the value 0