## Coordinate Correspondence
A coordinate correspondence between a line $L$ and the real number system $\mathbb{R}$ is determined by a zero point $O$ and a unit point $Q$ distinct from $O$. Then each point $X$ on $L$ is asigned the number $x$ such that $\left| x \right|$ is the distance from $O$ yo $X$, measured in terms of th segment $OQ$ as $\hspace{0pt}1$, and $x$ is poitive or negativeaccording as $X$ and $Q$ are on the same side of $O$ or on opposite sides
The [[Functions|mapping]] $X\mapsto x$ is the coordinate correspondence
# $\mathbb{R}^{2}$
Let $l$ be a stright line in [[Vectorspace Rn|$\mathbb{R}^{2}$]], and let $P_{0}(x_{0},y_{0})$ and $P_{1}(x_{1},y_{1})$ be any two distinct points on $l$
## Slope
The slope of this line is defined to be:
$$
m=\frac{y_{1}-y_{0}}{x_{1}-x_{0}}=\tan\theta, \text{provided }x_{1}\neq x_{0} 
$$
Where $\theta$ is the inclination of $l$; the angle between the positively directed $x$-caxis and $l$ measured in the couterclockwise direction. If $x_{1}=x_{0}$, then $l$ is a vertical line and the slope is undefined, and $\theta=\frac{\pi}{2}$
## Intercepts
If $l$ is a nonvertical line, then it intersects the $y$-axis at a point $(0,b)$, and $b$ is known as the $y$-intercept of $l$
Similarly, if $l$ is not horizontal , then it will intersect the $x$-axis at a point $(a,0)$. The number $a$ is called the $x$-intercept of $l$
## Equations
An equation for $l$ is an equation which involves two variables, say $x$ say $y$, and has the property that a point $P(x_{0},y_{0})$ lies on $l$ iff $x_{0}$ and $y_{0}$ satisfy the equation. Here are some standard forms
- Vertical line:
$$
x=a
$$
- Horizontal line:
$$
y=b
$$
- Point-slope form:
$$
y-y_{0}=m(x-x_{0})
$$
- two-point form:
$$
y-y_{0}=\frac{y_{1}-y_{0}}{x_{1}-x_{0}}(x-x_{0})
$$
- slope-intercept form:
$$
y=mx+b
$$
- two-intercept form:
$$
\frac{x}{a}+\frac{y}{b}=1
$$
- General form:
$$
Ax+By+C=0
$$
## Parallel Lines
Given two nonvertical lines $l_{1}$ and $l_{2}$ with slopes $m_{1}$ and $m_{2}$ respectively, then, are parallel iff $m_{1}=m_{2}$
## Perpendicular Lines
Given two nonvertical lines $l_{1}$ and $l_{2}$ with slopes $m_{1}$ and $m_{2}$ respectively, then, are perpendicular iff $m_{1}m_{2}=1$
## [[Angle Between Vectors|Angle Between two Lines]]
![[Lines in R2 2024-10-27 16.31.06.excalidraw]]
Consider two intersecting lines as shown in the image above, named $l_{1}$ and $l_{2}$ with inclinations $\theta_{1}$ and $\theta_{2}$. These lines form two angles $\alpha=\theta_{2}-\theta_{1}$ and $\pi-\alpha$. If these two angles are equal, then $\alpha=\frac{\pi}{2}$ and the lines are perpendicular. If $\alpha$ and $\pi-\alpha$ are not equal, then the smaller of the two is called the angle between $l_{1}$ and $l_{2}$,
$$
\tan\alpha=\left| \frac{m_{2}-m_{1}}{1-m_{1}m_{2}}\right|
$$

# $\mathbb{R}^{3}$
Lines can be described in a few ways in [[Vectorspace Rn|$\mathbb{R}^3$]]
## Parametric Description
![[Lines in R3 2024-10-15 11.52.34.excalidraw]]
We take a point $\underline{a}\in L$, and a vector $\underline{d}\neq 0$ parallel to $L$, then
$$
L=\{ \underline{a}+\lambda \underline{d}|\lambda \in \mathbb{R} \}
$$
## Cartesian Description
We can abstract this from the cartesian description, set:
$$
\underline{a}=\begin{pmatrix}
a_{1}\\a_{2}\\a_{3}
\end{pmatrix},\underline{d}=\begin{pmatrix}
d_{1}\\d_{2}\\d_{3}
\end{pmatrix}
$$
Then
$$
\begin{pmatrix}
x\\y\\z
\end{pmatrix}\in L\iff \begin{matrix}
a_{1}+\lambda d_{1}=x\\a_{2}+\lambda d_{2}=y\\a_{3}+\lambda d_{3}=z
\end{matrix}
$$
### Suppose $d_{1}\neq 0,d_{2}\neq 0,d_{3}\neq 0$, then
$$
\lambda=\frac{x-a_{1}}{d_{1}}=\frac{y-a_{2}}{d_{2}}=\frac{z-a_{3}}{d_{3}}
$$
So
$$
\begin{pmatrix}
x\\y\\z
\end{pmatrix}\in L\iff \frac{x-a_{1}}{d_{1}}=\frac{y-a_{2}}{d_{2}}=\frac{z-a_{3}}{d_{3}}
$$
$$
L=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3| \frac{x-a_{1}}{d_{1}}=\frac{y-a_{2}}{d_{2}}=\frac{z-a_{3}}{d_{3}} \right\}
$$
### If $d_{1},d_{2}\neq 0$, but $d_{3}=0$, then:
$$
\lambda=\frac{x-a_{1}}{d_{1}}=\frac{y-a_{2}}{d_{2}},z=a_{3}
$$
So
$$
L=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3| \frac{x-a_{1}}{d_{1}}=\frac{y-a_{2}}{d_{2}},z=a_{3} \right\}
$$
Similar expressions can be formed is one of $d_{1}$ or $d_{2}$ are instead zero
### If $d_{1}\neq 0$, but $d_{2}=d_{3}=0$, then
$$
L=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3 | y=a_{2},z=a_{3}\right\}
$$
Which will be a line parallel to the $x$-axis
This makes sense as in a cartesian description, you have $\hspace{0pt}3$ free variables that then you give two conditions for, reducing what we imagine the dimension to be from $\hspace{0pt}3$ to $\hspace{0pt}1$ 
You can also think of the cartesian form as a description that is the intersection of two planes from the two equations
## Intersection of Two [[Planes|Planes]]
Suppose we have two planes for $i=1,2$:
$$
\Pi_{i}=\{ \underline{x}\in \mathbb{R}^3|\underline{n}_{i}\cdot \underline{x} =l_{i}\}\subseteq \mathbb{R}^3
$$
Then what is $\Pi_{1}\cap \Pi_{2}$?
### If $n_{1},n_{2}$ are parallel (collinear)
Then either $\Pi_{1}=\Pi_{2}$, or they are parallel planes, so $\Pi_{1}\cap \Pi_{2}=\emptyset$
### If $n_{1},n_{2}$ are not parallel
Then their intersection is a line $L$
So
$$
L=\{ \underline{x}\in \mathbb{R}^3|\underline{n}_{1}\cdot \underline{x}=l_{1},\underline{n}_{2}\cdot \underline{x}=l_{2} \}
$$
Letting
$$
\underline{n}_{1}=\begin{pmatrix}
a\\b\\c
\end{pmatrix},\underline{n}_{2}=\begin{pmatrix}
d\\e\\f
\end{pmatrix}
$$
$$
L= \left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3\mid \begin{matrix}
ax+by+cz=l_{1}\\dx+ey+fz=l_{2}
\end{matrix}  \right\}
$$
### Converting between this description and parametric description
We need $\underline{a}\in L,\underline{d}\neq 0$ where $\underline{d}$ is parallel to $L$
![[Lines in R3 2024-10-17 10.40.14.excalidraw]]
$\underline{d}$ is parallel to $\Pi_{1}$ and $\Pi_{2}$ so
$$
\underline{d}\cdot \underline{n}_{1}=0,\underline{d}\cdot \underline{n}_{2}=0
$$
So set
$$
\underline{d}=\underline{n}_{1}\times \underline{n}_{2}=\begin{pmatrix}
a\\b\\c
\end{pmatrix}\times \begin{pmatrix}
d\\e\\f
\end{pmatrix}=\begin{pmatrix}
bf-ce\\cd-af\\ae-bd
\end{pmatrix}
$$
To find $\underline{a}\in L$, if $ae-bd\neq 0$, i.e. the third coordinate is non-zero, then $\underline{d}$ has some $z$-component, so must intersect the $x$-$y$ plane at a unique point when $z=0$, which we can take to be $\underline{a}$:
$$
\underline{a}=\begin{pmatrix}
g\\h\\0
\end{pmatrix}
$$
Where $g,h$ satisfy
$$
ag+bh=l_{1},dg+eh=l_{2}
$$
Which can be solved for $g,h$, if the third component is $\hspace{0pt}0$, the same technique can be used for one of the other components
#### Example
Find a parametric description of the intersection $L=\Pi_{1}\cap \Pi_{2}$ of the planes:
$$
\Pi_{1}:x+y+z=2
$$
$$
\Pi_{2}:2x-y+z=0
$$
We can find $\underline{d}$ by reading off the normal vectors
$$
\underline{d}=\underline{n}_{1}\times \underline{n}_{2}=\begin{pmatrix}
1\\1\\1
\end{pmatrix}\times \begin{pmatrix}
2\\-1\\1
\end{pmatrix}=\begin{pmatrix}
2\\1\\-3
\end{pmatrix}
$$
and then find 
$$
\underline{a}=\begin{pmatrix}
g\\h\\0
\end{pmatrix}\in L
$$
So
$$
g+h=2
$$
$$
 2g-h=0
$$
$$
 \iff h=\frac{4}{3},g=\frac{2}{3}
$$
So
$$
L=\left\{  \begin{pmatrix}
\frac{2}{3}\\ \frac{4}{3}\\0
\end{pmatrix}+\lambda \begin{pmatrix}
2\\1\\-3
\end{pmatrix}|\lambda \in \mathbb{R}  \right\}
$$


#Mathematics #LinAlg 