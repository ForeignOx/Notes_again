A useful inequlity linking [[Probabilities|probability]] to [[Expectation|expectation]] and [[Variance|variance]]
## Theorem
Let $X:\Omega\to \mathbb{R}$ be a [[Random Variables|random vaiable]], let $a(\in\mathbb{R})$, then
$$
\mathbb{P}(|X-\mathbb{E}(X)|\geq a)\leq \frac{1}{a^{2}}\mathbb{V}\mathrm{ar}(X)
$$
### Proof
$$
\mathbb{P}(|X-\mathbb{E}(X)|\geq a)=\mathbb{P}((X-\mathbb{E}(X))^{2}\geq a^{2})\leq \frac{1}{a^{2}}\mathbb{E}((X-\mathbb{E}(X))^{2})=\frac{1}{a^{2}}\mathbb{V}\mathrm{ar}(X)
$$
Using [[Markov's Inequality|Markov's inequality]]