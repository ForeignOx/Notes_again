 To prove a vesion of Cauchy's theorem, Goursat observed:
## Lemma: Continuity of the Difference Quotient Function
Suppose [[Complex Functions|$f:U\to \mathbb{C}$]] is [[Holomorphicity|holomorphic]] on an [[Open Sets|open set]]. Then the difference quotient function $g:U\to \mathbb{C}$ given (for any $w\in U$):
$$
g(z)=\begin{cases}
 \frac{f(z)-f(w)}{z-w} & z\in  U\setminus \left\{ w  \right\} \\
f'(w) & z=w
\end{cases}
$$
Is holomorphic on $U\setminus \left\{  w \right\}$ and continuous at $z=w$
### Proof
Trivial
## Lemma: Goursat's Lemma
Let $f:U\to \mathbb{C}$ be holomorphic on an open set $U$, then for any triangular region $\triangle \subset U$ (inside and boundary), then we have
$$
\int _{\partial\triangle}f(z) \, dz =0
$$
### Proof
Let $\triangle$ be a triangular region on which $f$ is holomorphic. Divide $\triangle$ into smaller triangles
## Theorem: Cauchy-Goursat's Theorem (for Starlike Domains)
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
## Cauchy's Integral Formula
