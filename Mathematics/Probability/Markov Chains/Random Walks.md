## Simple Random Walk on $\mathbb{Z}$
The simple random walk on $\mathbb{Z}$ is a [[Markov chains|Markov chain]] with diagram:
![[Pasted image 20260303164012.png]]
Where $0<p=1-q<1$
Consider $f_{0}=\mathbb{P}_{0}(\text{return to }0)$ and let $h_{i}=\mathbb{P}_{i}(\text{hit }0)$, then
$$
f_{0}=qh_{-1}+ph_{1}
$$
Using the [[strong Markov property|strong Markov property]] $h_{1}=q+ph_{1}^{2}$ the smallest solution is $h_{1}=\min\left\{ 1, \frac{q}{p} \right\}$. So if $q=p=\frac{1}{2}$ then $h_{-1}=h_{1}=1$ which implies $f_{0}=1$ and the random walk is recurrent
If $q<p$ then $h_{1}<1$ which implies $f_{0}<1$ and transience. Similarly, if $q>p$, then $h_{-1}<1$ and we have transience
___
We can also analyse this random walk by testing whether $\sum_{n=0}^{\infty}P_{00}^{n}$ is finite or infinite. This is a more complicated method, but is useful
Suppose we start at $\hspace{0pt}0$. Obviously, we cannot return to $\hspace{0pt}0$ after an odd number of steps, so $P_{00}^{2n+1}=0$ for all $n$
Any given sequence of steps of length $2n$ from $0$ to $0$ occurs with probability $p^{n}q^{n}$, there being $n$ steps right and $n$ steps left, and the number of such sequences is the number of way sof choosing the $n$ steps from $2n$, thus
$$
P_{00}^{2n}={2n \choose n } p^{n}q^{n}
$$
Stirling's approximation provies an approximation to $n!$ for large $n$, 
$$
n\neq A\sqrt{ n } \left( \frac{n}{e} \right)^{n}
$$

