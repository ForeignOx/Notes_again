## Theorem
Let $(X_{n})_{n\in\mathbb{N}_{0}}$ be [[Markov Chains|$Markov(\lambda,P)$]], and let $T$ be a [[Stopping Times|stopping time]] for $(X_{n})_{n\in\mathbb{N}_{0}}$. Assume that $\mathbb{P}(T<\infty,X_{T}=i)>0$. Conditionally on $T<\infty$ and $X_{T}=i$, $(X_{T+n})_{n\in\mathbb{N}_{0}}$ is $Markov(\delta_{i},P)$ and [[Independence|independent]] of $X_{0},X_{1},\dots,X_{T}$
### Proof
We recall that if $(X_{n})_{n\in\mathbb{N}_{0}}$ is $Markov(\lambda,P)$ and $\mathbb{P}(X_{m}=i)>0$, then conditional on $X_{m}=i$, the sequence $(X_{m+n})_{n\in\mathbb{N}_{0}}$ is $Markov(\delta_{i},P)$ and is independent of $X_{0},X_{1},\dots,X_{T}$
