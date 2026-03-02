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
\sum_{n=0}^{\infty}\mathbb{P}_{i}(X_{n}=i)=\sum_{n=0}^{\infty}\mathbb{E}_{i}()                 \sum_{n=0}^{\infty}P_{ii}^{n}=\infty
$$