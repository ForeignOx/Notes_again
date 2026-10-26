## Definition
Let $\underline{\alpha}:I\to \mathbb{R}^{3}$ be a [[Smooth Functions|smooth]] regular [[Curves|unit speed]] [[Spacecurves|curve]], let $\kappa:I\to \mathbb{R}_{\geq 0}$ be its [[curvature|curvature]]
If $\kappa(u)\neq 0$ for all $u\in I$, then $\underline{b}'(s)$ is parallel to $\underline{n}(s)$ and we define the torsion $\tau:I\to \mathbb{R}$ by
$$
\underline{b}'(s)=\tau(s)\underline{n}(s)
$$
Note that $\tau$ can be positive or negative, and only exists if $\kappa \neq 0$, as then we can't define $\underline{n}$
## Proposition
Let $\underline{\alpha}:I\to \mathbb{R}^{3}$ be a smooth regular curve. Assume that $\kappa(u)\neq 0$, so $\tau(u)$ exists and is given by
$$
\tau(u)=\frac{-(\underline{\alpha}'\times\underline{\alpha}'')\cdot\underline{\alpha}'''}{\lvert \lvert \underline{\alpha}'\times\underline{\alpha}'' \rvert \rvert ^{2}}
$$
### Proof
Let $u_{0}\in I$, 
$$
s=\ell(u)=\int_{u_{0}}^{u} \lvert \lvert \underline{\alpha}'(t) \rvert \rvert \, dt
$$
$u=\ell ^{-1}(s)$, define $\underline{\beta}=\underline{\alpha}\circ\ell ^{-1}:J\to \mathbb{R}^{3}$ be a unit speed parametrisation with same trace as $\underline{\alpha}$. Then
$$
\frac{d u}{ds} =(\ell ^{-1})'(s)=\frac{1}{\lvert \lvert \underline{\alpha}'(u) \rvert \rvert }
$$
For torsion:
$$
\tau_{\underline{\alpha}}(u)=\tau_\underline{\beta}(s)=\underline{b}_{\underline{\beta}}'(s)\times  \underline{n}_{\underline{\beta}}(s)
$$
As it should be independent of parametrisation. We then have
$$
\underline{n}_{\underline{\beta}}(s)=\frac{1}{\lvert \lvert \underline{t}_{\underline{\alpha}}'(u) \rvert \rvert }\underline{t}_{\underline{\alpha}}'(u)=\frac{1}{\lvert \lvert \underline{t}'_{\underline{\alpha}}(u) \rvert \rvert }\left( \frac{\underline{\alpha}'}{\lvert \lvert \underline{\alpha} \rvert \rvert } \right)'(u)
$$
And
$$
\underline{b}_{\underline{\beta}}'(s)=\frac{d }{ds} \underline{b}_{\underline{\alpha}}(u(s)) 
$$
$$
= \underline{b}'_{\underline{\alpha}}\frac{d u}{ds} =  \frac{\underline{b}_{\underline{\alpha}}'(u)}{\lvert \lvert \underline{\alpha}'(u) \rvert \rvert }
$$
And
$$
\underline{\beta}_{\underline{\alpha}}=\underline{b}_\underline{\beta}(s)=\underline{t}_{\underline{\beta}}(s)\times   \underline{n}_{\underline{\beta}}(s 
$$
$$
= \underline{t}_{\underline{\alpha}}(u)\times \left( \frac{1}{\lvert \lvert \underline{t}'_{\underline{\alpha}}(u) \rvert \rvert } \left( \frac{\underline{\alpha}'}{\lvert \lvert \underline{\alpha} \rvert \rvert } \right)'\underline{\alpha}' \right)
$$

=]




























































































































































































































































