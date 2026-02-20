## Lemma: Goursat's Lemma
Let [[Complex Functions|$f:U\to \mathbb{C}$]] be [[Holomorphicity|holomorphic]] on an [[open sets|open set]] $U$, then for any triangular region $\triangle \subset U$ (inside and boundary), then we have
$$
\int _{\partial\triangle}f(z) \, dz =0
$$
### Proof
Let $\triangle$ be a triangular region on which $f$ is holomorphic. Divide $\triangle$ into four smaller triangular regions $\triangle^{(1)},\triangle^{(2)},\triangle^{(3)},\triangle^{(4)}$ by considering the straight line that connect the midpoints of the sides bounding triangle $\partial\triangle$
![[Pasted image 20260220021621.png]]
We obtain, using properties of [[Contour Integration|contour integrals]]
$$
    \int _{\partial\triangle } f(z) \, dz=\sum_{i=1}^{4}\int _{\partial\triangle^{(i)}}f(z) \, dz  
$$
Since the sids of the smaller internal triangle are traversed twice in opposite directions by the contours (and this means their integral contribution cancels out)
By taking the absolute value and using the [[Triangle Inequality|triangle inequality]], we obtain:
$$
\left| \int _{\partial\triangle}f(z) \, dz  \right| \leq \sum_{i=1}^{4} \left| \int _{\partial\triangle^{(i)}} f(z) \, dz  \right| 
$$
Of these four smaller triangular regions, let $\triangle_{1}$ be the one associated with the maximal integral (that is, the triangular region for which $\left| \int _{\partial\triangle_{1}} f(z) \, dz \right|\geq \int _{\partial\triangle^{(i)}}f(z) \, dz$ for all $i\in\overline{4}$)
We then have
$$
\left| \int _{\partial\triangle} f(z) \, dz  \right| \leq 4\left| \int _{\partial\triangle_{1}}f(z) \, dz  \right| 
$$
Moreover, by construction we have that $L(\partial\triangle_{1})=\frac{1}{2}L(\partial\triangle)$
By repreating this process for $\triangle_{1}$ and so on, we obtain a sequence of triangular regions
$$
\triangle \supset \triangle_{1}\supset \triangle_{2}\supset \dots \supset \triangle_{n} \supset \dots
$$
For which
$$
\left| \int _{\partial\triangle}f(z) \, dz  \right| \leq 4^{n}\left| \int _{\partial\triangle_{n}}f(z) \, dz  \right| 
$$
And 
$$
L(\partial\triangle_{n})=\frac{1}{2^{n}}L(\partial\triangle)
$$
In particular, notice that $L(\partial\triangle_{n})\to 0$ as $n\to\infty$
As the triangles get smaler, they eventually limit to a single point this is due to $\mathbb{C}$ being a complete [[Metric Spaces|metric space]] and Cantor's intersection theorem
That is, $\bigcap_{n\in\mathbb{N}}\triangle_{n}=\left\{ w \right\}$ for some $w\in U$
The next step is to consider the [[Difference Quotient Function|difference quotient function]] 
$$
g(z):=\begin{cases}
\frac{f(z)-f(w)}{z-w} & z\in U\setminus \left\{ w \right\} \\
f'(w) & z=w
\end{cases}
$$
Where $w$ is the limiting point from above, which is continuous
We can consider the integral
$$
\int _{\partial\triangle_{n}}(z-w)(g(z)-g(w)) \, dz 
$$
Noting that $\int _{\partial\triangle_{n}} 1 \, dz=0=\int _{\partial\triangle_{n}}z \, dz$, by the [[Newton-Leibniz theorem|Newton-Leibniz theorem]], because integrands $1$ and $z^{2}$ have holomorphic antiderivatives $z$ and $\frac{z^{2}}{2}$ respectively.
It follows that
$$
\int _{\partial\triangle_{n}} (z-w)(g(z)-g(w)) \, dz=\int _{\partial\triangle_{n}}(f(z)-f(w)-(z-w)g(w)) \, dz 
$$
$$
 =\int _{\partial\triangle_{n}}f(z) \, dz  
$$
Since $w,f(w,g(w))$ are just constants. Therefore, we obtain
$$
\left| \int _{\partial\triangle}f(z) \, dz  \right| \leq 4^{n}\left| \int _{\partial\triangle_{n}}f(z) \, dz  \right| =4^{n}\left| \int _{\partial\triangle_{n}} (z-w)(g(z)-g(w)) \, dz  \right| 
$$
It is easy to see that for $z\in\partial\triangle_{n}$, we have $\left| z-w \right|<L(\partial\triangle_{n})$, since $w$ lies in the interior of the triangular region $\triangle_{n}$. Applying the [[ML inequality|ML inequality]], yields
$$
\left| \int _{\partial\triangle}f(z) \, dz  \right| \leq 4^{n}L(\partial\triangle_{n}) \sup_{z\in \partial\triangle_{n}}\left| (z-w)(g(z)-g(w)) \right| 
$$
$$
 <4^{n}L(\partial\triangle_{n})^{2}\sup_{z\in \partial\triangle_{n}}\left| g(z)-g(w) \right| =L(\partial\triangle)^{2}\sup_{z\in \partial\triangle_{n}}\left| g(z)-g(w) \right| 
$$
The left hand side is independent of $n$, so taking the limit $n\to\infty$ on the right hand side (so that $z\to w$), it follows from the continuity of $g$ that
$$
\sup_{z\in \partial\triangle_{n}}\left| g(z)-g(w) \right| \to \left| g(w)-g(w) \right| =0
$$
Thus
$$
\int _{\partial\triangle}f(z) \, dz=0 
$$
As required
## Remark
This result gives an indication as to the types of domain on which the Cauchy-Goursat theorem will hold. In order to calculate the integral around a triangular contour, we required the integrand to be holomorphpic on the region enclosed by this triangular contour
## Theorem: Cauchy-Goursat Theorem (for Starlike Domains)
If $f:D\to \mathbb{C}$ is holomorphic on a [[Starlike Domains|starlike]] [[Domains|domain]], then for any closed contour $\gamma \subset D$,
$$
\int _{\gamma} f(z)\, dz =0
$$
### Proof
Assume we can show $f$ has a holomorphic antiderivative on $D$, then by [[Newton-Leibniz Theorem|Newton-Leibniz]], $\int _{\gamma}f(z) \, dz=0$ for all closed $\gamma$
Let $a_{0}$ be the central point in our starlike domain, then by definition $\exists L_{z}$ joining $a_{0}$ to $z$
Define $F(z)=\int _{L_{z}}f(\xi) \, d\xi$
By Goursat's Lemma,
$$
\int _{\partial\triangle}f(\xi) \, d\xi 
$$
So
$$
F(z)-F(w)=\int _{L_{z}}f(\xi) \, d\xi -\int _{L_{w}}f(\xi) \, d\xi 
$$
And
$$
0=\int _{\partial\triangle}f(\xi) \, d\xi =\int _{L_{z}\cup(-\delta)\cup (-L_{w})} f(\xi) \, d\xi =\int _{L_{z}}f(\xi) \, d\xi-\int _{L_{w}}f(\xi) \, d\xi-\int _{\delta}f(\xi) \, d\xi   
$$
So yeahh finish this perchance perchance...