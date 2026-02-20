## Definition
Suppose [[Complex Functions|$f:U\to \mathbb{C}$]] is [[Holomorphicity|holomorphic]] on an [[Open Sets|open set]]. Then the difference quotient function $g:U\to \mathbb{C}$ given (for any $w\in U$):
$$
g(z)=\begin{cases}
 \frac{f(z)-f(w)}{z-w} & z\in  U\setminus \left\{ w  \right\} \\
f'(w) & z=w
\end{cases}
$$
Is holomorphic on $U\setminus \left\{  w \right\}$ and [[Continuity|continuous]] at $z=w$
### Proof
The function is clearly holomorphic on $U\setminus \left\{ w \right\}$ since it is the quotient of two holomorphic functions and $z-w\neq 0$
By the definition of the derivative $f'(w)$, we have
$$
\lim_{ z \to w } g(z)=\lim_{ z \to w } \frac{f(z)-f(w)}{z-w}=f'(w)=g(w)
$$
So the function $g$ is continuous at the point $w$