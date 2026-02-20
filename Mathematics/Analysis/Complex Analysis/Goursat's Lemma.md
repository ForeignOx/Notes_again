## Lemma
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
\frac{f(z)-f(w)}{z-w} & z\in U\setminus \left\{ w \right\}
\end{cases}
$$