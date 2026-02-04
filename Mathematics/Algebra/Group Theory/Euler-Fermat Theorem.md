## Theorem
If we take any $a,n\in \mathbb{N}$ such that $\text{gcd}(a,n)=1$, then
$$
a^{\varphi(n)}=1 \mod n
$$
Where $\varphi(n)=\left| (\mathbb{Z} /n)^{\times} \right|$ is the [[Euler Function|Euler function]]
### Proof
$$
a^{\varphi(n)} \equiv 1 \iff \overline{a}^{\varphi(n)}=\overline{1}\in  (\mathbb{Z} /n)^{\times}
$$
And since $\left| (\mathbb{Z} /n)^{\times} \right|=\varphi(n)$, by [[Lagrange's Theorem|Lagrange's theorem]], the order of any element of $(\mathbb{Z} /n)^{\times}$ divides $\varphi(n)$, so $\text{ord}(\overline{a})m=\varphi(n)$ for some $m$
$$
\implies \overline{a}^{\varphi(n)}=\overline{a}^{m\text{ord}(\overline{a})}=(\overline{a}^{\text{ord}(\overline{a})})^{m}=\overline{1}^{m}=\overline{1}
$$
___
## Corollary
[[Fermat's Little Theorem|Fermat's little theorem]] is a corrollary of this; as for some prime $p$, $\gcd(a,p)=1$, and since $p$ is prime, $\varphi(p)=p-1$, so
$$
a^{p-1}\equiv 1\mod p\implies a^{p}\equiv a\mod p
$$
