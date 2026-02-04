Bessel's Equation is a [[Second Order Ordinary Differential Equations|second order ODE]]:
$$
r^{2} \frac{d R}{dr} +r \frac{d R}{dr} +(\lambda r^{2}-n^{2})R=0
$$
We solve this using the [[Frobenius' Method|Frobenius' method]], so we asume:
$$
R=\sum_{n=0}^{\infty}a_{n}r ^{ n+\alpha}
$$
Then go ahead and do the long-winded process... to get
$$
J_{n}(x)=\sum_{m=0}^{\infty} \frac{(-1)^{m}}{m!\Gamma(m+n+1)}\left( \frac{x}{2} \right)^{2m+n}
$$
Which is a [[Convergence|convergent]] [[Power Series|power series]] around $x=0$, there is no analytic formula :(
A critical point is that there is one function for each integer $n$ which correspond to the different $\theta$ modes $\cos(n\theta),\sin(n\theta)$
## Derivatives
$$
\frac{ \partial  }{ \partial x } (x^{n}J_{n}(x))=x^{n}J_{n-1}(x)
$$
$$
 \frac{ \partial  }{ \partial x } (x^{-n}J_{n}(x))=-x^{-n}J_{n+1}(x)
$$
(this is our equivalent to $\sin'=\cos,\cos'=-\sin$)
## Orthogonality
The functions $J_{n}(x)$ are [[Orthogonality|orthogonal]] on the interval $[0,L_{r}]$ with respect to the weight $x$ over their zeros $j_{n,k}$:
$$
\int _{0}^{L_{r}}xJ_{n}\left( \frac{j_{n,k}x}{L_{r}} \right)J\left( \frac{J_{n,m}x}{L_{r}} \right) \, dx =\frac{L_{r}^{2}}{2}(J_{n+1}(j_{n,k}))^{2}\delta_{km}
$$
And the zeros $j_{n,k},J_{n}(j_{n,k})=0$ determine the [[Eigenvalues|eigenvalues]] $\left( \frac{\lambda_{n,k}}{L_{r}} \right)^{2}$