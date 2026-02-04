The $k$th convergent to a [[Continued Fraction]] $x=[a_{0};a_{1},\dots ]$ is $c_{k}=[a_{0};a_{1},\dots,a_{k}]$ for $k\leq n$. Note we usually write $c_{k}=\frac{p_{k}}{q_{k}}$
## Calculating Convergents
Let $x=[a_{0};a_{1},\dots,a_{n}]$, then its convergents $c_{k}=\frac{p_{k}}{q_{k}}$ can be calculated using the following recurrence relations:
$$
p_{0}=a_{0},\,p_{1}=a_{0}a_{1}+1,\,\text{for }k\geq 2,\, p_{k}=a_{k}p_{k-1}+p_{k-2}
$$
$$
q_{0}=1,\,q_{1}=a_{1},\text{ for }k\geq 2,\,q_{k}=a_{k}q_{k-1}+q_{k-2}
$$
### Proof
First verify for $k=0$:
$$
c_{0}=[a_{0}]=a_{0}
$$
$$
\frac{p_{0}}{q_{0}}=\frac{a_{0}}{1}=a_{0}
$$
So it is true for $k=0$, next verify for $k=1$:
$$
c_{1}=[a_{0};a_{1}]=a_{0}+\frac{1}{a_{1}}=\frac{a_{0}a_{1}+1}{a_{1}}
$$
$$
\frac{p_{1}}{p_{2}}=\frac{a_{0}a_{1}+1}{a_{1}}
$$
So it is true for $k=1$
For $k\geq 2$, $[a_{0};a_{1},\dots,a_{k}]=\frac{a_{k}p_{k-1}+p_{k-2}}{a_{k}q_{k-1}+q_{k-2}}$
Base case:
$$
LHS=[a_{0},a_{1},a_{2}]=a_{0}+\frac{1}{a_{1}+\frac{1}{a_{2}}}=a_{0}+\frac{1}{\frac{a_{1}a_{2}+1}{a_{2}}}=a_{0}+\frac{a_{2}}{a_{1}a_{2}+1}
$$
$$
=\frac{a_{0}a_{1}a_{2}+a_{0}+a_{2}}{a_{1}a_{2}+1}
$$
$RHS:$
$$
p_{2}=a_{2}p_{1}+p_{0}=a_{2}(a_{0}a_{1}+1)+a_{0}=a_{0}a_{1}a_{2}+a_{0}+a_{2}
$$
$$
q_{2}=a_{2}q_{1}+q_{0}=a_{2}a_{1}+1
$$
$$
\implies RHS=\frac{p_{2}}{q_{2}}=\frac{a_{0}a_{1}a_{2}+a_{0}+a_{2}}{a_{1}a_{2}+1}=LHS
$$
So claim is true for $k=2$
Assume claim is true for $k=r$:
$$
[a_{0};a_{1},\dots,a_{r}]=\frac{p_{r}}{q_{r}}
$$
Where
$$
p_{r}=a_{r}p_{r-1}+p_{r-2}
$$
$$
q_{r}=a_{r}q_{r-1}+q_{r-2}
$$
Consider $k=r+1$:
$$
[a_{0};a_{1},\dots,a_{r},a_{r+1}]=\left[ a_{0};a_{1},\dots,a_{r}+\frac{1}{a_{r+1}} \right]=\frac{\left( a_{r}+\frac{1}{a_{r+1}} \right)p_{r-1}+p_{r-2}}{\left( a_{r}+\frac{1}{a_{r+1}} \right)q_{r-1}+q_{r-2}}
$$
By assumption,
$$
=\frac{a_{r+1}a_{r}p_{r-1}+q_{r-1}+a_{r+1}p_{r-2}}{a_{r+1}a_{r}q_{r-1}+q_{r-1}+a_{r+1}q_{r-2}}=\frac{a_{r+1}(a_{r}p_{r-1}+p_{r-2})+p_{r-1}}{a_{r+1}(a_{r}q_{r-1}+q_{r-2})+q_{r-1}}
$$
$$
=\frac{a_{r+1}p_{r}+p_{r-1}}{a_{r+1}q_{r}+q_{r-1}}
$$
Which is the claim for $k=r+1$
Hence, if the claim is true for $k=r$ then the claim is true for $k=r+1$, and since we have shown that the claim is true for $k=2$, by induction, the claim is true for all $k\geq 2,k\in\mathbb{Z}$
## Two successive convergents satisfy $p_{k-1}q_{k}-p_{k}q_{k-1}=(-1)^{k}$
### Proof
Base case, let $k=1$:
$$
p_{0}q_{1}-p_{1}q_{0}=a_{0}a_{1}-1(a_{0}a_{1}+1)=-1=(-1)^{1}
$$
So the claim is true for $k=1$
Assume the claim is true for $k=r$:
$$
p_{r-1}q_{r}-p_{r}q_{r-1}=(-1)^{r}
$$
Consider the case when $k=r+1$:
$$
p_{r}q_{r+1}-p_{r+1}q_{r}=p_{r}(a_{r+1}q_{r}+q_{r-1})-(a_{r+1}p_{r}+p_{r-1})q_{r}=a_{r+1}p_{r}q_{r}+p_{r}q_{r-1}-a_{r+1}p_{r}q_{r}-p_{r-1}q_{r}
$$
$$
=p_{r}q_{r-1}-p_{r-1}q_{r}=-(-1)^{r}=(-1)^{r+1}
$$
Hence the claim is true by induction
## [[Greatest Common Divisor|$gcd(p_{k},q_{k})=1$]]
### Proof:
Assume $gcd(p_{k},q_{k})=d$, where $d>1$. Then $d|p_{k}$ and $d|q_{k}$ which imply $d|(p_{k-1}q_{k}-p_{k}q_{k-1})$ as this is a linear combination of $p_{k}$ and $q_{k}$ (see the Lemma for the [[Euclidean Algorithm]])
But we know $p_{k-1}q_{k}-p_{k}q_{k-1}=(-1)^{k}$, so this implied $d|(-1)^{k}$. This cannot hold for $d>1$
## A real number $x$ with convergents $c_{n}=\frac{p_{n}}{q_{n}}$ satisfies $| x-c_{n} |<\frac{1}{q_{n}q_{n+1}}$ 
### Proof
For each $n$, we can write $x=[a_{0};a_{1},\dots,a_{n},y_{n+1}]$ such that $y_{n+1}>a_{n+1}$ (assuming $a_{n+1}$ is not the final term), then
$$
\left| x-c_{n} \right|=\left| \frac{y_{n+1}p_{n}+p_{n-1}}{y_{n+1}q_{n}+q_{n-1}}-\frac{p_{n}}{q_{n}} \right|=\left| \frac{y_{n+1}p_{n}q_{n}+q_{n}p_{n-1}-y_{n+1}p_{n}q_{n}-p_{n}q_{n-1}}{q_{n}(y_{n+1q_{n}+q_{n-1}})} \right|
$$
$$
=\left| \frac{p_{n-1}q_{n}=p_{n}q_{n-1}}{q_{n}(y_{n+1}q_{n}+q_{n-1})} \right|=\left| \frac{(-1)^{n}}{q_{n}(y_{n+1}q_{n}+q_{n-1})} \right|= \frac{1}{q_{n}(y_{n+1}q_{n}+q_{n-1})}
$$
since $q_{n},y_{n+1},q_{n-1}>0$
$$
<\frac{1}{q_{n}(a_{n+1}q_{n}+q_{n-1})}=\frac{1}{q_{n}q_{n+1}}
$$
$$
\therefore \left| x-c_{n} \right|<\frac{1}{q_{n}q_{n+1}}
$$
## Convergents oscillate, Odd Numbered Convergents are always Greater than Even Convergents
If $x$ has convergents $c_{1},c_{2},\dots$ then
$$
c_{0}<c_{2}<c_{4}<\dots<c_{2n}<\dots<x<\dots<c_{2n-1}<\dots<c_{3}<c_{1}
$$
The convergents tend to $x$
### Proof
This is essentially a corollary of $p_{k-1}q_{k}-p_{k}q_{k-1}=(-1)^{k}$, dividing through by $q_{k}q_{k-1}$ gives:
$$
\frac{p_{k-1}}{q_{k-1}}-\frac{p_{k}}{q_{k}}=\frac{(-1)^{k}}{q_{k}q_{k-1}}
$$
$$
\implies c_{k-1}-c_{k}=\frac{(-1)^{k}}{q_{k}q_{k-1}}
$$
$$
\implies c_{k}-c_{k+1}=\frac{(-1)^{k+1}}{q_{k}q_{k+1}}
$$
By setting $k=2n+1$ gives:
$$
c_{2n+1}-c_{2n}=\frac{(-1)^{2n+2}}{q_{2n+1}q_{2n}}=\frac{1}{q_{2n+1}q_{2n}}>0
$$
So every odd convergent $c_{2n+1}$ is greater than its predecessor, the even convergent $c_{2n}$. By a similar argument we can also show that $c_{2n+1}>c_{2n+2}$. Then consider $c_{k}-c_{k-2}$:
$$
c_{k}-c_{k-2}=\frac{p_{k}}{q_{k}}-\frac{p_{k-2}}{q_{k-2}}=\frac{p_{k}q_{k-2}-q_{k}p_{k-2}}{q_{k}q_{k-2}}=\frac{q_{k-2}(a_{k}p_{k-1}+p_{k-2})-p_{k-2}(a_{k}q_{k-1}+q_{k-2})}{q_{k}q_{k-2}} 
$$
$$
=\frac{a_{k}(p_{k-1}q_{k-2}-p_{k-2}q_{k-1})}{q_{k}q_{k-2}}=\frac{a_{k}(-(-1)^{k-1})}{q_{k}q_{k-2}}=\frac{a_{k}(-1)^{k}}{q_{k}q_{k-2}}
$$
Hence if $k$ is even $c_{k}-c_{k-2}>0\implies \{ c_{2n} \}$ is an increasing [[Sequences|sequence]], if $k$ is odd, $c_{k}-c_{k-2}<0\implies \{ c_{2n-1} \}$ is a decreasing sequence
## At Least one of Every Two Consecutive Convergents Satisfies $\left| x-\frac{p_{k}}{q_{k}} \right|\leq \frac{1}{2q_{k}^{2}}$
### Proof
We know from above:
$$
\left| \frac{p_{k}}{q_{k}}-\frac{p_{k+1}}{q_{k+1}} \right|=\frac{1}{q_{k}q_{k+1}}
$$
Now consider the [[AM-GM Inequality]]
$$
\frac{a+b}{2}\geq \sqrt{ ab },a,b\geq 0\,a,b\in\mathbb{R}
$$
Take our two values to be: $\frac{1}{q_{k}^{2}}$ and $\frac{1}{q_{k+1}^{2}}$ (both non-negative real numbers)
$$
AM=\frac{\frac{1}{q_{k}^{2}}+\frac{1}{q_{k+1}^{2}}}{2}=\frac{1}{2q_{k}^{2}}+\frac{1}{2q_{k+1}^{2}}
$$
$$
GM=\sqrt{ \frac{1}{q_{k}^{2}}\times \frac{1}{q_{k+1}^{2}} }=\frac{1}{q_{k}q_{k+1}}
$$
$$
\therefore \frac{1}{q_{k}q_{k+1}}\leq \frac{1}{2q_{k}^{2}}+\frac{1}{2q_{k+1}^{2}}
$$
Hence we can bound the difference between our successive convergents as
$$
\left| \frac{p_{k}}{q_{k}}-\frac{p_{k+1}}{q_{k+1}} \right|\leq \frac{1}{2q_{k}^{2}}+\frac{1}{2q_{k+1}^{2}}
$$
Consider the differences between these convergents and $x$:
$$
\left| x-\frac{p_{k}}{q_{k}} \right|+\left| x-\frac{p_{k+1}}{q_{k+1}} \right|=\left| \frac{p_{k}}{q_{k}}-\frac{p_{k+1}}{q_{k+1}} \right|
$$
As by the previous proof, we know convergents oscillate, and exactly one of $c_{k}$, $c_{k+1}$ will ve larger than $x$ 
If we assume the claim is false for both convergents, i.e. $\left| x-c_{k} \right|>\frac{1}{2q_{k}^{2}}$ and $|x-c_{k+1}|>\frac{1}{2q_{k+1}^{2}}$, then
$$
\left| x-c_{k} \right|+\left| x-c_{k+1} \right|>\frac{1}{2q_{k}^{2}}+\frac{1}{2q_{k+1}^{2}}
$$
Which is a contradiction. Hence:
$$
\left| x-c_{k} \right|\leq \frac{1}{2q_{k}^{2}}
$$
or
$$
\left| x-c_{k+1} \right|\leq \frac{1}{2q_{k+1}^{2}}
$$
## At Fewest one of every 3 Consecutive Convergents Satisfies $\left| x-\frac{p_{k}}{q_{k}} \right|\leq \frac{1}{\sqrt{ 5 }q_{k}^{2}}$
### Proof
Assume this is false, i.e. that
$$
\left| x-\frac{p_{i}}{q_{i}} \right|>\frac{1}{\sqrt{ 5 }q_{i}^{2}}
$$
for $i= k,k+1,k+2,\dots$
As above, we know
$$
\left| x-\frac{p_{k}}{q_{k}} \right|+\left| x-\frac{p_{k+1}}{q_{k+1}} \right|=\frac{1}{q_{k}q_{k+1}}
$$
By assumbtion, we can replace the left hand side terms to give
$$
\frac{1}{q_{k}q_{k+1}}>\frac{1}{\sqrt{ 5 }q_{k}^{2}}+\frac{1}{\sqrt{ 5 }q_{k+1}^{2}}
$$
$$
\implies \sqrt{ 5 }>\frac{q_{k+1}}{q_{k}}+\frac{q_{k}}{q_{k+1}}
$$
Let $\alpha=\frac{q_{k+1}}{q_{k}}$, we know $a>1$ ($q_{k+1}>q_{k}$) and so:
$$
\alpha+\frac{1}{\alpha}<\sqrt{ 5 }
$$
Consider the points of intersection:
$$
x^{2}-\sqrt{ 5 }x+1=0
$$
$$
\implies x=\frac{1\pm \sqrt{ 5 }}{2}
$$
If we consider that $x+\frac{1}{x}$ has an asymtote at $x=0$, we know that the inequality solves to be like so:
$$
\frac{1-\sqrt{ 5 }}{2}<\alpha<\frac{1+\sqrt{ 5 }}{2}
$$
But we want $a>1$, so the relevant inequality is $\alpha<\frac{1+\sqrt{ 5 }}{2}$, hence
$$
\alpha=\frac{q_{k+1}}{q_{k}}<\frac{1+\sqrt{ 5 }}{2}
$$

$$
\therefore \frac{q_{k}}{q_{k+1}}>\frac{2}{1+\sqrt{ 5 }}=\frac{\sqrt{ 5 }-1}{2}
$$
We can use the same argument to show also that $\frac{q_{k+1}}{q_{k+1}}<\frac{\sqrt{ 5 }+1}{2}$
Note that:
$$
\frac{q_{k+2}}{q_{k+1}}=\frac{q_{k+2}q_{k+1}+q_{k}}{q_{k+1}}=q_{k+2}+\frac{q_{k}}{q_{k+1}}>1+\frac{\sqrt{ 5 }-1}{2}
$$
As $q_{k+2}\geq 1$ and from above we can say that with equals $\frac{\sqrt{ 5 }+1}{2}$ which is a contradiction
Hence $\left| x-c_{k} \right|\leq \frac{1}{\sqrt{ 5 }q_{k}^{2}}$ for at fewest one of every 3 consecutive convergents
### Corollary
For any irrational number $x$, there are infinitely many rational numbers $\frac{p}{q}$ such that
$$
\left| x-\frac{p}{q} \right|<\frac{1}{\sqrt{ 5 }q^{2}}
$$
This is becuase we have infinitely many convergents by the proposition above, at least one of these satisfies the required condition
This is part of a theorem which further states $\sqrt{ 5 }$ is the best we can do, for any larger constants in the denominator, this would only be there for finitely many approximations of $\varphi=\frac{1+\sqrt{ 5 }}{2}$, in fact, there is a discrete sequence of value $\mathscr{L}(x):\mathscr{L}$ is the [[Boundedness|supremum]] for which $\left| x-\frac{p}{q} \right|<\frac{1}{\mathscr{L}q^{2}}$, which holds for infinitely many $\frac{p}{q}$ ($p,q$ are coprime). It turns out $\mathscr{L}\in\{ \sqrt{ 5 },3 \}$
## For $x \in \mathbb{R} \backslash \mathbb{Q}$, if $\exists \frac{a}{b} \in\mathbb{Q}$ ($b\geq 1$): $\left| x-\frac{a}{b} \right|<\frac{1}{2b^{2}}$, then $\frac{a}{b}$ is one of the convergents of the continued fraction expansion of $x$
### Proof
Assume, for a contradiction, that $\frac{a}{b}$ is not a convergent of $x$, as the $q_{k}$ terms are slightly increasing and unbounded, we can find some $n:q_{n}\leq b<q_{n+1}$. Since we know convergents are the [[Best Approximation of the Second Kind|best approximations of the second kind]], so
$$
\left| bx-a \right|\geq \left| q_{n}x-p_{n} \right|
$$
So we can consider $\left| x-\frac{p_{n}}{q_{n}} \right|$ and that $q_{n}>0$
$$
\left| x-\frac{p_{n}}{q_{n}} \right|=\frac{1}{q_{n}}\left| q_{n}x-p_{n} \right|\leq \frac{1}{q_{n}}\left| bx-a \right|=\frac{b}{q_{n}}\left| x-\frac{a}{b} \right|<\frac{b}{q_{n}}\times \frac{1}{2b^{2}}=\frac{1}{2bq_{n}}
$$
Using the assumption, so if $\frac{a}{b}\neq \frac{p_{n}}{q_{n}}$ and so $\left| aq_{n}-bp_{n} \right|\geq 1$
Hence by replacing the numerator
$$
\frac{1}{bq_{n}}\leq \frac{\left| aq_{n}-bp_{n} \right|}{bq_{n}}=\left| \frac{a}{b}-\frac{p_{n}}{q_{n}} \right|\leq \left| \frac{a}{b}-x \right|+\left| x-\frac{p_{n}}{q_{n}} \right|<\frac{1}{2b^{2}}+\frac{1}{2bq_{n}}
$$
By triangle inequality and using the assumption
$$
\therefore \frac{1}{2bq_{n}}<\frac{1}{2b^{2}}
$$
$b<q_{n}$ since all terms are positive. This contradicts $q_{n}\leq b\leq q_{n+1}$, so $\frac{a}{b}$ must be a convergent of $x$



#Mathematics #Fractions #Definition #Theorem