## Definition
The state $i\in I$ is recurrent if 
$$
\mathbb{P}_{i}(X_{n}=i\text{ for infinitely many }n)=1
$$
A state $i$ is transient if 
$$
\mathbb{P}_{i}(X_{n}=1\text{ for infinitely many }n)=0
$$
## Question
We might wonder if a state can be neither, i.e. is it possible for
$$
\mathbb{P}_{i}(X_{n}=i\text{ for infinitely many }n)\in (0,1)
$$
Roughly, we can think about tossing a coin. It's possible that all coin tosses in the future are heads
Also it is possible that
$$
\mathbb{P}(\text{all toin cosses are heads})=0
$$
Recall that the first passage time to $i$ is
$$
T_{i}=\inf\left\{ n>0:\middle|: X_{n}=i \right\}
$$
## Theorem
The following dichotomy holds:
- If $\mathbb{P}_{i}(T_{i}<\infty)=1$ then $i$ is recurrent and
$$
\sum_{n=0}^{\infty}\mathbb{P}_{i}(X_{n}=i)=\sum_{n=0}^{\infty}\mathbb{E}_{i}(\mathbb{1}(X_{n}=i))=\mathbb{E}_{i}\left( \sum_{n=0}^{\infty} \mathbb{1}(X_{n}=i) \right)=                 \sum_{n=0}^{\infty}P_{ii}^{n}=\infty
$$
- If $\mathbb{P}_{i}(T_{i}<\infty)<1$, then $i$ is transient and 
$$
\sum_{n=0}^{\infty}P_{ii}^{n}<\infty \implies \mathbb{E}_{i}\left( \sum_{n=0}^{\infty}\mathbb{1}(X_{n}=i) \right)<\infty
$$
In particular, every state is either recurrent or transient
## Corollary
Recurrence/transience is a [[Class Properties|class property]]: if $i\leftrightarrow j$, then either they're both recurrent or both transient
### Proof
We suppose $i\leftrightarrow j$, so $\exists m,k>0$ such that
$$
P_{ij}^{m}>0,P_{ji}^{k}>0
$$
We define
$$
\xi=P_{ij}^{m}P_{ji}^{k}>0
$$
We claim
$$
\sum_{n=0}^{\infty} P_{jj}^{n}\geq \xi \sum_{n=0}^{\infty}P_{ii}^{n}
$$
This is since
$$
\sum_{n=0}^{\infty} P_{jj}^{n}\geq \sum_{n=m+k}^{\infty}P_{jj}^{n}=\sum_{n=0}^{\infty} P_{jj}^{n+m+k} \geq \sum_{n=0}^{\infty}P_{ji}^{k}P_{ij}^{m}P_{ii}^{n}=c\sum_{n=0}^{\infty}P_{ii}^{n}
$$
So $\sum_{n=0}^{\infty}P_{ii}^{n}=\infty\implies \sum_{n=0}^{\infty} P_{jj}^{n}=\infty$
Conversely we can switch $i$ and $j$ to get the theorem proved both ways, hence $i$ is transient iff $j$ is transient
By the theorem above, we get that $i$ is recurrent iff $j$ is recurrent
## Definition
A [[communicating classes|communicating class]] $C$ is recurrent/transient if every $i\in C$ is recurrent/transient respectively
## Definition
We define the $r$th passage time to $i$ as $T_{i}^{0}=0,$
$$
T_{i}^{r}=\inf\left\{ n>T_{i}^{r-1}:\middle|: X_{n}=i \right\}
$$
## Example
If
$$
I=\left\{ a,b,c \right\},(X_{n}(\omega))_{n\geq 0}=(a,a,c,b,a,b,b,a,b,b,a,b,\dots)
$$
What is 