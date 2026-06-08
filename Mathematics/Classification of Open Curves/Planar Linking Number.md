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