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
We define the $r$th excursion length as
$$
S_{i}^{r}=\begin{cases}
T_{i}^{r}-T_{i}^{r-1} & T_{i}^{r-1}<\infty \\
0 & T_{i}^{r-1}=\infty
\end{cases}
$$

## Example
If
$$
I=\left\{ a,b,c \right\},(X_{n}(\omega))_{n\geq 0}=(a,a,c,b,a,b,b,a,b,b,a,b,\dots)
$$
What are some passae times
$$
T_{a}^{1}(\omega)=1
$$
$$
 T_{b}^{1}(\omega)=3
$$
$$
T_{b}^{2}(\omega)=5
$$
$$
 T^{3}_{b}(\omega)=6
$$
The idea is that recurrent means infinitely many $T_{i}^{r}$ happen, so it can't spend forever not at $i$
## Lemma
For $r\geq \phi$ conditional on $\left\{ T_{i}^{r-1}<\infty \right\}$, the excurion length $S_{i}^{r}$ is independent of $X_{0},X_{1},\dots,X_{T_{i}^{r-1}}$ and
$$
\mathbb{P}_{i}(S^{r}_{i}=n\mid T_{i}^{r-1}<\infty)=\mathbb{P}_{i}(T_{i}= n)
$$
### Proof
We just need to translate things to apply the [[strong Markov property|strong Markov property]]
The strong Markov contition on $\left\{ T_{i}^{r-1} <\infty\right\}$
$(X_{T_{i}^{r-1}+n})_{n\in\mathbb{N}_{0}}$is $Markov(\delta_{i},P)$ and independent of $X_{0},\dots X_{T_{i}^{r-1}}$
If $\left\{ T_{i}^{r-1} <\infty\right\}$ then $S_{i}^{r}>0$ and 
$$
S_{i}^{r}=\inf\left\{ n\geq 1:\middle|: X_{T_{i}^{r-1}+n}=i \right\}
$$
Which is equal to the first passage time of $(X_{T_{i}^{r-1}+n})_{n\geq 0}$ to $i$
o the strong Markov property tells us that $\mathbb{P}(S_{i}^{r}=n\mid T_{i}^{r-1}<\infty)=\mathbb{P}_{i}(T_{i}=n)$ which is equal to in distribution to $(X_{n})_{n\geq 0}$
