What if $\sigma$ is unknown and $n$ is smol? If $X_{i}\sim N(\mu,\sigma^{2})$ or approximately normal
We still use $s$ to estimate $\sigma$, but now:
$$
\frac{\bar{X}-\mu}{\frac{S}{\sqrt{ n }}}\sim t_{n-1}
$$
This is a $t$-distribution with $n-1$ degrees of freedom
Everything proceeds as before, but we use $t_{n-1}$ tables instead of normal talbes :sob:
## Definition
A random variable $T-t$ (when measured) has a $t$-distribution with degrees of freedom parameter $\nu$, where $\nu=n-1$, if it has the following pdf:
$$
f(t|\nu)=\frac{\Gamma\left( \frac{\nu+1}{2} \right)}{\sqrt{ \nu \pi }\Gamma\left( \frac{\nu}{2} \right)}\left( 1+\frac{t^{2}}{\nu} \right)^{- \frac{\nu+1}{2}}
$$
We write
$$
T\sim t_{\nu}
$$
Note $E(T)=0$, $Var(T)=\frac{\nu}{\nu-2}$
The limit as $n\to \infty$ is $t_{n-1}\to N(0,1)$
## Examples
The number of flaws per square meter in a type of carpet is variable with mean $\mu=1.6$ flaws per square metre and standard deviation $\sigma=1.2$ flaws per square metre. The distrivution is not normal, in fact, it is discrete. An inspector studies $\hspace{0pt}200$ square metres of material, records the number of flaws found in each square metre $(X_{i},i=1,\dots,200)$ and calculates $\bar{X}$, the sample mean. What is the probability that $\bar{X}$ exceeds $\hspace{0pt}1.7$ flaws per square metre?
Here we have a random sample $X_{1},X_{2},\dots,X_{200}$ each with
$$
E(X_{i})=1.6,Var(X_{i})=1.2^{2}
$$
We don't know the distribution of the $X_{i}$'s, but we do know the distribution of $\bar{X}$, by the central limit theorem:
$$
\bar{X}\sim N\left( 1.6,\frac{1.2^{2}}{200} \right)
$$
We seek $\mathbb{P}(\bar{X}>1.7)$ 
$$
\mathbb{P}(\bar{X}>1.7)=\mathbb{P}\left(   \frac{\bar{X}-\mu}{\frac{\sigma}{\sqrt{ n }}}> \frac{1.7-\mu}{\sigma /\sqrt{ n }} \right)
$$
$$
= \mathbb{P}\left( Z> \frac{1.7-1.6}{0.085} \right)
$$
Where $Z\sim N(0,1)$
$$
=\mathbb{P}(Z>1.18)=0.1190
$$
___
A light bulb manufacturer claims that the mean life of a lightbulb is $\hspace{0pt}1200$ hours. A consumer association randomly selects $\hspace{0pt}16$ bulbs with intention of rejecting the manufacturer's claim if $\bar{X}$ is less than $\hspace{0pt}1160$ hours.
The sample standard deviation $s=200$
1. If the manufacturers are in fact honest, what is the probability that they will be declared dishonest?
2. Find a value $c$ so that $\mathbb{P}(\bar{X}<c)=0.05$
By our theory, the distribution of the standardised sample mean is:
$$
T= \frac{\bar{X}-\mu}{\frac{S}{\sqrt{ n }}}\sim t_{15}
$$
Once measured, we get $\frac{\bar{X}-1200}{\frac{200}{\sqrt{ 16 }}}$. Now the probability that this sample mean is smaller than $\hspace{0pt}1160$ is:
$$
\mathbb{P}(\bar{X}<1160)=\mathbb{P}\left( \frac{\bar{X}-1200}{\frac{200}{\sqrt{ 16 }}}<\frac{1160-1200}{\frac{200}{\sqrt{ 16}}} \right)
$$
$$
= \mathbb{P}(T<-0.8)
$$
Since the $t$-distribution is symmetric
$$
=\mathbb{P}(T>0.8)
$$
By looking at the the stupid tables, we see that:
$$
\mathbb{P}(T>0.691)=0.285,\mathbb{P}(T>0.866)=0.2
$$
Then the probability we require is between $\hspace{0pt}0.2$ and 0.25
The $t$-distribution is most often used in reverse: we want $c$ such that 
$$
\mathbb{P}(\bar{X}<c)=0.05
$$
From the stupid table,
$$
\mathbb{P}(T<-1.753)=\mathbb{P}(T>1.753)=0.05
$$
$$
\implies \mathbb{P}\left( \frac{\bar{X}-1200}{\frac{200}{\sqrt{ 16 }}}<-1.753 \right)=0.05
$$
$$
\implies \mathbb{P}(\bar{X}<1200-(50)(1.753))=0.05
$$
$$
\implies \mathbb{P}(X<1112.35)=0.05
$$
We should use this threshold instead of the (dangerous) $\hspace{0pt}1160$ and we will only be wrong 5% of the time