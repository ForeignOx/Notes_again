## Normal Approximation
We can look at probabilities for proportions:
- Consider a [[Binomial Distribution|binomially distributed]] [[Random Variables|random variable]] $X$ with parameters $n$ and $p$
- The population parameter $p$ is unknown and is to be estimated from the data
- The sample proportion $\hat{p}=Y=\frac{X}{n}$ can be used as an estimator for $p$ (we will mainly use $Y$ notation instead of $\hat{p}$ as it allows us to represent the observed sample proportion $y$)
- $E(Y)=p$ means that the estimator of $Y$ is unbiased
- $Var(Y)=\frac{p(1-p)}{n}$ means that the variance of the estimator get's smaller as $n$ increases
___
One issue with this is that $p$ is unknown, so $Var(Y)$ is also unkown, so we can find the maximum of $p(1-p)=\frac{1}{4}$, but this is the worst case scenario... We can do better
If $n$ is large, then
$$
Var(Y)=\frac{y(1-y)}{n}
$$
As $y\approx p$, where $y$ is our observed sample proportion (if $n=1000$, $X=x=283$, then $y=\frac{483}{1000}=0.483$)
___
Another issue with this is that the sampling distribution of $Y$ (binomial) is hard to calculate
If $np\geq 10$, and $n(1-p)\geq 10$, then the normal approximation is valid. Therefore, with a slight abuse of notation, we can write:
$$
Y\sim N\left( p,\underbrace{ \frac{y(1-y)}{n} }_{ \text{abuse} } \right)
$$
Or equivalently,
$$
\frac{Y-p}{\sqrt{ \frac{y(1-y)}{n} }}\sim N(0,1)
$$
We have developed methodology for making inference about population parameters given an estimatro and its sampling distribution so we can construct confidence intervals and do [[Hypothesis Testing|hypothesis tests]]
The $1-\alpha$ confidence interval for $p$ is 
$$
y\pm z^{*}\sqrt{ \frac{y(1-y)}{n} }
$$
Where $z^{*}$ as usual
$$
\mathbb{P}(-z^{*}\leq Z\leq z^{*})=1-\alpha
$$
With $Z\sim N(0,1)$
The $p$-value for the hypothesis test:
- $H_{0}:p=p_{0}$ (the hypothesised value for $p$)
- $H_{a}:p\neq p_{0}$
Is given by
$$
p\text{-value}=2\left( 1-\mathbb{P}\left( Z\leq \frac{\left| y-p_{0} \right| }{\sqrt{ \frac{y(1-y)}{n} }} \right) \right)
$$
Which is the probability of seeing something more extreme than the data
### Proof
![[Inference for a Proportion 2025-02-24 15.30.14.excalidraw]]
$$
\delta=\left| y-p_{0} \right| 
$$
Then the $p$-value for proportionas is the probability of $Y$ as extreme as $y$, given $H_{0}:p=p_{0}$ which is equal to
$$
\mathbb{P}(Y\leq p_{0}-\left| y-p_{0} \right| )+\mathbb{P}(Y\geq p_{0}+\left| y-p_{0} \right| )=\mathbb{P}(Y\leq p_{0}-\delta)+\mathbb{P}(Y\geq p_{0}+\delta)
$$
Which by the symmetry of the approximate Normal distribution is equal to
$$
2\mathbb{P}(Y\geq p_{0}+\delta)=2\mathbb{P}\left(\underbrace{  \frac{Y-p_{0}}{\sqrt{ \frac{y(1-y)}{n} }} }_{ Z\sim N(0,1) }\geq \frac{\delta}{\sqrt{ \frac{y(1-y)}{n} }} \right)
$$
$$
= 2\mathbb{P}\left( Z\geq \frac{\delta}{\sqrt{ \frac{y(1-y)}{n} }} \right)=2\left( 1-\mathbb{P}\left( Z\leq  \frac{\delta}{\sqrt{ \frac{y(1-y)}{n} }} \right) \right)
$$
$$
= 2\left( 1-\mathbb{P}\left( Z\leq  \frac{\left| y-p_{0} \right| }{\sqrt{ \frac{y(1-y)}{n} }} \right) \right)
$$
## Better Approximations
It has been shown that the above confidence interval for $p$ is not that reliable especially for extreme values of $p$ or low $n$
More detailed calculations yield improved Confidence Intervals for $p$
For example:
### The Wilson Interval
$$
\frac{y+\frac{t}{2}}{1+t}\pm \frac{\sqrt{ y(1-y)t+\frac{t^{2}}{4} }}{1+t}
$$
Where $t=\frac{(z^{*})^{2}}{n}$
### The Agresti-Coull Interval
$$
\tilde{y}\pm z^{*}\sqrt{ \frac{\tilde{y}(1-\tilde{y})}{\tilde{n}} }
$$
With $\tilde{y}=\frac{ny+2}{n+4}$, $\tilde{n}=n+4$


### Examples
Drop out rates at UK Universities. Suppose we want to estimate the first year drop out rate $p$ across the country and take a simple random sample of size $n=250$ and see $\hspace{0pt}28$ students failed to continue beyond 1st year 
We want to calculate a $95\%$ confidence interval for $p$ and the Wilson $95\%$ confidence interval
$$
y=\frac{x}{n}=\frac{28}{250}=0.112
$$
Then the standard confidence interval for $p$ is ($z^{*}=1.96$ for $95\%$ interval)
$$
y\pm z^{*}\sqrt{ \frac{y(1-y)}{n} }=0.122\pm1.96\sqrt{ \frac{0.112\times 0.888}{250} }=[0.073,0.151]
$$
The Wilson Interval gives:
$$
t=\frac{(z^{*})^{2}}{n}=\frac{1.96^{2}}{250}=0.0154
$$
$$
\frac{y+\frac{t}{2}}{1+t}\pm\frac{  \sqrt{ y(1-y)t+\frac{t^{2}}{4} }}{1+t}=[0.079,0.157]
$$