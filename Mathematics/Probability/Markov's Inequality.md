A useful inequality linking [[Probabilities|probability]] and [[Expectation|expectation]] 
## Theorem
If [[Random Variables|$X\geq 0$]], then for any $a>0$,
$$
\mathbb{P}(X\geq a)\leq \frac{\mathbb{E}(X)}{A}
$$
### Proof
Observe 
$$
X\geq a\mathbb{1}_{\{ X\geq a \}}=\begin{cases}
a&\text{if }X(\omega)\geq a\\0&\text{otherwise}
\end{cases}
$$
Hence
$$
\mathbb{E}(X)\geq \mathbb{E}(a\mathbb{1}_{\{ X\geq a \}})=a\mathbb{E}(\mathbb{1}_{\{ X\geq a \}})=a\mathbb{P}(X\geq a)
$$
___
## More General Version
Let $g:[0,\infty)\to[0,\infty)$ be an [[Monotonic Functions|increasing]] [[Functions|function]]. Then for each random variable $X\geq 0$ and fixed $a>0$ we have
$$
\mathbb{P}(X\geq a)\leq \frac{\mathbb{E}(g(X))}{g(a)}
$$
### Proof
Because $g$ increases, for each fixed $a>0$ and all $x\geq 0$, we have $g(x)\geq g(x)\mathbb{1}_{x\geq a}\geq g(a)\mathbb{1}_{x\geq a}\geq 0$
By applying this inequality to the random variable $X\geq 0$ and taking expectations, we obtain
$$
\mathbb{E}(g(X))\geq g(a)\mathbb{E}(\mathbb{1}_{X\geq a})\equiv g(a)\mathbb{P}(X\geq a)
$$
As $g(a)>0$ we are done
## Remark
This is trivially true unless $\mathbb{E}(g(X))<\infty$
When $g(x)\equiv x$ we clearly have the standard Markov's inequality
Similarly, when $g(x)=x^{2}$ for $x\geq 0$ and $X=\left| Y-\mathbb{E}(Y) \right|$ for some random variable $Y$, this becomes [[Chebychev's Inequality|Chebychev's inequality]]
