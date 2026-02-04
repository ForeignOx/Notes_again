We can construct sufficient statistics which are simply [[Functions|functions]] (i.e. summaries) of the data that, were we to know them, the [[Likelihood|likelihood]] then tells us that we can discard the rest of the data $x_{i}$ as irrelevant. This is quite the strong statement
## Sufficiency via the Factorisation Theorem
If we have a [[Samples|sample]] of data $x_{1},\dots,x_{n}$, then a statistic $T(x_{1},\dots,x_{n})$ is said to be sufficient for $\theta$ iff we can factorise the likelihood in the following form:
$$
\ell(\theta)=f(x_{1},\dots ,x_{n}|\theta)=g(T,\theta)h(x_{1},\dots,x_{n})
$$
Where we see that all the $\theta$ behaviour is tied together with $T$ through the function $g$, but $h(x_{1},\dots,x_{n})$ is irrelevant. Therefore, a sufficient statistic $T$ contains all of the information about the parameter $\theta$ that we can extract from the sample $x_{1},\dots,x_{n}$
$T$ can in fact be instead a list of statistics. We see that if $T$ is a sufficient statistic for $\theta$ and if we partially differentiate the likelihood to find the [[Maximum Likelihood Estimation|M.L.E.]]:
$$
\frac{ \partial \ell(\theta) }{ \partial \theta } =\frac{ \partial  }{ \partial \theta } (g(T,\theta)h(x_{1},\dots,x_{n}))=h(x_{1},\dots,x_{n})\frac{ \partial g(T,\theta) }{ \partial \theta } 
$$
So the MLE $\hat{\theta}_\text{MLE}$ satisfies:
$$
h(x_{1},\dots,x_{n})\frac{ \partial g(T,\hat{\theta}_\text{MLE} ) }{ \partial \theta  } =0
$$
$$
 \iff \frac{ \partial g(T,\hat{\theta}_\text{MLE} ) }{ \partial \theta } =0
$$
We see that the MLE $\hat{\theta}_\text{MLE}$ which would be a solution will onlhy be a function of $T$, and not of any other components of the data $x_{1},\dots,x_{n}$
## Sufficiency for [[Bernoulli Distribution|Bernoulli]]
For Bernoulli trials we had a likelihood ($\theta=p$):
$$
\ell(p)=f(x_{1},\dots,x_{n}|p)=p^{x}(1-x)^{n-x}
$$
Where $x=\sum_{ i=1} ^{ n} x_{i}$, which can be written:
$$
\ell(p)=g(\underbrace{ x }_{ =T },p)h(x_{1},\dots,x_{n})
$$
With
$$
g(x,p)=p^{x}(1-p)^{x}
$$
And $h(x_{1},\dots ,x_{n})=1$, so $T=x$ is the sufficient statistic for our parameter of interest $p$ (assuming that $n$ is fixed and known), or we say $T=\left\{ x,n \right\}$
## Sufficiency for [[Binomial Distribution|Binomial]]
In a binomial scenario we had
$$
\ell(p)=f(x|p)={n \choose x }p^{x}(1-p)^{n-x}
$$
Which can be written
$$
\ell(p)=g(x,p)h(x_{1},\dots,x_{n})
$$
Where $g(x,p)=p^{x}(1-p)^{n-x},h(x_{1},\dots,x_{n})={n \choose x }$, so again, $T=x$ is the sufficient statistic for $\theta=p$, assuming we know $n$
This shows a deeper insight into the connection between the Beroulli and Binomial scenarios. We see that the Binomial distribution $f(x|p)$ is in fact the direct distribution of the Bernoulli trials' sufficient statistic $T=x$ itself, hence the Binomial analysis must return the same MLE as the direct Bernoulli analysis, which uses all the data $x_{1},\dots x_{n}$
We also see that there is no further simplification to the Bernoulli trial that one could make (e.g. roundin to the nearest number)
## Sufficiency for [[Poisson Distribution|Poisson]]
For the poisson scenario we have:
$$
\ell(\lambda)=f(x_{1},\dots x_{n}|\lambda)=\frac{e^{ -n\lambda }\lambda^{\sum_{ i=1} ^{ n}  x_{i}}}{\prod_{ i=1} ^{ n}  x_{i}!}=e^{ -n\lambda }\lambda^{n\bar{x}}\left( \frac{1}{\prod_{ i=1} ^{ n}  x_{i}!} \right)
$$
We rewrite this in the form of the factorisation theorem:
$$
\ell(\lambda)=g(\bar{x},\lambda)h(x_{1},\dots,x_{n})
$$
With 
$$
g(\bar{x},\lambda)=e^{ -n\lambda }\lambda^{n\bar{x}}
$$
$$
 h(x_{1},\dots,x_{n})=\frac{1}{\prod_{ i=1} ^{ n}  x_{i}!}
$$
Now we have $T=\bar{x}$ is the sufficient statistic for our parameter $\theta=\lambda$ again, assuming we know $n$