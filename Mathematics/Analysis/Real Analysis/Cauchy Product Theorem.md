If we have two [[Series|series]] $\sum_{k=0}^{\infty} a_{k}$ and $\sum_{k=0}^{\infty} b_{k}$ that are both [[Absolute Convergence|absolutely convergent]] with limits $a$ and $b$ respectively. We set
$$
c_{n}=\sum_{k=0}^{n}a_{k}b_{n-k}=a_{0}b_{n}+a_{1}b_{n-1}+\dots+a_{n}b_{0}
$$
Then the Cauchy Product which is
$$
\sum_{n=0}^{\infty} c_{n} 
$$
Converges absolutely with limit $ab$
You can think of this as taking our two partial sums and multiplying them out:
$$
\left( \sum_{k=0}^{n} a_{k}  \right)\left( \sum_{k=0}^{n} b_{k}  \right)
$$
$$
= a_{0}b_{0}+a_{1}b_{0}+a_{2}b_{0}+\dots+a_{n}b_{0}
$$
$$
 +a_{0}b_{1}+a_{1}b_{1}+a_{2}b_{1}+\dots+a_{n}b_{1}
$$
$$
 \vdots
$$
$$
 +a_{0}b_{n}+a_{1}b_{n}+a_{2}b_{n}+\dots+a_{n}b_{n}
$$
Then sorting them by the diagonals; the first diagonal is $c_{0}=a_{0}b_{0}$, the next is $c_{1}=a_{0}b_{1}+a_{1}b_{0}$ and so on, and since you have created an order, we can take the limit of the series
We can also consider the partial sums to $2n$ and the $c_{2n}$ diagonal that goes from $a_{0}b_{2n}+\dots+a_{n}b_{n}+\dots+a_{2n}b_{0}$
## Proof
First consider the grid above for a fixed $n$:
$$
\sum_{k=0}^{n}\left| c_{k} \right| \leq \left( \sum_{k=0}^{n}\left| a_{k} \right|  \right)\left( \sum_{k=0}^{n}\left| b_{k} \right|  \right)\leq \sum_{k=0}^{2n}\left| c_{k} \right| 
$$
For the first inequality we are only considering the upper diagonal of the grid, and clearly the square is larger than the triangle for the absolute value, since there are more terms. Then for the second, the larger triangle includes the square in it, so by the same reasoning we obtain the result
For the first inequality, we can also say
$$
\sum_{k=0}^{n}\left| c_{k} \right| \leq\left( \sum_{k=0}^{\infty} \left| a_{k} \right|   \right)\left( \sum_{k=0}^{\infty} \left| b_{k} \right|   \right)=\tilde{a}\tilde{b}
$$
Since both series are absolutely convergent, and adding more absolute terms holds the inequality
$\left| c_{k} \right|$ is an increasing [[Boundedness|bounded]] [[Sequences|sequence]], so the [[Every Increasing Sequence which is Bounded Above, Converges|limit exists]] so we have absolute convergence for $\sum_{k=0}^{\infty} c_{k}=\tilde{c}$
We also have $\sum_{k=0}^{2n}\left| c_{k} \right|$ also converges to the same number $\tilde{a}\tilde{b}$, so our first inequality is giving us $\tilde{a}\tilde{b}\leq\tilde{c}$ and the second is giving us $\tilde{a}\tilde{b}\geq \tilde{c}$, so $\tilde{a}\tilde{b}=\tilde{c}$
So given $\varepsilon>0$ there exists $n_{0}$ such that $\forall n\geq n_{0}$:
$$
\left|\left( \sum_{k=0}^{\infty} \left| a_{k} \right|   \right)\left( \sum_{k=0}^{\infty} \left| b_{k} \right|   \right)-\sum_{k=0}^{2n}\left| c_{k} \right|\right|<\varepsilon
$$
Where
$$
\left( \sum_{k=0}^{\infty} \left| a_{k} \right|   \right)\left( \sum_{k=0}^{\infty} \left| b_{k} \right|   \right)-\sum_{k=0}^{2n}\left| c_{k} \right|=\sum_{0\leq i,j\leq 2n:i+j\geq n+1}
\left| a_{i} \right| \left| b_{j} \right| $$
Now to prove $\sum_{k=0}^{\infty} c_{k}=ab$
We take $\varepsilon>0$, again, take $n_{0}$ as above, then
$$
\left| \left( \sum_{k=0}^{n}a_{k} \right)\left( \sum_{k=0}^{n}b_{k} \right)-\sum_{k=0}^{2n}c_{k} \right| =\left| \sum_{i,j\leq 2n:i+j\geq n+1}a_{i}b_{j} \right| \leq \sum_{i,j}\left| a_{i} \left|  \right|b_{j} \right|<\varepsilon 
$$
The absolute value is the absolute value of the sum of the values below the diagonal, which must be less than or equal to the individual terms being the absolute value, so we get less than epsilon from above, so we know
$$
\lim_{ n \to \infty } \sum_{k=0}^{2n}c_{k}=\lim_{ n \to \infty } \left( \sum_{k=0}^{n}a_{k} \right)\lim_{ n \to \infty } \left( \sum_{k=0}^{n}b_{k} \right)=ab
$$
Since $\sum_{k=0}^{n}c_{k}$ converges (absolute convergence), we get
$$
\sum_{k=0}^{\infty} c_{k} =ab
$$
## Remark
You can in fact loosen the definition to only one of the series being absolutely convergent, but the proof is different. You cannot loosen the definition to allow both series being absolutely convergent
## Why do we care?
The first reason is that if we are multiplying two series together, doing so by the diagonals is a very sensible thing to do
The other reason is that if we consider:
$$
\left( \sum_{k=0}^{\infty} a_{k} x^{k} \right)\left( \sum_{k=0}^{\infty} b_{k}x^{k}  \right)=\sum_{n=0}^{\infty} c_{n} =\sum_{k=0}^{\infty} \tilde{c}_{n}x^{n} 
$$
Where
$$
c_{n}=\sum_{k=0}^{n}a_{k}x^{k}b_{n-k}x^{n-k}=x^{n}\sum_{k=0}^{n}a_{k}b_{n-k}=:\tilde{c}_{n}x^{n}
$$
Which means that if we multiply two power series, we get another power series
### Example
Set
$$
f(x):=\sum_{k=0}^{\infty} \frac{x^{k}}{k!} 
$$
The [[Ratio Test|ratio test]] gives convergence for all $x\in\mathbb{R}$, so now consider
$$
f(x)f(y)=\sum_{k=0}^{\infty} c_{n} 
$$
$$
c_{n}=\sum_{k=0}^{n} \frac{x^{k}}{k!} \frac{y^{n-k}}{(n-k)!}=\frac{1}{n!}\sum_{k=0}^{n} \frac{n!}{k!(n-k)!} x^{k}y^{n-k}=\frac{1}{n!}(x+y)^{n}
$$
So 
$$
\sum_{k=0}^{\infty} c_{k}=f(x+y) 
$$
Thus we have
$$
f(x)f(y)=f(x+y)
$$
$f(x)=0$ has that property, and also [[Exponential Functions|exponential functions]] also have this property
We can at some point prove that in fact
$$
f(x)=\sum_{k=0}^{\infty} \frac{x^{k}}{k!} =e^{ x }
$$
Which would then allow us to derive all other features of the exponential function from there
