We assume that there is a [[Population|population]] with a mean $\mu$, and [[Standard Deviation|standard deviation]] $\sigma$ (often both unknown), our main aim is to estimate with little bias and small variance, $\mu$.
Our secondary aim is to estimate $\sigma$
We take a [[Sampling|simple random sample]] of size $n$ from the population (of size $N\gg n$), we denote the [[Samples|sample]] values as $X_{1},X_{2},\dots,X_{n}$ where $X_{i}$ are random variables with $X_{i}\in\mathbb{R}$ (not $\hspace{0pt}0$,1)
Before we see their values, each $X_{i}$ is a [[Random Variables|random variable]] having the same mean and standard deviation:
$$
E(X_{i})=\mu 
$$
$$
 Var(X_{i})=\sigma^{2}
$$
$$
\implies SD(X_{i})=\sigma
$$
We also assume the $X_{i}$ are [[Independent and Identically Distributed|IID]], we define the sample mean:
$$
\bar{X}=\frac{1}{n}\sum_{ i=1} ^{ n}  X_{i}
$$
Note that the sample mean is not equal to $\mu$, the population mean
We now derive the properties of the sample mean estimator:
$$
E(\bar{X})=E\left( \frac{1}{n}\sum_{ i=1} ^{ n}   X_{i}\right)=\frac{1}{n}E\left( \sum_{ i=1} ^{ n}  X_{i} \right)=\frac{1}{n}\sum_{ i=1} ^{ n}  E(X_{i})=\frac{1}{n}\sum_{ i=1} ^{ n}  \mu=\frac{1}{n}n\mu=\mu
$$
Therefore $\bar{X}$ is an unbiased estimator of the population mean $\mu$, next want $Var(\bar{X})$:
$$
Var(\bar{X})=Var\left( \frac{1}{n}\sum_{ i=1} ^{ n}  X_{i} \right)=\frac{1}{n^{2}}Var\left( \sum_{ i=1} ^{ n}  X_{i} \right)=\frac{1}{n^{2}}\sum_{ i=1} ^{ n}  Var(X_{i})=\frac{1}{n^{2}}\sum_{ i=1} ^{ n}  \sigma^{2}
$$
$$
= \frac{1}{n^{2}}n\sigma=\frac{\sigma^{2}}{n}
$$

Therefore, as $Var(\bar{X})=\frac{\sigma^{2}}{n}$, it can be controlled via $n$, (double $n$ means halving variance, but standard deviation goes down by just $\sqrt{ 2 }$)
Also $Var(\bar{X})$ depends on $\sigma^{2}$, so it is not easily bounded
Hence $\bar{X}$ should be a good estimator for $\mu$
Furthermore, if the main population of $X_{i}$ is [[Normal Distribution|normally distributed]] with mean $\mu$ and variance $\sigma^{2}$ i.e.
$$
X_{i}\sim N(\mu,\sigma^{2})
$$
$$
\implies \bar{X}=\left( \mu, \frac{\sigma^{2}}{n} \right)
$$
Due to the sum of normal random variables being also Normal
![[Pasted image 20250207144339.png]]

#Mathematics #Statistics 