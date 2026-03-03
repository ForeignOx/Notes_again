## Simple Random Walk on $\mathbb{Z}$
The simple random walk on $\mathbb{Z}$ is a [[Markov chains|Markov chain]] with diagram:
![[Pasted image 20260303164012.png]]
Where $0<p=1-q<1$
Consider $f_{0}=\mathbb{P}_{0}(\text{return to }0)$ and let $h_{i}=\mathbb{P}_{i}(\text{hit }0)$, then
$$
f_{0}=qh_{-1}+ph_{1}
$$
Using the [[strong Markov property|strong Markov property]] $h_{1}=q+ph_{1}^{2}$ the smallest solution is $h_{1}=\min\left\{ 1, \frac{q}{p} \right\}$. So if $q=p=\frac{1}{2}$ then $h_{-1}=h_{1}=1$ which implies $f_{0}=1$ and the random walk is [[Recurrence and Transience|recurrent]]
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
n!\sim A\sqrt{ n } \left( \frac{n}{e} \right)^{n}
$$
For some $A\in[1,\infty)$ (we do not need here that $A=\sqrt{ 2\pi }$), thus
$$
P_{00}^{2n}= \frac{(2n)!}{(n!)^{2}}(pq)^{n} \sim \frac{(4pq)^{n}}{A\sqrt{ \frac{n}{2} }}\text{ as }n\to\infty
$$
In the symmetric case $p=q=\frac{1}{2}$, we have that $4pq=1$ and so for some $N$ and all $n\geq N$,
$$
P_{00}^{2n}\geq \frac{1}{2A\sqrt{ n }}
$$
So
$$
\sum_{n=N}^{\infty} P_{00}^{2n}\geq \frac{1}{2A}\sum_{n=N}^{\infty} \frac{1}{\sqrt{  n }}=\infty
$$
Which shows that the random walk is recurrent
On the other hand, if $p\neq q$, then $4pq = r<1$, so by a similar argument, for some $N$,
$$
\sum_{n=N}^{\infty} P_{00}^{2n}\leq \frac{1}{A} \sum_{n=N}^{\infty} r^{n}<\infty
$$
And so the random walk is transient
## Simple Symmetric Random Walk on $\mathbb{Z}^{2}$
The simple random walk on $\mathbb{Z}^{2}$ has diagram:
![[Pasted image 20260303165550.png]]
And transition probabilities:
$$
p_{ij}=\begin{cases}
\frac{1}{4} & \left| i-j \right| =1 \\
0 & \text{otherwise}
\end{cases}
$$
Suppose we start at $0$, let us call the walk $X_{n}$ and write $X_{n}^{+}$ and $X_{n}^{-}$ for the projection of the walk on the diagonal lines $y=\pm x$,
![[Pasted image 20260303165722.png]]
Then $X_{n}^{+}$ and $X_{n}^{-}$ are independent symmetric random walks on $\frac{1}{\sqrt{ 2 }}\mathbb{Z}$ and $X_{n}=0$ iff $X_{n}^{+}=X_{n}^{-}=0$, this makes clear that for $X_{n}$ we have
$$
P_{00}^{2n}=\left( {2n \choose n }\left( \frac{1}{2} \right)^{2n} \right)^{2}\sim \frac{2}{A^{2}n}\text{ as }n\to\infty
$$