We want to estimate or predict if and when something will happen with [[Markov Chains|Markov chains]]
For example let $A\subset I$ be a thing of interest, for example $A=\left\{ i\in I:\middle|:\text{ it is raining} \right\}$ if the set of states is the set of possible weather patterns. Importantly $A=\left\{ i \right\}$ for some state $i$
## Definition
The hitting time of some subset of states $A\subset I$ is the [[Random Variables|random variable]] 
$$
H^{A}:\Omega\to \mathbb{N}_{0}\cup \left\{ \infty \right\}
$$
is defined by
$$
H^{A}:=\min\left\{ n\geq 0:\middle|: X_{n}\in  A \right\}
$$
with the convention that $\min \emptyset=\infty$
So it's the first time, including $n=0$, that the Markov chain is in $A$
## Definition
$h^{A}_{i}:=\mathbb{P}(H^{A}<\infty)$ is called the [[Probabilities|probability]] of hitting $A$ starting at $i$
$k_{i}^{A}:=\mathbb{E}_{i}(H^{A})$ is the [[Expectation|expected]] hitting time (also known as the mean hitting time) of $i$ starting from $i$
Note that $k_{i}^{A}=\infty$ is $\mathbb{P}_{i}(H^{A}=\infty)>0$
If $A$ is a [[Communicating Classes|closed class]], $h_{i}^{A}$ is the absorption probability
## Theorem
The [[Vectors|vector]] of hitting probabilities $(h_{i}^{A})_{i\in I}$ is the minimal non-negative solution to the linear system
$$
\begin{cases}
h_{i}^{A}=1 & i\in  A \\
h_{i}^{A}=\sum_{j\in  I}P_{ij}h_{j}^{A} & i\not\in  A
\end{cases}
$$
By the minimal non-negative solution, we mean that if $(x_{i})_{i\in I}$ solves the above and $x_{i}\geq 0$ for all $i\in I$, then $h_{i}^{A}\leq x_{i}$ for all $i \in I$
## Example
Fint $\mathbb{P}_{b}(H^{\left\{ d \right\}}<\infty)$, and $\mathbb{E}_{b}(H^{\left\{ a,b \right\}})$ for the following Markov chain:
![[Pasted image 20260216213434.png]]
First we set $h_{i}=\mathbb{P}_{i}(H^{\left\{ d \right\}}<\infty)$ notice that $h_{a}=0$ and $h_{d}=1$
Further, we will show that
$$
h_{b}=\frac{1}{2}h_{a}+\frac{1}{2}h_{c}
$$
We will prove this with the Markov property, as follows,
$$
h_{b}=\mathbb{P}_{b}(H^{\left\{ d \right\}}<\infty)=\mathbb{P}_{b}(H^{\left\{  d \right\}}<\infty,X_{1}=a)+\mathbb{P}_{b}(H^{\left\{ d \right\}}<\infty,X_{1}=c)
$$
By the [[Partition Theorem|partition theorem]], 
$$
=\mathbb{P}(H^{\left\{ d \right\}}<\infty\mid X_{1}=a)\mathbb{P}_{b}(X_{1}=a)+\mathbb{P}(H^{\left\{ d \right\}}<\infty\mid X_{1}=c)\mathbb{P}_{b}(X_{1}=c)
$$
by [[Conditional Probability|conditional probability]],
$$
= \mathbb{P}_{a}(H^{\left\{ d \right\}}<\infty)\frac{1}{2}+\mathbb{P}_{c}(H^{\left\{ d \right\}}<\infty)\frac{1}{2}=\frac{1}{2}h_{a}+\frac{1}{2}h_{c}
$$
Similarly, $h_{c}=\frac{1}{2}h_{b}+\frac{1}{2}h_{d}$. We've reduced the problem to a [[systems of linear equations|system of linear equations]] So $h_{a}=0$ implies that $h_{b}=\frac{1}{2}h_{c}$. Then using $h_{d}=1$ and $h_{c}=\frac{1}{2}h_{b}+\frac{1}{2}h_{d}$, we have that $h_{c}=\frac{1}{4} h_{c}+\frac{1}{2}$, so $h_{c}=\frac{2}{3}$ and hence $h_{b}=\frac{1}{3}$
For this we can find the vector of h