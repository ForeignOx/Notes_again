Consider $n\in\mathbb{N}$, $a,b\in\mathbb{R}$, then:
$$
(a+b)^{n}=\sum_{ r=0} ^{ n}  \begin{pmatrix}
n\\r
\end{pmatrix}a^rb^{n-r}
$$
## Proof
By [[Proof by Mathematical Induction!!!!!|mathematical induction]]
For $n=1$:
$$
\sum_{r=0}^{1}\begin{pmatrix}
1\\r
\end{pmatrix}a^{1-r}b^{r}=a+b
$$
So is true for $n=1$ 
Assume true for $n\in\mathbb{N}$:
$$
(a+b)^{n+1}=(a+b)(a+b)^{n}=(a+b)\sum_{ k=0}^{ n} \begin{pmatrix}
n\\k
\end{pmatrix}  a^{n-k}b^{k}
$$
$$
= \sum_{ k=0} ^{ n}  \begin{pmatrix}
n\\k
\end{pmatrix}a^{n+1-k}b^{k}+\sum_{ k=0} ^{ n}  \begin{pmatrix}
n\\k
\end{pmatrix}a^{n-k}b^{k+1}
$$
$$
 = a^{n+1}+b^{n+1}+\sum_{ k=1} ^{ n}a^{n+1-k}b^{k}+  \sum_{ k=1} ^{ n}  \begin{pmatrix}
n\\k-1
\end{pmatrix}a^{n+1-k}b^{k}
$$
$$
=a^{n+1}+b^{n+1} \sum_{ k=1} ^{ n}  \left( \begin{pmatrix}
n\\ k
\end{pmatrix}+\begin{pmatrix}
n\\k-1
\end{pmatrix} \right)a^{n+1-k}b^{k}
$$
$$
= \sum_{ k=0} ^{ n+1}  \begin{pmatrix}
n+1\\k
\end{pmatrix}a^{n+1-k}b^{k}
$$
## Examples
Prove for integer $n\geq 0$
$$
\sum_{ k=0} ^{ n}\begin{pmatrix}
n\\k
\end{pmatrix}=2^{n}  
$$
For $n\geq 1$
$$
\sum_{ k=0} ^{ n}\begin{pmatrix}
n\\k
\end{pmatrix}(-1)^{k}=0
$$
For $n\geq 0$
$$
\sum_{ k=0} ^{ n}\begin{pmatrix}
n\\k
\end{pmatrix}2^{k}=3^{n}  
$$
$$
\sum_{ k=0} ^{ n}\begin{pmatrix}
n\\k
\end{pmatrix}k=n\times 2^{n-1}
$$
To solve these, we can consider the binomial theorem in the form:
$$
(1+x)^{n}=\sum_{k=0}^{n}\begin{pmatrix}
n\\k
\end{pmatrix}x^{k}
$$
For the first one, let $x=1$,
$$
(1+1)^{n}=\sum_{ k=0} ^{ n}  \begin{pmatrix}
n\\k
\end{pmatrix}=2^{n}
$$
For the second, let $x=-1$
$$
(1-1)^{n}=\sum_{ k=0} ^{ n}  \begin{pmatrix}
n\\k
\end{pmatrix}(-1)^{k}=0
$$
For the third, let $x=2$
$$
(1+2)^{n}=\sum_{ k=0} ^{ n}  \begin{pmatrix}
n\\k
\end{pmatrix}2^{k}=3^{n}
$$
For the fourth, the trick is to differentiate both sides with respect to $n$:
$$
n(1+x)^{n-1}=\sum_{k=0}^{n}\begin{pmatrix}
n\\k
\end{pmatrix}kx^{k-1}
$$
Now let $x=1$
$$
n(1+1)^{n-1}=\sum_{k=0}^{n}\begin{pmatrix}
n\\k
\end{pmatrix}k=n 2^{n-1}
$$
## Extended Theorem
For integers $n$ and $k$ with $0\leq k\leq n$ we saw that
$$
\begin{pmatrix}
n\\k
\end{pmatrix}
$$
is the coefficient of $x^{k}$ in $(1+x)^{n}$ which expands to give the polynomial
$$
\sum_{ k=0} ^{ n}\begin{pmatrix}
n\\k
\end{pmatrix}x^{k}
$$
We extend the definition to allow any real number $n$ which we will instead call $\alpha \in\mathbb{R}$
We define
$$
\begin{pmatrix}
\alpha\\k
\end{pmatrix}
$$
to be the coefficient of $x^{k}$ in the expansion $(1+x)^{\alpha}$ as a (possibly infinite) power series in $x$ around $x=0$:
$$
(1+x)^{a}=\begin{pmatrix}
\alpha\\0
\end{pmatrix}x^{0}+\begin{pmatrix}
\alpha\\1
\end{pmatrix}x^{1}+\begin{pmatrix}
\alpha\\2
\end{pmatrix}x^{2}+\dots+\begin{pmatrix}
\alpha\\k
\end{pmatrix}x^{k}+\dots=\sum_{ k=0} ^{\infty}\begin{pmatrix}
\alpha\\k
\end{pmatrix}x^{k}  
$$
Where using [[Taylor Series|Maclaurin's theorem]], for $\alpha \in\mathbb{R}$ and integer $k\geq 0$ we define
$$
\begin{pmatrix}
\alpha\\k
\end{pmatrix}:=\frac{\alpha(\alpha-1)\dots(\alpha-k+1)}{k!}
$$
Note that if $\alpha \in\mathbb{Z}^+$, then
$$
\begin{pmatrix}
\alpha\\k
\end{pmatrix}=\frac{\alpha!}{k!(\alpha-k)!}
$$
If $\alpha \in\mathbb{Z}^+$ and $k>\alpha$, then
$$
\begin{pmatrix}
\alpha\\k
\end{pmatrix}=0
$$
Since the power series terminates after finitely many terms (it is a polynomial of degree $\alpha$)
In general, if $\alpha$ is not an integer, then the numberator includes no $\hspace{0pt}0$, so
$$
\begin{pmatrix}
\alpha\\k
\end{pmatrix}\neq 0
$$
And the power series for $(1+x)^{\alpha}$ has infinitely many terms
### Principle of Upper Negation
If $n$ and $k$ are positive integers, then:
$$
\begin{pmatrix}
-n\\k
\end{pmatrix}=(-1)^{k}\begin{pmatrix}
n+k-1\\k
\end{pmatrix}=(-1)^{k}\begin{pmatrix}
n+k-1\\n-1
\end{pmatrix}
$$
Note the similarity to [[Ordered Grouping of Indistinguishable Objects]]
### Proof
$$
\begin{pmatrix}
-n\\k
\end{pmatrix}=\frac{(-n)(-n-1)(-n-2)\dots(-n-k+1)}{k!}
$$
$$
= (-1)^{k} \frac{n(n+1)(n+2)\dots(n+k-1)}{k!}
$$
$$
= (-1)^{k} \frac{(n+k-1)!}{(n-1)!k!}
$$
Which is the claimed result
___
This means that for positivee integers $n$,
$$
(1+x)^{-n}=\sum_{ k=0} ^{\infty}{-n \choose k }x^{k}=\sum_{ k=0} ^{\infty} (-1)^{k} {k+n-1 \choose  n-1}  x^{k}
$$
And taking $x=-y$, we obtain:
$$
(1-y)^{-n}=\sum_{ k=1} ^{\infty}  {k+n-1 \choose n-1 }y^{k}
$$

#Mathematics #Discrete #Theorem 