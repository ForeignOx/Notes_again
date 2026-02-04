# For Norms
## Real Case
Suppose we have a [[Vectorspaces|vectorspace]] $V$, with real [[Inner Product|inner product]] $(,)$; a real [[Inner Product Spaces|inner product space]], then $\forall \underline{u},\underline{v}\in V$,
$$
(\underline{u},\underline{v})^{2}\leq(\underline{u},\underline{u})(\underline{v},\underline{v})
$$
$$
\implies \left| (\underline{u},\underline{v}) \right| \leq \lvert \lvert \underline{u} \rvert \rvert \lvert \lvert \underline{v} \rvert \rvert 
$$
Where $\lvert \lvert . \rvert \rvert$ is the [[Norms|norm]] induced by the inner product
We get equallity iff $\underline{u},\underline{v}$ are [[Linear Independence|linearly independent]] 
### Proof
If $\underline{v}= \underline{0}$, it's trivial, so let's assume $\underline{v}\neq  \underline{0}$, so $\lvert \lvert \underline{v} \rvert \rvert\neq 0$
Consider:
$$
\underline{w}=\underline{u}- \frac{(\underline{u},\underline{v})}{\lvert \lvert \underline{v} \rvert \rvert ^{2}}\underline{v}
$$
Which is a [[Linear Combinations|linear combination]] of $\underline{u},\underline{v}$, so $\underline{w}\in V$, so
$$
0\leq \lvert \lvert \underline{w} \rvert \rvert ^{2}=(\underline{w},\underline{w})=\left( \underline{u}-\frac{(\underline{u},\underline{v})}{\lvert \lvert \underline{v} \rvert \rvert ^{2}}\underline{v}, \underline{u}-\frac{(\underline{u},\underline{v})}{\lvert \lvert \underline{v} \rvert \rvert ^{2}}\underline{v}\right)
$$
$$
= (\underline{u},\underline{u})-\frac{2(\underline{u},\underline{v})^{2}}{\lvert \lvert \underline{v} \rvert \rvert ^{2}}+ \frac{(\underline{u},\underline{v})^{2}}{\lvert \lvert \underline{v} \rvert \rvert ^{2}}=(\underline{u},\underline{u})- \frac{(\underline{u},\underline{v})^{2}}{(\underline{v},\underline{v})}\geq 0
$$
So, since $(\underline{v},\underline{v})\geq 0$, we get our result:
$$
(\underline{u},\underline{u})(\underline{v},\underline{v})\geq (\underline{u},\underline{v})^{2}
$$
We get equality iff $\lvert \lvert \underline{w} \rvert \rvert=0\iff \underline{w}= \underline{0}$, but then:
$$
\underline{u}=\frac{(\underline{u},\underline{v})}{\lvert \lvert \underline{v} \rvert \rvert ^{2}} \underline{v}
$$
So $\underline{u},\underline{v}$ would not be linearly independent
## Complex Case
If $\left\{ V,\left< , \right> \right\}$ is a [[Complex Numbers|complex]] inner product space, with $\lvert \lvert . \rvert \rvert$ being the norm induced by the [[Hermitian Inner Product|hermitian inner product]] $\left< , \right>$, then
$$
\left| \left< \underline{u},\underline{v} \right>  \right| ^{2}\leq \lvert \lvert \underline{u} \rvert \rvert ^{2}\lvert \lvert \underline{v} \rvert \rvert ^{2}
$$
$\forall \underline{u},\underline{v}\in V$, with equality when $\underline{u},\underline{v}$ are linearly dependent.
# For Probability
Let $X$ and $Y$ be [[Random Variables|random variables]] with finite [[Expectation|expectation]] for their second [[Moment (in Probability)|moments]], $\mathbb{E}(\left| X \right|^{2})<\infty$ and $\mathbb{E}(\left| Y \right|^{2})<\infty$, then
$$
\mathbb{E}(XY)\leq \sqrt{ \mathbb{E}(X^{2})\mathbb{E}(Y^{2}) }
$$
### Proof
Without loss of generality, we may and shall assume that $\mathbb{E}(\left| X \right|^{2})$ and $\mathbb{E}(\left| Y \right|^{2})$ are positive, as otherwise $X$ or $Y$, and therefore $XY$ vanish with probability 1
For positive $\lambda$, considwer the random variable $(X-\lambda Y)^{2}\geq 0$, the latter has non-negative expectation, equivalently,
$$
0\leq \mathbb{E}(X^{2})-2\lambda \mathbb{E}(XY)+\lambda^{2}\mathbb{E}(Y^{2})
$$
By rearranging and simplifying we get
$$
\mathbb{E}(XY)\leq \frac{1}{2\lambda}\mathbb{E}(X^{2})+\frac{\lambda}{2}\mathbb{E}(Y^{2})
$$
Setting $\lambda=\sqrt{ \frac{\mathbb{E}(X^{2})}{\mathbb{E}(Y^{2})} }$ gives us our inequality
## Remark
If $\mathbb{E}(X^{4})\leq C$ and $\mathbb{E}(Y^{4})\leq C$ for some finite constant $C\geq 0$, then the Cauchy-Schwarz inequality gives $\mathbb{E}(X^{2}Y^{2})\leq C$ as well






#Mathematics #LinAlg 