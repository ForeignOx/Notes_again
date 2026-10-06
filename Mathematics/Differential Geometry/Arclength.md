## Definition
The arclength of a segment of a curve $\underline{\alpha}:I\to \mathbb{R}^{n}$ given by $\underline{\alpha}|_{[a,b]}$ with $[a,b]\in I$.
We choose a partition of $[a,b]$, that is,
$$
a=u_{0}<u_{1}<\dots<u_{m}=b
$$
And approximaate the length of $\underline{\alpha}:[a,b]\to \mathbb{R}^{n}$By the expression
$$
\sum_{i=0}^{m-1}\lvert \lvert \underline{\alpha}(u_{i+1})-\underline{\alpha}(u_{i}) \rvert \rvert 
$$
Which is nothing but the length of the piecewise linear approxiamtion of $\underline{\alpha}|_{[a,b]}$ by consecutive points $\underline{\alpha}(u_{0}),\underline{\alpha}(u_{1}),\dots ,\underline{\alpha}(u_{m})$ on the curve
If we take a refinement of this partition, the corresponding piecewise linear approximation is closer to the curve, so we take the supremum over all partitions
## Proposition
Let $\underline{\alpha}:I\to \mathbb{R}^{n}$ be a smooth curve, and $[a,b]\subset I$, then the length of $\underline{\alpha}([a,b])$ is given by
$$
L(\underline{\alpha}|_{[a,b]})=\int ^{b}_{a} \lvert \lvert \underline{\alpha}'(u) \rvert \rvert  \, du 
$$
### Justification
We justify this by giving the following heuristics:
$$
    \sum_{i=0}^{m-1} \lvert \lvert \underline{\alpha}(u_{i+1}-\underline{\alpha}(u_{i})) \rvert \rvert =\sum_{i=0}^{m-1}\left\lvert  \left\lvert   \frac{\underline{\alpha}(u_{i+1})-\underline{\alpha}(u_{i})}{u_{i+1}-u_{i}}  \right\rvert  \right\rvert (u_{i+1}-u_{i})\overset{m\to \infty}{\to}\int ^{b}_{a} \lvert \lvert \underline{\alpha}'(u) \rvert \rvert  \, du 
$$
By using the fact that
$$
\lim_{ u_{i+1} \to u_{i} } \frac{\underline{\alpha}(u_{i+1})-\underline{\alpha}(u_{i})}{u_{i+1}-u_{i}}=\underline{\alpha};
$$
