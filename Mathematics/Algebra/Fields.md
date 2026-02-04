## Definition
A [[Rings|ring]] $(R,+,\cdot)$ is called a field if:
- $R$ is commutative
- $1\neq 0$ (i.e. $R$ has at least two elements)
- For every $a\in R$, such that $a\neq 0$, $\exists b\in R:ab=1$ ($b$ is called the inverse of $a$, denoted $a^{-1}$)
## Uniqueness of Inverses:
If $ab=1$ and $ab'=1$, then 
$$
b'=abb'=bab'=b
$$
## Fields as Quotients
We have seen that if $R$ is commutative and $I\subseteq R$ is a maximal [[Ideals|ideal]], then $R /I$ is a field. Moreover, if $a\in R$ is irreducible and $R$ is a [[Principle Ideal Domains|principle ideal domain]], then $(a)$ is a maximal ideal
Thus, in this case, $R /(a)$ is a field, e.g.
$$
\mathbb{R}[x] /(x^{2}+1) \cong \mathbb{C}
$$
$$
\mathbb{Q}[x] /(x^{2}-2) \cong \mathbb{Q}[\sqrt{ 2 }]
$$
Recall from linear algebra that [[Vectorspaces|vectorspaces]] can be defined over any field
### Theorem
Let $\mathbb{F}$ be a field and $f(x)\in \mathbb{F}[x]$ be any irreducible [[Polynomials|polynomial]], then $\mathbb{F}[x] /(f(x))$ is a field, and is a vectorspace over $\mathbb{F}$ with [[Basis|basis]] $B:=\left\{ \overline{1},\overline{x},\overline{x^{2}},\dots,\overline{x^{n-1}} \right\}$, where $n=\deg f$. That is, every element in $\mathbb{F}[x] /(f(x))$ can be written uniquely as
$$
\overline{a_{0}+a_{1}x+\dots+a_{n-1}x^{n-1}}
$$
For $a_{i}\in \mathbb{F}$
#### Proof
By the above discussion, $\mathbb{F}[x] /(f(x))$ is a field, and is a vectorspace over $\mathbb{F}$, as it is an abelilan group, with scalar multiplication given by:
$$
\alpha\cdot (\overline{g(x)}):=\overline{\alpha g(x)}\forall \alpha \in  \mathbb{F}
$$
We can check that this is a vectorspace by checking all the axioms, but that's boring as hell.
The set $B$ spans $\mathbb{F}[x] /(f(x))$: by division with remainder, any $g(x)\in \mathbb{F}[x]$ with $\deg g>n$ can be written $g(x)=q(x)f(x)+r(x)$ with $\deg r<n$, so 
$$
\overline{g(x)}=\overline{q(x)f(x)+r(x)}=\overline{r(x)}
$$
Since the span of $B$ contains any polynomial in $\overline{x}$ of degree at most $n-1$, it will contain $\overline{r(x)}$ and hence $\overline{g(x)}$, so it works for all elements.
Finally $B$ is linearly independent: This is equivalent to 
$$
\sum_{i=0}^{n-1}a_{i}  \overline{x}^{i}= \overline{0}
$$
Then all $a_{i}$ should be zero if $\sum a_{i} \overline{x}^{i}=\overline{0}$, then $\sum a_{i}x^{i}\in I=(f(x))$, so $f(x)$ divides $\sum a_{i}x^{i}$, hence $\deg f=n\leq n-1$, which is a contradictiton unless $a_{1}=a_{2}=\dots=a_{n-1}=0$, so $B$ is a basis
### Example
$\mathbb{Q}[x] /(x^{3}-2)$ has basis $\left\{ 1,\overline{x},\overline{x^{2}} \right\}$, which means it has dimension 3
___
$(\mathbb{Z}/2) /(x^{2}+x+\overline{1})$ has basis $\left\{ \overline{1},\overline{x}\right\}$ with [[Dimension|dimension]] $\hspace{0pt}2$ over $\mathbb{Z} /2$, i.e. this field has $2^{2}$ elements $\left\{ \overline{0},\overline{1},\overline{x},\overline{1+x} \right\}$
This field is denoted $\mathbb{F}_{4}$
## Finite Fields
We already know that $\mathbb{Z} /p$ is a field with $p$ elements for each prime number $p$
We know
$$
\mathbb{Z} /n= \mathbb{Z} /(n)=\mathbb{Z} /n\mathbb{Z}
$$
Warning: $\mathbb{Z} /p^{n}$ for $n>1$ must not be a field (it has [[Zero Divisors|zero divisors]]). Thus $\mathbb{Z} /4 \not\cong \mathbb{F}_{4}$ 
### Theorem
For any prime $p \in\mathbb{Z}$, $n\in \mathbb{N}$, there exists a polynomial $f(x)\in(\mathbb{Z} /p)[x]$ of degree $n$ that is [[Irreducibles|irreducible]]. Thus $(\mathbb{Z} /p)[x] /(f(x))$ is a field with $p^{n}$ elements. Any two such fields with $p^{n}$ elements are isomorphic and we denote this by $\mathbb{F}_{p^{n}}$ 
### Example
Construct $\mathbb{F}_{27}$. Firt we find an irreducible polynomial in $(\mathbb{Z} /3)[x]$ of degree $\hspace{0pt}3$. Can take 
$$
f(x)=x^{3}+x^{2}+x+ \overline{2}
$$
Thus by our theorem, we have
$$
\mathbb{F}_{27}\cong (\mathbb{Z} /3)[x] /(f(x))
$$
And its elements can be written as $\overline{ax^{2}+bx+c}$
Calculating with elements in $\mathbb{F}_{27}$, we need to remember $\overline{x^{3}+x^{2}+x+\overline{2}}=\overline{0}$, for example
$$
(\overline{2}\overline{x}^{2}-\overline{x}+\overline{2})(\overline{x}^{2}+\overline{x}+1)=\overline{2}\overline{x}^{4}+\overline{x}^{3}+\overline{x}+\overline{ 2}
$$
$$
= \dots
$$