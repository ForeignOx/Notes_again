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
![[Pasted image 20260309132035.png]]
Then $\pi=\left( \frac{\beta}{\alpha+\beta},\frac{\alpha}{\alpha+\beta} ,0,0,0\right)$ and $\tilde{\pi} =\left( 0,0,\frac{2}{5},\frac{2}{5},\frac{1}{5} \right)$ are both invariant distributions, in fact, $\delta \pi+(1-\delta)\tilde{\pi}$ is invariant for all $\delta \in[0,1]$, so there are infinitely many
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
For the second part, this is a computation called the cycle trick. The idea is that $\gamma_{i}^{k}$ is the expected number of visits to $i$ in $\left\{ 0,1,\dots,T_{k-1} \right\}=RHS$, then we want to show
$$
LHS_{i}=\sum_{j\in  I}\gamma_{j}^{k}P_{ji}= \mathbb{E}(\text{number of visits to }i\text{ in }\left\{ 1,\dots,T_k \right\}) 
$$
$$
= \mathbb{E}_{k}(\text{number of visits to }i\text{ in }\left\{ 0,\dots,T_{k}-1 \right\})
$$
Note that we're using the knowledge that $T_{k}$ definitely occurs, which relies on recurrence for the lasst equality. Making this more precise, we had
$$
\gamma_{i}^{k}=\mathbb{E}_{k}\left( \sum_{n=1}^{T_{k}}\mathbb{1}(X_{n}=i) \right)=\mathbb{E}_{k}\left( \sum_{n=1}^{\infty} \mathbb{1}(X_{n}=i,T_{k}\geq n) \right)
$$
$$
 =\sum_{n=1}^{\infty}\mathbb{P}_{k}(X_{n}=i,T_{k}\geq n)
$$
Now
$$
\mathbb{P}_{k}(X_{n}=i,T_{k}\geq n)=\sum_{j\in  I}\mathbb{P}_{k}(X_{n}=i,X_{n-1}=j,T_{k} \geq n)
$$
We now consider the terms in the sum, and calculate
$$
\mathbb{P}_{k}(X_{n}=i,X_{n-1}=j,T_{k}\geq n)=\mathbb{P}_{k}(X_{n}=i\mid X_{n-1}=j,T_{k}\geq n)\mathbb{P}_{k}(X_{n-1}=j,T_{k}\geq n) 
$$
$$
= \mathbb{P}_{k}(X_{n}=i\mid X_{n-1}=j)\mathbb{P}_{k}(X_{n-1}=j,T_{k}\geq n)
$$
By laws of [[conditional probability|conditional probability]] and the Markov property at time $n-1$, therefore
$$
\mathbb{P}_{k}(X_{n}=i,T_{k}\geq n)=\sum_{j\in  I}\mathbb{P}_{k}(X_{n-1}=j,T_{k}\geq n)P_{ji}
$$
Sooo
$$
\gamma_{i}^{k}=\sum_{n=1}^{\infty} \sum_{j\in  I}P_{ji}\mathbb{P}_{k}(X_{n-1}=j,T_{k}\geq n) 
$$
$$
= \sum_{j\in  I}P_{ji}\sum_{n=1}^{\infty} \mathbb{P}_{k}(X_{n-1}=j,T_{k}\geq n) 
$$
$$
= \sum_{j\in  I} P_{ji}\mathbb{E}_{k}\left( \sum_{n=0}^{T_{k}-1} \mathbb{1}(X_{n}=j) \right)=\sum_{j\in  I}P_{ji}\gamma_{j}^{k}=(\gamma^{k}P)_{i}
$$
yay
For the third part, irreducibility implies that for any $i,k\in I$ there exists $m,n>0$ such that $P_{ik}^{m}>0,~P_{ki}^{n}>0$, thus by the second part,
$$
\gamma_{i}^{k}=(\gamma^{k}P)_{i}=(\gamma^{k}P^{m})_{i}\geq \gamma_{k}^{k}P_{ki}^{m}>0
$$
So $\gamma_{i}^{k}>0$ for all $i\in I$. The same reasoning implies that $\gamma _{k}^{k}\geq\gamma_{i}^{k}P_{ik}^{n}$, and so $\gamma_{i}^{k}\leq \frac{\gamma^{k}_{k}}{P_{ik}^{n}}<\infty$, so $\gamma_{i}^{k}<\infty$ for all $i\in I$
## Theorem
If $P$ is irreducible, $\lambda$ is an invariant measure for $P$ and $\lambda_{k}=1$, then
- $\lambda_{i}\geq \gamma_{i}^{k}$ for all $i\in I$
- if $P$ is recurrent, then $\lambda=\gamma^{k}$
### Proof
For the first part,  this is similar to minimising hitting probabilities, check this?
For the second part, since $P$ is recurrent, the above theorem tells us $\gamma^{k}$ is invariant. We now define $(\mu_{j})_{j\in I}$ by $\mu_{j}=\lambda_{j}-\gamma_{j}^{k}$ so $\mu_{j}\geq 0$ for all $j\in I$ by the first part and $\mu_{k}=1-1=0$
Since both $\lambda$ and $\gamma$ are invariant,
$$
\mu P=\lambda P-\gamma P=\lambda-\gamma=\mu
$$
So $\mu$ is also invariant. Therefore
$$
0=\mu_{k}=\sum_{j\in  I}\mu_{j} P^{n}_{jk}\text{ for all }n\geq 0
$$
$$
 \geq \mu_{i}P_{ik}^{n}\text{ for all }n\geq 0,i\in I 
$$
$$
 \geq 0
$$
Therefore $\mu_{i}P_{ik}^{n}=0$ for all $n\geq 0$, $i\in I$
However irreucibility implies that for all $i\in I$ there exists $n>0$ such that $P^{n}_{ik}>0$ implying that $\mu _{i}=0$ for all $i\in I$
## Theorem
Irreducible finite state Markov chains have unique stationary distributions
This result is very powerful! Any method to find a stationary distribution is good
### Proof
The existence part come from the theorem two above, since the state space is finite, $\sum_{i}\gamma_{i}^{k}<\infty$, so we see that
$$
\left( \frac{\gamma_{i}^{k}}{\sum_{j\in  I}\gamma_{j}^{k}} \right)_{i\in  I}
$$
Is an invariant distribution. The main content of the theorem is the uniqueness part.
Note that if Markov chain is irreducible and finite, then it must be recurrent which means every stationary measure $\lambda$ with $\lambda_{k}=1$ is $\gamma_{i}^{k}$ by the theorem above
Now suppose that $\gamma$ is an invariant distrrubution, so we must have $\gamma_{i}>0$ for some $i$. Then for any other $j\in I$, there exists $n>0$ such that $P_{ij}^{n}>0$ by irreducibility, hence
$$
\lambda_{j}= (\lambda P^{n})_{j}=\sum_{\ell}\lambda_{\ell}P_{\ell j}^{n}\geq \lambda_{i}P_{ij}^{n}>0
$$
Therefore, $\lambda_{j}>0$ for all $j\in I$
Now suppose we have two invariant distributions $\lambda$ and $\overline{\lambda}$, and fix $k\in I$. Then, by dividing by $\lambda_{k}$ (which we can do) we see that both
$$
\left( \frac{\lambda_{i}}{\lambda_{k}} \right)_{i\in I}\text{ and }\left(  \frac{\tilde{\lambda}_{i}}{\tilde{\lambda}_{k}} \right)_{i\in I}
$$
Are invariant measurew which take the value $1$ at $i=k$
Therefore, by the thorem above
$$
\frac{\lambda_{i}}{\lambda_{k}}=\gamma_{i}^{k}=\frac{\tilde{\lambda}_{i}}{\tilde{\lambda}_{k}}
$$
For  $i\in I$ since both $\lambda$ and $\tilde{\lambda}$ are both distributions,
$$
\sum_{i}\lambda_{i}=\sum_{i}\tilde{\lambda}_{i}=1
$$
Therefore, taking the sum of both sides over $i$, we get
$$
\frac{1}{\lambda_{k}}=\frac{\sum_{i}\lambda_{i}}{\lambda_{k}}=\frac{\sum_{i}\tilde{\lambda}_{i}}{\tilde{\lambda}_{k}}=\frac{1}{\tilde{\lambda}_{k}}
$$
Hence $\lambda_{k}=\tilde{\lambda}_{k}$
## Theorem
Suppose that $P$ is recurrent. Then it has an invariant measure, which is unique up to rescaling. This means that if $\lambda$ and $\tilde{\lambda}$ are two invariant measure for $P$, then there exists $c\in \mathbb{R}_{>0}$ such that $\lambda_{i}=c\tilde{\lambda}_{i}$ for all $i\in I$. More precisely, for any $k\in I$, the invariant measures for $P$ are given by $(\gamma_{i}^{k})_{i\in I}$ and all positive multiples of this
## Theorem
Consider the stochastic matrix $P$ on the state space $I$
- If $C$ is a non-closed communicating class for $P$, then $\pi(i)=0$ for all $i \in C$ and all stationary distributions $\pi$ for $P$
- If $C$ is a null recurrent or transient closed communicating class for $P$, then $\pi(i)=0$ for all $i\in C$ and all stationary distributions $\pi$ for $P$
- If $C$ is a [[Positive Recurrence|positive recurrent]] or transient communicating class for $P$, then there is a unique stationary distribution for $P$ which is supported on $C$, which we denote by $\pi^{C}$ 
- Enumerate the closed and positive recurrent communicating classes for $P$ as $C_{1},C_{2},\dots$ (which may be either finite or infinite), then the set of all stationary distributions for $P$ is given by
$$
\left\{ \sum_{i}a_{i}\pi^{C_{i}} :\middle|: a_{i}\geq 0 ~\forall i\text{ and }\sum_{i}a_{i}=1\right\}
$$
    Here $\pi^{C_{i}}$ is the unique stationary distribution supported on $C_{i}$
## Example
Consider the following example