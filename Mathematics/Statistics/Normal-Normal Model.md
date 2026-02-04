## Known Variance
This is an example of a [[Conjugacy|conjugate]] [[Bayesian Statistics|prior]] for [[Normal Distribution|normally distributed]] data:
$$
X_{i}\sim N(\mu,\sigma^{2})
$$
With $\mu,\sigma^{2}$ both fixed. The conjugate prior family for the mean $\mu$ is also itself normal. We assume $\sigma^{2}$ is known and constant. To use the [[Variance|variance]] directly is a bit cumbersome, so instead, we work with the [[Precision|precision]], so let $\tau=\frac{1}{\sigma^{2}}$, then we can write
$$
X\sim N\left( \mu,\frac{1}{\tau} \right)
$$
And its pdf is
$$
f(x|\mu,\tau)=\sqrt{ \frac{\tau}{2\pi} }e^{ -\frac{\tau}{2}(x-\mu)^{2} }
$$
Let $X_{1},\dots,X_{n}$ be [[Independent and Identically Distributed|IID]] variables, with $X_{i}\sim N\left( \mu,\frac{1}{\tau} \right)$ with precision $\tau>0$ known.
Suppose our prior pdf for uncertain $\mu$ is:
$$
\mu \sim N\left( m,v^{2}=\frac{1}{t} \right),t>0
$$
Then our posterior pdf for $\mu|x$ is also Normal such that:
$$
\mu|\underline{x}\sim N\left( m_{1},v_{1}^{2}=\frac{1}{t_{1}} \right)
$$
Where $m_{1},v_{1},t_{1}$ are the updated ones:
$$
t_{1}=t+n\tau
$$
$$
m_{1}=\frac{tm+n\tau \bar{x}}{t+n\tau}
$$
We can re-write the posterior mean as:
$$
m_{1}=E(\mu|\underline{x})=\frac{t}{t_{1}}m+\frac{n\tau}{t_{1}}\bar{x}=km+(1-k)\bar{x}
$$
Where $k=\frac{t}{t+n\tau}$. Thus, again, the posterior mean is a weighted average of the prior mean $m$ and sample mean $\bar{x}=\frac{1}{n}\sum_{ i=1} ^{ n} x_{i}$ with weights proportional to the respective precisions.
The data precision is $n\tau$, which, if we just reintroduce $\sigma^{2}$, is just $\frac{n}{\sigma^{2}}=\frac{1}{\frac{\sigma^{2}}{n}}$ i.e. the precision of the sample mean $\bar{X}$, as we can recall from the [[Central Limit Theorem|CLT]]:
$$
\bar{X}\sim N\left( \mu,\frac{\sigma^{2}}{n} \right)
$$
Note each data point we observe increases our precision by $\tau$
This also tells us that the [[Samples|sample]] mean is [[Sufficiency|sufficient]] 
Before we prove this, we need to find the [[Core of a Distribution|core]] for a normal density, $X\sim N\left( \mu,\frac{1}{\tau} \right)$/ As the random variable is $X$ here, we only care about the terms in $x$, so we find:
$$
f(x|\mu,\sigma^{2})\propto e^{ -\frac{1}{2\sigma^{2}}(x-\mu)^{2} }=e^{ -\frac{\tau}{2}(x-\mu^{2}) }
$$
But we can multiply out the quadratic inside the exponential to get:
$$
f(x|\mu,\sigma^{2})\propto \exp\left( -\frac{1}{2\sigma^{2}}(x^{2}+\mu^{2}-2x\mu) \right)
$$
$$
\propto\exp\left( -\frac{1}{2\sigma^{2}}(x^{2}-2x\mu) \right)=\exp\left( -\frac{\tau}{2}(x^{2}-x\mu) \right)
$$
Which is the core of the normal distribution
### Proof
First we need to construct the [[Likelihood|likelihood]] for our IID data:
$$
X_{i}|\mu,\sigma^{2}\sim N\left( \mu,\sigma^{2}=\frac{1}{\tau} \right)
$$
Note that the normalisation constant $\frac{1}{\sqrt{ 2\pi\sigma^{2} }}$ does not depend on $\mu$, (which is our $\theta$; our parameter of interest), so we can absorb it into the proportionality
$$
\implies \ell(\mu)=f(x_{1},\dots,x_{n}|\mu,\tau)=f(\underline{x}|\mu,\tau)=\prod_{i=1}^{n}f(x_{i}|\mu,\tau )
$$
$$
\propto \prod_{i=1}^{n}\exp\left( -\frac{\tau}{2}(x_{i}-\mu)^{2} \right)=\exp\left( -\frac{\tau}{2}\sum_{i=1}^{n}(x_{i}-\mu)^{2} \right)
$$
We can rewrite this sum:
$$
\sum_{i=1}^{n}(x_{i}-\mu)^{2}=\sum_{ i=1} ^{ n}  (x_{i}-\bar{x}+\bar{x}-\mu)^{2}=\dots=n(\bar{x}-\mu)^{2}+\sum_{ i=1} ^{ n}  (x_{i}-\bar{x})^{2}
$$
And $\sum_{ i=1} ^{ n} (x_{i}-\bar{x})^{2}$ is constant for a given sample as it is purely a function of the data $x_{i}$ and not of $\mu$, so we can absorb this into the proportionality
So our likelihood is:
$$
f(\underline{x}|\mu,\tau)\propto \exp\left( -\frac{n\tau}{2}(\bar{x}-\mu)^{2} \right)
$$
Our prior pdf for $\mu$ is also normal:
$$
f(\mu|m,t)=f(\mu)\propto \exp\left( -\frac{t}{2}(\mu-m)^{2} \right)
$$
Thus our posterior pdf for $\mu|x_{1},\dots,x_{n}=\mu|\underline{x}$ is proportional to the product of the likelihood of the prior; by the fundamental equation of Bayesian statistics:
$$
\text{posterior}\propto \text{likelihood}\times \text{prior}
$$
Then suppressing $\tau$ etc:
$$
f(\mu|x_{1},\dots,x_{n})=f(\mu|\underline{x})\propto f(\underline{x}|\mu)f(\mu)
$$
$$
 \propto \exp\left( -\frac{n\tau}{2}(\bar{x}-\mu)^{2} \right)\exp\left( -\frac{t}{2}(\mu-m)^{2} \right)
$$
$$
\propto \exp\left( -\frac{n\tau}{2}(\bar{x}-\mu)^{2}-\frac{t}{2}(\mu-m)^{2} \right)
$$
$$
 \propto \exp\left( -\frac{1}{2} (n\tau(\mu^{2}-2\mu \bar{x}+\bar{x}^{2})+t(\mu^{2}-2\mu m+m^{2}))\right)
$$
$$
 \propto \exp\left( -\frac{1}{2}((n\tau+t)\mu^{2}-2(n\tau \bar{x}+tm)\mu+(n\tau \bar{x}^{2}+tm^{2})) \right)
$$
$$
 \propto \exp \left(  -\frac{n\tau+t}{2}\left( \mu^{2}-2\mu\left( \frac{n\tau \bar{x}+tm}{n\tau+t} \right) \right) \right) 
$$
$$
 \propto \exp\left( -\frac{t_{1}}{2}(\mu^{2}-2\mu m_{1}) \right)
$$
Which we can see is the core of the normal distribution $N\left( m_{1},\frac{1}{t_{1}} \right)$, so therefore:
$$
\mu|\bar{x}\sim N\left( m_{1},\frac{1}{t_{1}} \right)
$$
With
$$
t_{1}=t+n\tau 
$$
$$
 m_{1}=\frac{tm+n\tau \bar{x}}{t+n\tau}
$$
As required
### Example
A process for testing water contamination by a particular agent produces normal data:
$$
X_{i}\sim N(\mu,\sigma^{2})
$$
With $\sigma=135$, so $\tau=\frac{1}{\sigma^{2}}=\frac{1}{325^{2}}$
The prior beliefs are normal:
$$
\mu \sim N\left( m,\frac{1}{t} \right)
$$
With $m=750$ and a $95\%$ probability that $250<\mu<1250$, so for a prior standard deviation $v$, we need $1.96v=500\implies v\approx 250$, so $t=\frac{1}{v^{2}}=\frac{1}{250}^{2}$, so to estimate $\mu$, we take $n=18$ iid samples with $\bar{x}=603.22$ so our posterior for $\mu$ is:
$$
\mu|x\sim N\left( m_{1},v_{1}^{2}=\frac{1}{t_{1}} \right)
$$
$$
 t_{1}=t+n\tau=\frac{1}{250^{2}}+\frac{18}{135^{2}}=1\times 10^{-5}
$$
$$
 \implies v_{1}=\sqrt{ \frac{1}{t_{1}} }=31.56
$$
$$
m_{1}=\frac{t}{t_{1}}m+\frac{n\tau}{t_{1}}\bar{x}=605.53
$$
So a new $95\%$ [[Credible Intervals|credible interval]] is:
$$
E(\mu|\underline{x})\pm z^{*}_{\frac{\alpha}{2}}\sqrt{ Var(\mu|\underline{x}) }
$$
$$
 =m_{1}\pm \frac{1}{96}v_{1}
$$
$$
= [543.67,667.38]
$$

