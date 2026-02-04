## Definition
The set of integers $\mathbb{Z}$ is given by:
$$
\mathbb{Z}=\{ n|n\in \mathbb{N}_{0} \text{ or }-n\in \mathbb{N} \}\subset \mathbb{R}
$$
$$
\mathbb{Z}=\{ \dots,-3,-2,-1,0,1,2,3,\dots \}=\{ 0,\pm1,\pm2,\dots \}
$$
A subset of the integers is the positive integers which is equivalent to the [[Natural Numbers]]:
$$
\mathbb{Z}^+=\mathbb{N}=\{ 1,2,3,4,\dots \}
$$
Another subset of the integers is the positive integers including 0:
$$
\mathbb{Z}_{0}^+=\{ 0,1,2,3,\dots \}
$$
___
## Arithmetic in $\mathbb{Z}$
### [[Divisibility|Divisibility]] in $\mathbb{Z}$
We divide with remainder in $\mathbb{Z}$. Let $a,b\in\mathbb{Z}$, $b\neq 0$. Then there exist $q,r\in\mathbb{Z}$ such that $a=q\cdot b+r$ and $0\leq r<\left| b \right|$ where $q$ is the called the quotient and $r$ is called the remainder.
#### Proof
First, we can assume that $b>0$. Indeed, if $b<0$, then we can apply the result to $-b>0$ and use $-q$ instead of $q$; this does not change $\left| b \right|$.
We define 
$$
S^{+}=\left\{ a+bk\mid k\in \mathbb{Z},a+bk\geq0 \right\}\subset S=\left\{ a+bk\mid k\in\mathbb{Z} \right\}
$$
$S^{+}$ is non-empty since both $a+b\cdot0=a\in S$ and $a+b(-a)\in S$ and one of these is always $\geq 0$, since if $a<0$, then $a+b(-a)=(-a)(b-1)\ge 0$
So by the [[Natural Numbers#Well Ordering Principle|well ordering principle]], $S^{+}$ contains a smallest element $r=a=bk$ for some $k\in \mathbb{Z}$
Also $r-b=a+b(k-1)\in S$, but this cannot lie in $S^{+}$, since $r-b<r$ and $r$ is the smallest element.
Thus $r-b<0$ because $r-b$ is in $S$, but not in $S^{+}$, so $r<b$.

#### Example
Find the quotient and remainder of $435$ divided by $43$ in $\mathbb{Z}$. Long division:
$$
435=10\cdot 43+5
$$
$5<43$, so we stop and the quotient is $\hspace{0pt}10$ and the remainder is 5.


#Mathematics #Set

