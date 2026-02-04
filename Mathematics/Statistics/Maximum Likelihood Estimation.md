Why is [[Likelihood|likelihood]] useful? Many reasons, but a major one is that it gives us a way to find good estimators for $\theta$
This procedure is known as the Maximum Likelihood Estimation; we just find the value of $\theta$ that maximises $\ell(\theta)$ for the given sample $x_{1},\dots,x_{n}$
We typically denote this as $\hat{\theta}_\text{MLE}$ (where MLE stands for Maximum Likelihood Estimator)
$$
\hat{\theta}_\text{MLE} \equiv \arg\max_{\theta}  \ell(\theta)=\arg\max_{\theta}\mathscr{L}(\theta)
$$
Note that the $\hat{\theta}_\text{MLE}$ maximises both $\ell(\theta)$ and $\mathscr{L}(\theta)$ as $\log$ is a [[Monotonic Functions|monotonic]] transform (so it can't change the location of the maximum)
This is a very general technique. As we can find $\hat{\theta}_\text{MLE}$ for general data $x_{1},\dots,x_{n}$ we consider it a full estimator. In general MLEs have good properties, especially for large $n$, but note that they are not always unbiased
## MLE for Bernoulli
For Bernoulli Trials, we know that 
$$
\mathscr{L}(p)=x\log p+(n-x)\log(1-p)
$$
And we found:
$$
\frac{ \partial \mathscr{L}(p) }{ \partial p }=\frac{x}{p}-\frac{n-x}{1-p}=0 \iff \hat{p}_\text{MLE} =\frac{x}{n} 
$$
Note that to ensure this is a maximum, we should also check the second derivative:
$$
\frac{ \partial^{2}\mathscr{L}(p) }{ \partial p^{2} } =-\frac{x}{p^{2}}+\frac{n-x}{(1-p)^{2}}<0
$$
So $\hat{p}_\text{MLE}$ is at a maximum
## MLE for Binomial
$$
\mathscr{L}(p)=\log {x \choose n }+  x\log p+(n-x)\log(1-p)
$$
$$
 \frac{ \partial \mathscr{L}(p) }{ \partial p } =0 \iff \hat{p}_\text{MLE} =\frac{x}{n}
$$
Which is the same for Bernoulli! This is interesting for some reason...
We have already checked the second derivative; it is the same as Bernoulli.
We can check if this estimator $\hat{p}_\text{MLE}$ s unbiased:
$$
E(\hat{p}_\text{MLE} )=p
$$
Yippee
## MLE for Poisson
For the IID Poisson data, where $X_{i}\sim \text{Po}(\lambda)$
$$
\mathscr{L}(\lambda)=-n\lambda+\left( \sum_{ i=1} ^{ n}  x_{i} \right)\log\lambda-\log\left( \prod_{ i=1} ^{ n}  x_{i}! \right)
$$
To find the MLE, $\hat{\lambda}_\text{MLE}$ for $\lambda$ we just partially differentiate with respect to $\lambda$:
$$
\frac{ \partial \mathscr{L}(\lambda) }{ \partial \lambda } =-n+\frac{1}{\lambda}\sum_{ i=1} ^{ n}  x_{i}-0
$$
$$
\iff \frac{\sum_{ i=1} ^{ n}  x_{i}}{\hat{\lambda}_\text{MLE} }=n \iff \hat{\lambda}_\text{MLE} =\frac{1}{n}\sum_{ i=1} ^{ n}  x_{i}=\bar{x}
$$
We can then check second derivative, but who cares....
Before the data is measured, we can view the general MLE as
$$
\hat{\lambda}_\text{MLE} =\frac{1}{n}\sum_{ i=1} ^{ n}  X_{i}=\bar{X}
$$
$$
\implies E(\hat{\lambda}_\text{MLE} )=E\left( \frac{1}{n}\sum_{ i=1} ^{ n}  X_{i} \right)=\frac{1}{n}\sum_{ i=1} ^{ n} \underbrace{  E(X_{i}) }_{ =\lambda }=\frac{1}{n}\sum_{ i=1} ^{ n}  \lambda=\lambda
$$
