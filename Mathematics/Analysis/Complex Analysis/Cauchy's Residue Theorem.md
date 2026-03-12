## Theorem
Suppose [[Complex Functions|$f$]] is [[Meromorphicity|meromorphic]] on and inside a simple closed contour $f$, and assume $f$ has no [[Poles|pole]] on $\gamma$, then
$$
\oint_{\gamma}f(z)~dz = 2\pi i \sum_{j=1}^{m}\mathrm{Res}_{z=a_{j}}(f)
$$
Where $a_{1},\dots,a_{m}$ are the poles of $f$ inside $\gamma$
### Proof
If $S_{\gamma}=\left\{ a_{1},\dots,a_{m} \right\}$ is the set of poles inside the countour is empty, we are done, by [[Cauchy-Goursat Theorem|Cauchy-Goursat]],
Otherwise for each pole $z=a_{j}$, we have a [[Laurent Series|Laurent series]] around $z=a_{j}$ on some ball. Let
$$
pp_{j}(z)=\sum_{n=-k_{j}}^{-1}c_{n,j}(z-a_{j})^{n}
$$
Be the principle parts of the Laurent series around $z=a$
Each $pp_{j}(z)$ is just a finite sum of reciprocals of $(z-a_{j})$, so these extend to holomorphic functions on $\mathbb{C}\setminus \left\{ a_{j} \right\}$
It makes sense to consider
$$
\oint_{\gamma} pp_{j}(z)~dz=\oint_{\gamma}\sum_{n=-k}^{-1} c_{n,j}(z-a_{j})^{n}~dz  
$$
$$
= \sum_{n=-k}^{-1} c_{n,j}\oint_{\gamma}(z-a_{j})^{n}~dz=2\pi i c_{-1,j}=2\pi i\mathrm{Res}_{z=a_{j}}(f)
$$
Cauchy considered
$$
g(z)=f(z)-\sum_{j=1}^{m}pp_{j}(z)
$$
$$
\implies g(z)=f(z)-pp_{i}(z)-\sum_{j\neq i} pp_{j}(z)=ap_{i}(z)-\sum_{j\neq i}pp_{j}(z)
$$
Where $ap_{i}$ is the analytic part of $f$ at $z=a_{i}$ and all the principle parts at $a_{j}$ where $j\neq i$ must all be holomorphic at $a_{i}$, so by Cauchy-Goursat,
$$
0=\oint_{\gamma}g(z)~dz
$$
=oint