Because of the [[Vectorspaces|commutative and associative laws for addition]], the sum of a finite [[Sets|set]] of [[Vectors|vectors]] is the same for all posible ways of adding them, for example, the sum of the three vectors $\alpha_{a},\alpha_{b},\alpha_{c}$ can be calculated in $\hspace{0pt}12$ ways, all of which give the same result, for example, a few of these combinations are:
$$
(\alpha_{a}+\alpha_{b})+\alpha_{c}=\alpha_{c}+(\alpha_{a}+\alpha_{b})=(\alpha_{c}+\alpha_{a})+\alpha_{b}=\alpha_{b}+(\alpha_{c}+\alpha_{a})=\dots
$$
So if $I=\left\{ a,b,c \right\}$ is the [[Sets of Indices|set of indices]] used, the notation
$$
\sum_{i \in  I}\alpha_{i}
$$
Which indicates the sum of all the $\alpha_{i}$s is unambiguous and uniquely determined
The indexed set $I$ is often a block of [[Integers|integers]] $\overline{n}=\left\{ 1,\dots,n \right\}$, in this case the vectors $\alpha_{i}$ form an $n$-tuple $\left\{ \alpha_{i} \right\}_{1}^{n}$, and unless we wish to otherwise, we add them in their natural order and write the sum as
$$
\sum_{i=1}^{n}\alpha_{i}=\alpha_{1}+\alpha_{2}+\dots+\alpha_{n}
$$
Note that the way they are grouped is left arbitrary
Frequently, however, we have to use indexed sets that are not ordered. For example the general polynomial of degree at most $\hspace{0pt}5$ in the two variables $s$ and $t$ is:
$$
\sum_{0\leq i+j\leq 5}c_{ij}s ^{i}t^{j}
$$
And the finite set of monomials $\left\{ s ^{i}t^{j} \right\}_{i+j\leq 5}$ has no natural order
## Theorem
The sum of a finite collection of vectors is independent of how we add them
### Proof
By [[Proof by Mathematical Induction!!!!!|induction]]
We begin the induction with two vectors, in which case the commutative law $\alpha_{a}+\alpha_{b}=\alpha_{b}+\alpha_{a}$ displays the identity of all possible sums.
Suppose then that the assertion is ture for index sets having fewer than $n$ elements, and consideer a collection $\left\{ \alpha_{i}\mid i \in I \right\}$ having $n$ members
Let $\beta$ and $\gamma$ be the sum of these vectors computed in two ways. In the computation of $\beta$, there was a last addition performed, so that 
$$
\beta=\left( \sum_{i\in J_{1}}\alpha_{i} \right)+\left( \sum_{i\in J_{2}}\alpha_{i} \right)
$$
Where $\left\{ J_{1},J_{2} \right\}$ [[Set Partition|partitions]] $I$ and where we can write these two partial sums without showing how they were formed, since by our inductive hypothesis, all possible ways of adding them give the same result
Similarly, 
$$
\gamma=\left( \sum_{i\in K_{1}}\alpha_{i} \right)+\left( \sum_{i\in  K_{2}}\alpha_{i} \right)
$$
Where again, $\left\{ K_{1},K_{2} \right\}$ partitions $I$. Now set
$$
L_{jk}=J_{j}\cap K_{k},\xi_{jk}=\sum_{i\in L_{jk}}\alpha_{i}
$$
Where it is understood that $\xi_{jk}=0$ it $L_{jk}$ is [[Empty Set|empty]]
Then $\sum_{i\in J_{1}}=\xi_{1 1}+\xi_{12}$ by the inductive hypothesis, and similarly for the other three sums. Thus 
$$
\beta=(\xi_{11}+\xi_{12})+(\xi_{21}+\xi_{22})=(\xi_{11}+\xi_{21})+(\xi_{12}+\xi_{22})=\gamma
$$
Which completes our proof
## Some Properties
$$
\sum_{i=m}^{m+n}a_{i}=a_{m}+a_{m+1}+a_{m+2}+\dots+a_{m+n}
$$
$$
\sum_{ r=1} ^{ n}a_{r}=\sum_{ i=1} ^{ n}  a_{i}
$$
$$
\sum_{ i=0} ^{ n}  i f(i)= \sum_{ i=1} ^{ n}  i f(i)
$$
$$
\sum_{ i=0} ^{ n}f(i)=\sum_{ j=k} ^{ n+k}f(j-k)   
$$
$$
\sum_{ r=1} ^{ n}  \lambda a_{r}=\lambda \sum_{ r=1} ^{ n}a_{r}
$$
$$
\sum_{ r=n} ^{ n}  a_{r}=a_{n}=\sum_{ r=n+1} ^{ n+1}a_{r-1}=\sum_{ r=n-1} ^{ n-1} a_{r+1}   
$$


#Mathematics #Functions #Definition 