Consider [[Integers|$\mathbb{Z}$]] with operation $+$, identity $0$. This is an infinite [[Abelian Groups|abelian]] [[Groups|group]]
Fix an integer $n\in\mathbb{N}$, with $n\geq 2$, then consider the [[Equivalence Relation|equivalence relation]] on $\mathbb{Z}$: $p\sim q\iff n|(p-q)$; $n$ divides $p-q$; $p=q+nk,k\in\mathbb{Z}$, then
$$
[p]=\left\{ q\in \mathbb{Z}:\middle|:p \sim q \right\}
$$
This is a congruence class of the integers modulo $n$, then we define addition via
$$
[p]+[q]=[p+q]
$$
The set $\mathbb{Z}_{n}=\left\{ [0],[1],\dots,[n-1] \right\}=\frac{\mathbb{Z}}{n\mathbb{Z}}$ forms a finite abelian group of order $n$ under addition modulo $n$, and is called the cyclic group of order $n$. This can also be thought of as roots of unity and rotations
In $\mathbb{Z}_{n}$, everything has finite order
Cyclic groups are [[Subgroups|subgroups]] of [[Dihedral Groups|dihedral groups]] and [[Symmetric Groups|symmetric groups]]
In the cyclic group $\mathbb{Z} /p$, any element except $\overline{0}$ has order $p$
## Lemma
If $G$ is a finite cyclic group of order $n$, $G=\left< x \right>$, then
- $\text{ord}(x^{a})=\frac{n}{\gcd(a,n)}$
- $\left< x^{a} \right>=\left<  x \right>$ iff $\gcd(a,n)=1$


#Mathematics #Group #Definition