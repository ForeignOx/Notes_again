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
___
Gambler's ruin but more innit
So before we computed $\mathbb{P}_{i}(H^{\left\{ 0 \right\}}<\infty)$ i.e. the time of bancruptcy, but now we can use the strong Markov property to compute
$$
\mathbb{P}_{i}(H^{\left\{ 0 \right\}}=n)
$$
The idea is to introduce the [[Probability Generating Functions|probability generating function]] 
$$
\Phi_{X}(s)=\sum_{n=0}^{\infty} s ^{n}\mathbb{P}(X=n)
$$
For random variables $X:\Omega\to \mathbb{N}$
We know by the rules of differentiation, that
$$
\frac{1}{n!}\frac{d ^{n}}{ds ^{n}} \Bigg{|}_{s=0} \Phi_{X}(s )=\sum_{n=m}^{\infty} m(m-1)\dots(m-n+1)s^{m-n}\Bigg{|}_{s=0} \mathbb{P}(X=m)=\mathbb{P}(X=n)
$$
We observe that if $(X_{n})_{n\in\mathbb{N}_{0}}$ is $Markov(\delta_{2},P)$, then
$$
H_{0}=H_{1}+\tilde{H}_{0}
$$
I.e;. if we start from $\hspace{0pt}2$, then the time to hit zero is equal to the time to hit $\hspace{0pt}1$ plus the time after hitting one to hit 0
But by translational symmetry, they have the same probabilistic distribution
Letting $\Phi_{n}(s)$ be the probability generating function of thehitting time starting from $n$, thus
$$
\Phi_{n}(s)=\mathbb{E}_{n}(s^{H_{0}})
$$
We claim that $\Phi_{2}=\Phi_{1}^{2}$
$$
\Phi_{2}(s)=\mathbb{E}_{2}(s ^{H_{0}})=\mathbb{E}( s^{H_{0}}\mathbb{1}_{H_{1}<\infty}) 
$$
$$
= \mathbb{E}_{2}(s^{H_{0}}\mid H_{1}<\infty)\mathbb{P}_{2}(H_{1}<\infty) 
$$
$$
= \mathbb{E}_{2}(s^{H_{1}}\mid H_{1}<\infty)\mathbb{E}_{2}(s^{\tilde{H}_{0}}\mid H_{1}<\infty)\mathbb{P}_{2}(H_{1}<\infty) 
$$
$$
= \mathbb{E}(s^{H_{1}}\mathbb{1}_{H_{1}<\infty})\mathbb{E}(s^{\tilde{H}_{0}}\mid H_{1}<\infty) 
$$
$$
= \mathbb{E}_{2}(s^{H_{1}})\mathbb{E}_{1}(s^{H_{0}})=(\Phi(s))^{2}
$$
Where we use the strong Markov property a few times
But we also have
$$
\Phi(s)=\mathbb{E}_{1}(s^{H_{0}})=\mathbb{E}_{1}(s^{H_{0}}(\mathbb{1}_{X_{1}=0}+\mathbb{1}_{X_{1}=2})) 
$$
$$
= \mathbb{E}_{1}(s^{H_{0}}\mid X_{1}=2)\mathbb{P}_{1}(X_{1}=2)+\mathbb{E}_{1}(s^{H_{0}}\mid X_{1}=0)\mathbb{P}_{1}(X_{1}=0)
$$
$$
 =p\mathbb{E}_{1}(s^{H_{0}}\mid X_{1}=2)+qs 
$$
$$
=ps\mathbb{E}_{2}(s^{H_{0}})+qs 
$$
$$
= ps(\Phi(s))^{2}+qs
$$
Therefore $\Phi(s)$ solves the quadratic equation $psx^{2}-x-qs=0$, hence
$$
\Phi(s)= \frac{1\pm \sqrt{ 1-4pqs^{2} }}{2ps}
$$
We know the Taylor series for $\sqrt{ 1-x }$:
$$
\sqrt{ 1-x }=1-\frac{x}{2}+\frac{x^{2}}{8}-\dots=\sum_{n=0}^{\infty} x^{n}(-1)^{n}{\frac{1}{2} \choose n }
$$
