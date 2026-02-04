## Partition [[Functions|Function]] for [[Natural Numbers|Natural Numbers]]
A partition of a positive integer $n$ is an expression of $n$ as an unordered sum of positive integers, called the parts of the partition
Let $p(n)$ denote the number of partitions of $n$
## Example
What is $p(5)$?
We can write
$$
5=5
$$
$$
= 4+1
$$
$$
= 3+2
$$
$$
= 3+1+1
$$
$$
= 2+2+1
$$
$$
= 2+1+1+1
$$
$$
= 1+1+1+1+1
$$
There are $\hspace{0pt}7$ partitions, so $p(5)=7$
In how many ways can $\hspace{0pt}5$ identical balls be distributed among $\hspace{0pt}5$ identical boxes?
Interpret the distribution of balls into boxes as a partition of $\hspace{0pt}5$, whereby balls in the same box represents units of $\hspace{0pt}5$ in the same part. So this is the same as the previous example, and the answer is $\hspace{0pt}7$
___
What is $p(n)$?
This is a hard question that goes to the root of some very deep mathematical problems, some still unsolved. There is no simple general formula for $p(n)$
There is an asymptotic fomula due to Hardy and Ramanujan, which says that:
$$
p(n)\sim \frac{1}{4n\sqrt{ 3 }}\exp\left( \pi \sqrt{ \frac{2n}{3} } \right)
$$
as $n\to \infty$
### [[Generating Functions|Generating Function]]
Find the generating function of the number $a_{n}$ of partitions of $n$ into distinct positive integers
In such a partition, a given positive integer $k$ is present either once (in which case it counts $k$ towards the total) or not at all (in which case it counts $\hspace{0pt}0$). Thus if $e_{k}$ is the contribution of positive integer $k$ to the partition, we can describe the partition by $(e_{1},e_{2},e_{3},\dots)$ satisfying
$$
e_{1}+e_{2}+e_{3}+\dots=n
$$
Where $e_{k}\in\{ 0,k \}$ for each $k$. So to the variable $e_{k}$ we associate the expression $1+x^{k}$ and for the generating function, we have
$$
(1+x)(1+x^{2})(1+x^{3})\dots=\prod_{ k=1} ^{ \infty}  (1+x^{k})
$$
Which will generate $a_{n}$ as the coefficient of $x^{n}$ in the resulting infinite producet
Looking at the first few terms:
$$
(1+x)(1+x^{2})(1+x^{3})(1+x^{4})(1+x^{5})\dots=1+x+x^{2}+2x^{3}+2x^{4}+3x^{5}
$$
So, for example $a_{5}=3$ representing $5=3+2=4+1$ as the only $\hspace{0pt}3$ partitions of $\hspace{0pt}5$ into distinct parts
A similar idea extends to the general case, where multiple parts of the same size are allowed:
The number of partitions $p(n)$ of $n$ is the coefficient of $x^{n}$ in the power series expansion of the infinite product
$$
\prod_{ k=1} ^{ \infty}  (1-x^{k})^{-1}=\sum_{ n=0} ^{\infty}  x^{n}p(n)
$$



#Mathematics #Discrete 