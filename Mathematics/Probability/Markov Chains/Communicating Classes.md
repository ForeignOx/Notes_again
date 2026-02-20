## Definition
We define for each [[Markov Chains|$i \in I$]], the set
$$
C_{i}=\left\{ k\in  I:\middle|: i\leftrightarrow  k \right\}
$$
Then for any $i,j\in I$, either $C_{i}=C_{j}$ or $C_{i}\cap C_{j}=\emptyset$. These are communicating [[Class Structure|classes]].
This means the communicating classes [[set partition|partition]] $I$ into [[Disjoint Families of Sets|disjoint sets]]. These are the "simplest" pieces that make up a Markov chain
## Showing that they form an Equivalence Relation
To show that communicating classes form an [[Equivalence Relation|equivalence relation]], we need to check $i\leftrightarrow i$, $i\leftrightarrow j\implies j\leftrightarrow i$ and $i\leftrightarrow j\land j\leftrightarrow k\implies i\leftrightarrow k$
For the first part, $i\leftrightarrow i$ is true as 
$$
\mathbb{P}_{i}(X_{0}=i)=1>0
$$
For the second, 
$$
i\leftrightarrow  j \to \mathbb{P}_{i}(X_{n}=j\text{ for some }n)>0 \text{ and }\mathbb{P}_{j}(X_{m}=i\text{ for some }m)\implies j\leftrightarrow  i
$$
For the third, we know that there exist $n\geq 0$ and $m\geq 0$, such that $P_{ij}^{n}>0,P_{jk}^{m}>0$, so
$$
P_{ik}^{n+m}=\sum_{i}P_{ij}^{n}P_{jk}^{m}\geq P_{ij}^{n}P_{jk}^{m}>0\implies \mathbb{P}_{i}(X_{r}=k\text{ for some }r)>0
$$
And the same works in the opposite direction,
$$
\mathbb{P}_{k}(X_{s}=i\text{ for some }s)>0
$$
Which is what we wanted
## Definition
A communicating class $C$ is closed if $i\in C$, $i\to j$ implies $j\in C$. You cannot escape a closed communicating class
___
A state $i$ is absorbing if $\left\{ i \right\}$ is a closed communicating class. So there are no more changes once you reach an absorbing state