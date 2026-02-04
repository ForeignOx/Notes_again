 Probability is a measure of chance that we assign to [[Events|events]] [[Sigma Algebra|$A\in\mathfrak{F}$]] 
Associated to [[Sample Spaces|$\Omega$]], there is a collection denoted as $\mathfrak{F}$, which is the collection of all possible events:
$$
\mathfrak{F}=\left\{ A :\middle|: A\subseteq\Omega \right\}
$$
## Definition of Probability
A probability $\mathbb{P}$ on a sample space $\Omega$, with $\mathfrak{F}$ is a mapping such that for every event in $\mathfrak{F}$, $\mathbb{P}(A)$ is a real number satisfying the following [[Axiom|axioms]]:
$$
\mathbb{P}:\mathfrak{F}\to \mathbb{R}
$$
- $\mathbb{P}(A)\geq 0$ (Probability is always non-negative)
- $\mathbb{P}(\Omega)=1$ (Sample space has full probability)
- If $A,B\in\mathfrak{F}$ and $A$ and $B$ are disjoint, that is, $A\cap B=\emptyset$, then $\mathbb{P}(A\cup B)=\mathbb{P}(A)+\mathbb{P}(B)$ (Finite additivity)
- If you have a collection of events $A_{1},A_{2},\dots$ that are pointwise disjoint, i.e. $A_{i}\cap A_{j}=\emptyset$, for all $i\neq j$, then $\mathbb{P}\left( \bigcup_{n=1}^\infty A_{n}\right)=\sum_{n=1}^\infty\mathbb{P}(A_{n})$ (Countable additivity, this is an equivalent axiom to the previous one)
We call the number $\mathbb{P}(A)$ the probability of $A$
$$
(\Omega,\mathfrak{F},\mathbb{P})
$$
Is the triplet known as the probability space 
## Consequences
- $A,B\in\mathfrak{F}$ then $\mathbb{P}(B\setminus A)=\mathbb{P}(B)-\mathbb{P}(A\cap B)$
### Proof
Note that:
$$
(B\setminus A)\cup(A\cap B)=B
$$
$$
\implies \mathbb{P}(B)=\mathbb{P}((B\setminus A)\cup(A\cap B))
$$
And since $B\setminus A$ and $A\cap B$ are disjoint by definition of set difference, we can use the third axiom to say:
$$
\mathbb{P}(B)=\mathbb{P}(B\setminus A)+\mathbb{P}(A\cap B)
$$
$$
\implies \mathbb{P}(B\setminus A)=\mathbb{P}(B)-\mathbb{P}(A\cap B)
$$
# 
___
- $A\in\mathfrak{F}$ then $\mathbb{P}(A^c)=1-\mathbb{P}(A)$
### Proof
Since:
$$
A\cup A^c=\Omega
$$
And $A$ and $A^c$ are disjoint, then, using the third axiom:
$$
\mathbb{P}(A\cup A^c)=\mathbb{P}(\Omega)
$$
And so using the second axiom:
$$
 \implies \mathbb{P}(A)+\mathbb{P}(A^c)=1
$$
 
$$
\implies \mathbb{P}(A^c)=1-\mathbb{P}(A)
$$
#
___
- $\mathbb{P}(\emptyset)=0$
### Proof
$$
\emptyset=\Omega^c
$$
Using the previous consequence and the second axiom,
$$
 \implies \mathbb{P}(\emptyset)=\mathbb{P}(\Omega^c)=1-\mathbb{P}(\Omega)=1-1=0
$$
#
___
- $A\in\mathfrak{F},\mathbb{P}(A)\leq 1$
### Proof#
Since $\mathbb{P}(A)\geq 0$ and $\mathbb{P}(A)+\mathbb{P}(A^c)=1$, we are adding two probabilites greater than $\hspace{0pt}0$ that sum to $\hspace{0pt}1$, so each must be less than or equal to $\hspace{0pt}1$, so $0\leq\mathbb{P}(A)\leq 1$
# 
___
- If $A\subseteq B$, then $\mathbb{P}(A)\leq \mathbb{P}(B)$, known as monotonicity
# 
___
- If $A\subseteq B$, then $\mathbb{P}(B)=\mathbb{P}(A)+\mathbb{P}(B\setminus A)$
### Proof
Since $B=A\cup(B\setminus A)$ is a disjoint union, then
$$
\mathbb{P}(B)=\mathbb{P}(A)+\mathbb{P}(B\setminus A)\geq \mathbb{P}(A)
$$
### Proof
If $A\subseteq B$ then $\mathbb{P}(A\cap B)=\mathbb{P}(A)$, and $\mathbb{P}(B\setminus A)\geq 0$ from the first axiom, so, from the consequence above for the set difference:
$$
\mathbb{P}(B\setminus A)=\mathbb{P}(B)-\mathbb{P}(A\cap B)=\mathbb{P}(B)-\mathbb{P}(A)\geq 0
$$
$$
\implies \mathbb{P}(B)\geq \mathbb{P}(A)
$$
# 
___
- For any two events $A$ and $B$, $\mathbb{P}(A\cup B)=\mathbb{P}(A)+\mathbb{P}(B)-\mathbb{P}(A\cap B)$
### Proof
Consider the fact that $B\setminus A\cap A=\emptyset$, and $B\setminus A\cup A=B\cup A$, we can use the third axiom to say:
$$
\mathbb{P}(A\cup B)=\mathbb{P}(B\setminus A\cup A)=\mathbb{P}(B\setminus A)+\mathbb{P}(A)
$$
And with the consequence above for the set difference:
$$
\mathbb{P}(A\cup B)=\mathbb{P}(A)+\mathbb{P}(B)-\mathbb{P}(A\cap B)
$$
# 
___
- If events $A_{1},A_{2},\dots,A_{k}$ are pairwise disjoint (so $A_{i}\cap A_{j}=\emptyset$ if $i\neq j$) then we call finite additivity the property that:
$$
\mathbb{P}\left( \bigcup_{i=1}^kA_{i} \right)=\sum_{i=1}^{k}\mathbb{P}(A_{i})
$$
### Proof
Consider the case when $k=2$, then
$$
\mathbb{P}\left( \bigcup_{i=1}^2A_{i} \right)=\mathbb{P}(A_{1}\cup A_{2})=\mathbb{P}(A_{1})+\mathbb{P}(A_{2})=\sum_{i=1}^2\mathbb{P}(A_{i})
$$
Using the third axiom, since $A_{1}$ and $A_{2}$ are disjoint
Assume the proposition is true for $k=n$, then
$$
\mathbb{P}\left( \bigcup_{i=1}^n A_{i} \right)=\sum_{i=1}^n\mathbb{P}(A_{i})
$$
Consider an even $A_{n+1}$ that is pairwise disjoint with all other $A_{1},A_{2},\dots,A_{n}$, then
$$
\mathbb{P}\left( \left( \bigcup_{i=1}^n A_{i} \right)\cup A_{n+1} \right)=\mathbb{P}\left( \bigcup_{i=1}^n A_{i} \right)+\mathbb{P}(A_{n+1})=\sum_{i=1}^n\mathbb{P}(A_{i})+\mathbb{P}(A_{n+1})
$$
$$
\therefore \mathbb{P}\left( \bigcup_{i=1}^{n+1}A_{i} \right)=\sum_{i=1}^{n+1}\mathbb{P}(A_{i})
$$
So if it is true for $k=n$ it is also true for $k=n+1$, and since it is true for $k=2$, it is true for all $k=2,3,4,\dots$ by mathematical induction
# 
___
- Boole's inequality: For any events $A_{1},A_{2},\dots$ (they need not be disjoint):
$$
\mathbb{P}\left( \bigcup_{i=1}^\infty A_{i} \right)\leq \sum_{i=1}^\infty \mathbb{P}(A_{i})
$$
- It is also valid in the finite case for events $A_{1},A_{2},\dots,A_{k}$:
$$
\mathbb{P}\left( \bigcup_{i=1}^k A_{i} \right)\leq \sum_{i=1}^k \mathbb{P}(A_{i})
$$
### Proof
Let $B_{1}=A_{1}$, $B_{2}=A_{2}\setminus B_{1}$, $B_{3}=A_{3}\setminus (B_{1}\cup B_{2})$ and in general
$$
B_{n}=A_{n} \setminus \bigcup_{k=1}^{n-1}B_{k}
$$
And the $B_{i}$'s are mutually disjoint by construction; $B_{i}\cap B_{j}=\emptyset$ if $i\neq j$
We observe that
$$
\bigcup_{n=1}^{\infty} B_{n}=\bigcup_{n=1}^{\infty}A_{n}
$$
And $B_{n}\subseteq A_{n}$ by construction
Suppose that $\omega \in A_{n}$, there is a smallest index $k\leq m$ such that $\omega \in A_{k},\omega \not\in A_{1},\dots,A_{k-1}$
Then 
$$
\omega \in  B_{k}\implies \omega \in  \bigcup_{n=1}^{\infty} B_{n}
$$
$$
 \mathbb{P}\left( \bigcup_{n=1}^{\infty}A_{n} \right)=\mathbb{P}\left( \bigcup_{n=1}^{\infty}B_{n} \right)=\sum_{n=1}^{\infty}\mathbb{P}(B_{n})\leq \sum_{n=1}^{\infty}\mathbb{P}(A_{n})
$$
As $B_{n}\subseteq A_{n}$



For the finite case, we can use induction. Let $k=2$
$$
\mathbb{P}\left( \bigcup_{i=1}^2A_{i} \right)=\mathbb{P}(A_{1}\cup A_{2})=\mathbb{P}(A_{1})+\mathbb{P}(A_{2})-\mathbb{P}(A_{1}\cap A_{2})
$$
From the consequence above. From the first axiom, we also know $\mathbb{P}(A_{1}\cap A_{2})\geq 0$, so we then know:
$$
\mathbb{P}\left( \bigcup_{i=1}^2A_{i} \right) \leq \mathbb{P}(A_{1})+\mathbb{P}(A_{2})=\sum_{i=1}^2A_{i}
$$
So the proposition is true for $k=2$
Now assume that the proposition is true for $k=n$:
$$
\mathbb{P}\left( \bigcup_{i=1}^n A_{i} \right)\leq \sum_{i=1}^n \mathbb{P}(A_{i})
$$
Now consider:
$$
\mathbb{P}\left( \bigcup_{i=1}^n A_{i}\cup A_{n+1}\right)=\mathbb{P}\left( \bigcup_{i=1}^n A_{i} \right)+\mathbb{P}(A_{n+1})-\mathbb{P}\left( \bigcup_{i=1}^n A_{i}\cap A_{n+1}\right)
$$
Again, the third term is greater than $\hspace{0pt}0$, so:
$$
\mathbb{P}\left( \bigcup_{i=1}^n A_{i}\cup A_{n+1}\right)\leq \mathbb{P}\left( \bigcup_{i=1}^n A_{i} \right)+\mathbb{P}(A_{n+1})\leq \sum_{i=1}^n\mathbb{P}(A_{i})+\mathbb{P}(A_{n+1})
$$
$$
\therefore \mathbb{P}\left( \bigcup_{i=1}^{n+1} A_{i} \right)\leq \sum_{i=1}^{n+1} \mathbb{P}(A_{i})
$$
So if the statement is true for $k=n$, it is also true for $k=n+1$, and since it is true for $k=2$, it is true for all $k=2,3,4,\dots$ by induction
# 
___
- Boole's other inequality: For any events $A_{1},A_{2},\dots$:
$$
\mathbb{P}\left( \bigcap_{i=1}^\infty A_{i} \right)\geq 1-\sum_{i=1}^\infty \mathbb{P}(A^c_{i})
$$
### Proof
Consider Boole's inequality for events $A^c_{1},A^c_{2},\dots$:
$$
\mathbb{P}\left( \bigcup_{i=1}^\infty A^c_{i} \right)\leq \sum_{i=1}^\infty \mathbb{P}(A^c_{i})
$$
By [[Law of De Morgan|De Morgan's law]], we can rewrite this as:
$$
\mathbb{P}\left(\left( \bigcap_{i=1}^\infty A_{i} \right)^c\right)\leq \sum_{i=1}^\infty \mathbb{P}(A^c_{i})
$$
Using the consequence above about the compliment of an event, we can say:
$$
1-\mathbb{P}\left( \bigcap_{i=1}^\infty A_{i} \right)\leq \sum_{i=1}^\infty \mathbb{P}(A^c_{i})
$$
$$
\implies \mathbb{P}\left( \bigcap_{i=1}^\infty A_{i} \right)\geq 1-\sum_{i=1}^\infty \mathbb{P}(A^c_{i})
$$
# 
___
- Continuity along monotone limits. If $A_{1}\subseteq A_{2}\subseteq\dots$ is an increasing sequence of events, then:
$$
\mathbb{P}\left( \bigcup_{i=1}^\infty A_{i} \right)=\lim_{ i \to \infty }\mathbb{P}(A_{i}) 
$$
- If $A_{1} \supseteq A_{2} \supseteq\dots$ is a decreasing sequence of events, then
$$
\mathbb{P}\left( \bigcap_{i=1}^\infty A_{i} \right)=\lim_{ i \to \infty } \mathbb{P}(A_{i})
$$

## Examples
$$
\Omega=\{ \omega_{1},\omega_{2},\dots,\omega_{m} \}
$$
Let $\omega_{i},1\leq i\leq m$ be distinct
$$
A=\{ \omega_{1},\omega_{2},\omega_{3} \}\subseteq\Omega
$$
Since they are distinct, by the third axiom, and since:
$$
\{ \omega_{1} \}\subseteq\Omega,\{ \omega_{2} \}\subseteq\Omega,\{ \omega_{3} \}\subseteq\Omega
$$
Then
$$
\mathbb{P}(A)=\mathbb{P}(\{ \omega_{1} \}\cup \{ \omega_{2} \}\cup \{ \omega_{3} \})=\sum_{i=1}^3\mathbb{P}(\{ \omega_{i} \})
$$
So if $\mathbb{P}(\{ \omega_{i} \})=p_{i}\geq 0$ ($1\leq i\leq m$), such that $\sum_{i=1}^mp_{i}=1$, 
$$
\Omega=\bigcup_{i=1}^m\{ \omega_{i} \}
$$
Therefore
$$
\mathbb{P}(\Omega)=\sum_{i=1}^m\mathbb{P}(\{ \omega_{i} \})=1
$$
Then $A\subseteq\Omega$,
$$
\mathbb{P}(A)=\sum_{i|w_{i}\in A}p_{i}
$$
This is an example of [[Equally Likely Outcomes|equally likely outcomes]]
___
What is the probability that, in an indefinitely long sequence of tosses of a fair coin, we will eventually see heads?
The sample space $\Omega$ is infinite and consists of all sequences $\omega=(\omega_{1},\omega_{2},\dots)$ with $\omega_{i}=\{ H,T \}$
What is $\mathbb{P}$? It certainly would not be desirable  that if we restrict to just a finite sequence of $n$ tosses, then each of the $2^{n}$ possible outcomes (sequences) should be equally likely. It is a special case of a general theorem that such a $\mathbb{P}$ exists and is unique. Now let $A=\{ H\text{ occurs} \}$, then the only way $A$ can not occur is if there are no heads, so $A^{c}=\{ (TTT\dots) \}$. This is a single sequence out of infinitely many, and it is intuitively clear that it should have a probability $\hspace{0pt}0$. To prov this, it is enough to observe that $A^{c}\subseteq \{ \text{first }n\text{ tosses }T \}$, so by monotonicity,
$$
\mathbb{P}(A^{c})\leq \mathbb{P}(\{ \text{first }n\text{ tosses }T \})\leq 2^{-n}
$$
Since this is true for any $n$, we must have $\mathbb{P}(A^{c})=0$
Another way to see this is as follows. Consider evens defined for $n=1,2,3\dots$ by
$$
A_{n}=\{ \text{first }H\text{ occurs on toss }n \}=\{ \omega\mid\omega_{k}=T,\forall k<n,\omega_{n}=H \}
$$
For example $A_{1}$ consists of sequences $H\dots$, $A_{2}$ consists of sequences $TH\dots$ Now the even we are interested in is
$$
A=\bigcup_{n=1}^{\infty}A_{n}
$$
$$
\mathbb{P}(A)=\sum_{ n=1} ^{\infty}\mathbb{P}(A_{n})=\sum_{ n=1} ^{\infty}  2^{-n}=1
$$
Note that a similar arcument works if the coin is biased with probability $p \in(0,1)$ of heads
In fact the sequence space is not even [[Countable Sets|countable]]. To see this, a sequence $(d_{1},d_{2},\dots)$ with each $d_{i}\in\{ 0,1 \}$ is called a dyadic expansion of $x\in[0,1]$ if $x=\sum_{ i=1} ^{\infty} 2^{-i}d_{i}$. For example, $(1,0,0,\dots)$ is a dyadic expansion of $\frac{1}{2}$, $(1,1,0,0,\dots)$ is $\frac{3}{4}$ and so on. The map between $x$ and $(d_{1},d_{2},\dots)$ is almost a bijection, but is not due to non-uniqueness of the dyadic expansion, so for example $(0,1,1,1,\dots)$ is another expansion for $\frac{1}{2}$. It turns out that this problem only occurs for rational $x$, and can be circumvented, thus we have a bijection between $[0,1]$ and the space of infinite sequences of $0$s and 1s, which is another name for our coin tossing space $\Omega$. This shows $\Omega$ is uncountable
It is remarkble that the probability $\mathbb{P}$ on infinite sequences of coin tosses that was claimed to exist turns out to correspond (under the bijection by the dyadic expansion) to nothing other than the [[Uniform Distribution|uniform distribution]] on $[0,1]$, that is the measure defined by lengths of intervals, known as the famous [[Measures|Lebesgue measure]]

#Mathematics #Probability 


