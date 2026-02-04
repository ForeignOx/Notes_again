If $kn+1$ objects ($k\ge 1$ not necessarily finite) are distributed among $n$ boxes, one of the boses will contain at least $k+1$ objects.
## Examples
Prove that every set of $\hspace{0pt}10$ two-digit integer numbers has two disjoint subsets with the same sum of elements.
Let $S$ be the set of $\hspace{0pt}10$ numbers. It has $2^{10}-2=1022$ subsets that differ from both $S$ and $\emptyset$. They are the "pigeons". If $A\subset S$, the sum of elements of $A$ cannot exceed $91+91+\dots+99=855$. The numbers between $1$ and $\hspace{0pt}855$, which are all possible sums, are the "holes". Because the number of "pigeons" exceeds the number of "holes", there will be two "pigeons" in the same "hole". Specifically, there will be two subsets with the same number of elements. Deleting the common elements, we obtain two disjoint sets with the same sum of elements.
___
Given a set $M$ of $\hspace{0pt}1985$ distinct positive integers, none of which has a prime divisor greater than $\hspace{0pt}26$, prove that $M$ contains at least one subset of four distinct elements whose product is the fourth power of an integer.
We show more generally that if the prime divisors of elements in $M$ are among the prime numbers $p_{1},p_{2},\dots p_{n}$ and $M$ has at least $3\cdot 2^{n}+1$ elements, then it contains a subset of four distinct elements whose product is a fourth power.
To each element $m\in M$ we associate an $n$-tuple $(x_{1},x_{2},\dots ,x_{n})$, where $x_{i}$ is $\hspace{0pt}0$ if the exponent of $p_{i}$ in the prime factorisation of $m$ is even, and $1$ otherwise. These $n$-tuples are the "objects". The "boxes" are the $2^{n}$ possible choices of $0$'s and $1$'s.
Hence, by the pigeonhole principle, every subset of $2^{n}+1$ elements of $M$ contains two distinct elements with the same associated $n$-tuple, and the product of these two elements is then a square.
We can repeatedly take aside such pairs and replace them with two of the remaining numbers. From the set $M$, which has at least $3\cdot2^{n}+1$ elements, we can select $2^{n}+1$ such pairs or more. Consider the $2^{n}+1$ numbers that are products of the two eleemts of each pair. The argument can be repeated for their square roots, giving $\hspace{0pt}4$ elements $a,b,c,d$ in $M$ such that $\sqrt{ ab }\sqrt{ cd }$ is a perfect square. Then $abcd$ is a fourth power and we are done. For our problem, $n=9$, while $1985>3\cdot 2^{9}+1=1537$.
___
Prove that for every set $X=\left\{ x_{1},x_{2},\dots,x_{n} \right\}$ of $n$ real numbers, there exists a nonempty subset $S$ of $X$ and an integer $m$ such that
$$
\left| m+\sum_{s \in  S}s \right|<\frac{1}{n+1} 
$$
Recall that the fractional part of a real number $x$ is $x-\lfloor x \rfloor$. Let us look at the fractional parts of the numbers $x_{1},x_{1}+x_{2},\dots,x_{1}+x_{2}+\dots+x_{n}$. If any of them is either in the interval $\left[ 0,\frac{1}{n+1} \right]$ or $\left[ \frac{n}{n+1},1 \right]$, then we are done. If not, we consider these $n$ numbers as the "pigeons" and the $n-1$ intervals $\left[ \frac{1}{n+1},\frac{2}{n+1} \right],\left[ \frac{2}{n+1},\frac{3}{n+1} \right],\dots,\left[ \frac{n-1}{n+1},\frac{n}{n+1} \right]$ as the "holes".
By the pigeonhole principle, two of these sums, say $x_{1}+x_{2}+\dots+x_{k}$ and $x_{1}+x_{2}+\dots+x_{k+m}$ belong to the same interval. But then their different $x_{k+1}+x_{k+2}+\dots+x_{k+m}$ lies within a distance of $\frac{1}{n+1}$ of an integer, and we are done.




#Mathematics 