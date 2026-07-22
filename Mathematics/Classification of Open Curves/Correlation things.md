## Correlation between details and writhe
### Local Writhe density and local detail coefficient
Let the detail coefficents at level $m$ be:
$$
\underline{d}^{(m)}=\begin{pmatrix}
\underline{d}_{1} & \underline{d}_{2} & \dots & \underline{d}_{\frac{N}{2}}
\end{pmatrix}
$$
We can define a metric for writhe density per edge as
$$
w_{i}=\sum_{j}\left| K_{ij} \right| 
$$
Which is the total amount of pairwise writhe in which edge $i$ participates, then we compare a detail coefficient with the writhe from the two edges it produces; which we represent with:
$$
W_{k}=\frac{1}{2}(w_{2k-1}+w_{2k})
$$
And we find $\mathrm{corr}(\left| d_{k} \right|,W_{k})$ which informs us whether edges carrying a lot of writhe also carry large geometric detail
### Correlation between writhe change and Detail Coefficient
Consider the writhe change:
$$
\Delta w_{i}(t)=w_{i}(t+\tau)-w_{i}(t)
$$
And we can form our average:
$$
\Delta W_{k}(t)=\frac{1}{2}(\Delta w_{2k}(t)+\Delta w_{2k-1}(t))
$$
And we can investgate the correlation $\mathrm{corr}(\left| d_{i}(t)\left| , \right|\Delta W_{k}(t) \right|)$ for different amounts of lag $\tau$, which should give us information as to whether large detail coefficients predict where writhe will change later
### Correlation between detail coefficient and pair increment
Instead of using the total writhe per edge, we could use the pair increment matrices, for edge $i$;
$$
p_{i}=\sum_{j}\left| \Delta K_{ij} \right| 
$$
