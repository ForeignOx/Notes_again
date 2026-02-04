To set up the general approach to [[Bayesian Statistics|Bayesian analysis]] of binomial data, we need to identify an appropriate prior for the probability parameter. The distribution we shall use for this is the beta distribution, which is very flexible and defined over $[0,1]$, so is ideal for representing probability. The [[Beta Distribution|Beta distribution]] has a similar functional form as the binomial likelihood, so we can investigate whether it is a conjugate prior
We have data $Y_{1},Y_{2},\dots,Y_{n}$ where each $Y_{i}$ is $\hspace{0pt}1$ in the even of success with probability $p$, and $0$ otherwise. Assuming the $Y_{i}$ are independent and $p$ is constant, then our data are [[Independent and Identically Distributed|IID]] [[Bernoulli Distribution|Bernoulli]] random variables with parameter $p$. If we cound the number of successes, $X=\sum_{i}Y_{i}$, then we have $X\sim B(n,p)$
To find the prosterior for $p|X$, we need to combine the binomial likelihood with a prior for $p$. The beta distribution is an ideal candidate
___
Suppose we observe a [[Random Variables|random variable]] $X=x$ where $X|p\sim Bin(n,p)$ is [[Binomial Distribution|binomially distributed]]. If our [[Bayesian Statistics|prior]] distribution for $p=\theta$ is such that $p\sim Beta(a,b)$, then the posterior distribution for $p|x$ is:
$$
p|x \sim Beta(a+x,b+n-x)
$$
$\implies f(p|x)$ is the beta p.d.f. hence the beta distribution is a conjugate prior for the binomial [[Likelihood|likelihood]]
## Proof
Say we have a beta prior and binomila likelihood and observe $X=x$ successes, therefore our posterior, using [[Bayes' Theorem|Bayes' theorem]] is:
$$
f(p|x)\propto f(x|p)f(p)={n \choose x }p^{x}(1-p)^{n-x}\times  \frac{1}{\beta(a,b)}p^{a-1}(1-p)^{b-1}
$$
$$
 \propto p^{a+x-1}(1-p)^{b+n-x-1}=p^{\tilde{a}-1}(1-p)^{\tilde{b}-1}
$$
Where $\tilde{a}=a+x,\tilde{b}=b+n-x$
So what distribution is this? This is of course the core of the $B eta(\tilde{a},\tilde{b})=Be ta(a+x,b+n-x)$ distribution
Thus
$$
p|x\sim Be ta(a+x,b+n-x)
$$
As required. As the posterior has the same family (Beta) as the prior, this is a conjugate prior
___
We can now write the full posterior:
- Posterior:
$$
f(p|x)=\frac{1}{\beta(a+x,b+n-x)}p^{a+x-1}(1-p)^{b+n-x-1}
$$
- Prior:
$$
f(p)=  \frac{1}{\beta(a,b)}p^{a-1}(1-p)^{b-1}
$$
So the Bayesian update is simple:
$$
a\to a+x
$$
$$
 b\to b+n-x
$$
This is the convenience of conjugacy!
A heavy calculation of the posterior is reduced to adding
This gives great insight into the meaning of the the prior parameters $a$ and $b$. We see from the posterior that:
- $a$ is “like” $x$ which is the number of successes
- $b$ is “like” $n-x$ which is the number of failures
We can think of our prior as representing an equivalent hypothetical prior samplee of size $(a+b)$ in which we observe $a$ successes and $b$ failures
We also note that we can express the posterior [[Expectation|expectation]] for $p|x$ as
- Prior: 
$$
E(p)=\frac{a}{a+b}
$$
- Posterior: 
$$
E(p|x)=\frac{\tilde{a}}{\tilde{a}+\tilde{b}}=\frac{a+x}{(a+x)+(b+n-x)}=\frac{1}{a+b+n}+\frac{x}{a+b+n}
$$
$$
= \frac{a}{a+b}\left( \frac{a+b}{a+b+n} \right)+\frac{x}{n}\left( \frac{n}{a+b+n} \right)
$$
$$
\implies E(p|x)=E(p)\lambda+\hat{p}_\text{MLE} (1-\lambda)
$$
Where
$$
\lambda=\frac{a+b}{a+b+n}
$$
So the posterior expectation is just the weighted average between our prior expectation $E(p)$ and the [[Maximum Likelihood Estimation|MLE]] $\hat{p}_\text{MLE}$
For large $n\to \infty$, $\lambda\to0$, so $E(p|x)\to \hat{p}_\text{MLE}=\frac{x}{n}$

