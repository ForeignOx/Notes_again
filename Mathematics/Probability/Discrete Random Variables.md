Let $X$ be a [[Random Variables|random variable]], $X$ is discrete if there exists $\chi \subseteq X(\Omega)$ such that $\chi$ is either finite or [[Countable Sets|countable]], i.e.
$$
\mathbb{P}(X \in  \chi)=1
$$
## Probability Mass Function
We will define
$$
p:\chi\to[0,1]
$$
$$
p(x)=\mathbb{P}(X=x)
$$
For every $x\in\chi$ 
$p(x)$ is known as the probability mass [[Functions|function]] (pmf)
## Theorem
Let $X$ be a discrete random variable with pmf $p$, then for any $A\subseteq \chi$, 
$$
\mathbb{P}(X \in A)=\sum_{x \in A}p(x)
$$
Furthermore,
$$
\sum_{x\in \chi}p(x)=1
$$
### Proof
$A\subseteq \chi$, where $\chi$ is countable or finite, so you can enlist/enumerate the elements of $A$
Let $A=\{ a_{1},a_{2},\dots \}$, so
$$
A=\bigcup_{i=1}^{\infty}\{ a_{i} \}
$$
So
$$
\mathbb{P}(X \in A)=\mathbb{P}\left( \bigcup_{i=1}^{\infty}\{ X=a_{i} \} \right)
$$
Observe that $\{ X=a_{i} \}\cap \{ X=a_{j} \}=\emptyset$ for $i\neq j$, so by the 4th axiom of [[Probabilities|probability]]:
$$
\mathbb{P}(X \in A)=\sum_{i=1}^{\infty}\mathbb{P}(X=a_{i})=\sum_{i=1}^{\infty}p(x)=\sum_{x \in A}p(x)
$$
We have to show that $\sum_{x\in\chi}p(x)=1$, since we have established the first part,
$$
\mathbb{P}(X\in \chi)=\sum_{x\in \chi}p(x)
$$
And we know when we defined $\mathbb{P}_{X}$ that $\mathbb{P}(X \in\chi)=1$, so that completes the proof:
$$
\sum_{x\in \chi}p(x)=1
$$
## Joint Distribution
The joint pmf:
Let $(X,Y)$ be a bivariate random vector, such that $\mathbb{P}((X,Y)\in Z)=1$, then the joint pmf is given by
$$
p(x,y)=\mathbb{P}(X=x,Y=y)=\sum_{(x,y):x\in A,y\in B}p(x,y)
$$
For all $(x,y)\in Z$
### $(X,Y)$ is Discrete iff $X$ and $Y$ are both Discrete
Let $X$ and $Y$ be $\hspace{0pt}2$ random variables on the same probability space $\Omega$, then the bivariate random variable $(X,Y)$ is discrete iff both $X$ and $Y$ are discrete
Moreover if $\mathbb{P}(X \in\chi)={{\mathbb{P}(Y\in\Gamma)}}=1$, then:
$$
p_{X}(x):=\mathbb{P}(X=x)=\sum_{y\in \Gamma}p(x,y)
$$
$$
 p_{Y}(y):=\mathbb{P}(Y=y)=\sum_{x\in \chi}p(x,y)
$$
So the pmfs for $X$ and $Y$ become the [[Marginal|marginals]] of $X$ and $Y$
#### Proof
$$
\mathbb{P}(X=x)=\mathbb{P}(X=x,Y\in \Gamma)=\mathbb{P}\left( \bigcup_{y\in \Gamma}\{ X=x,Y=y \} \right)
$$
Which by the [[Partition Theorem|partition theorem]], is equal to:
$$
=\sum_{y\in \Gamma}\mathbb{P}(X=x,Y=y)=p(x,y)
$$
By symmetry, the same is true for $Y$
### Subsets
If $X$ and $Y$ are jointly discfrete, then $A\subseteq Z$, where $\mathbb{P}((X,Y)\in Z)=1$, then for any $A\subseteq Z$,
$$
\mathbb{P}((X,Y)\in A)=\sum_{(x,y)\in A}p(x,y)
$$
### Independce

#Mathematics #Probability #Functions