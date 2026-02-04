Credible [[Intervals|intervals]] are the [[Bayesian Statistics|Bayesian]] equivalent of the frequentist confidence interval
A $100(1-\alpha)\%$ credible interval $[l,u]$ from $l$ lower and $u$ upper for a [[Random Variables|random variable]] $\theta \in\mathbb{R}$ satisfies:
$$
\mathbb{P}(l\leq\theta \leq u)=\mathbb{P}(\theta \in [l,u])=1-\alpha
$$
Similarly, a $100(1-\alpha)\%$ credible interval for $\theta$ given the data $X=x$ satisfies:
$$
\mathbb{P}(l\leq\theta \leq u|X=x)=1-\alpha
$$
Such an interval contains the regions of highest probability density
![[Credible Intervals 2025-03-20 09.18.32.excalidraw]]
EQT has equal sized tails, HPD minimised the interval. HPD usually better.
## Approximate Normal Credible Intervals
Given a random variable $\theta$, an approximate $100(1-\alpha)\%$ credible interval or $\theta$ is given by
$$
E(\theta)\pm z^{*}_{\frac{\alpha}{2}}\sqrt{ Var(\theta) }
$$
Often, we would instead use the posterior distribution of $\theta|x$:
$$
E(\theta|x)\pm z^{*}_{\frac{\alpha}{2}}\sqrt{ Var(\theta|x) }
$$
This is justified for unimodal (single peaked) posteriors which are close to the [[Normal Distribution|Normal distribution]]
### Example
Say we have posterior
$$
\theta|x\sim Be ta(12,6)
$$
We need [[Expectation|expectation]] and [[Variance|variance]] for the [[Beta Distribution|Beta distribution]]:
$$
E(\theta|x)=\frac{\hat{a}}{\hat{a}+\hat{b}}=\frac{12}{12+6}=\frac{2}{3}
$$
$$
Var(\theta|x)=\frac{\hat{a}\hat{b}}{(\hat{a}+\hat{b})^{2}(\hat{a}+\hat{b}+1)}=0.01170
$$
So our approximate normal distribution is:
$$
\theta|x\sim N(E(\theta|x),Var(\theta|x))
$$
So the normal approximation for $95\%$ credible interval is:
$$
E(\theta|x)\pm z^{*}_{\frac{\alpha}{2}}\sqrt{ Var(\theta|x) }
$$
$$
 0.6666\pm 1.96\sqrt{ 0.01170 }=[0.4547,0.8786]
$$

