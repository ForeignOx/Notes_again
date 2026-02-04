Suppose we are interested in a single unknown [[Population|population]] parameter $\theta$ for example $\mu$ ect. 
We define the null and alternative hypotheses like so:
- $H_{0}$: the null hypothesis that $\theta$ is equal to the value $r$
- $H_{a}$: the alternate hypothesis, which denies the null hypothesis (the type of denial makes it a one-sided or a two-sided test)
For example a two-sided test would look like:
- $H_{0}:\theta=r$
- $H_{a}:\theta \neq r$
And a one-sided test would look like:
- $H_{0}:\theta=r$
- $H_{a}:\theta>r$ or $H_{a}:\theta<r$
Given a particular [[Samples|sample]], should we reject the null hypothesis or not?
## Confidence Intervals
### Method: Two-Sided Case
If we have:
- A two-sided hypothesis (as above)
- An estimator for $\theta$ e.g. $\bar{X}\sim N\left( \mu, \frac{\sigma^{2}}{n} \right)$
- The sampling distribution of the estimator (as a function of $\theta$)
- A level of significance $\alpha$
Then we can construct a $(1-\alpha)$ confidence interval for $\theta$, and then we:
- Reject $H_{0}$ if $r$ lies outside the confidence interval, and we find the test statistically significant at the $\alpha$% level of significance
- Fail to reject $H_{0}$ if $r$ is in the confidence interval and find the test not signifiicant at the $\alpha$% level of significance 
### Method: One-Sided Case
If we have:
- A one-sided hypothesis (as above)
- An estimator for $\theta$ e.g. $\bar{X}\sim N\left( \mu, \frac{\sigma^{2}}{n} \right)$
- The sampling distribution of the estimator (as a function of $\theta$)
- A level of significance $\alpha$
Then we can contruct a $(1-2\alpha)$ confidence interval for $\theta$, and then we:
- Reject $H$ if $r$ falls to the right/left of the confidence interval
- Fail to reject $H_{0}$ otherwise
## $p$-Values
An alternative way to test hypotheses is to calculate an appropriate test statistic for the data. We can then work our the probability of observing a value at least as extreme as the statistic under the assumption that $H_{0}$ is true. This probability is known as the $p$-value. The more extreme the statistic, the more unlikely it is that $H_{0}$ is true: small $p$-value implies reject $H_{0}$
The threshold for $p$-value is equal to the level of significance $\alpha$
Note: finding the $p$-value is like finding the confidence interval that just touches the Hypothesised value
### One Sided Test
The $p$-value is just the tail probability corresponding to be "at least as extreme" as the test statistic
### Two-Sided Test
Must remember we can be extreme in both directions, so $p$-value will come from both tails (often double the one-sided case)

## Example
For cuckoo egg data, we had a $95\%$ confidence interval for $\mu$ (mean egg length) $[22.36,22.78]$
This would suggest evidence against $\mu=22$ as it is not inside the interval
We can perform hypothesis testing by checking whether a proposed value of $\mu$ lies inside the confidence interval
___
If we have $\hspace{0pt}6$ randomly selected chocolate bars wighing $\hspace{0pt}103$,$\hspace{0pt}101$,$\hspace{0pt}97$,$\hspace{0pt}95$,$\hspace{0pt}101$,$\hspace{0pt}98$ grams, $\bar{x}=99.17$, $s=2.99$, test the hypothesis that mean weight $\mu$ is 100g (of all such chocolate bars)
Let's choose the significance level of $\alpha=5\%$, we do a two sided test:
- $H_{0}:\mu=100\pu{ g}$
- $H_{a}:\mu \neq 100\pu{ g}$
$\sigma$ is unknown, so we use $s$ to estimate, but $n$ is small, so we can use the [[t-Distribution|t-Distribution]], but only if the [[Population|population]] is [[Normal Distribution|normal]]-ish, so we plot a normal quantile plot and as it turns out, yay it is
So a $95\%$ confidence interval looks a bit like:
$$
\bar{x}\pm \frac{t_5^{*}s}{\sqrt{ n }}=99.17\pm2.571  \frac{2.99}{\sqrt{ 6 }}=[96.03,102.31]
$$
So a $95\%$ confidence interval contains $\mu=100$, so we fail to reject $H_{0}$ at the $5\%$ significance level
___
Test the mean nicotine content of a brand of cigarettes and whether it is the advertised $1.4\pu{ mg}$. Concern is that it's higher so the company can get you more addicted
A sample of $n=80$ cigarettes with $\bar{x}=1.5,s=0.3$, we do a one-sided test:
- $H_{0}:\mu=1.4\pu{ mg}$
- $H_{a}:\mu> 1.4\pu{ mg}$
Would we reject $H_{0}$ at the $5\%$ significance level?
Since $n$ is large, we have a normal approximation for $\bar{X}$ and $s\approx\sigma$, for a $5\%$ significance level, since it is one-sided we need to construct $(1-2\alpha)$ confidence interval $=90\%$ confidence interval:
$$
\bar{x}\pm z^{*} \frac{s}{\sqrt{ n }}=1.5\pm1 .645  \frac{0.3}{\sqrt{ 80 }}=[1.44,1.56]
$$
And $\mu$ is to the left of this interval, so we reject $H_{0}$ at the $5\%$ level of significance
___



## Errors in Hypothesis Testing
We can make two kinds of mistakes in hypothesis testing:

|                        | $H_{0}$ True     | $H_{0}$ False    |
| ---------------------- | ---------------- | ---------------- |
| Fail to reject $H_{0}$ | Correct Decision | Type II error    |
| Reject $H_{0}$         | Type I error     | Correct Decision |

We have significance level $\alpha$ given by:
$$
\alpha=\mathbb{P}(\text{type I error}|H_{0})
$$
So a low significance level is desirable
We also have something called the power of the test, $\beta$:
$$
\beta=1-\mathbb{P}(\text{type II error}|H_{a} )
$$
High power is desirable 
Our aim is to design a test to have high power and low significance level
![[Hypothesis Testing 2025-02-21 14.45.09.excalidraw]]
## Dangers of Hypothesis Testing
Why should we fail to reject $H_{0}$ at a $p$-value of $5.00000001\%$ and rejecting at $5\%$, surely some sort of scale would be more reasonable
We always want to explore the data first
## Are Hypothesis Tests Meaningful?
We reject $H_{0}$ if $p$-value ois small, and the $p$-value is the probability the thing we're testing is at least as extreme as the one observed given the hypothesis was true.
Really, we should calculate the probability that $H_{0}$ is true given the sample mean