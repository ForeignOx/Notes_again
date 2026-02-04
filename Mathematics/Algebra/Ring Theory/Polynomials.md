## Definition
For some [[Fields|field]] $\mathbb{F}$, we define the [[Sets|set]] $\mathbb{F}[x]$ as
$$
\mathbb{F}[x]=\left\{a_{0}+a_{1}x+\dots+a_{n}x^{n}\mid a_{0},a_{1},\dots,a_{n}\in  \mathbb{F}  \right\}
$$
Which is the set of polynomials
A polynomial is called monic if its leading coefficient is 1.
## Degree of Polynomial
For $f(x)=a_{0}+a_{1}x+\dots+a_{n}x^{n}\in\mathbb{F}[x]$, then its degree:
$$
\deg f:=\begin{cases}
 \max\left\{ i\mid a_{i}\neq 0 \right\} & \text{if }f(x)\neq 0 \\
-\infty & \text{if }f(x)=0
\end{cases}
$$
For all $f(x),g(x)\in \mathbb{F}[x]$:
- $\deg(fg)=\deg f+\deg g$
- $\deg(f+g)\le \max\left\{  \deg f,\deg g \right\}$ (equality holds if $\deg g \neq\deg g$)
Why is $\deg(0)=-\infty$? The reason is to make sure both of the above properties hold for $f(x)=0$ or $g(x)=0$.
For example if $f(x)=0$ and $\deg 0=\deg(0\cdot g)=\deg0+\deg g$, we can't allow $\deg 0$ to lie in $\mathbb{Z}$, but it will work if $\deg0=-\infty$
## [[Divisibility|Divisibility]] on $\mathbb{F}[x]$
Let $f(x),g(x)\in \mathbb{F}[x],g(x)\neq 0$, then there exist polynomials $q(x),r(x)\in \mathbb{F}[x]$ such that
$$
f(x)=q(x)g(x)+r(x)
$$
With $\deg r<\deg g$
### Proof
If $\deg g>\deg f$, take $q(x)=0$ and $r(x)=f(x)$.
If $\deg g\le\deg f$, let
$$
f(x)=a_{0}+\dots+a_{m}x^{m},a_{m}\neq 0
$$
$$
g(x)=b_{0}+\dots+b_{n}x^{n},b_{n}\neq 0
$$
Let $d=m-n$, now we induct on $d$.
Base case:
Let $d=0$, $m=n$, Set $q(x)=\frac{a_{m}}{b_{n}}$ and $r(x)=f(x)-q(x)g(x)$. Note that $\deg r<m=\deg g$.
Inductive step:
Assume the existence of $q(x)$ and $r(x)$ for all $d<k$ for some $k\ge 0$. Now consider $d=k$, so that $m=n+k$. Let $f_{1}(x):=f(x)-\frac{a_{m}}{b_{n}}x^{m-n}g(x)$. Note that $\deg f_{1}<\deg f$, so by induction, there exist polynomials $q_{1}(x),r_{1}(x)$ such that $\deg r_{1}<\deg g$ and $f_{1}(x)=q_{1}(x)g(x)+r_{1}(x)$ thus 
$$
f(x)=f_{1}(x)+ \frac{a_{m}}{b_{n}}x^{m-n}g(x)=\underbrace{ \left( q_{1}(x)+\frac{a_{m}}{b_{n}}x^{m-n} \right) }_{ :=q(x) }g(x)+\underbrace{ r_{1}(x) }_{ :=r(x) }
$$
so the statement is true for $d=k$, hence it is true for all $d\ge 0$ by induction.
### Example
If $f(x)=x^{3}+x^{2}-3x-3$, $g(x)=x^{2}+3x+2$, then we can do long division with remainder:
![[Pasted image 20251008114933.png]]
Now $\deg f_{2}< \deg g$, so we can stop. Substituting back,
$$
f(x)=f_{1}(x)+xg(x)=f_{2}(x)-2g(x)+xg(x)
$$
$$
= (x-2)g(x)+x+2
$$
Where $x-2$ is the quotient and $x+1$ is the remainder.
## Factorisation of Polynomials
Let $\mathbb{F}$ be a field, we have seen that non-constant polynomials in $\mathbb{F}[x]$ factor uniquely into [[Irreducibles|irreducibles]]. Just like factoring integers into [[Prime Elements|prime numbers]] has many applications to pure maths and cryptography, factorising polynomials is equally important both in Galois Theory, Algebraic geometry, Coding, Polynomial equations and [[Eigenvalues|eigenvalues]] of [[Matrices|matrice]] etc
Note that whether a polynomial is irreducible depends on what our field is (e.g. $x^{2}+1$)
### Irreducible Polynomials in $\mathbb{F}[x]$
If $f(x)\in \mathbb{F}[x]$, such that $\deg f\le 4$, then there are useful ways of deciding whether $f(x)$ is irreducible
#### Proposition
- If $\deg f=1$, then $f(x)$ is irreducible
- If $\deg f=2$ or $3$, then $f(x)$ is irreducible iff $f(x)$ has no roots in $\mathbb{F}$
- If $\deg f=4$, then $f(x)$ is irreducible iff it has no roots in $\mathbb{F}$ and it is not the product of two quadratic polynomials
##### Proof
- See tutorial :eyes:
- Let $\alpha \in\mathbb{F}$ be a root of $f(x)$, we write 
$$
f(x)=q(x)(x-\alpha)+r(x),\deg r<1
$$
    Setting $x=\alpha$ we get $0=r(\alpha)$, but $r$ is a constant, so it must in fact be the zero polynomial, hence $(x-\alpha)|f(x)$, so $f(x)$ is not irreducible
    We need to show the converse holds; if it is not irreducible then $f(x)=g(x)h(x)$, where $\deg g,\deg h\ge 1$, but then $\deg f=\deg g+\deg h$, but we know that $\deg f$ is either $\hspace{0pt}2$ or $\hspace{0pt}3$, so we must have either $\deg g=1$ or $\deg h=1$. This means that WLOG, $g(x)=ax+b,a\neq 0$, hence $g\left( -\frac{b}{a} \right)=0\implies f\left( -\frac{b}{a} \right)=0$, so $f$ has the root $-\frac{b}{a}$
#### Irreducible Plynomials in $\mathbb{Q}[x]$ and $\mathbb{Z}[x]$
First note that to check whether $f(x)\in \mathbb{Q}[x]$ has a root $\alpha \in \mathbb{Q}$ such that $f(\alpha)=0$, then it is enough to clear the denominators, i.e. multiply $f(x)$ by some $d\in\mathbb{Z}$ (e.g. the product of all the denominators of the coefficients of $f(x)$) and check whether $df(x)\in \mathbb{Z}[x]$ has a root
#### The rational root test
Let $f(x)=a_{0}+a_{1}x+\dots+a_{n}x^{n}\in\mathbb{Z}[x]$ with $\deg f\geq 1$. If $f\left( \frac{p}{q} \right)=0$ for $p,q\in\mathbb{Z}$ and $\gcd(p,q)=1$, then $p|a_{0}$ and $q|a_{n}$
##### Proof
We have 
$$
f\left( \frac{p}{q} \right)=a_{0}+a_{1} \frac{p}{q}+\dots+a_{n} \left( \frac{p}{q} \right)^{n}=0
$$
Multiplying by $q^{n}$ to clear the denominators and taking out a factor of $p$:
$$
p(a_{1}q^{n-1}+a_{2}pq^{n-2}+\dots+a_{n}p^{n-1})=-a_{0}q^{n}
$$
Thus $p|a_{0}q^{n}$, and $a \nmid q^{n}$ (as $\gcd(p,q)=1$), so $p|a_{0}$
Now we shift the leading term of our original equation to the other side and multiply by $q^{n}$, we get
$$
q(a_{0}q^{n-1}+\dots+a_{n-1}p^{n-1})  =-a_{n}p^{n}
$$
Thus $q|a_{n}p^{n}$, hence (since $\gcd(p,q)=1$) $q|a_{n}$
___
We have to be carefull, because $2x+2$ is irreducible in $\mathbb{Q}[x]$, but not in $\mathbb{Z}[x]$ (because $2x+2=2(x+1)$ and $\hspace{0pt}2$ is not a unit in $\mathbb{Z}$)
### Gauss' Lemma
Let $f(x)\in\mathbb{Z}[x],\deg f\geq 1$ such that the GCD of all its coefficients is $\hspace{0pt}1$, then $f(x)$ is irreducible in $\mathbb{Z}[x]$ iff it is irreducible in $\mathbb{Q}[x]$
#### Proof
$\impliedby$: 
Assume that $f(x)$ is irreducible in $\mathbb{Q}[x]$. Let $f(x)=g(x)h(x)$ for some $g(x),h(x)\in\mathbb{Z}[x]$.
Assume that the factorisation is proper, i.e. $\deg g\geq 1,\deg h \geq 1$. Then t$f(x)=g(x)h(x)$ is also a proper factorisation in $\mathbb{Q}[x]$, contradicting irreducibility in $\mathbb{Q}[x]$
Thes either $\deg g=0$ orr $\deg h=0$, say $\deg g=0$, then we know $g(x)\in\mathbb{Z}$
If $g(x)\neq \pm 1$, then there will exist a prime number $p\in\mathbb{Z}$ dividing $g(x)$, hence dividing $f(x)$, hence dividing every coefficient of $f(x)$, violating that the $\gcd$ of the coefficients is $\hspace{0pt}1$. Thus $g(x)=\pm1$, a unit in $\mathbb{Z}[x]$, so $f(x)$ has no proper factorisation in $\mathbb{Z}[x]$, so $f(x)$is irreducivle in $\mathbb{Z}[x]$
$\implies$: omitted :((( (ffuture me can fill it in surely)
### Eisenstein's Criterion
Let $f(x)=a_{0}+a_{1}x+\dots+a_{n}x^{n}\in \mathbb{Z}[x]$ and let $p\in\mathbb{Z}$ be a prime such that $p|a_{0},p|a_{1},\dots,p|a_{n-1}$ and $p\nmid a_{n}$, and $p^{2}\nmid a_{0}$, then $f(x)$  is irreducible in $\mathbb{Q}[x]$
#### Proof
If $d=\gcd(a_{0},\dots,a_{n})\neq 1$, let $\tilde{a}_{i}:=\frac{a_{i}}{d}$, then
$$
\tilde{f}(x):=\frac{f(x)}{d}=\tilde{a}_{0}+\dots+\tilde{a}_{n}x^{n}\in  \mathbb{Z}[x]
$$
And $\gcd(\tilde{a}_{0},\dots,\tilde{a}_{n})=1$. If we show that $\tilde{f}(x)$ is irreducible in $\mathbb{Q}[x]$, then by this [[Irreducibles#Another Lemma|lemma]], we can now WLOG assume that $\gcd(a_{0},\dots,a_{n})=1$. 
Assume that $f(x)$ is not irreducible in $\mathbb{Q}[x]$, then by Gauss' Lemma, $f(x)$ is not irreducible in $\mathbb{Z}[x]$. Thus $f(x)$ can be factorised in $\mathbb{Z}[x]$ as
$$
f(x)=(b_{0}+b_{1}x+\dots b_{r}x^{r})(c_{0}+c_{1}x+\dots+c_{s}x^{x})
$$
Where $b_{i},c_{j}\in \mathbb{Z}$ and $r,s\geq 1$. Note that $r,s<n$
Comparing constant terms, $a_{0}=b_{0}c_{0}$, by hyppothesis, $p|a_{0}$, so $p|b_{0}$ or $p|c_{0}$
Without loss of generality, $p|b_{0}$, since $p^{2} \nmid a_{0}$, we must have $p\nmid c_{0}$ (!!)
Comparing leading terms $a_{n}=b_{r}c_{s}$, $p\nmid b_{r}$ (as $p\nmid a_{n}$ by assumption), now let $k$ be the least integer $0<k\leq r$ such that $p\nmid b_{k}$, i.e. $p|b_{i}$ for $i<k$ and $p\nmid b_{k}$
Expanding the above product, we get 
$$
\underbrace{ a_{k} }_{ \text{div by }p }=\underbrace{ b_{0}c_{k}+b_{1}c_{k-1}+\dots+b_{k-1}c_{1} }_{ \text{divisible by }p }+b_{k}c_{0}
$$
This implies that $p|b_{k}c_{0}$, so $p| b_{k}$ or $p|c_{0}$, but we decided that $p\nmid c_{0}$, so $p|b_{k}$, which is a contradiction
#### Example
Prove that $f(x)=x^{7}+48x-24$ is irreducible in $\mathbb{Q}[x]$
$48=3\cdot2^{4}$ and $24=3\cdot 2^{3}$, so Eisenstein's criterion with $p=3$ shows that $f(x)$ is irreducible