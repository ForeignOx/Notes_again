## Theorem
Every [[Boundedness|bounded]] [[Holomorphicity|entire]] [[complex functions|function]] is constant
### Proof
Let $f$ be entire and let $M$ be such that $\left| f(z) \right|\leq M$
Our strategy is to show that $f(w)=f(0)$ for every $w\in \mathbb{C}$
We shall pick a circular contour of radius $\rho$ with $\left| \rho \right|>w$ we have, by [[Cauchy's integral formula|Cauchy's integral formula]]
$$
\left| f(w)-f(0) \right| =\left| \frac{1}{2\pi i}\oint_{\left| z \right| =\rho} \frac{f(z)}{z-w}~dz-\frac{1}{2\pi i}\oint_{\left| z \right| =\rho} \frac{f(z)}{z}~dz \right| 
$$
$$
= \frac{1}{2\pi} \left| \oint_{\left| z \right| =\rho}f(z)\left(  \frac{1}{z-w} -\frac{1}{z} \right)~dz \right| =\frac{w}{2\pi}\left| \oint_{\left| z \right| =\rho} f(z) \frac{1}{z(z-w)}~dz \right| 
$$
We use the [[ML inequality|ML inequality]]
$$
\leq \frac{\left| w \right| }{2\pi}\cdot 2\pi \rho\cdot\sup_{\left| z \right| =\rho} \left| \frac{f(z)}{z(z-w)} \right| 
$$
Which by assumption,
$$
\leq \left| w \right| \rho \cdot \frac{M}{\rho}\cdot\sup_{\left| z \right| =\rho} \frac{1}{\left| z-w \right| }\leq \left| w \right| M\sup_{\left| z \right| =\rho} \frac{1}{\left| \left| z \right| -\left| w \right|  \right| }= \frac{\left| w \right| M}{\rho-\left| w \right| }
$$
As $\rho\to \infty$, we choose a bigger and bigger circle and $\frac{\left| w \right|M}{\rho-\left| w \right|}\to 0$
So the function is constant

