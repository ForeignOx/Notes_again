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
### Proof
The implication of the first to the second is trivial, 
For the second to the third, since $k$ is positive recurrent, it is recurrent and hence, there exists an invariant measure, given by $(\gamma_{i}^{k})_{i\in I}$. Now recall
$$
\gamma_{i}^{k}=\mathbb{E}_{k}\left( \sum_{n=0}^{T_{k}-1}\mathbb{1}_{\left\{ X_{n}=i \right\}} \right)
$$
Where $T_{k}$ is the return time to $k$, therefore,
$$
\sum_{i\in I}\gamma_{i}^{k}=\sum_{i\in I}\mathbb{E}_{k}\left( \sum_{n=0}^{T_{k}-1} \mathbb{1}_{\left\{ X_{n}=i \right\}} \right)=\mathbb{E}_{k}\left( \sum_{i\in I}\sum_{n=0}^{T_{k}-1}\mathbb{1}_{\left\{ X_{n}=i \right\}} \right) 
$$
$$
= \mathbb{E}_{k}\left( \sum_{n=0}^{T_{k}-1}\underbrace{ \sum_{i\in I}\mathbb{1}_{\left\{ X_{n}=i \right\}}  }_{ =1 }\right)=\mathbb{E}_{k}(T_{k})=m_{k}
$$
Where we used Tonelli's theorem multiple time to exchange sums and expectations and the two sums since they were non-negative
Since $k$ is positive recurrent, $m_{k}=\mathbb{E}_{k}(T_{k})<\infty$, so
$$
\sum_{i\in I}\gamma_{i}^{k}<\infty
$$
This means that the invariant measure $(\gamma_{i}^{k})_{i\in I}$ is normalisable, i.e. we have an invariant distribution given by
$$
\pi_{i}=\frac{\gamma_{i}^{k}}{\sum_{j\in  I}\gamma_{j}^{k}}
$$
To show the third implies the first, we suppose that we have an invariant ditribution $\pi$, we have $\pi_{k}>0$ for some $k$, so
$$
\frac{\pi_{i}}{\pi_{k}}\geq \gamma_{i}^{k}
$$
By a previous theorem, and hence $\pi_{j}>0$ for all $j\in I$, since $\gamma_{j}^{k}>0$
We showed that $m_{k}=\sum_{j\in I}\gamma_{j}^{k}$, so
$$
m_{k} =\sum_{j\in  I}\gamma_{j}^{k}\leq \sum_{j\in  I} \frac{\pi_{j}}{\pi_{k}}=\frac{1}{\pi_{k}}<\infty
$$
For all $k\in I$
Finally to show that $\pi_{i}=\frac{1}{m_{i}}$,
By recurrence, we have
$$
\frac{\pi_{i}}{\pi_{k}}=\gamma^{k}_{i}~i\in I
$$
Now we showed that
$$
m_{k}=\sum_{i\in I}\gamma_{i}^{k}
$$
Therefore
$$
\underbrace{ \sum_{i\in I} \frac{\pi_{i}}{\pi _{k}} }_{ =\frac{1}{\pi_{k}} }=\underbrace{  \sum_{i\in I}\gamma^{k}_{i} }_{ =m_{k} }
$$
And we are done

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
For some $c\in \mathbb{R}_{>0}$, but since $\sum_{i\in \mathbb{Z}}1=\infty$, this can't be normalisable, so there is no invariant distribution
Therefore the theorem above tells us we can't have positive recurrence, so we have null recurrence
___
One can work out the stationary distribution fot the following Markov chain