If $y_{1},y_{2}$ are solutions of a homogeneous [[Linear|linear]] [[Differential Equations|differential equation]], then $y=\alpha y_{1}+\beta y_{2}$ is also a solution
Applying this by induction, we can have for some [[Linear Differential Operators|linear differential operator]] $\mathcal{L}$:
$$
\mathcal{L}\left( \sum_{i=0}^{\infty}a_{i}y_{i} \right)=\sum_{i=0}^{\infty}a_{i}\mathcal{L}y_{i}
$$
But we do have to worry about convergence of this series now
## Proof
For an [[Linear Ordinary Differential Equations|ODE]]:
$$
\frac{d ^{n}y}{dx^{n}} +p_{1}(x)\frac{d ^{n-1}y}{dx^{n-1}} +\dots+p_{n}(x)y
$$
$$
= \frac{d ^{n}}{dx^{n}} (\alpha y_{1}+\beta y_{2})+p_{1}(x)\frac{d ^{n-1}}{dx^{n-1}} (\alpha y_{1}+\beta y_{2})+\dots+p_{n}(x)(\alpha y_{1}+\beta y_{2})
$$
$$
= \alpha \frac{d ^{n}}{dx^{n}} y_{1}+\beta\frac{d ^{n}}{dx^{n}} y_{2}+p_{1}(x)\left( \alpha \frac{d ^{n-1}}{dx^{n-1}}y_{1}+\beta \frac{d ^{n-1}}{dx^{n-1}} y_{2}  \right)+\dots+\alpha p_{n}(x)y_{1}+\beta p_{n}(x)y_{2}
$$
$$
= \alpha\underbrace{ \left( \frac{d ^{n}y_{1}}{dx^{n}}+p_{1}(x)\frac{d ^{n-1}y_{1}}{dx^{n-1}}+\dots+p_{n}(x)y_{1}   \right) }_{ =0 }+\beta\underbrace{ \left( \frac{d ^{n}y_{2}}{dx^{n}}+p_{1}(x)\frac{d ^{n-1}y_{2}}{dx^{n-1}}+\dots+p_{n}(x)y_{2}   \right) }_{ =0 }
$$
$$
= \alpha \times 0+\beta \times 0=0
$$

