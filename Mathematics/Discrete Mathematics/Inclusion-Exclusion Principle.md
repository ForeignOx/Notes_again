How do we find the size of a [[Union|union]] of several [[Sets|sets]] $A_{1},\dots ,A_{n}$? If the sets are pairwise disjoint, we may use the [[Rule of Sum|rule of sum]]: if $A_{i}\cap A_{j}=\emptyset$ for all $i\neq j$,
$$
|A_{1}\cup A_{2}\cup\dots \cup A_{n}|=|A_{1}|+|A_{2}|+\dots+|A_{n}|
$$
If the sets are not pairwise disjoint, we can use the formula:
$$
|A_{1}\cup A_{2}|=|A_{1}|+|A_{2}|-|A_{1}\cap A_{2}|
$$
If we have more than two sets, we apply this repeatedly, for example
$$
|A_{1}\cup A_{2}\cup A_{3}|=|A_{1}|+|A_{2}|+|A_{3}|-|A_{1}\cap A_{2}|-|A_{1}\cap A_{3}|-|A_{2}\cap A_{3}|+|A_{1}\cap A_{2}\cap A_{3}|
$$
or another way of thinking about this is:
Consider any element $x\in A_{1}\cup A_{2}\cup A_{3}$, on the LHS it is counded exatly one, we must show it is counted exactly once on the RHS too.
If $x$ is in exactly one of the sets, say $A_{1}$, it is indeed just counted once, in $|A_{1}|$
If $x$ is in exactly two sets, say $A_{1}$ and $A_{2}$, it appears with a positive sign in $|A_{1}|$ and $|A_{2}|$ and with a negative sign in $|A_{2}\cap A_{1}|$, so is also counted once in total
If $x$ is in all three sets, it is counted a total of $1+1+1-1-1-1-1+1=1$ times
___
The more general version is conceptually no more difficult, but requires some more notation
Suppose we have sets $A_{1},A_{2},\dots A_{n}$. A typical $k$-fold intersection $(1\leq k\leq n)$ of a selection of these sets can be written as:
$$
A_{i_{1}}\cap A_{i_{2}}\cap\dots \cap A_{i_{k}}
$$
Where $1\leq i_{1}\leq i_{2}\leq\dots \leq i_{k}\leq n$. Let
$$
S_{k}=\sum_{i_{1}<i_{2}<\dots<i_{k}}|A_{i_{1}}\cap A_{i_{2}}\cap\dots \cap A_{i_{k}}|
$$
be the sum of the sizes of all possible $k$-fold intersections. For example, in the case $n=3$:
$$
S_{1}=|A_{1}|+|A_{2}|+|A_{3}|
$$
$$
 S_{2}=|A_{1}\cap A_{2}|+|A_{1}\cap A_{3}|+|A_{2}\cap A_{3}|
$$
$$
 S_{3}=|A_{1}\cap A_{2}\cap A_{3}|
$$
Then the case with $\hspace{0pt}3$ can be written as $|A_{1}\cup A_{2}\cup A_{3}|=S_{1}-S_{2}+S_{3}$. More generally, we have the following:
For a positive integer $n$ and finite sets $A_{1},A_{2},\dots,A_{n}$,
$$
|A_{1}\cup A_{2}\cup\dots \cup A_{n}|=\sum_{ k=1} ^{ n}  (-1)^{k+1}S_{k}
$$
This is a fundamental principle in discrete mathematics
## Proof
Base case: $n=1$
$$
|A_{1}|=S_{1}
$$
$$
\sum_{k=1}^{1}(-1)^{k+1}S_{k}=(-1)^{2}S_{1}=S_{1}
$$
Hence true
Assume true for $n=m$:
$$
\left| A_{1}\cup A_{2}\cup\dots \cup a_{m} \right| =\sum_{k=1}^{m}(-1)^{k+1}S_{k}
$$
Consider $n=m+1$
$$
\left| A_{1}\cup \dots \cup A_{m+1} \right|=\left| A_{1}\cup\dots \cup A_{m} \right| +\left| A_{m+1} \right| -\left| A_{m+1}\cap(A_{1}\cup \dots \cup A+m) \right| 
$$
$$
=\left| A_{1}\cup\dots \cup A_{m} \right|+\left| A_{m+1} \right| -\left| (A_{m+1}\cap A_{1})\cup(A_{m+1}\cap A_{2})\cup\dots \cup(A_{m+1}\cap A_{m}) \right| 
$$
The first and last terms both follow the principle as they have $m$ terms each, giving:
$$
=\sum_{1\leq i\leq m}\left| A_{i} \right| -\sum_{1\leq i_{1}\leq i_{2}\leq n}\left| A_{i_{1}}\cap A_{i_{2}} \right| +\dots+(-1)^{n+1}\left| A_{1}\cap \dots A+m \right| +\left| A_{m+1} \right| 
$$
$$
-\left( \sum_{1\leq i\leq m}\left| A_{m+1}\cap A_{i}\right|-\sum_{1\leq i_{1}\leq i_{2}\leq m}\left| A_{m+1}\cap A_{i_{1}}\cap A_{i_{2}} \right|   +\dots+(-1)^{n+1}\left| A_{1}\cap\dots \cap A_{m+1} \right| \right)
$$
$$
=\sum_{1\leq i\leq m+1}\left| A_{i} \right| -\sum_{1\leq i_{1}\leq i_{2}\leq m+1}\left| A_{i_{1}}\cap A_{i_{2}} \right| +\dots\underbrace{ -(-1)^{n+1} }_{ +(-1)^{n+2} }\left| A_{1}\cap\dots \cap A_{m+1} \right| 
$$
$$
 =\sum_{k=1}^{m+1}S_{k}
$$
Hence proved by induction
## Examples
Consider 5-letter words using the letters "PQR", how many have at least one letter missing
Let $A_{1}=\{ \text{words missing P} \}$, $A_{2}=\text{words missing Q}$, $A_{3}=\text{words missing R}$, we want
$$
\left| A_{1}\cup A_{2}\cup A_{3} \right| =\left| A_{1} \right| +\left| A_{2} \right| +\left| A_{3} \right| -\left| A_{1}\cap A_{2} \right| -\left| A_{1}\cap A_{3} \right| -\left| A_{2}\cap A_{3} \right| +\left| A_{1}\cap A_{2}\cap A_{3} \right| 
$$
Here 
$$
\left| A_{1} \right| =\left| A_{2} \right| =\left| A_{3} \right| =2^{5}
$$
$$
\left| A_{1}\cap A_{2} \right| =\left| A_{1}\cap A_{3} \right|=\left| A_{2}\cap A_{3} \right| =1
$$
$$
\left| A_{1}\cap A_{2}\cap A_{3} \right| =0
$$
Hence
$$
\left| A_{1}\cup A_{2}\cup A_{3} \right| =3\times 2^{5}-3\times 1+0=93
$$


#Mathematics #Set 