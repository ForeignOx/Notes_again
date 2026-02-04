An $n$th order differential operator can be written:
$$
\mathcal{L}=r_{n}(x)\frac{d ^{n}}{dx^{n}} +r_{n-1}(x)\frac{d ^{n-1}}{dx^{n-1}} +\dots+r_{1}(x)\frac{d }{dx} +r_{0}(x)
$$
Just how [[Functions|functions]] are maps from numbers to numbers, $\mathcal{L}$ is a map from a function to a function, so for example:
$$
\mathcal{L}(y(x))=r_{n}(x)\frac{d ^{n}y}{dx^{n}} +r_{n-1}(x)\frac{d ^{n-1}y}{dx^{n-1}} +\dots+r_{1}(x)\frac{d y}{dx} +r_{0}(x)y
$$
It is not only a map, but a [[Linear Maps|linear map]], so
$$
\mathcal{L}(\alpha y_{1}+\beta y_{2})=\alpha \mathcal{L}(y_{1})+\beta \mathcal{L}(y_{2})
$$
So we can think of it as an infinite-[[Dimension|dimensional]] [[Matrices|matrix]] on the [[Vectorspaces|vectorspace]] of all functions
## Example
We can rewrite [[Legendre's Equation|Legendre's equation]]:
$$
(1-x^{2})\frac{d ^{2}y}{dx^{2}} -2x\frac{d y}{dx} +\lambda y=0
$$
As
$$
\underbrace{ \left[ (x^{2}-1)\frac{d ^{2}}{dx^{2}} +2x\frac{d }{dx}  \right] }_{  =\mathcal{L}_{L}}y=\lambda y
$$
## Theorem
If $\left\{ p_{0},p_{1},\dots p_{n} \right\}$ is an [[Orthonormal Vectors|orthonormal]] [[Sets|set]] of polynomials with respect to an [[Inner Product|inner product]] $(,)$ with $\deg(p_{j})=j$ and $\mathcal{L}:\mathbb{R}[x]\to \mathbb{R}[x]$ is a [[Self-Adjoint|self-adjoint]] linear operator with respect to the same inner product such that
$$
\deg(\mathcal{L}(p(x)))\leq \deg(p(x))\forall p(x)\in \mathbb{R}[x]
$$
then each $p_{j}(x)$ is an [[Eigenfunctions|eigenfunction]] of $\mathcal{L}$:
$$
\mathcal{L}(p_{j}(x))=\lambda_{j}p_{j}(x),\lambda_{j}\in \mathbb{R}
$$
