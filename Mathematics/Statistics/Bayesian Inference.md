What is the point of [[Bayesian Statistics|Bayesian Stats]] nonsense?
We have seen how to find the Bayesian posterior $f(\theta|x)$, but
- What can we do with this? 
- What does it give us?
Apparently, it gives us everything. (this is a **very** dubious statement but ok Ian pop off)
We can now answer any question about $\theta$ and by extension about future measurements probabilistically
This is often used in Decision Theory to make optimal decisions under uncertainty. It is hard to overstate the importance of this capability! (average stats propaganda)
## Simple Summaries of $f(\theta|x)$
We can draw plots, do location summaries (mean, median, mode), spread summaries (varience, quartiles)
## Probabilities
We use hte pdf $f(\theta|x)$ to directly calculate relevant probabilities, such as $\mathbb{P}(\theta>a|x)$
## Point Estimates
Summarise the pdf in terms of a single "best" given value of $\theta$, often a location summary
Two obvious choices of point estimate are:
### Posterior Mode of $MAP$ estimate $\hat{\theta}_\text{MAP}$
MAP stands for "Maximum a Posteriori" which is the value of $\theta$ that maximises $f(\theta|x)$:
$$
\hat{\theta}_\text{MAP}=\arg\max_{\theta}f(\theta|x) 
$$
Which analogues to the [[Maximum Likelihood Estimation|MLE]] 
### Posterior Mean, $E(\theta|x)=\int _{\theta}\theta f(\theta|x) \, d\theta$
Which is simply the posterior [[Expectation|expectation]]
#### Example
If we have [[Binomial Distribution|$X|\theta \sim B(16,\theta)$]] where $X$ is the total number of successes. If we observe $x=11$ and used a [[Uniform Distribution|uniform]] prior $\theta \sim U(0,1)$, then using the [[Beta-Binomial Model|beta-binomial model]], we will get a porterior [[Beta Distribution|$x|\theta \sim Beta(12,6)$]]. From the properties of the beta dirtibution, we can find our MAP and posterior mean of $\theta$
Recall if $Y\sim Be ta(a,b)$,
$$
Mode(Y)=\frac{a-1}{a+b-2}
$$
$$
 E(Y)=\frac{a}{a+b}
$$
So
$$
\hat{\theta}_\text{MAP}=\frac{12-1}{12+6-2}=\frac{11}{16}\left( =\frac{x}{n}=\hat{\theta}_\text{MLE}  \right) 
$$
$$
E(x|\theta)=\frac{12}{12+6}=\frac{12}{18}
$$
Obviously for a uniform prior, $\hat{\theta}_\text{MLE}=\hat{\theta}_\text{MAP}$
However, our second prior was $f(\theta)=2\theta\implies\theta|x\sim Be ta(13,6)$, so
$$
\hat{\theta}_\text{MAP}=\frac{13-1}{13+6-2}=\frac{12}{17}
$$
$$
 E(\theta|x)=\frac{13}{13+6}=\frac{13}{18} 
$$
## Predictions
Use $f(\theta|x)$ to make predictions about future data $X^{*}$

## Intervals and Regions
Find intervals that capture a proportion of the possible values of $\theta$, such as the intergval $[l,u]$, where:
$$
\mathbb{P}(l<\theta<u)=1-\alpha
$$

