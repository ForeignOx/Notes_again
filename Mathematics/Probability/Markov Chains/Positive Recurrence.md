There are in fact two types of [[Recurrence and Transience|recurrence]], recall that if $i\in I$ is recurrent if, started from $i$, you will definitely return to $i$. It turns out that whether the return time has finite or infinite expectation will be important
## Definition
A state $i\in I$ is positive recurrent if the expected time to return to $i$, from $i$ is finite,
$$
m_{i}:=\mathbb{E}_{i}(T_{i})<\infty
$$
Conversely, a recurrent state $i\in I$ with
$$
m_{i}:=\mathbb{E}(T_{i})=\infty
$$
Is null recurrent
## Theorem
Suppose $P$ is irreducible. The following are equivalent
- Every state $i\in I$ is positive recurrent
- Some state $k\in I$ is positive recurrent
- $P$ has an [[Invariant Distributions|invariant distribution]] $\pi$
When any (and hence all) of these conditions hold,
$$
\pi_{i} = \frac{1}{m_{i}}
$$
## Example
Consider the simple random walk on $\mathbb{Z}$, as described below:
![[Pasted image 20260323145259.png]]
This has $\mathbb{P}_{i}(T_{i}<\infty)=1$, so it is recurrent, but $\mathbb{E}_{i}(T_{i})=\infty$, so it is null recurrent
We proved before that a simple [[Random Walks|random walk]] on $\mathbb{Z}$ is recurrent
So the problem is to determine if we have positive recurrence. We observe that
$$
\pi_{i}=1~\forall i\in I
$$
Is an invariant measure, so we know by a theorem that any invariant measure is of the form 
$$
c\pi_{i}=c,~i\in I
$$
For some $c\in \mathbb{R}_{>0}$