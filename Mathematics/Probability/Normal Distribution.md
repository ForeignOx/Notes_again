A [[Continuous Random Variables|continuous]] [[Random Variables|random variable]] $X$ is normally distributed with parameters $\mu,\sigma^{2}$, ($\mu,\sigma \in\mathbb{R},\sigma>0$) if the pdf is given by
$$
f(x)=\frac{1}{\sqrt{ 2\pi }\sigma}e^{ -\frac{(x-\mu^{2})}{2\sigma^{2}} }
$$
The curve follows a symmetric bell shape, with mean at the peak:
![[Pasted image 20241114183806.png]]
## Standard Normal
A random variable $Z$ is said to be a standard normal if it has the following pdf:
$$
\varphi(z)=\frac{1}{\sqrt{ 2\pi }}e^{ -z^{2}/2 }
$$
With $z\in\mathbb{R}$, and also have the following [[Cumulative Distribution Functions|cdf]]:
$$
\Phi(z)=\frac{1}{\sqrt{ 2\pi }}\int _{-\infty}^{x}e^{ -t^{2}/2 } \, dt 
$$
$Z$ is used to denote $N(0,1)$
### Converting
Let $X\sim N(\mu,\sigma^{2})$ and $Z\sim N(0,1)$, then 
$$
\frac{X-\mu}{\sigma}\sim N(0,1)
$$
$$
\mu+\sigma Z\sim N(\mu,\sigma^{2})
$$
### Proof
Let $Y$ be the random variable $\frac{X-\mu}{\sigma}$ where $X\sim N(\mu,\sigma^{2})$
$$
\mathbb{P}(Y\leq y)=\mathbb{P}\left( \frac{X-\mu}{\sigma}\leq y \right)=\mathbb{P}(X\leq \mu+\sigma y)
$$
$$
= \frac{1}{\sqrt{ 2\pi }\sigma}\int _{-\infty}^{\mu+\sigma y}e^{ -(t-\mu)^{2}/2\sigma^{2} } \, dt 
$$
Let $z=\frac{t-\mu}{\sigma}$, then $t \to -\infty,z\to \infty,t+\mu+\sigma y,z=y,\sigma dz=dt$, so we get:
$$
\mathbb{P}(Y\leq y)=\frac{1}{\sqrt{ 2\pi }}\int _{-\infty}^{y}e^{ -z^{2}/2 } \, dz =\Phi(y)
$$
Where $\Phi$ is the cdf of a $N(0,1)$
## Properties of Stadard Normal
The standard normal density function is symmetric around the origin; $\phi(z)=\phi(-z)$, similarly the pdf of $N(\mu,\sigma)$ is symmetric around $\mu$
### Proof
$$
\phi(z)=\frac{1}{\sqrt{ 2\pi }}e^{ -z^{2}/2 }=\phi(-z)
$$
Due to the square
___
$$
\Phi(z)=1-\Phi(-z)
$$
### Proof
$$
\Phi(z)=\frac{1}{\sqrt{ 2\pi }}\int _{-\infty}^{z}e^{ -t^{2}/2 } \, dt 
$$
Letting $t=-u$, $dt=-du$, $t\to -\infty,u\to \infty,t=z,u=-z$, which putting back into the integral gives:
$$
\Phi(z)=-\frac{1}{\sqrt{ 2\pi }}\int _{\infty}^{-z}e^{ -u^{2}/2 } \, du=\frac{1}{\sqrt{ 2\pi }}\int _{z}^{\infty}e^{ -u^{2}/2 } \, du
$$
$$
 =\mathbb{P}(Z\geq-z)=1-\Phi(-z)
$$
## [[Expectation|Expectation]]
Let $Z\sim N(0,1)$, find $\mathbb{E}(Z)$
$$
\mathbb{E}(Z)=\int_{-\infty}^{\infty} z\phi(z) \, dx 
$$
$$
=\underbrace{ \frac{1}{\sqrt{ 2\pi }} \int _{-\infty}^{0}ze^{ -z^{2}/2 } \, }_{ =I_{1} } dx +\underbrace{ \frac{1}{\sqrt{ 2\pi }}\int _{0}^{\infty}ze^{ -z^{2}/2 } \, dx  }_{ =I_{2} }
$$
Then $z\to-t$, $dx=-dt$, $z\to-\infty$, $z=0$, $t=0$, then
$$
    I_{1}=\frac{1}{\sqrt{ 2\pi }}\int _{-\infty}^{\infty} t e^{ -t^{2}/2 } \, dx =-\frac{1}{\sqrt{ 2\pi }}\int _{0} ^{\infty } te^{ -t^{2}/2 }\, dx =I_{2}
$$
Therefore $E[Z]=E[-Z]=-\mathbb{E}(Z)$, so $\mathbb{E}(Z)=0$
Now $Z=\frac{X-\mu}{\sigma}$, so $X=\mu+\sigma Z$, so by linearity:
$$
\mathbb{E}(X)=\mu+\sigma \mathbb{E}(Z)=\mu
$$
___
## [[Variance|Variance]]
Assume for now $\mathbb{V}\mathrm{ar}(Z)=1$, then $\mathbb{V}\mathrm{ar}(X)=\mathbb{V}\mathrm{ar}(\mu+\sigma X)=\sigma^{2}\mathbb{V}\mathrm{ar}(Z)=\sigma^{2}$



#Mathematics #Probability #Definition 