## Theorem
Let [[Complex Functions|$f:U\to \mathbb{C}$]] be [[Holomorphicity|holomorphic]] on some ball $B_{r}(a)$ then $f$ can be represented by a [[power series|power series]], which we call the [[Taylor Series|Taylor series]] of $f$ at point $a$, on $B_{r}(a)$:
$$
f(w)=\sum_{n=0}^{\infty} c_{n}(a-a)^{n}
$$
In particular, $f$ is infinitely many times complex [[Differentiation|differentiable]] at $a$ and
$$
c_{n}= \frac{f^{(n)}(a)}{n!}=\frac{1}{2\pi i}\int _{\left| z-a \right| =\rho} \frac{f(z)}{(z-a)^{n+1}}\, dz 
$$
For any $0<\rho<r$
### Proof
We know by Cauchy's integral formula,
$$
    f(w)=\frac{1}{2\pi i} \int _{\gamma} \frac{f(z)}{z-w} \, dz = \frac{1}{2\pi i}\int _{\gamma} \frac{f(z)}{z-a}\sum_{n=0}^{\infty}\left( \frac{w-a}{z-a} \right)^{n} \, dz 
$$
$$
= \sum_{n=0}^{\infty} \underbrace{ \frac{1}{2\pi i} \int _{\gamma} \frac{f(z)}{(z-a)^{n+1}} \, dz  }_{ =c_{n} }(w-a)^{n}
$$
## Corollary: Holomorphic Functions have Infinitely Many Holomorphic Derivatives
If $f:U\to \mathbb{C}$ is holomorphic on an [[Open Sets|open set]] $U$, then it has derivatives of all orders and they are all holomorphic
Essentiallyy holomorphic functions are equivalent to [[Analytic Functions|analytic functions]] holey moley
## Example
$e^{ z }$ can be represented as:
$$
e^{ z }=\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}z^{n}=\sum_{n=0}^{\infty} \frac{z^{n}}{n!}
$$
## Corollary: Cauchy's Derivative Formula
Suppose $f$ is holomorphic on some ball $B_{r}(a)$, then
