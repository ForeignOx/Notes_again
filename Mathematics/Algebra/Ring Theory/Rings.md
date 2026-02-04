## Examples
- The [[Integers|integers]] are an example of a ring as you can add, subtract and multiply and stay within the ring 
- The [[Rational Numbers|rational numbers]] are also an exaple of a ring for the same reason, as are the [[Real Numbers|real numbers]] and the [[Complex Numbers|complex numbers]]. For these we can also divide, giving some extra structure
- [[Polynomials|Polynomials]], such as $\mathbb{Q}[x]=\left\{ a_{0}+a_{1}x+\dots+a_{n}x^{n}\mid a_{i}\in\mathbb{Q} \right\}$
- [[Matrices]], such as $M_{n}(\mathbb{Q})=\left\{ n\times n\text{ matrices with entries in }\mathbb{Q} \right\}$ we can add/subtract/multiply matrices.
- [[Functions|Functions]] are also rings, such as $C(\mathbb{R})=\left\{ f:\mathbb{R}\to \mathbb{R}\mid f\text{ is continuous} \right\}$. We can add/subtract and multiply functions: $(f\pm g)(x)=f(x)\pm g(x)$, $(f\cdot g)(x)=f(x)g(x)$

From this we can understand an informal definition of a ring to give us intuition about what they actually are: 
    A ring is a set of objects where we can add/subtract/multiply two objects while remaining in the set. If we can also divide, then it is called a field.

- A nonexample would be something like [[Natural Numbers|$\mathbb{N}$]] which is not a ring, as it does not include negatives, so you can't subtract.
- $\mathbb{R}^{3}$ is also a ring under $+$ and $\times$? The answer is no, because there are vectors such that $\underline{u}\times(\underline{v}\times \underline{w})\neq (\underline{u}\times \underline{v})\times \underline{w}$, and that's a key feature of what we deem multiplication; this missing property is called associativity

## Definition
For a [[Sets|set]] $R$ to be a ring, we need two [[Binary Operations|binary operations]], usually written $+,\times$ 
A ring is a triple $(R,+,\cdot)$ such that $(R,+)$ is an [[Abelian Groups|abelian group]] and such that:
- $\exists 1\in\mathbb{R}: 1\cdot x=x\cdot1=x\forall x\in R$ (identity) - some definitions don't require this, but it is more convenient and useful to do so.
- $x(yz)=(xy)z,\forall x,y,z\in R$ (associativity)
- $x(y+z)=xy+xz$ and $(y+z)x=yx+zx$ (distributivity) - note that this stipulation is because the multiplication doesn't necessarily need to be commutative
Note that we can always subtract as $(R,+)$ is abelian which implies that for any $x\in R$, $-x\in R$, so we can define subtraction as $x-y:=x+(-y)$.
## Degree Function
We want a way of comparing size in arbitrary [[Rings|rings]] for things such as remainders, so we define the degree function:
$$
d:R\setminus \left\{ 0 \right\}\to \mathbb{N}\,(R=\mathbb{Z}\text{ or }\mathbb{F}[x])
$$$$
d(a):=\begin{cases}
\left| a \right|  & \text{if }a\in \mathbb{Z} \\
\deg a & \text{if }a\in \mathbb{F}[x]
\end{cases}
$$
## General Divisibility
Using our degree function, we can write a general divisiblity rule:
Let $R$ be either $\mathbb{Z}$ or $\mathbb{F}[x]$, then for any $a,b\in R,b\neq 0,\exists q,r\in R$ such that $a=qb+r$ with $r=0$ or $d(r)<d(b)$
## Lemma
Let $R$ be either $\mathbb{Z}$ or $\mathbb{F}[x]$, if $a,b\in R$ such that $a|b$, then $d(a)\le d(b)$
### Proof
$a|b$ means $b=am$ for some $m\in R$, then
$$
d(b)=d(am)=\begin{cases}
\left| a \right| \left| m \right| \ge \left|  a \right|  & \text{for }\mathbb{Z} \\
d(a)+d(m)\ge d(a) & \text{for }\mathbb{F}[x]
\end{cases}
$$