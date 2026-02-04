We also want a name for the "nice" rings that don't have non-[[Zero Divisors|zero divisors]]
## Definition
A [[Rings|ring]] $R$ which is commutative, has at least two elements and does not have any zero-divisors apart from $\hspace{0pt}0$, is called an integral domain.
The essential property of an integral domain is cancellation;
$$
ax=bx,x\neq 0 \implies a=b
$$
Which is not the same as dividing, this may hold even if $x$ is not invertible
## Examples
[[Integers|$\mathbb{Z}$]] is an integral domain, as is any [[Fields|field]], or any subring of a field
___
Is [[Integers Modulo n|$\mathbb{Z} / 3$]] an integral domain?
Yes, it is a field even, but you can also see this from the multiplication table
Is $\mathbb{Z} / 4$ an integral domain?
No, since $\overline{2}\cdot \overline{2}=\overline{0}$
We can tell exactly when $\mathbb{Z} /n$ is an integral domain:
## Lemma
$\mathbb{Z} /n$ is an integral domain iff $n$ is a prime
### Proof
Suppose that $\mathbb{Z} / n$ is an integral domain and that $n$ is not prime, then $n=ab$, $a,b\in \mathbb{Z}$, $2\leq a,b\leq n-1$, thus $\overline{a}\overline{b}=\overline{n}=\overline{0}\in\mathbb{Z} /n$, so $\overline{a}$ and $\overline{b}$ are zero divisors
Conversely, suppose $n$ is prime, and that $\overline{a}\in \mathbb{Z}/n$ is a zero divisor, then there exists $\overline{b}\neq \overline{0}$ such that $\overline{a}\overline{b}=0$ thus $n|ab$, so $n|a$ or $n|b$, as $n$ is prime, in other words, $\overline{a}=\overline{0}$ or $\overline{b}=\overline{0}$, but we have said that $\overline{b}\neq 0$, so $\overline{a}= \overline{0}$, thus $\overline{0}$ is the only divisor, so the ring is an integral domain
## Proposition
If $R$ is an integral domain, then [[Polynomials|$R[x]$]] is also an integral domain.
### Proof
$R[x]$ is commutative and $1\neq 0$, by definition of the ring, by definition, we need to show that $R[x]$ has no non-zero divisors
We assume the opposite, for a contradiction, i.e. that there exist $f(x),g(x)\in R[x]$ where $f(x),g(x)\neq 0$ such that $f(x)g(x)=0$. We write
$$
f(x)=a_{0}+a_{1}x+\dots+a_{m}x^{m},m=\deg f \ge 0,a_{m}\neq 0
$$
$$
 g(x)=b_{0}+b_{1}x+\dots+b_{n}x^{n},n=\deg g\ge 0,b_{n}\neq 0
$$
If we expand $f(x)g(x)$, the leading term, of degree $n+m$ is $a_{m}b_{n}x^{m+n}$, the product being zero implies that $a_{m}b_{n}$ must be $\hspace{0pt}0$, but since neither of them are $\hspace{0pt}0$, and $R$ is an integral domain gives a contradiction.