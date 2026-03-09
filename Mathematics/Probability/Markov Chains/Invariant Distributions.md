An import thing to wonder about is what are the long term statitical properties of Markov chains??
To answer this, we will need invariant distributions  who wouldda thunk it 
## Terminology
A measure is a row vector with non-negative entries
A distribution is a measure whose entries sum to one
## Definition
If $P$ is stochastic, a measure $\lambda$ is invariant if $\lambda P=\lambda$ (this makes sense as matrix multiplication since $\lambda$ is a row vector)
We also use the terms that $\lambda$ is an equilibrium or stationary measure if $\lambda P=\lambda$ (different names reflect different ways of thinking what $\lambda P=\lambda$ means)
## Remark
We are mostly interested in distributions, so why do we introduce measures?
If $\lambda$ is a measure and $\sum_{i\in I}\lambda_{i}<\infty$, then
$$
\pi_{i}:= \frac{\lambda_{i}}{\sum_{i\in I}\lambda_{i}}
$$
Is a distribution. If $\lambda$ is invariant, so is $\pi$, as the equation $\lambda P=\lambda$ is linear in $\lambda$
Measures are theoretically useful for many reasons
## Theorem
If $(X_{n})_{n\in\mathbb{N}_{0}}$ is $Markov(\lambda,P)$ and $\lambda$ is invariant for $P$, then for any $m\geq 0$, $(X_{m+n})_{n\in\mathbb{N}_{0}}$ is $Markov(\lambda,P)$
### Proof
The Markov property says that $(X_{m+n})_{n\in\mathbb{N}_{0}}$ is $Markov(\mu,P)$, where
$$
\mu_{i}:=\mathbb{P}_{\lambda}(X_{m}=i)
$$
Since
$$
\mathbb{P}_{\lambda}(X_{m+n}\in  A)=\sum_{i\in I}\mathbb{P}((X_{m+n})_{n\in\mathbb{N}_{0}}\in  A\mid X_{m}=i)\mathbb{P}(X_{m}=i) 
$$
$$
= \sum_{i\in I} \mathbb{P}_{i}((X_{n})_{n\in\mathbb{N}_{0}}\in  A\mid X_{m}=i)\mu_{i}\mathbb{P}_{\mu}((X_{n})_{n\in\mathbb{N}_{0}}\in  A)
$$
But we know
$$
\mu_{i}=\mathbb{P}(X_{m}=i)=(\lambda P^{n})_{i}=(\lambda PP^{n-1})_{i}=(\lambda P^{n-1})_{i}=\dots = \lambda_{i}
$$
## Theorem
Suppose $\left| I \right|<\infty$ and there exists $i\in I$ such that the limit
$$
\lim_{ n \to \infty } P^{n}_{ij}=\pi_{j}\text{ exists for all }j\in  I
$$
Then $\pi=(\pi_{j})_{j\in I}$ is an invariant distribution
### Proof
Using the Chapman-Kolmogorov equations,
$$
\pi_{j}=\lim_{ n \to \infty } P_{ij}^{n}=\lim_{ n \to \infty } \sum_{k\in  I}P_{ik}^{n-1}P_{kj} 
$$
$$
= \sum_{k\in  I} (\lim_{ n \to \infty } P^{n-1}_{ik})P_{kj} 
$$
$$
= \sum_{k\in  I} \pi_{k} P_{jk}=(\pi P)_{j}
$$
## Remark
Note that $\left| I \right|<\infty$, is essential, this is not true in general if $\left| I \right|=\infty$, for example, the simple random walk on $\mathbb{Z}$ has $P_{ij}^{n}\to 0$ as $n\to\infty$ for all $i,j$
This theorem says that if you settle into a limiting distribution, then it must be invariant
## Example
Let $0<\alpha<\beta<1$ and consider the following Markov chain:
$$
B= \begin{pmatrix}
P_{aa} & P_{ab} \\
P_{ba} & P_{bb} 
\end{pmatrix}=\begin{pmatrix}
1-\alpha & \alpha \\
\beta & 1-\beta
\end{pmatrix}
$$
![[Pasted image 20260220164136.png]]
Then we recall that
$$
P^{n}_{aa}= \frac{\beta}{\alpha+\beta}+\frac{\alpha}{\alpha+\beta}(1-\alpha-\beta)^{n}\to \frac{\beta}{\alpha+\beta}
$$
And
$$
P^{n}_{ab}\to \frac{\alpha}{\alpha+\beta}\text{ as }n\to\infty
$$
So $\left( \frac{\beta}{\alpha+\beta}, \frac{\alpha}{\alpha+\beta} \right)$ is invariant
___
We can check that
$$
\lim_{ n \to \infty } \begin{pmatrix}
0 & 1 & 0 \\
0 & \frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & 0 & \frac{1}{2}
\end{pmatrix}^{n}=\begin{pmatrix}
\frac{1}{5} & \frac{2}{5} & \frac{2}{5} \\
\frac{1}{5} & \frac{2}{5} & \frac{2}{5} \\
\frac{1}{5} & \frac{2}{5} & \frac{2}{5}
\end{pmatrix}
$$
Is the stationary distrubution, so yeah (note that all the rows are the same, this must always be the case)
## Question
Do we always have a unique stationary distribution?
No. In fact, there might not be any stationary distribution and there may be more than one stationary distribution
## Example
Consider the Markov chain

## A Key Object
We might guess that irreducibility plays a role...
A key object to consider for $i,k\in I$, the expected time at $i$ before returning to $k$:
$$
\gamma_{i}^{k}=\mathbb{E}\left( \sum_{n=0}^{T_{k}-1}\mathbb{1}(X_{n}=I) \right)
$$
Where $T_{k}:= \inf \left\{ n>0:\middle|: X_{n}=k \right\}$
For example, if $I=\left\{ a,b,c,d,e \right\}$, if
$$
(X_{n}(\omega))_{n\geq 0}=(a,b,c,d,e,b,c,b,a,e,c,a, \dots)
$$
Then what's inside the expectation? The answer is 2
## Example
So returning to the above eample, let's compute $(\gamma_{i}^{k})_{i\in I}$ in our example $I=\left\{ C,D,E \right\}$. The number of visits to $D$ before returning to $C$ must be $Geo\left( \frac{1}{2} \right)$ hence $\gamma_{D}^{C}=2$ (by the expectation of [[Geometric Distribution|geometric]] random variables)
By the same argument, we see that $\gamma_{E}^{C}=2$, finally $\gamma_{C}^{C}=1$, sooo
$$
(\gamma_{i}^{C})_{i\in  \left\{ C,D,E \right\}} = (1,2,2)
$$
We can normalise to get the distribution
$$
\left( \frac{1}{5},\frac{2}{5},\frac{2}{5} \right)
$$
Similarly, let's try to find $(\gamma_{i}^{D})_{i \in \left\{ C,D,E \right\}}$
For $\gamma_{C}^{D}$, with probability $\frac{1}{2}$ $T_{D}=1$ and in this case we don't visit $C$. Otherwise, we visit $C$ exactly once before $T_{D}$. Therefore $\gamma_{C}^{D}=\frac{1}{2}\times 0+\frac{1}{2}\times 1=\frac{1}{2}$
For $\gamma_{D}^{D}$ we definitely visit $D$ once up to time $T_{D}$, namely at time $T_{D}$
For $\gamma_{E}^{D}$, with probability $\frac{1}{2}$, $T_{D}=1$ and we don't visit $E$. Otherwise the number of visits to $E$ is $Geo\left( \frac{1}{2} \right)$ whose expectation is $2$, therefore $\gamma_{E}^{D}=\frac{1}{2}\times 0+\frac{1}{2}\times 2=1$, soo
$$
(\gamma_{i}^{D})_{i \in \left\{ C,D,E \right\}}=\left( \frac{1}{2},1,1 \right)
$$
WHich is different to above, but when normalised, we get the same as above
This is in fact the invariant distribution for the Markov chain holly moly
Let's make this rigorous !
## Theorem
Let $P$ be irreducible and recurrent. Then:
- $\gamma_{k}^{k}=1$
- $\gamma_{k}P=\gamma^{k}$
- $0<\gamma_{i}^{k}<\infty$ for all $i\in I$
This means that $(\gamma_{i}^{k})_{i\in I}$ is an invariant measure for $P$
### Proof
For the fist part, $X_{0}=k$, $X_{T_{k}}=k$ and $X_{n}\neq k$, for $0<n<T_{k}$, so yeah




For the third part, irreducibility implies that for any $i,k\in I$ there exists $m,n>0$ such that $P_{ik}^{m}>0,~P_{ki}^{n}>0$, thus by the second part,
$$

$$