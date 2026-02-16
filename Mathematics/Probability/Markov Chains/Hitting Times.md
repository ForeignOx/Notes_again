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
So it's the firsst time, including $n=0$, that the Markov chain is in $A$
## Definition
$h^{A}_{i}:=\mathbb{P}(H^{A}<\infty)$ is called the probability of hitting $A$ starting at $i$
$k_{i}^{A}:=\mathbb{E}_{i}(H^{A})$ is the [[Expectation|expected]] hitting time (also known as the mean hitting time) of $i$ starting from $i$
Note that $k_{i}^{A}=\infty$ is $\mathbb{P}_{i}(H^{A}=\infty)>0$
If $A$ is a [[Communicating Classes|closed class]], $h_{i}^{A}$ is the absorption probability
## Example
