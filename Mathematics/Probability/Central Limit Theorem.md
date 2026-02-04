Anything is a normal distribution if you squint hard enough
Let $X_{1},X_{2},\dots$ be an [[Independent and Identically Distributed|IID]] sequence of [[Random Variables|random variables]]. Let $\mu=\mathbb{E}(X_{i})$ and define:
$$
\overline{X}_{n}=\frac{1}{n}\sum_{ i=1} ^{ n}  X_{i}
$$
and
$$
S_{n}=\sum_{ i=1} ^{ n}  X_{i}
$$
Let
$$
Z_{n}=\frac{S_{n}-n\mu}{\sigma \sqrt{ n }}=\frac{\overline{X}_{n}-\mu}{\frac{\sigma}{\sqrt{ n }}}
$$
Let $F_{Z_{n}}(\cdot)$ denote the [[Cumulative Distribution Functions|cdf]] of $Z_{n}$. Then for any $z\in\mathbb{R}$,
$$
\lim_{ n \to \infty } F_{Z_{n}}(z)=\lim_{ n \to \infty } \mathbb{P}(Z_{n}\leq z)=\Phi(z)
$$
Where $\Phi(z)$ is the cdf of the [[Normal Distribution#Standard Normal|standard normal]], so essentially $Z_{n}$ converges in distribution to a standard normal random variable
## Interpretation
$$
Z_{n}\approx N(0,1)
$$
So
$$
E(Z_{n})=\frac{E(\overline{X}_{n})-\mu}{\frac{\sigma}{\sqrt{ n }}}=\frac{\mu-\mu}{\frac{\sigma}{\sqrt{ n }}}=0
$$
$$
Var(Z_{n})=\frac{1}{\sigma^{2}n}Var(S_{n})=\frac{1}{\sigma^{2}n}\sum_{ i=1} ^{ n}  Var(X_{i})
$$
Since the $X_{i}$'s are independent
$$
=\frac{1}{\sigma^{2}n}n\sigma^{2}=1
$$
Which roughly tells us that
$$
S_{n}\approx N(n\mu,n\sigma^{2})
$$
$$
\overline{X}_{n}\approx N\left( \mu, \frac{\sigma^{2}}{n} \right)
$$
$$
\mathbb{P}(S_{n}\leq x)\approx \Phi\left( \frac{x-n\mu}{\sqrt{ n }\sigma} \right)
$$
$$
\mathbb{P}(\overline{X}_{n}\leq x)\approx \Phi\left( \frac{x-\mu}{\frac{\sigma}{\sqrt{ n }}} \right)
$$
A stronger version of CLT is the Lindeberg Feller (for triangular array)
## Example
Suppose we have potaties with average weight $100\pu{ g}$, and standard deviation $40\pu{ g}$. Packe in a bag to contain at least $2500\pu{ g}$ What is the chance that we need more than $\hspace{0pt}30$ potatoes
Given
$$
\Phi(2.282)=0.989
$$
Let
$$
N:=\text{number of potaties needed to exceed }2000\pu{ g}
$$
Let $X_{i}$ be the weight of the $i$th potato

#Mathematics #Probability #Theorem 