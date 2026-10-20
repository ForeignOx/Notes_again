## Definition
Let $X$ be a [[topology|topological]] space and $x\in X$. A [[sets|set]] $N\subseteq X$ is called a neighbourhood of $x$ if there exists an [[open sets|open set]] $U\subseteq X$ such that $x\in U$ and $U\subseteq N$
___
Neighbourhoods give a convenient criterion to check whether a set is an open set
## Lemma
Let $X$ be a topological space. A subset $U\subseteq X$ is open iff for every $x\in U$ there is a neighbourhood $N$ of $x$ contained in $U$
### Proof
If $U$ is open, then $U$ is a neighbourhood by definition
If every $x\in U$ has a neighbourhood $N$ contained in $U$, we also get an open neighbourhood $U_{x}\subseteq U$ of $x$, now
$$
U=\bigcup_{x\in  U}U_{x}
$$
Is the union of open sets, so is also open