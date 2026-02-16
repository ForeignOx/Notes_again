## Theorem
Let $(X_{n})_{n\in\mathbb{N}_{0}}$ be [[Markov Chains|$Markov(\lambda,P)$]], and let $T$ be a [[Stopping Times|stopping time]] for $(X_{n})_{n\in\mathbb{N}_{0}}$. Assume that $\mathbb{P}(T<\infty,X_{T}=i)>0$. Conditionally on $T<\infty$ and $X_{T}=i$, $(X_{T+n})_{n\in\mathbb{N}_{0}}$ is $Markov(\delta_{i},P)$ and [[Independence|independent]] of $X_{0},X_{1},\dots,X_{T}$
### Proof
We recall that if $(X_{n})_{n\in\mathbb{N}_{0}}$ is $Markov(\lambda,P)$ and $\mathbb{P}(X_{m}=i)>0$, then conditional on $X_{m}=i$, the sequence $(X_{m+n})_{n\in\mathbb{N}_{0}}$ is $Markov(\delta_{i},P)$ and is independent of $X_{0},X_{1},\dots,X_{m-1}$
We fix $i_{1},i_{2},\dots,i_{m}\in I$, for $m>0$. Our goal is to show that
$$
\mathbb{P}(X_{T+1}=j_{1},\dots,X_{T+m}=j_{m}\mid T<\infty,X_{T}=i)=\mathbb{P}_{i}(X_{n+1}=j_{1},\dots,X_{n+m}=j_{m})
$$
We now fix $n\geq 0$ for the time being. Since $\left\{ T=n \right\}$ depends only on the first $n$ times, we can write $\left\{ T=n,X_{T}=i \right\}=A\cap \left\{ X_{n}=i \right\}$, where $A$ depends only upon $X_{0},\dots,X_{n-1}$ (because if $X_{n}=i$, then $X_{n}$ i determined, so then $A$ depends only on the first $n-1$ times)
Therefore
$$
\mathbb{P}(T=n,X_{T}=i,X_{T+1}=j_{1},\dots,X_{T+m}=j_{m})
$$
$$
 =\mathbb{P}(A\cap \left\{ X_{n}=i \right\}\cap X_{n+1}=j_{1},\dots,X_{n+m}=j_{m})
$$
$$
=\mathbb{P}(A\cap \left\{ X_{n}=i \right\})\mathbb{P}_{i}(X_{n+1}=j_{1},\dots,X_{n+m}=j_{m})
$$
$$
= \mathbb{P}(T=n,X_{T}=i)\mathbb{P}_{i}(X_{n+1}=j_{1},\dots,X_{n+m}=j_{m})
$$
Where we are using the Markov property for the second equality
Now we take the sum over $n$, uing countable additivity and the fact that events for different values of the stopping time are disjoint to get
$$
\mathbb{P}(T<\infty,X_{T}=i,X_{T+1}=j_{1},\dots,X_{T+m}=j_{m})
$$
$$
 =\sum_{n=0}^{\infty} \mathbb{P}(T=n,X_{T}=i,X_{T+1}=j_{1},\dots,X_{T+m}=j_{m})
$$
$$
=\sum_{n=0}^{\infty} \mathbb{P}(T=n,X_{T}=i)\mathbb{P}(A\cap \left\{ X_{n}=i \right\})\mathbb{P}_{i}(X_{n+1}=j_{1},\dots,X_{n+m}=j_{m}) 
$$
$$
= \mathbb{P}(T<\infty,X_{T}=i)\mathbb{P}_{i}(X_{n+1}=j_{1},\dots,X_{n+m}=j_{m})
$$
Now dividing both sides by $\mathbb{P}(T<\infty,X_{T}=i)$ and using the rules for [[Conditional Probability|conditional probabilities]], we get
$$
\mathbb{P}(X_{T+1}=j_{1},\dots,X_{T+m}=j_{m}\mid T<\infty,X_{T}=i)=\mathbb{P}_{i}(X_{n+1}=j_{1},\dots,X_{n+m}=j_{m})
$$
Which is what we wanted
## Example
Let $A$ be an event. Write $\mathbb{1}_{A}$ for the [[Indicator Function|indicator]] of $A$
Write 
$$
T_{j}^{n}:=\inf\left\{ m>T_{j}^{n-1}:\middle|:X_{m}=j \right\},~T^{0}_{j}=0,~T^{1}_{j}=\frac{T}{j}
$$
For the $n$th passage time to $j$. We can show these are stopping times
Consider if $i\neq j$
$$
\sum_{m=0}^{T^{n}_{j}}\mathbb{1}(X_{m}=i)
$$
For $Markov(\delta_{j},P)$, thi is
$$
\underbrace{ \sum_{m=0}^{T_{1}^{1}-1}\mathbb{1}(X_{m}=i) }_{ =Y_{1} }+\underbrace{ \sum_{m=T_{j}^{1}}^{T_{j}^{2}-1}\mathbb{1}(X_{m}=i) }_{ =Y_{2} }+\dots+\underbrace{ \sum_{m=T_{j}^{n-1}}^{T^{n}_{j}-1}\mathbb{1}(X_{m}=i) }_{ =Y_{n} }
$$
Assume $\mathbb{P}(T_{j}^{n}<\infty)=1$. Then the strong Markov property says that the $Y_{m}$ are [[Independent and Identically Distributed|independent and identically distributed]] random variables!
This suggests that there is some regularity to how often $X_{n}$ returns to a given state $i$, by the [[strong law of large numbers|law of large numbers]] 