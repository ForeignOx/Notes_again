Using the [[Indicator Function|Indicator random variable]], we know
$$
\mathbb{1}_{A}(\omega)=1
$$
From this:
$$
E(\mathbb{1}_{A})=1\times \mathbb{P}(A)+0\times \mathbb{P}(A^{c})=\mathbb{P}(A)
$$
So the conditional expectation of $X$ given $A$, is
$$
E(X|A):=\frac{E(X \mathbb{1}_{A})}{\mathbb{P}(A)}
$$
Where $\mathbb{P}(A)>0$ and is interpreted as the expectation of $X$ with respect to the probability of $\mathbb{P}(\cdot|A)$ 
Let us assume that $\mathbb{P}(B)>0$,
$$
E(\mathbb{1}_{A}|B)=\frac{E(\mathbb{1}_{A}\mathbb{1}_{B})}{\mathbb{P}(B)}=\frac{E(\mathbb{1}_{A\cap B})}{\mathbb{P}(B)}
$$
From above we know that $E(\mathbb{1}_{A})=\mathbb{P}(A)$, so
$$
E(\mathbb{1}_{A}|B)=\frac{\mathbb{P}(A\cap B)}{\mathbb{P}(B)}
$$
## Theorem
Let $X$ be a [[Discrete Random Variables|discrete]] [[Random Variables|random variable]], 
$$
E(X|A)=\sum_{x}x\mathbb{P}(X=x|A)
$$
### Proof
Define $Y=X\mathbb{1}_{A}$
$$
E(X\mathbb{1}_{A})=E(Y)=\sum_{x}x\mathbb{P}(Y=x)
$$
And
$$
\mathbb{P}(Y=x)=\mathbb{P}(X\mathbb{1}_{A}=x)=\mathbb{P}(\{ X=x \}\cap A)=\mathbb{P}(X=x|A)\mathbb{P}(A)
$$
Substituting this back gives:
$$
E(X\mathbb{1}_{A})=\sum_{x}x\mathbb{P}(X=x|A)\mathbb{P}(A)=\mathbb{P}(A)\sum_{x}x\mathbb{P}(X=x|A)
$$
Which shows that 
$$
E(X|A)=\frac{E(X\mathbb{1}_{A})}{\mathbb{P}(A)}=\sum_{x}x\mathbb{P}(X=x)|A
$$
## Example
$X$ and $Y$ are two random variables, let $B\subseteq Y$(?) and $(X,Y)$ has joint pmf $p$, let $g:\mathbb{R}\to \mathbb{R}$, what is $E(g(X)|Y\in B)$?
Consider $B=\{ y \}$,
$$
E(g(x)|Y=y)=\sum_{z}z\mathbb{P}(g(X)=z|Y=y)
$$
$$
= \sum_{x}g(x) \frac{p(x,y)}{p_{Y}(y)}=\sum_{x}g(x)p_{X|Y}(x|y)
$$
Similarly, for any set $B$, we can write
$$
E(g(X)|Y\in B)=\sum_{x}g(x) \frac{\sum_{y\in B}p(x,y)}{\sum_{y\in B}p_{Y}(y)}
$$
### Continuous case
With a jooint pdf $f$, we have a similar formula:
$$
E(g(x)|Y\in B)=\frac{\int _{\mathbb{R}}g(x) \int _{y\in B}f(x,y) \, dy  }{\int _{y\in B} f(y)\, dy }
$$
## Example
In a raffle game, one prze of worth £$\hspace{0pt}500$, and $\hspace{0pt}5$ prizes worth £$\hspace{0pt}100$, $\hspace{0pt}2000$ raffle tickets to choose from. Let $X$ be our winning and $A$ be the event that we get the top prize. We can only choose one ticket. Find $E(X|A)$
$$
\mathbb{P}(X=500|A)=\frac{\mathbb{P}(X=500\cap A)}{\mathbb{P}(A)}=\frac{\mathbb{P}(A)}{\mathbb{P}(A)}=1
$$
So
$$
E(X|A)=\frac{E(X\mathbb{1}_{A})}{\mathbb{P}(A)}=500\times \frac{\mathbb{P}(X=500\cap A)}{\mathbb{P}(A)}=500
$$
## Definition
Let $X,Y:\Omega\to \mathbb{R}$, we define $g:Y(\Omega)\to \mathbb{R}$ by
$$
g(y)=E(X|Y=y)
$$
The conditional expectation of $X$ given $Y=y$, is a random variable denoted by $E(X|Y)$ and defined by:
$$
E(X|Y):=g(Y)
$$
So
$$
E(X|Y(\omega))=E(X|Y=Y(\omega))
$$
For example if $E(X|Y)$ is a random variable which takes the value $E(X|Y=y)$ with probability $\mathbb{P}(Y=y)$ (? is this going anywhere??? thx debleena)