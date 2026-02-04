## Fundamental Principle of Bayesian Statistics
Everything that is uncertain can be treated as random and be associated with its own probability distribution, provided we use a subjecive interpretation of probability
___
We can hence treat the parameter $\theta$ as a random variable. We describe our uncertainty by a (subjective) pdf $f(\theta)$. The [[Likelihood|likelihood]] can be viewed as the conditional probability distribution $f(x|\theta)$ of the data given the parameter.
## Fundamental Procedure of Bayesian Statistics
To “learn about $\theta$ from data $x$” which becomes trivial. We use conditional probability with $f(\theta)$ and $f(x|\theta)$ to find $f(\theta|x)$, which is the conditional pdf of the parameter $\theta$ given the data $x$
___
The problem of being unable to make direct probability statements about $\theta$ in the standard frequntist approach have now been resolved. We can use $f(\theta|x)$ to answer all questions and test hypotheses directly. This allows us to ask and answer the question we wanted to ask:
    "What values of $\theta$ are most likely given the data under this model?"
In Bayesian methods, large samples aren't necessary for the method to be valid, and we don't need to imagine many hypothetical replications of our experiment
The main criticism of the Bayesian approach si that it asks for more: we need to be specific with the initial (prior) distribution for $\theta$; $f(\theta)$. This is subjective and some don't like this as they prefer maths and science to be objective, but hey this is stats, so say goodbye to that dream...
As the Bayesian approach is more complex, the calculations are also typically more complex
## $\hspace{0pt}4$ Bayesian Stages
### $\hspace{0pt}1$. Prior
We assign a prior distribution for the parameter $\theta$ (that describes a statistical model) denoted $f(\theta)$
### $\hspace{0pt}2$. Data
We observe data $X=x$, we can now formulate the likelihood $f(x|\theta)$. Same as $\ell(\theta)$, but now viwewed as a full conditional pdf
### $\hspace{0pt}3$. Posterior
After seeing the data $x$, we can evaluate the likelihood and then use [[Bayes' Theorem|Bayes' theorem]] to obtain the posterior distribution for $f(\theta|x)$ which expresses our uncertainty/beliefs about $\theta$, now we have seen the data $x$
### $\hspace{0pt}4$. Inference
Using the posterior distribution $f(\theta|x)$, the problem of inference becomes one of making statements about the posterior distribution, such as probability intervals; $\mathbb{P}(a<\theta<b)=0.95$, credibal intervals, point estimates of the probability of particular hypothesis
## Fundamental Equation of Bayesian Statistics: The Posterior
Any Bayesian statsitic problem can then be simply expressed as:
$$
f(\theta|x)=\frac{f(x|\theta)f(\theta)}{f(x)}
$$
$$
 \text{posterior}=\frac{\text{likelihood}\times \text{prior}}{\text{data probability}}
$$
We can simplify once the data has been measured, i.e. $X=x$, then $x$ is now just a constant, so $f(x)$ is just a constant, so
$$
f(\theta|x)=\frac{f(x|\theta)f(\theta)}{f(x)}=Cf(x|\theta)f(\theta)
$$
$$
\implies f(\theta|x)\propto f(x|\theta)f(\theta) 
$$
$$
\text{posterior}\propto \text{likelihood}\times \text{prior}
$$
This proportional form is seen to be not enough say to find probabilities of $\theta$ in intervals etc, however often enough it is used to spot the form of the posterior and identify it as a distribution we already know
Or, we can simply [[Integration|integrate]] and choose $C$ so that the integral
$$
\int_{-\infty}^{\infty} f(\theta|x) \, d\theta =1
$$
## Example
Drug trial has a binomial scenario
$$
X|\theta \sim B(16,\theta)
$$
Where $\theta=p$, we observed $x=11$ patients with a positive response
We don't know $\theta$, so we represent our knowledge about it via a prior $f(\theta)$
If we don't know musch about $\theta$, we could view all values of $\theta \in[0,1]$ as equally likely using the [[Uniform Distribution|unifom distribution]]:
$$
\theta \sim \text{Unif}(0,1)=U(0,1)
$$
Thus we have:
- Prior: $f(\theta)=1,\theta \in[0,1]$
- Likelihood: $f(x=11|\theta)={n \choose x }\theta^{x}(1-\theta)^{x}={16 \choose 11 }\theta^{11}(1-\theta)^{5}$
- Posterior: $f(\theta|x)\propto f(x=11|\theta)f(\theta)={16 \choose 11 }\theta^{11}(1-\theta)^{5}$, so
$$
f(\theta|x)=C\theta^{11}(1-\theta)^{5}
$$
And we can find $C$ by integrating that $C=74256$
This acutally corresponds to a $\text{Beta}(12,6)$ distribution
![[Bayesian Statistics 2025-03-10 15.41.24.excalidraw]]
```desmos-graph
left=-0.5
right = 1.5
top = 7
bottom = -0.5
---
\frac{x^{11}\left(1-x\right)^{5}}{\int_{0}^{1}x^{11}\left(1-x\right)^{5}dx}\{0<=x<=1\}
y=1\{0<=x<=1\}
```
The posterior peak (the mode) is at $\hat{\theta}=\frac{11}{16}$, this is the same as the [[Maximum Likelihood Estimation|MLE]]
We can now ask various questions e.g. what is the probability that the drug as a generally positive effect?
We could interpret this as $\mathbb{P}(\theta>0.5)$ which we can find by integration (by computer), and we end up getting
$$
\mathbb{P}(\theta>0.5)=0.9283
$$
What if we thought in advance that larger values of $\theta$ were indeed more likely, we could have instead specified the prior
## The Prior
The presence of the prior distribution in calculations is one of the primary differences between the Bayesian and the likelihood method to statistics, and as such it is often the most important issue for Bayesian methods (and also a main source of controversy). We need a prior distribution for our parameters in order to apply the Bayesian methodology, and the results we obtain will be somewhat sensitive to that prior, so this is important. In general there are two types of priors:
- Informative priors - $f(\theta)$ expresses specific knowledge about the behaviour of $\theta$. In principle, we must (subjectively) choose or specify a distribution that represents our knowledge about $\theta$, or else we must elicit one from someone else. This is particularly difficult when $\theta$ is high-dimensional or not well understood
- Noninformative priors (aka diffule, vague or objective priors) - $f(\theta)$ is deliberately (and in some sense, rigorously) vague about the behaviour of $\theta$. The simplest form being a uniform prior, to express that all values of $\theta$ are equally likely. Typically, this leads to similar results to a frequentist likelihood-based analysis, al only the likelihood carries any information in the prosterior. It is common to ue uniform priors even if they don't integrate to $1$. Such a prior is called improper and is sometimes acceptable, as the posterior that results can turn out to be proper
The distiction between use of informative and noninformative priors is another source of debate. In particular, critics would argue that incorporating subjective information into the problem is “not scientific”. Essentially, if we have prior information about the behaviour f $\theta$, then we should try to include that information into an informative prior. If we know nothing about $\theta$, then a noninformative prior would be appropriate.
Another relevant consideration is convenience. Bayesian statistics for general problems with arbitrary priors and likelihoods require explicit calculation of the conditional distribution, which will require substantial integration. With arbitrary distributions, these integrals are not guaranteed to be analytically tractable. In such cases, the only approach is to perform some form of numerical integration which can be computationally expensive