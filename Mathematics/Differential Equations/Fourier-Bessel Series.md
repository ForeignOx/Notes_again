We can show a function $f(r,\theta)$ as:
$$
f(r,\theta)=\sum_{n=0}^{\infty}\sum_{k=1}^{\infty}rJ_{n}(\sqrt{ \lambda_{n,k} }r)(A_{n,k}\cos(n\theta)+B_{n,k}\sin(n\theta))
$$
Which is useful for solving PDEs and is similar to representing functions using [[Fourier Series|Fourier series]]
To actually work out the coefficients $A_{n,k},B_{n,k}$ we impose (radial) Bessel [[Orthogonality|orthogonality]]:
$$
\int_{0}^{L_{r}} rJ_{n}(\sqrt{ \lambda_{n,k} }r)J_{n}(\sqrt{ \lambda_{n,k'} }r) \, dr=0\text{ for }k\neq k'
$$
And angular (Fourier) orthogonalityL
$$
\int_{0}^{2\pi} \cos(n\theta)\cos(m\theta) \, d\theta =\int_{0}^{2\pi} \sin(n\theta)\sin(m\theta) \, d\delta=\pi\delta_{mn}
$$
$$
 \int_{0}^{2\pi} \cos(n\theta)\sin(m\theta) \, d\theta =0 
$$
So to get $A_{n,k}$, we multiply both sides of the expansion for $f(r,\theta)$ by $rJ_{n}(\sqrt{ \lambda_{n,k} }r)\cos(n\theta)$ and integrate over the full disk:
$$
\int_{0}^{2\pi} \int_{0}^{L_{r}} rf(r,\theta)J_{n}(\sqrt{ \lambda_{n,k} }r)\cos(n\theta) \, dr\,d\theta 
$$
$$
= \int_{0}^{2\pi} \int_{0}^{L_{r}} rJ_{n}(\sqrt{ \lambda_{n,k} }r)\cos(n\theta)\sum_{n'=0}^{\infty}\sum_{k'=1}^{\infty}J_{n'}(\sqrt{ \lambda_{n',k'}r })(A_{n',k'}\cos(n'\theta)+B_{n',k'}\sin(n'\theta)) \, dr  \, d\theta
$$
Using the orthogonality, all terms vanish except those with $n'=n,k'=k$ and cross terms between $\sin$ and $\cos$ also vanish, soo
$$
\pi A_{n,k}\int_{0}^{L_{r}} r\left(J_{n}(\sqrt{ \lambda_{n,k} }r)\right)^{2} \, dr=\int_{0}^{2\pi} \int_{0}^{L_{r}} rf(r,\theta)J_{n}(\sqrt{ \lambda_{n,k} }r)\cos(n\theta) \, dr  \, d\theta 
$$
$$
\implies A_{n,k}=\frac{\int_{0}^{2\pi} \int_{0}^{L_{r}} rf(r,\theta)J_{n}(\sqrt{ \lambda_{n,k} }r)\cos(n\theta) \, dr  \, d\theta }{\pi\int_{0}^{L_{r}} r\left(J_{n}(\sqrt{ \lambda_{n,k} }r)\right)^{2} \, dr}
$$
If instead you repeat with $rJ_{n}(\sqrt{ \lambda_{n,k} }r)\sin(n\theta)$, you get the $B_{n,k}$ coefficients:
$$
\implies B_{n,k}=\frac{\int_{0}^{2\pi} \int_{0}^{L_{r}} rf(r,\theta)J_{n}(\sqrt{ \lambda_{n,k} }r)\sin(n\theta) \, dr  \, d\theta }{\pi\int_{0}^{L_{r}} r\left(J_{n}(\sqrt{ \lambda_{n,k} }r)\right)^{2} \, dr}
$$
