# Planar Linking Number
An orientation can be assigned to a [[Link Diagrams|link diagram]] by assigning orientations to all its constituent knots. A sign is applied to all mutual crossings, then half the total sum of signs yields the planar linking number
## Definition
Conisder a [[Link Diagrams|link diagram]] $L$ which contains $m$ constituent [[knots|knots]] $\mathcal{K}_{1},\dots,\mathcal{K}_{m}$ (all oriented). If knots $\mathcal{K}_{i}$ and $\mathcal{K}_{j}$ themselves generate $n_{ij}$ mutual crossings, these crossings are labelled $\mathcal{C}_{k}^{ij}$ for $k=1,\dots,n_{ij}$
For each knot pairing we denote the total $\mathcal{L}_{ij}$ between $\mathcal{K}_{i}$ and $\mathcal{K}_{j}$ as the sum of all signed crossings:
$$
\mathcal{L}_{ij}(\mathcal{K}_{i},\mathcal{K}_{j})=\frac{1}{2}\sum_{k=1}^{n_{ij}}\mathcal{S}(\mathcal{C}_{k}^{ij})
$$
And $\mathcal{L}(L)$ represents the sum of all $\mathcal{L}_{ij}$ between all knot combinations. There exists no redundancy in this calculation, so crossings are only counted once:
$$
\mathcal{L}(L)=\sum_{i=1}^{m-1}\sum_{j=i+1}^{m}\mathcal{L}_{ij}
$$
It can be shown that the measure $\mathcal{L}$ is independent of the choice of projection direction
# 3D Linking Number
The extent to which two closed spacecurves $\underline{x}(s)$ and $\underline{y}(s')$ are linked in $\mathbb{R}^{3}$ over $\sin n[0,L]$, $s'\in[0,M]$, can be evaluated as follows:
$$
\mathcal{L}\equiv \frac{1}{4\pi}\oint_{\underline{x}}\oint_{\underline{y}} \frac{\underline{\hat{T}}_{\underline{x}}(s)\times \underline{\hat{T}}_{\underline{y}}(s')\cdot(\underline{x}(s)-\underline{y}(s'))}{\left| \underline{x}(s)-\underline{y}(s') \right| ^{3}}~dsds'
$$
This expression can be applied to open [[ribbons|ribbons]] as well
The equation represents the average of the planar linking number as averaged over all posible projection. Each projection can be thought of as a particular viewing angle of the link
Since the planar linking number can be shown to be independent of viewing angle, $\mathcal{L}$ above is equivalent to the planar linking number. It can be inferred from this that $\mathcal{L}$ must always be of integer value for closed spacecurves
Furthermore, the evaluation of $\mathcal{L}$ is independent of chosen parametrisations
$\mathcal{L}$ is trivially related to the [[crossing number|crossing number]], so
$$
\mathcal{L}=\frac{1}{2}C(\hat{n})
$$
$\mathcal{L}$ as applied to a ribbon $R(\underline{x},\underline{v})(t)$ is invariant to the transformations $t\to-t,s\to-s$; this is a result of both curves reversing simultaneously
