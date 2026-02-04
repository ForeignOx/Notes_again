A derangement is a [[Permutations|permutation]] of an [[Arrangements old|arrangement]] if no element ends up in its correct position
For $n$ objects, how many of the $n!$ permutation are derangements? Denote this number by $d(n)$
We can use the [[Inclusion-Exclusion Principle|inclusion-exclusion principle]] to find a formula
Start by fixing $n$. For $1\leq i\leq n$, let $A_{i}$ be the [[Sets|set]] of permutations of $1,2,\dots,n$ in which $i$ is in the $i$th place
Then $|A_{i}|=(n-1)!$, since after placing $i$ in the $i$th place, we can arrange the remaining $n-1$ numbers in the remaining $n-1$ places in $(n-1)!$ ways
Similarly, for $i\neq j$, $A_{i}\cap A_{j}$ consists of permutations with both $i$ and $j$ fixed, so:
$$
|A_{i}\cap A_{j}|=(n-2)!
$$
Since after fixing $i$ and $j$, there are $n-2$ free places
In general, is $1\leq i_{1}<i_{2}<\dots<i_{k}\leq n$, then
$$
|A_{i_{1}}\cap A_{i_{2}}\cap\dots A_{i_{k}}|=(n-k)!
$$
Since we place each of the $i_{j}$ in its proper place and arrange the remaining $n-k$ numbers in $(n-k)!$ ways
There are ${n \choose k }$ ways of selecting the $i_{1}<i_{2}<\dots<i_{k}$, so
$$
S_{k}=\sum_{i_{1}<i_{2}<\dots<i_{k}}|A_{i_{1}}\cap A_{i_{2}}\cap\dots \cap A_{i_{k}}|={n \choose k }(n-k)! = \frac{n!}{k!}
$$
So the inclusion-exclusion formula tells us that the number of non-deragnements is:
$$
|A_{1}\cup A_{2}\cup\dots \cup A_{n}|=\sum_{ k=1} ^{ n}  (-1)^{k+1} \frac{n!}{k!}
$$
So the number of deragements can be found by subtracting the number of non-deragements from $n!$
$$
d(n)=n!-\sum_{ k=1} ^{ n}  (-1)^{k+1} \frac{n!}{k!}
$$
$$
= n!\left( 1+\sum_{ k=1} ^{ n}  (-1)^{k+1} \frac{n!}{k!} \right)
$$
$$
= n!\sum_{k=0}^{n}(-1)^{k} \frac{1}{k!}
$$
In particular, the proportion of permutations to derangements is
$$
\frac{d(n)}{n!}=\sum_{k=0}^{n}(-1)^{k} \frac{1}{k}
$$
Note that we can take the limit:
$$
\lim_{ n \to \infty } \frac{d(n)}{n}=\sum_{k=0}^{\infty}(-1)^{k} \frac{1}{k!}=\frac{1}{e}
$$
#Mathematics #Discrete #Definition