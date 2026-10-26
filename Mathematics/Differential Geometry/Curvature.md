## Motivation
We want a quantitative characterisation of the shape of a curve at every point. This goal leads to the notion of curvature $~\kappa$. Desired properties of $\kappa$ are:
- $\kappa=0$ for all points on a straight line,
- $\kappa$ at a point of the curve should be independent of the parametrisation
- $\kappa\to0$ for points on increasing circles
- $\kappa=\pm \frac{1}{r}$ for points on circles of radius $r$
It happens that curvature is related to the change of unit vector
# [[Plane Curves|Plane Curves]]
Since for a unit speed plane curve $\underline{\alpha}$, $\underline{t}'(s)$ is a multiple of $\underline{n}(s)$, we define the curvature of $\underline{\alpha}$ at $s$ as the proportionality factor.
### Definition
The (signed) curvature $\kappa(s)$ of a unit speed plane curve $\underline{\alpha}:I\to \mathbb{R}^{2}$ at $s \in I$ is defined by
$$
\underline{t}'(s)=\kappa(s)  \underline{n}(s)
$$
### Remark
For a given unit speed plane curve $\underline{\alpha}:I\to \mathbb{R}^{2}$, we can compute $\kappa(s)$ for $\sin n I$ via
$$
\underline{t}'(s)\cdot  \underline{n}(s)=\kappa(s)  \underline{n}(s)\cdot  \underline{n}(s)=\kappa(s)\lvert \lvert  \underline{n}(s) \rvert \rvert ^{2}=\kappa(s)
$$
So if $\underline{t}(s)=(x(s),y(s))$, then $\underline{n}'(s)=(-y(s),x(s))$ and $\underline{t}'(s=(x'(s),y'(s)))$$, soo
$$
\kappa(s)=\underline{t}'(s)  \underline{n}(s)=(x'(s),y'(s))\cdot(-y(s),x(s))=-x'(s)y(s)+y'(s)x(s)
$$
## Proposition
Let $\underline{\alpha}:I\to \mathbb{R}^{2}$ be a smooth regular plane curve with $\underline{\alpha}(u)=(x(u),y(u))$ (not necessarily parametrised by arclength), we have
$$
\kappa=\frac{x'y''-x''y'}{((x')^{2}+(y')^{2})^{\frac{3}{2}}}
$$
### Proof
The idea is that curv ature does not depend on parametrisation, so we need to do a change of variable. Let $u_{0}\in I$,
$$
s=\ell(u)=\int _{u_{0}}^{u}\lvert \lvert \underline{\alpha}'(t) \rvert \rvert  \, dt 
$$
Write $\underline{\beta}=\underline{\alpha}\circ \ell ^{-1}$ to get a unit speed parametrisation, so $\kappa_{\underline{\alpha}}(u)=\kappa_{\underline{\beta}}(s)$, where $s=\ell(u)$, so
$$
t'(s)=\kappa_{\underline{\beta}}(s) \underline{n}(s)\iff \underline{t}'(\ell(u))=\kappa_{\underline{\beta}}(\ell(u))  \underline{n}(\ell(u))
$$
Then
$$
\underline{t}(s)=\underline{\beta}'(s)=(\underline{\alpha}\circ \ell ^{-1})'(s)=\underline{\alpha}'(\ell ^{-1}(s))(\ell ^{-1})'(s)
$$
We know that
$$
(\ell ^{-1})'(s)=\frac{1}{\lvert \lvert \underline{\alpha}'(\ell ^{-1}(s)) \rvert \rvert }
$$
So
$$
\underline{\alpha}(u)=(x(u),y(u))
$$
$$
\implies\underline{\alpha}'(u)=(x'(u),y'(u))
$$
$$
 \underline{t}(s)=\frac{(x'(u),y'(u))}{\lvert \lvert \underline{\alpha}'(u) \rvert \rvert } 
$$
$$
 \underline{n}(s)=\frac{(-y'(u),x'(u))}{\lvert \lvert \underline{\alpha}'(u) \rvert \rvert }
$$

We now want to find
$$
\frac{d \underline{t}}{ds} =\frac{d \underline{t}}{du} \frac{d u}{ds} =\frac{1}{\lvert \lvert \underline{\alpha}'(\ell ^{-1}(s)) \rvert \rvert }\frac{d \underline{t}(u)}{du}
$$
$$
  =\frac{1}{((x')^{2}+(y')^{2})^{\frac{1}{2}}} \frac{d }{du} \left( \frac{(x'(u),y'(u))}{\sqrt{ (x'(u)^{2}+y'(u)^{2}) }} \right)
$$
$$
= \frac{1}{\sqrt{ (x')^{2}+(y')^{2} }}\left( \frac{(x''(u),y''(u))}{\sqrt{ (x')^{2}+(y')^{2} }}-\frac{1}{2}(2x'x''+2y'y'') \frac{(x',y')}{ ((x')^{2}+(y')^{2})^{\frac{3}{2}}} \right) 
$$
$$
= \frac{((x')^{2}+(y')^{2})(x'',y'')-(x'x''+y'y'')(x',y')}{((x')^{2}+(y')^{2})^{2}} 
$$
$$
= \frac{((y')^{2}x''-x'y'y'',(x')^{2}y''-x'y'x'')}{((x')^{2}+(y')^{2})^{2}} 
$$
$$
= \frac{(x'y''-y'x'')}{((x')^{2}+(y')^{2})^{\frac{3}{2}}} \underbrace{ \frac{(-y',x')}{((x')^{2}+(y')^{2})^{\frac{1}{2}}} }_{ = \underline{n}(s) }
$$
Soooo
$$
\kappa=\frac{x'y''-y'x''}{ ((x')^{2}+(y')^{2} )^{\frac{3}{2}}}
$$
## Example
Take an ellipse $\underline{\alpha}(u)=(a\cos u,b\sin u)$, so
$$
\underline{\alpha}'(u)=(-a\sin u,b\cos u),~~\underline{\alpha}''(u)=(-a\cos(u),-b\sin(u))
$$
We can't work out the arclength, since, choosing $u_{0}=0$, it is equal to the elliptic integral:
$$
\int _{0}^{u}\sqrt{ a^{2}\sin ^{2}u+b^{2}\cos ^{2}u } \, du 
$$
Which cannot be expressed in closed form, so to find it's curvature, we can use the proposition
So
$$
\kappa(u)=\frac{x'y''-x''y'}{((x')^{2}+(y')^{2})^{\frac{3}{2}}} = \frac{(-a\sin u)(-b\sin u)-(-a\cos u)(b\cos u)}{((-a\sin(u))^{2}+(b\cos(u))^{2})^{\frac{3}{2}}} 
$$
$$
= \frac{ab\sin ^{2}(u)+ab \cos ^{2} u}{(a^{2}\sin ^{2} u+b^{2}\cos ^{2} u)^{\frac{3}{2}}} 
$$
$$
= \frac{ab}{(a^{2}\sin ^{2}u+b^{2}\cos ^{2}u)^{\frac{3}{2}}}
$$
Note that this expression simplifies to $\frac{r^{2}}{r^{3}}=\frac{1}{r}$ in the special case $a=b=r$, so that fits with curvature of circle
## Remark
A geometric interpretation of curvature $\kappa(u)$ of a smooth regular plane curve $\underline{\alpha}$ at $\underline{\alpha}(u)$ is that $\left| \kappa(u) \right|$ is the reciprocal of the radius of a circle approximating a small neighbourhood $\underline{\alpha}([u-\varepsilon,u+\varepsilon])$ as best as possible (the circle has at least 3-point contact with the curve), and the sign of $\kappa(u)$ determines whether the circle is on the left or right of $\underline{\alpha}(u)$. This approximating circle is called the curvature circle at $\underline{\alpha}(u)$
## Definition
Let $\underline{\alpha}:I\to \mathbb{R}^{2}$ be asmooth regular plane curve, $\kappa:I\to \mathbb{R}$ be its curvature function and $\underline{n}:I\to \mathbb{R}^{2}$ be its unit normal vector. Assume $\kappa(u)\neq 0$, then the radius of curvature is given by
$$
r(u)=\frac{1}{\left| \kappa(u) \right| }
$$
And
$$
e(u)=\underline{\alpha}(u)+\frac{1}{\kappa(u)} \underline{n}(u)\in  \mathbb{R}^{2}
$$
Is called the centre of curvature of $\underline{\alpha}$ at $\underline{\alpha}(u)$. The corresponding curvature circle of $\underline{\alpha}$ at $\underline{\alpha}(u)$ is given by
$$
\left\{ P \in \mathbb{R}^{2}:\middle|: \lvert \lvert P-e(u) \rvert \rvert =r(u) \right\}
$$
## Lemma
Let $\underline{\alpha}:I\to \mathbb{R}^{2}$ be a smooth unit speed plane curve and $\kappa:I\to \mathbb{R}$ be its curvature function, then we have
$$
\underline{t}'(s)=\kappa(s) \underline{n}(s)
$$
$$
 \underline{n}'(s)=\underline{t}(s)\begin{pmatrix}
0 & 1 \\
-1  & 0
\end{pmatrix}
$$
### Proof
The first equation is the definition of curvature
Since we obtain by differentiation and $\underline{n}(s)=\underline{t}(s)\begin{pmatrix}0 & 1 \\-1 & 0 \end{pmatrix}$ 
$$
\underline{n}'(s)=\underline{t}'(s)\begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix}
$$
$$
=\kappa(s)\underline{n}(s)\begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix}
$$
$$
= \kappa(s)\underline{t}(s)\begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix}^{2}=-\kappa(s)\underline{t}(s)
$$
### Remark
Geometrically, we can think of the pair $\underline{t}(s), \underline{n} (s)$ as being a frame of two orthornormal basis vectors moving along the plane curve $\underline{\alpha}(s)$ and the above lemma descrive the relation between these two moving vectors
___
The orthonormal frame $\underline{t}(u), \underline{n}(u)$ along $\underline{\alpha}(u)$ exists also for smooth regular plane curves which are not unit speed, however, in this case, the frame equations above do not hold without taking the speed of the curve into account
# Spacecuves
Let $\underline{\alpha}:I\to \mathbb{R}^{3}$ be a smooth unit speed spacecurve and $\underline{t}(s)=\underline{\alpha}'(s)$ be its unit tangent vector. The curvature of $\underline{\alpha}$ at $\underline{\alpha}(s)$ is thus defined as:
$$
\kappa(s)=\lvert \lvert \underline{t}'(s) \rvert \rvert =\lvert \lvert \underline{\alpha}''(s) \rvert \rvert 
$$
## Remark
Since any plane curve $\underline{\alpha}:I\to \mathbb{R}^{2}$ can be viewed as a spacecurve $\underline{\tilde{\alpha}}(u)=(x(u),y(u),0)$, it is natural to consider the relation between these? and it turns out we have $\kappa_{\underline{\tilde{a}}}=\left| \kappa_{\underline{a}} \right|$ 
## Proposition
Let $\underline{\alpha}:I\to \mathbb{R}^{3}$ be a smooth regular spacecurve, then 
$$
\kappa(u)=\frac{\lvert \lvert \underline{\alpha}'\times\underline{\alpha}'' \rvert \rvert }{\lvert \lvert \underline{\alpha}' \rvert \rvert ^{3}}
$$
### Proof
Let $u_{0}\in I$, 
$$
s=\ell(u)=\int_{u_{0}}^{u} \lvert \lvert \underline{\alpha}'(t) \rvert \rvert \, dt
$$
$u=\ell ^{-1}(s)$, define $\underline{\beta}=\underline{\alpha}\circ\ell ^{-1}:J\to \mathbb{R}^{3}$ be a unit speed parametrisation with same trace as $\underline{\alpha}$. Then
$$
\frac{d u}{ds} =(\ell ^{-1})'(s)=\frac{1}{\lvert \lvert \underline{\alpha}'(u) \rvert \rvert }
$$
