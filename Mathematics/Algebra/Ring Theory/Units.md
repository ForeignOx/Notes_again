$\pm 1$ in [[Integers|$\mathbb{Z}$]] and nonzero constant polynomials in [[Polynomials|$\mathbb{F}[x]$]] respectively have the property in common of being precisely the invertible elements in the [[Rings|ring]]
## Definition
Let $R$ be a ring, an element $a\in R$ is said to be invertible or a unit if $\exists b\in R$ such that $ab=ba=1$, then $b$ is the inverse, $a^{-1}$
The [[Sets|set]] of units in $R$ is denoted $R^{\times}$
If $u$ is a unit, its inverse is unique using the same argument as for fields
## $R^{\times}$ Forms a [[Groups|Group]]
$R^{\times}$ forms a group under multiplication in $R$, since if $a,b\in R^{\times},ab\in R^{\times}$ because $(ab)(b^{-1}a^{-1})=1$, and all the other axioms can be checked
## Examples
In $\mathbb{Z}$ we of course have $\pm 1$, and in $\mathbb{F}[x]$, we have
$$
\mathbb{F}[x]^{\times}=\left\{ \text{non-zero constants} \right\}=\mathbb{F}\setminus \left\{ 0 \right\}=\mathbb{F}^{\times}
$$
Because if $a(x)\in \mathbb{F}[x]$ has an inverse, then $a(x)b(x)=1$, which implies $\deg a+\deg b=0$, so the only possibilty is $\deg a=0$
___
If $R=M_{n}(\mathbb{F})$, for a [[Fields|field]] $\mathbb{F}$, then $R^{\times}=\left\{ X \in M_{n}(\mathbb{F})\mid \det(X)\neq 0 \right\}$, also known as the [[General Linear Group|general linear group]], $GL_{n}(\mathbb{F})$
___
Units in [[Integers Modulo n|$\mathbb{Z} / n$]]:
An element $\bar{a}\in\mathbb{Z} / n$ is a unit iff $\gcd(a,n)=1$;
$$
(\mathbb{Z} /n)^{\times}=\left\{ \bar{a}\in  \mathbb{Z} / n\mid \gcd(a,n)=1 \right\}
$$
#### Proof
Let $d=\gcd(a,n)$, then $d|a$ and $d|n$. First suppose that $\bar{a}$ is a unit. Let $\bar{b}=\bar{a}^{-1}$, which means that $ab\equiv 1 \mod n$. This in turn is equivalent to $ab-1=nx$, for some $x\in \mathbb{Z}$. Thus $1=ab-nx$, and since $d|a$ and $d|n$, $d|RHS$, so $d|1$, implying $d=1$
Conversly assume that $d=1$, by the [[Euclidean Algorithm|Euclidean algorithm]], $\exists x,y \in \mathbb{Z}$ such that $xa+ny=1$.
This implies that $xa \equiv 1 \mod n$ which in turn implies that $\overline{xa}=\overline{1}$ in $\mathbb{Z} /n$, hence $\bar{a}$ is a unit
#### Corollary
As a consequence, we get that $\mathbb{Z} /p$ is a field iff $p$ is a prime
##### Proof
We prove first that if $p$ is a prime, then $\mathbb{Z} / p$ is a field
If $p$ is a prime, then by the proof above, every element $\overline{1},\overline{2},\dots,\overline{p-1}$ is a unit, so all elements in $\mathbb{Z} /p$, except $\overline{0}$, are units
Conversly ..

