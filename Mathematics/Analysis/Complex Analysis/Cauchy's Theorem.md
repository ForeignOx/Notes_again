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
