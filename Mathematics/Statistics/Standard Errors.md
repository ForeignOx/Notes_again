If we have an unknown distribution, but we know $\mu$ and $\sigma$, we can use the central limit theorem to estimate them, but we need to know $\sigma^{2}$ for this, and we often don't (we may in the case of scientific equipment)
## If $\sigma$ is unknown and $n$ is large
We just estimate the population standard deviation by the sample standard deviation in terms of random variables $S$:
$$
S=\sqrt{ \frac{1}{n-1}\sum_{ i=1} ^{ n}  (X_{i}-\bar{X})^{2} }=\sqrt{ \frac{1}{n-1}\left( \sum_{ i=1} ^{ n}  (X_{i}^{2})-n\bar{X}^{2} \right)}
$$
After the data has veen measured, it becomes $s$:
$$
s=\sqrt{ \frac{1}{n-1}\sum_{ i=1} ^{ n}  (x_{i}-\bar{x})^{2} }=\sqrt{ \frac{1}{n-1}\left( \sum_{ i=1} ^{ n}  x_{i}^{2}-n\bar{x}^{2} \right) }
$$
Under certain conditions, $E(S^{2})=\sigma^{2}$, but $S^{2}$ so $S^{2}$ is an unbiased estimator for $\sigma^{2}$ (which is why we need the factor of $\frac{1}{n-1}$ instead of $\frac{1}{n}$). One can think of it in terms of degrees of freedom, since we have a fixed $\bar{x}$, there are only $n-1$ things that can vary
So we estimate the standard deviation of the sample mean $\bar{x}$, $\frac{\sigma}{\sqrt{ n }}$ by the "standard error of the sample mean" $\frac{s}{\sqrt{ n }}$
Putting this into the central limit theorem (valid for largeish $n$):
$$
\bar{X}\sim N\left( \mu, \frac{\sigma^{2}}{n} \right)\iff \bar{X}-\mu \sim N\left( 0, \frac{\sigma^{2}}{n} \right)
$$
$$
 \iff \frac{\bar{X}-\mu}{\frac{\sigma}{\sqrt{ n }}}\sim N(0,1)
$$
Now replace with $\frac{s}{\sqrt{ n }}$ (valid for largerish $n$)
$$
\iff  \frac{\bar{X}-\mu}{\frac{S}{\sqrt{ n }}}\sim N(0,1)
$$
However if $n$ is not sufficientlly large, then $s$ is a poor estimate for $\sigma$, and $\frac{\bar{X}-\mu}{\frac{S}{\sqrt{ n }}}$ is no longer normally distributed :(