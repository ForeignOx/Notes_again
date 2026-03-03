An import thing to wonder about is what are the long run statitical properties of Markov chains??
To answer this, we will need invariant distributions  who wouldda thunk it 
## Terminology
A measure is a row vector with non-negative entries
A distribution is a measure whose entries sum to one
## Definition
If $P$ is stochastic, a measure $\lambda$ is invariant if $\lambda P=\lambda$ (this makes sense as matrix multiplication since $\lambda$ is a row vector)
We also use the terms that $\lambda$ is an equilibrium or stationary measure if $\lambda P=\lambda$ (different names reflect different ways of thinking what $\lambda P=\lambda$ means)
## Remark
We are mostly interested in distributions, so why do we introduce measures?
If $\lambda$ is a measure and $\sum_{i\in I}\lambda_{i}<\infty$, then
$$
\pi_{i}:= \frac{\lambda_{i}}{\sum_{i\in I}\lambda_{i}}
$$
Is a distribution. If $\lambda$ is invariant, so is $\pi$, as the equation $\lambda P=\lambda$ is linear in $\lambda$
Measures are theoretically useful for many reasons
## Theorem
If $(X_{n})_{n\in\mathbb{N}_{0}}$ is $Markov(\lambda,P)$ and $\lambda$ is invariant for $P$, then for any $m\geq 0$, $(X_{m+n})_{n\in\mathbb{N}_{0}}$ is $Markov(\lambda,P)$
### Proof
The Markov property says that $(X_{m+n})_{n\in\mathbb{N}_{0}}$ is $Markov(\mu,P)$, where
$$
\mu_{i}:=\mathbb{P}_{\lambda}(X_{m}=i)
$$
Since
$$
\mathbb{P}_{\lambda}(X_{m+n}\in  A)=\sum_{i\in I}\mathbb{P}((X_{m+n})_{n\in\mathbb{N}_{0}}\in  A\mid X_{m}=i)\mathbb{P}(X_{m}=i) 
$$
$$
= \sum_{i\in I} \mathbb{P}_{i}((X_{n})_{n\in\mathbb{N}_{0}}\in  A\mid X_{m}=i)\mu_{i}\mathbb{P}_{\mu}((X_{n})_{n\in\mathbb{N}_{0}}\in  A)
$$
But we know
$$
\mu_{i}=\mathbb{P}(X_{m}=i)=(\lambda P^{n})_{i}=(\lambda PP^{n-1})_{i}=(\lambda P^{n-1})_{i}=\dots = \lambda_{i}
$$
## Theorem
Suppose $\left| I \right|<\infty$ and there exists $i\in I$ such that the limit
$$
\lim_{ n \to \infty } P^{n}_{ij}=\pi_{j}\text{ exists for all }j\in  I
$$
Then $\pi=(\pi_{j})_{j\in I}$ is an invariant distribution
### Proof
Using the Chapman-Kolmogorov equations,
$$
\pi_{j}=\lim_{ n \to \infty } P_{ij}^{n}=\lim_{ n \to \infty } \sum_{k\in  I}P_{ik}^{n-1}P_{kj} 
$$
$$
= \sum_{k\in  I} (\lim_{ n \to \infty } P^{n-1}_{ik})P_{kj} 
$$
$$
= \sum_{k\in  I} \pi_{k} P_{jk}=(\pi P)_{j}
$$
## Remark
Note that $\left| I \right|<\infty$, is essential, this is not true in general if $\left| I \right|=\infty$, for example, the simple random walk on $\mathbb{Z}$ has $P_{ij}^{n}\to 0$ as $n\to\infty$ for all $i,j$
Thi theorem says that if you settle into a limiting distribution, then it must be invariant