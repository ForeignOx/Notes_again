Given a [[Proposition|proposition]] $A(n)$ depending on positive [[Integers|integers]] $n$, 
- if $P(n_{0})$ is true for some positive integer $n_{0}$, and
- if for every $k\geq n_{0}$, $P(k)\implies P(k+1)$,
Then $P(n)$ is true for all $n\geq n_{0}$
### Examples
$1^{3}+2^{3}+3^{3}+\dots+n^{3}=\frac{n^{2}(n+1)^{2}}{4}$, which we can call $A(n)$
Check $A(1)$, $LHS=1$, $RHS=\frac{1^{2}2^{2}}{4}=1=LHS$ 
Assume $A(k)$ is true, for some $k\in\mathbb{N}$:
$$
1+2^{3}+3^{3}+\dots+k^{3}+(k+1)^{3}=\frac{k^{2}(k+1)^{2}}{4}+(k+1)^{3}
$$
$$
= (k+1)^{2}\left( \frac{k^{2}}{4}+k+1 \right)=\frac{(k+1)^{2}}{4}(k^{2}+4k+4)=\frac{(k+1)^{2}(k+2)^{2}}{4}
$$
So $A(k+1)$ is true
Thus by induction it holds for all $n\in\mathbb{N}$
___
Let $a_{1},\dots,a_{n}$ be positive real numbers with $a_{1}\cdot a_{2}\cdot\dots a_{n}=1$, then $a_{1}+a_{2}+\dots+a_{n}\geq n$ with equality if and only if all $a_{i}=1$. This will be $A(n)$
Consider $A(1)$, we must have $\hspace{0pt}1$ real number and it must be equal to $1$, so $1\geq 1$ and there is equality since all terms are 1
Assume $A(k)$ is true, consider $A(k+1)$, take positive real numbers $a_{1},\dots,a_{k+1}$ with $a_{1}+\dots+a_{k+1}\geq n+1$ with equality if all $a_{i}=1$
The equality is easy to show, if all $a_{i}=1$, their sum is $n+1$
Now assume they are not all $1$, so some $a_{i}\neq 1$, we can assume $a_{i}<1$, now there must be some real number $a_{j}>1$ to make their product equal to $\hspace{0pt}1$, we can say without loss of generality $i=1$, $j=2$, so $a_{1}<1,a_{2}>1$, consider $(a_{1}-1)(a_{2}-1)$ which will be negative as $a_{1}-1$ is negative and $a_{2}-1$ is positive. 
$$
(a_{1}-1)(a_{2}-1)=a_{1}a_{2}-a_{2}-a_{1}+1<0
$$
$$
 \iff a_{1}a_{2}<a_{1}+a_{2}-1
$$
Now consider $k$ positive numbers $a_{1}a_{2},a_{3},\dots,a_{k+1}$ which also have a product of $\hspace{0pt}1$, now by induction assumbtion we have that:
$$
k\leq a_{1}a_{2}+a_{3}+\dots+a_{k+1}<a_{1}+a_{2}+a_{3}+\dots+a_{k+1}-1
$$
$$
 \implies a_{1}+a_{2}+..+a_{k+1}>n+1
$$
Thus it is proved
___
Finitely many lines divide the plane into regions. Show that these regions can be coloured by two colours in such a way that neighbouring regions have different colours
The base case $n=1$ is obvious, colour one half-plane black, the other white
For the inductive step, assume that we know how to colour any map defined by $k$ lines. Add the $k+1$th line to the picture and keep the colour of the regions on one side of this line, and swapping the colours on the other side
![[Proof by Mathematical Induction!!!!! 2025-06-28 14.08.13.excalidraw]]
So regions that were adjacent previously still have different colours. Regions that share a segment of the $k+1$th line, which were part of the same region previously, now lie on opposite sides of the line. So they have different colours too. This shows that the new map satisfies the required property and the induction is complete
___
For a positive integer $n$ and an integer greater than $\hspace{0pt}2$, define $f_{1}(n)=n$, $f_{2}(n)=n^{f_{1}(n)},\dots,f_{i+1}(n)=n^{f_{i}(n)},\dots$. Prove that:
$$
f_{m}(n)<n!!\cdots!<f_{m+1}(n)
$$
Where the term in the middle has $m$ factorials.
Solution: For convenience, let us introduce $g_{0}(n)=n$, and recursively $g_{i+1}(n)=(g_{i}(n))!$. The double inequality now reads:
$$
f_{m}(n)<g_{m}(n)<f_{m+1}(n)
$$
For $m=1$ this is obviously true, and it is only natural to think of this as the base case. We start by proving the inequality on the left by induction on $m$. First note that if $t>2n^{2}$ is a positive integer, then
$$
t!>(n^{2})^{t-n^{2}}=n^{t}n^{t-2n^{2}}>n^{t}
$$
Now, it is not hard to check that $g_{m}(n)>2n^{2}$ for $m\geq 2$ and $n\geq 3$. With this in mind, let us assume the inequality to be true for $m=k$. Then
$$
g_{k+1}(n)=(g_{k}(n))!>n^{g_{k}(n)}>n^{f_{k}(n)}=f_{k+1}(n)
$$
which proves the inequality for $m=k+1$. This verifies the inductive step and solves half of the problem.
Here we pause for a short observation. Sometimes the proof of a  mathematical statement becomes simpler if the statement is strengthened. This is the case with the second inequality, which we replace by the much stronger
$$
g_{0}(n)g_{1}(n)\dots g_{m}(n)<f_{m+1}(n)
$$
Holding true for $m$ and $n$ as aboe. As an intermediate step, we establish, by induction on $m$, that
$$
g_{0}(n)g_{1}(n)\dots g_{m}(n)<n^{g_{0}(n)g_{1}(n)\dots g_{m-1}(n)}
$$
For all $m$ and all $n\geq 3$. The base case $m=1$ is obvious: $n\cdot n!<n^{n}$. Now assume that the inequality is true for $m=k$, and prove it for $m=k+1$. We have
$$
g_{0}(n)g_{1}(n)\dots g_{k+1}(n)=g_{0}(n)g_{0}(n!)\dots g_{k}(n!)<g_{0}(n)(n!)^{g_{0}(n!)g_{1}(n!)\dots g_{k-1}(n!)}
$$
$$
 <n(n!)^{g_{1}(n)\dots g_{k}(n)}<(n\cdot n!)^{g_{1}(n)\dots g_{k}(n)}<(n^{n})^{g_{1}(n)\dots g_{k}(n)}=n^{g_{0}(n)g_{1}(n)\dots g_{k}(n)}
$$
Completing the induction, and proving the claim.
Next, we show, also by induction on $m$, that $g_{0}(n)g_{1}(n)\dots g_{m}(n)<f_{m+1}(n)$ for all $n$. The base case $m-1$ is $n\cdot n!<n^{n}$; it follows by multiplying $1\cdot2<n$ and $2\cdot4\cdots n<n^{n-2}$. Let's see the inductive step. Using the inequality for the $g_{m}$'s proved above and the assumption that the inequality holds for $m=k$, we obtain
$$
g_{0}(n)\dots g_{m}(n)g_{m+1}(n)<n^{g_{0}(n)\dots g_{m}(n)}<n^{f_{m+1}(n)}=f_{m+2}(n)
$$
Which is the ineuality for $m=k+1$. This completes the last induction, and with it the solution to the problem.
## Strong Induction
Given a proposition $A(n)$ depending on positive integers $n$,
- If $P(n_{0}),P(n_{0}+1),\dots,P(n_{0}+m)$ are true for some positive integer $n_{0}$ and non-negative number $m$, and
- If for every $k>n_{0}+m$, $P(j)$ is true for all $n_{0}\leq j<k$ implies $P(k)$ is true, then $P(n)$ is true for all $n\geq n_{0}$ by strong induction
### Examples
Let $f:\mathbb{N}\to \mathbb{N}$ be a strictly increasing function such that $f(2)=2$ and $f(mn)=f(m)f(n)$ for every relatively prime pair of positive integers $m$ and $n$. Prove that $f(n)-n$ for every positive integer $n$.
The proof is by induction on $n$. Monotonicity implies tht $f(1)=1$. However, the base case is not the given $f(2)=2$, but $f(2)=2$ and $f(3)=3$. So let us find $f(3)$. Because $f$ is strictly increasing, 
$$
f(3)f(5)=f(15)<f(18)=f(2)f(9)
$$
Hence$f(3)f(5)<2f(9)$ and 
$$
f(9)<f(10)=f(2)f(5)=2f(5)
$$
so combining these we get
$$
f(3)f(5)<4f(5)
$$
So $f(3)<4$, and $f(3)>f(2)=2$, so $f(3)=3$.
The inductive step is fairly straightforward. Let $k>3$ and assume that $f(j)=j$ for $j<k$. Consider $2^{r}(2m+1)$ to be the smallest even integer greater than or equal to $k$ that is not a power of $2$.. This number is equal to either $k,k+1,k+2$ or $k+3$ since $k>3$, both $2^{r}$ and $2m+1$ are strictly less than $k$. From the induction hypothesis, we obtain 
$$
f(2^{r}(2m+1))=f(2^{r})f(2m+1)=2^{r}(2m+1)
$$
So by monotonicity, combined with the fact that there are at most $2^{r}(2m+1)$ values that the function can take in the interval $[1,2^{r}(2m+1)]$, implies that $f(l)=l$ for $l\leq 2^{r}(2m+1)$. In particular, $f(k)=k$. We conclude that $f(n)=n$ for all positive integers $n$
## Cauchy Induction
This is another form of induction derived by Cauchy.
Given a proposition $A(n)$ devpending on the positive integers greater than or equal to $\hspace{0pt}2$, the technique of Cauchy Induction is to prove that:
- $A(2)$ is true, and that 
- $A(n)$ implies $A(2n)$. This implies that $A(2^{m})$ is true for all $m>0$.
- Finally then prove that $A(n)$ implies $A(n-1)$.
Then $A(n)$ is true for all $n\ge 2$.
This can in fact be generalised with the second step, one needs only show that $A(n)$ implies $A(f(n))$ for any $f(n)$ such that $f(n)>n$.
### Examples
Let $a_{1},a_{2},\dots,a_{n}$ be real numbers greater than $1$. Prove the inequality:
$$
\sum_{ i=1} ^{ n}  \frac{1}{1+a_{i}} \ge \frac{n}{1+\sqrt[n]{a_{1}a_{2}\dots a_{n}  }}
$$
As always we start with the base case:
$$
\frac{1}{1+a_{1}}+\frac{1}{1+a_{2}}\geq \frac{2}{1+\sqrt{ a_{1}a_{2} }}
$$
$$
\iff (2+a_{1}+a_{2})(1+\sqrt{ a_{1}a_{2} })\ge 2(1+a_{1}+a_{2}+a_{1}a_{2})
$$
$$
\iff 2\sqrt{ a_{1}a_{2} }+(a_{1}+a_{2})\sqrt{ a_{1}a_{2} }\geq a_{1}+a_{2}+2a_{1}a_{2}
$$
$$
\iff 2\sqrt{ a_{1}a_{2} }(1-\sqrt{ a_{1}a_{2} })+(a_{1}+a_{2})(\sqrt{ a_{1}a_{2} }-1)\ge 0
$$
$$
\iff (\sqrt{ a_{1}a_{2} }-1)(a_{1}+a_{2}-2\sqrt{ a_{1}a_{2} })\geq 0
$$
This inequality is now obvious since $a_{1}a_{2}\geq 1$ and $a_{1}+a_{2}\geq 2\sqrt{ a_{1}a_{2} }$ (By [[AM-GM Inequality|AM-GM]])
Now we prove the inequality holds for $n=2^{k}$ by assuming it true for $k$, we can write
$$
\sum_{i=1}^{2^{k+1}} \frac{1}{1+a_{i}}= \sum_{i=2}^{2^{k}} \frac{1}{1+a_{i}}+\sum_{n=2^{k}+1}^{2^{k+1}} \frac{1}{1+a_{i}}
$$
$$
 \ge 2^{k}\left( \frac{1}{1+\sqrt[2^{k}]{a_{1}a_{2}\dots a_{2^{k}}  }}+\frac{1}{1+\sqrt[2^{k}]{ a_{2^{k}+1} a_{2^{k}+2}\dots a_{2^{k+1}}}}  \right)
$$
$$
 \ge 2^{k} \frac{2}{1+\sqrt[2^{k+1}]{a_{1}a_{2}\dots a_{2^{k+1}}  }}
$$
Where the first inequality follows from the induction hypothesis, and the second is the base case.
Now we have to cover the cases in which $n$ is not a power of $\hspace{0pt}2$. We do the induction backward, namely, we assume that the inequality holds for $n+1$ numbers and prove it for $n$.
Let $a_{1}a_{2},\dots,a_{n}$ be some real numbeers greater than one. Attach to them the number $a_{n+1}=\sqrt[n]{a_{1}a_{2}\dots a_{n}  }$. When writing out the inequality for these $n+1$ numbers, we obtain
$$
\frac{1}{1+a_{1}}+\dots+\frac{1}{1+\sqrt[n]{a_{1}a_{2}\dots a_{n}  }}\ge \frac{n+1}{1+\sqrt[n+1]{a_{1}a_{2}\dots a_{n}\sqrt[n]{a_{1}a_{2}\dots a_{n}  }  }}
$$
Then we can reorganise $\sqrt[n+1]{a_{1}a_{2}\dots a_{n}\sqrt[n]{a_{1}a_{2}\dots a_{n}  }}=\sqrt[n]{a_{1}a_{2}\dots a_{n}  }$. After cancelling the last term on the left, we obtain
$$
\frac{1}{1+a_{1}}+\frac{1}{1+a_{2}}+\dots+\frac{1}{1+a_{n}}\ge \frac{n}{1+\sqrt[n]{ a_{1}a_{2}\dots a_{n} }}
$$
As desired. The inequality is now proved, sine we can reach any positive integer $n$ by starting with a sufficiently large power of $2$ and working backwards.


#Mathematics #Logic 