Let $\sum_{k=1}^{\infty} a_{k}$ be a [[Conditional Convergence|conditionally convergent]] [[Series|series]], and $L\in\mathbb{R}$. Then there exists a rearrangement of the natural numbers $\sigma:\mathbb{N}\to \mathbb{N}$ which is [[Bijective Functions|bijective]] such that the rearranged sum
$$
\sum_{k=1}^{\infty} a_{\sigma(k)} 
$$
Converges to $L$
Moreover, there is a rearrangement that is divergent
## Proof
Let 
$$
a_{k}^{+}=\frac{|a_{k}|+a_{k}}{2}=\begin{cases}
a_{k}&\text{if }a_{k}\geq 0\\0&\text{if }a_{k}<0
\end{cases}
$$
$$
a_{k}^{-}=\frac{|a_{k}|-a_{k}}{2}=\begin{cases}
0&\text{if }a_{k}\geq 0\\\left| a_{k} \right| &\text{if }a_{k}<0
\end{cases}
$$
Both $\sum_{k=1}^{\infty} a_{k}^{+}$ and $\sum_{k=1}^{\infty} a_{k}^{-}$ are divergent, as 
$$
a_{k}=a_{k}^{+}-a_{k}^{-},\left| a_{k} \right|=a_{k}^{+}+a_{k}^{-}
$$
So if one of them were convergent, so would be the other (if $\sum_{k=1}^{\infty} a_{k}^{+}$ is convergent, then $a_{k}^{-}=a_{k}^{+}-a_{k}$), if both are convergent, the series is absolute convergent
Now let $b_{k}$ be the $k$th element of the [[Sequences|sequence]] $(a_{n})_{n\in\mathbb{N}}$ which is $\geq 0$, and $c_{k}$ is the $k$th element which is $<0$, so $(b_{k})_{k\in\mathbb{N}}$ and $(c_{k})_{k\in\mathbb{N}}$ are [[Subsequences|subsequences]]
Then $\sum_{k=1}^{\infty} b_{k}$ and $\sum_{k=1}^{\infty} c_{k}$ are also divergent, note
$$
\sum_{ k=1} ^{ n}c_{k}=-\sum_{ k=1} ^{ _{k_{n}}}a_{k}^{-}
$$
Where $k_{n}$ is the $n$th element which gives $a_{k_{n}}<0$
Given $L\in\mathbb{R}$, let $n_{0}$ be the first index with
$$
\sum_{k=1}^{n_{0}}b_{k}>L
$$
(if $L<0$, then $n_{0}=0$ will work)
Now let $n_{1}$ be the first index such that
$$
\sum_{k=1}^{n_{0}}b_{k}+\sum_{k=1}^{n_{1}}<L
$$
Now pick $n_{2}>n_{1}$ such that
$$
\sum_{k=1}^{n_{0}}b_{k}+\sum_{k=1}^{n_{1}}c_{k}+\sum_{k=n_{0}+1}^{n_{2}}b_{k}>L
$$
Continue this, and we have
$$
\lim_{ n \to \infty } b_{k}=\lim_{ n \to \infty } c_{k}=0
$$
And this allows us to get convergence to $L$ with right rearragnement
## Theorem
Let $\sum_{k=1}^{\infty} a_{k}$ be an [[Absolute Convergence|absolutely convergent]] series and $\sigma:\mathbb{N}\to \mathbb{N}$ a bijection. Then $\sum_{k=1}^{\infty} a_{\sigma(k)}$ is also absolutely convergent, and we have
$$
\sum_{k=1}^{\infty} a_{k} =\sum_{k=1}^{\infty} a_{\sigma(k)} 
$$
### Proof
Look at $s_{n}=\sum_{k=1}^{n}\left| a_{k} \right|$ which is a monotonically increasing sequence which converges to $a$, and so $s_{n}\leq a$
For $s_{n}'=\sum_{k=1}^{n}\left| a_{\sigma(k)} \right|\leq s_{m}$ is also a monotonically increasing sequence where $m=\text{max}\{ \sigma(1),\dots,\sigma(n) \}$
This implies $s_{n}'\leq a$ for all $n$, so $(s_{n}')_{n\in\mathbb{N}}$ is a convergent series
This shows absolute convergentce of $\sum_{k=1}^{\infty} a_{\sigma(k)}$ with limit $a'=\sum_{k=1}^{\infty} \left| a_{\sigma(k)} \right|$
Note that $\sum_{k=1}^{\infty} \left| a_{k} \right|$ is a rearrangement of $\sum_{k=1}^{\infty} \left| a_{\sigma(k)} \right|$ which using $\sigma ^{-1}$ implies that $a\leq a'\leq a$, so $a=a'$
Look at $b_{k}=a_{k}+\left| a_{k} \right|\geq 0$. then
$$
\sum_{k=1}^{\infty} a_{k} +\left| a_{k} \right| =\sum_{k=1}^{\infty} a_{\sigma(k)}+\left| a_{\sigma(k)} \right|  
$$
So by [[Calculus of Limits Theorem|CoLT]],
$$
\sum_{k=1}^{\infty} a_{k} +\sum_{k=1}^{\infty} \left| a_{k} \right| =\sum_{k=1}^{\infty} a_{\sigma(k)}+\sum_{k=1}^{\infty} \left| a_{\sigma(k)} \right|    
$$
$$
\implies \sum_{k=1}^{\infty} a_{k} =\sum_{k=1}^{\infty} a_{\sigma(k)}
$$
As required

#Mathematics #Analysis #Theorem 