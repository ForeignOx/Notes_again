Let $p$ be a prime number, and $n$ be a positive integer, then $n^{p}-n$ is divisible by $p$, or
$$
n^{p}\equiv n \mod p
$$
## Proof
We [[Proof by Mathematical Induction!!!!!|induct]] on $n$. The base case $n=1$ is obvious. Let us assume that the property is true for $n=k$ and prove it for $n=k+1$, using the induction hypothesis, we obtain:
$$
(k+1)^{p}-(k+1)=
k^{p}+\sum_{j=1}^{p-1}{p \choose j }k^{j}+1-k-1\equiv \sum_{j=1}^{p-1}{p \choose j }k^{j}\mod p
$$
Then using the fact that for $1\leq j\leq p-1$, ${p \choose j }$ is divisible by $p$, we see this by examining:
$$
{p \choose j }=\frac{p(p-1)\cdot\cdot\cdot(p-j+1)}{1\cdot2\cdot\cdot\cdot j }
$$
It is easy to see that when $1\leq j\leq p-1$, the numerator is divisible by $p$, while the denominator is not. Therefore, $(k+1)^{p}-(k+1)\equiv0\mod p$, completing the induction