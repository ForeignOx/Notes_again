## Theorem
Let $R$ be $\mathbb{Z}$ or $\mathbb{F}[x]$ for $\mathbb{F}$ a [[Fields|field]] and let $a\in R$ be a non-zero element, then $a$ can ve factorised uniquely into a product of irreducible elements, up to order of the factors and units
### Proof (Existance of Factorisation)
We work by [[Proof by Mathematical Induction!!!!!|induction]] on $d(a)$, the degree function
Notice that the units of $R^{\times}=\left\{ a\in R\mid d(a)=d(1) \right\}$ and that $d(1)$ is the smallest value of $d$
Base case: 
If $d(a)=d(1)+1$, then $a$ is either $\pm 2$ (for $\mathbb{Z}$) or linear, non-constant polynomials (for $\mathbb{F}[x]$), hence is irreducible.
Induction step:
Assume that we have a factorisation into irreducibles for all $x\in R$ such that $d(1)<d(x)<d(a)$. If $a$ is irreducible, we are done. If not, $a=bc$ for $b,c\in R$, such that $d(b)>d(1),d(c)>d(1)$. By assumption, (since $d(b),d(c)<d(a)$) both $b$ and $c$ have factorisations into irreducibles, and putting these together, we get a factorisation of $a$
### Proof (Uniqueness)
Suppose $a=p_{1}p_{2}\dots p_{m}=q_{1}q_{2}\dots q_{n}$ where all $p_{i},q_{i}$ are irreducible and without loss of generality, we can assume $m\geq n$
Then $p_{1}|q_{1}\dots q_{n}$, so $p_{1}$ divides one of the factors $q_{i}$ by [[Irreducibles#Lemma|this lemma]], so by rearranginng, without loss of generality, we can say $p_{1}|q_{1}$, i.e. $q_{1}=p_{1}u_{1},u_{1}\in R$. But $p_{1}$ and $q_{1}$ are both irreducible, $u_{1}$ must be a unit
Thus 
$$
p_{1}p_{2}\dots p_{m}=p_{1}u_{1}q_{2}\dots q_{n}
$$
so after cancelling,
$$
p_{2}\dots p_{m}=uq_{2}\dots q_{n}
$$
Repeating the argument with $p_{2},\dots p_{m}$, we obtain
$$
p_{n+1}\dots p_{m}=u_{1}\dots u_{m}
$$
This implies $p_{n+1}$ divides one of the units $u_{i}$. This is impossible, as it implies that $u_{i}=p_{n+1}x$, for some $x\in R$, which implies that also $p_{n+1}$ is a unit, which it isn't, since it is irreducible
The only possibility, is therefore that $m=n$, so $1=u_{1}\dots u_{m}$, which means that up to reordering and multiplication by units $u_{i}$, the factorisations are the same
