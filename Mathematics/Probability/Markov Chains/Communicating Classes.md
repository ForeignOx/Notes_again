## Definition
We define for each [[Markov Chains|$i \in I$]], the set
$$
C_{i}=\left\{ k\in  I:\middle|: i\leftrightarrow  k \right\}
$$
Then for any $i,j\in I$, either $C_{i}=C_{j}$ or $C_{i}\cap C_{j}=\emptyset$. These are communicating [[Class Structure|classes]].
This means the communicating classes [[set partition|partition]] $I$ into [[Disjoint Families of Sets|disjoint sets]]. These are the "simplest" pieces that make up a Markov chain
## Showing that they form an Equivalence Relation
To show that communicating classes form an [[Equivalence Relation|equivalence relation]], we need to check $i\leftrightarrow i$, $i\leftrightarrow j\implies j\leftrightarrow i$ and $i\leftrightarrow j\land j<-$
## Definition
A communicating class $C$ is closed if $i\in C$, $i\to j$ implies $j\in C$. You cannot escape a closed communicating class
___
A state $i$ is absorbing if $\left\{ i \right\}$ is a closed communicating class. So there are no more changes once you reach an absorbing state