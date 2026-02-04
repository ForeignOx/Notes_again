We imagine that we will gather data $X_{i}$ with $i=1,2,\dots,n$. Now we may not know the precise distribution that generated this data, but we may suspect that the distribution is one of a family of possible distributions laelled on parameterised by a parameter $\theta$ ($\theta$ could even represent a list of parameters). An example of this is saying $X_{i}\sim \text{Bernoulli}(p)$, here $\theta=p$. We also often write $X_{i}\sim N(\mu,\sigma^{2})$, here $\theta=\left\{ \mu,\sigma \right\}$
The joint pdf of the data is simply represented as:
$$
f(x_{1},x_{2},\dots,x_{n}|\theta)
$$
However, once we measure the data:
$$
X_{1}=x_{1},X_{2}=x_{2},\dots,X_{n}=x_{n}
$$
This joint pdf can now be viewed as just a function of $\theta$ as the data are now fixed
## The Likelihood Function
Suppose we have $X_{1},\dots,X_{n}$ that have joint pdf $f(x_{1},x_{2},\dots,x_{n}|\theta)$, then the likelihood function $\ell(\theta)$ is simply the pdf of the observed data considered as a function of $\theta$ only i.e.
$$
\ell(\theta)\equiv\ell(\theta;x_{1},\dots,x_{n})=f(x_{1},\dots,x_{n}|\theta)
$$
And the log-likelihood function is:
$$
\mathscr{L}(\theta)\equiv \log(\ell(\theta))=\log(f(x_{1},x_{2},\dots,x_{n}|\theta))
$$
___
## Likelihood for [[Independent and Identically Distributed|IID]] data
If the $X_{i}$ are independent and identically distrubuted (IID), then the expression for the likelihood takes a more pleasant form. Suppose each $X_{i}$ has pdf given by $f(x_{i}|\theta)$ and that all $X_{i}$ are IID then
$$
\ell(\theta)=f(x_{1},x_{2},\dots x_{n}|\theta)=\prod_{i=1}^{n}f(x_{i}|\theta)
$$
$$
\mathscr{L}(\theta)=\log(f(x_{1},\dots x_{n}|\theta))=\log\left( \prod_{i=1}^{n}f(x_{i}|\theta) \right)=\sum_{i=1}^{n}\log(f(x_{i}|\theta))
$$
This is useful as we can differentiate sums much more easily than products
Note that $\ell(\theta)$ is not a probability density function with respect to $\theta$, as $\theta$ is just a fixed but unknown parameter (at this point), so $\ell(\theta)$ will not integrate to $1$ with respect to $\theta$
However, $\ell(\theta)$ is still really useful as it shows us which values of $\theta$ are more likely to have generated the data 
### For Bernoulli
Likeihood for Bernoulli trials. say we have IID
$$
X_{i}\sim \text{Bernoulli}(p)
$$
So each $X_{i}$ is discrete and equal to $1$ or $0$ with probability $p$ or $1-p=q$, hence
$$
f(x_{i}|p)=\begin{cases}
p^{x_{i}}q^{1-x_{i}}&\text{for }x_{i}=0,1\\0&\text{otherwise}
\end{cases}
$$
Hence our parameter of interest is $\theta=p$, so we write our likelihood as $\ell(p)$ instead of $\ell(\theta)$:
$$
\ell(p)=f(x_{1},\dots,x_{n}|p)=\prod_{i=1}^{n}f(x_{i}|p)=\prod_{i=1}^{n}p^{x_{i}}q^{1-x_{i}}=p^{\sum_{i=1}^{n}x_{i}}q^{\sum_{i=1}^{n}1-x_{i}}=p^{x}q^{n-x}
$$
Where $x=\sum_{ i=1} ^{ n} x_{i}$, and
$$
\mathscr{L}(p)=\log(\ell(p))=\log(p^{x}q^{n-x})=x\log(p)+(n-x)\log(1-p)
$$
Which we can now maximise by differentiating to find an estimator for $p$ 
### For Binomial
In a binomial scenario, we have that $X$ is the sum or count of the successes from $n$ Bernoulli trials with parameter $p$, so
$$
X\sim \text{Bin}(n,p)
$$
When viewed in this binomial framework, we have one single experiment, that yields the realisation $X=x$
Hence due to a single experiment, the likelyhood is simply ($n$ is known)
$$
\ell(p)=f(x|p)={n \choose x }p^{x}q^{n-x}
$$
And the log-likelyhood is:
$$
\mathscr{L}(p)=\log(f(x|p))=\log\left( {n \choose x }p^{x}q^{n-x} \right)=\log\left( \frac{n!}{(n-x)!x!} \right)+x\log(p)+(n-x)\log(1-p)
$$
Note that differentiating this with respect to $p$ gives an identical result as with the bernoulli trials, since their log-likelihoods differ only by a constant
### For Poisson
The poisson distribution is often used to model radioactive decay counts and a wide range of other phenomena (traffic, guessing on tests)
If the data has a poisson distribution, we say $X_{i}\sim \text{Po}(\lambda)$, where $\lambda$ is the parameter of interest (it is also the expected number of counts), so the poisson distribution is given by:
$$
f(x_{i}|\lambda)=\begin{cases}
\frac{e^{ -\lambda }\lambda^{x_{i}}}{x_{i}!}&\text{for } x_{i}\in \mathbb{N}_{0}\\0&\text{otherwise}
\end{cases}
$$
Therefore the likelihood of $n$ IID data values $X_{i}=x_{i}$ is:
$$
\ell(\lambda)=f(x_{1},x_{2},\dots,x_{n}|\lambda)=\prod_{i=1}^{n}f(x_{i}|\lambda)=\prod_{ i=1} ^{ n}   \frac{e^{ -\lambda }\lambda^{x_{i}}}{x_{i}!}=\frac{e^{ -n\lambda }\lambda^{\sum_{i=1}^{n}x_{i}}}{\prod_{i=1}^{n}x_{i}!}
$$
And the log-likelihood is
$$
\mathscr{L}(\lambda)=\log(\ell(\lambda))=\log\left( \frac{e^{ -n\lambda }\lambda^{\sum_{i=1}^{n}x_{i}}}{\prod_{i=1}^{n}x_{i}!} \right)=-n\lambda+\left( \sum_{ i=1} ^{ n}  x_{i} \right)\log\lambda-\log\left( \prod_{ i=1} ^{ n}  x_{i}! \right)
$$



