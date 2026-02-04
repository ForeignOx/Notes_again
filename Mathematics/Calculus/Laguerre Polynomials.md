If we are looking for an [[Orthonormal Vectors|orthonormal]] [[Basis|basis]] of $\mathbb{R}[x]_{n}$ with respect to the [[Inner Product|inner product]]
$$
(p,q)=\int ^{\infty}_{0} e^{ -x } p(x)q(x) \, dx
$$
Using [[Gram-Schmidt Procedure|Gram-Schmidt]], we get the polynomial solutions to be Laguerre polynomials
These have a [[Self-Adjoint|self-adjoint]] [[Linear Maps|linear operator]] associated with it:
$$
\mathcal{L}_{La}f=xf''+(1-x)f'
$$
## Proof of Self-Adjointness
We need to show:
$$
(\mathcal{L}_{La}(f),g)=(f,\mathcal{L}_{La}(g))
$$
$$
(\mathcal{L}_{La}f,g)=\int_{0}^{\infty} e^{ -x }(xf''+(1-x)f')g \, dx 
$$
$$
= \int_{0}^{\infty} \frac{d }{dx} (xe^{ -x }f')g \, dx =[xe^{ -x }f'g]_{0}^{\infty}-\int_{0}^{\infty} xe^{ -x }f'g' \, dx
$$
And if $f,g\in\mathbb{R}[x]$, then $[xe^{ -x }f'g]_{0}^{\infty}=0$, so
$$
(\mathcal{L}_{La}(f),g)=-\int_{0}^{\infty} xe^{ -x }f'g' \, dx =(\mathcal{L}_{La}(g),f)=(f,\mathcal{L}_{La}(g))
$$
