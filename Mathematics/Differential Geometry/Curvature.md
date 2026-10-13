## Motivation
We want a quantitative characterisation of the shape of a curve at every point. This goal leads to the notion of curvature $~\kappa$. Desired properties of $\kappa$ are:
- $\kappa=0$ for all points on a straight line,
- $\kappa$ at a point of the curve should be independent of the parametrisation
- $\kappa\to0$ for points on increasing circles
- $\kappa=\pm \frac{1}{r}$ for points on circles of radius $r$
It happens that curvature is related to the change of unit vector
## [[Plane Curves|Plane Curves]]
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
\kappa=\frac{x'y''-y'x''}{\sqrt{ (x')^{2}+(y')^{2} }}
$$
## Example
Take an ellipse $\underline{\alpha}(u)=(a\cos u,b\sin u)$