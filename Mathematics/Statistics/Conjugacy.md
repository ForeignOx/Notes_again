For certain combinations of [[Bayesian Statistics|priors]] and [[Likelihood|likelihoods]], the posterior we obtain is particularly mathematically convenient. Identifying and using such combinations can simplify the computation and analysis substantially
A conjugate prior distribution is one where the form of the posterior distribution is the same as the form of the prior distribution. That is, $f(\theta)$ and $f(\theta|x)$ are pdfs belonging to the same family. In which case we say:
- $f(\theta)$ is a conjugate prior for (or is conjugate with, or is closed under sampling from) the likelihood $f(x|\theta)$
- the set of all such priors forms a conjugate family for the likelihood $f(x|\theta)$
___
Conjugacy implies that the prior, $f(\theta)$ and the posterior, $f(\theta|x)$ have the same functional form. For example, both could be [[Normal Distribution|normal distributions]]. This relationship holds for all possible sample values and sample sizes. However, despite sharing a common type of distribution, the prior and posterior will differ in the parameter values of the common distribution
Clearly the form of the conjugate prior depends on the form of the likelihood. So there is a different conjugate distribution for a different data distribution. In some cases, there is no conjugate prior distribution
Conjugacy is a mathematical convenience which reduces the potentially difficult Bayesian update to a simple change in the parameters of the distribution from prior to posterior. We could use other priors, but obviously it makes the mathematics and computation more complex. We should be mindful of the fact that we often choose conjugate priors to make the calculation simpler, not because it represents genuine prior information about the behaviour of $\theta$
## More Formal Definition
Suppose data $x$ are to be observed with distribution $f(x|\theta)$. A family $\mathcal{F}$ of prior distributions for $\theta$ is said to be conjugate with $f(x|\theta)$ if for every prior distribution $f(\theta)\in\mathcal{F}$, the posterior ditribution $f(\theta|x)\propto f(x|\theta)f(\theta)$ is also in $\mathcal{F}$

