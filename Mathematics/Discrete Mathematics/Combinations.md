A combination from a [[Sets|set]] of objects is an unordered selection of elements of that set. Repeats may be allowed
So $STOAT$ and $TOAST$ are different [[Arrangements|arrangements]], but the same combinations
Formally a combination on set $S$ is identified by factors $m_{i}$, $i\in S$, where $m_{i}=$ number of times element $i$ appears
In our example, $A:1,O:1,S:1,T:2$ 
The size at combination is the total number of selections (without replacement) we call a combination of size $k$ a $k$-combination
___
How many $k$-combinations without repetitions do we have from a set of size $n$
If we start with $n$ distinct objects, each selection, or combination, of $k$ of these objects, with no reference to order, corresponds to $k!$ [[Permutations|permutations]] of a size $k$ from the $n$ objects. Thus the number of combinations of size $r$ forom a collection of size $n$, denoted $C(n,k)$, where $0\leq k\leq n$ satisfies $(k!)C(n,k)=P(n,k)$, so:
$$
C(n,k)=\, ^nC_{k}=C^k_{n}=\begin{pmatrix}
n\\k
\end{pmatrix}:=\frac{P(n,k)}{k!}=\frac{n!}{k!(n-k)!}=\frac{n(n-1)(n-2)\dots(n-k+1)}{k!}
$$
Note that:

$$
\begin{pmatrix}
n\\k
\end{pmatrix}=\begin{pmatrix}
n\\n-k
\end{pmatrix}=\begin{pmatrix}
n-1\\k-1
\end{pmatrix}+\begin{pmatrix}
n-1\\k
\end{pmatrix}
$$
The second equality is also known as Pascal's formula, and is derived by the fact that every entry in the interior of Pascal's triangle is the sum of the two entries just above it
Also note that $^nC_{k}$ is also a binomial coefficient, and appears in the [[Binomial Theorem|binomial expansion]] of $(1+x)^{n}$
The fact that ${n \choose k }={n \choose n-k }$ shows a correspondence between the selection of size $k$ from a collection of $n$ and the selection of the $n-k$ objects left behind
Also also note that a combination of size $k$ 
## Example
Suppose that Ellen draaws five cards from a standard deck of $\hspace{0pt}52$ cards, in how many ways can her selection result in a hand with no clubs?
If we examine this more closely, we see that Ellen is restricted to selecting her $\hspace{0pt}5$ cards from the $\hspace{0pt}39$ cards in the deck that are not clubs. Consequently, she can make her selection in ${39 \choose 5 }$ ways
Now, suppose we want to count the number of Ellen's 5-card selections that contain at least one club. These are precisely the selections that were not counted in the previous question, and since there are ${52 \choose 5 }$ possible 5-card hands in total, we find that
$$
{52 \choose 5 }-{39 \choose 5 }=2023203
$$
Of all 5-card hands contain at least one club
Can we obtain this result in another way? For example, since Ellen wants to have at least one club in the 5-card hand, let her first select a club. This she can do in ${13 \choose  1}$ ways, and now she doesn't care what comes up for the other $\hspace{0pt}4$ cards, so after she eliminates the $\hspace{0pt}1$ club, she can then select the other $\hspace{0pt}4$ cards in ${51 \choose 4 }$ ways. Therefore, by [[Rule of Product|rule of product]], we count the number of selections here as:
$$
{13 \choose 1 }{51 \choose 4 }=3248700
$$
Which is different... This answer is larger than the previous one by more than $\hspace{0pt}1000000$ hands, the reason for this is overcounting. Imagine for example, that first Ellen selects $\hspace{0pt}3$ of clubs to start, then $\hspace{0pt}5$ of clubs then king of clubs, then $\hspace{0pt}7$ of hearts then jack of spades, that is not different to if she selected $\hspace{0pt}5$ of clubs to start, then $\hspace{0pt}3$ of clubs, king of clubs, $\hspace{0pt}7$ of hearts, jack of spades. There is also another identical case if she selected king of clubs to start
Another way then to do this properly is to consider exact numbers of clubs, as demonstrated in the table below:

| Number of clubs | Numer of Ways to Select this Number of Clubs | Number of Non-Clubs | Number of Ways to Select this Number of Non-Clubs |
| --------------- | -------------------------------------------- | ------------------- | ------------------------------------------------- |
| 1               | ${13 \choose 1 }$                            | 4                   | ${39 \choose 4 }$                                 |
| 2               | ${13 \choose 2 }$                            | 3                   | ${39 \choose 3 }$                                 |
| 3               | ${13 \choose 3 }$                            | 2                   | ${39 \choose 2 }$                                 |
| 4               | ${13 \choose 4 }$                            | 1                   | ${39 \choose 1 }$                                 |
| 5               | ${13 \choose 5 }$                            | 0                   | ${39 \choose 0 }$                                 |
Since no two of these cases have any 5-card hand in common, the number of hands that Ellen can select with at least one club is:
$$
{13 \choose 1 }{39 \choose 4 }+{13 \choose 2 }{39 \choose 3 }+{13 \choose 3 }{39 \choose 2 }+{13 \choose 4 }{39 \choose 1 }+{13 \choose 5 }{39 \choose  0}=\sum_{i=1}^{5}{13 \choose i }{39 \choose 5-i }=2023203
$$
Yay
## Combinations with Repetition
To start with let's look at how many $k$-combinations with repetitions from $n$ objects there are in which each object is chosen at least once in the combination?
This question clearly has a non-zero answer only if $k\geq n$
The way to think of this is that you can fix some order for the $n$ objects, sorting each $k$-combination so that its objects respect this order. There are $k-1$ gaps between items in the list. Each combination is described uniquely by inserting $n-1$ markers into the $k-1$ gaps, where markers indicate the boundary between successive types of objects, so the answer is
$$
{k-1 \choose n-1 }
$$
## Example
Find the number of $5$-combinations from $\{ 1,2,3 \}$ in which each number appears at least once. Since order doesn't matter, we represent each combination with its items in non-decreasing order, like $\hspace{0pt}1$ $\hspace{0pt}1$ $\hspace{0pt}1$ $\hspace{0pt}2$ $\hspace{0pt}3$, then insert markers such as $|$ where the numbers change, to get something like $111|2|3$, now we don't care that much about what the numbers are, so we can replace them with stars like so: $** *|*|*$ now we are finding the number of ways to place those bars, so there are $\hspace{0pt}4$ places to put $\hspace{0pt}2$ bars, so there are ${4 \choose 2 }$ combinations
# 
___
We can then extend this to finding the number of $k$-combinations from $n$ different objects with repetition. By the same process, we convert this problem into a problem of [[Ordered Grouping of Indistinguishable Objects|ordered grouping of indistinguishable objects]] and we can use the stars and bars method again to find the number to be:
$$
{k+n-1 \choose n-1 }={k+n-1 \choose k }
$$

#Mathematics #Discrete 