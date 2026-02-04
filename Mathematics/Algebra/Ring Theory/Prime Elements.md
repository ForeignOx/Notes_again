## Definition
Let $R$ be a commutative [[Rings|ring]], an element $x\in R$ is called prime (or a prime element) if:
- $x\neq 0$, and $x \not\in R^{\times}$ ($x$ is not a [[Units|unit]])
- If $x|ab$, for $a,b\in R$, then $x|a$ or $x|b$
## Remark
The usual definition of prime numbers in [[Integers|$\mathbb{Z}$]] is as a positive [[Irreducibles|irreducible]] element, but we know that an irreducible element in $\mathbb{Z}$ or $\mathbb{F}[x]$ is prime
For the other direction, we have something even more general: 
## Lemma
Let $R$ be an [[Integral Domains|integral domain]] and $x \in R$ is a prime element, then $x$ is irreducible
### Proof
We first note that $x\neq 0$ or a unit by definition of prime. Assume that $x=ab$, for $a,b \in R$, so we need $a$ is a unit or $b$ is a unit. By definition off prime elements, since $x| ab$, $x|a$ or $x|b$. WLOG assume that $x|a$, then $a=rx$ for some $r \in R$ and so
$$
x=rxb
$$
SInce $R$ is an integral domain, we can cancel $x$ on both sides
$$
1=rb
$$
So $b$ is a unit and $x=ab$ is not a proper factorisation
## Examples
Consider the ring $N:\mathbb{Z}[\sqrt{ -5 }]\to \mathbb{Z}$, $N(a+b\sqrt{ -5})=a^{2}+5b^{2}=Z \overline{Z}$
Thus $N(xy)=(xy)(\overline{xy})=x\overline{x}y\overline{y}=N(x)N(y)$ 
We show that $2$ is irreducible (igf $2=(x+y\sqrt{ -5 })(z+w\sqrt{ 5 })$), for $x,y,z,w\in \mathbb{Z}$, then
$$
N(2)=4=N(x+y\sqrt{ 5 })N(2+m\sqrt{ -5 })
$$
We know that $N(x+y\sqrt{ -5 })$ divides $\hspace{0pt}4$, so equals $\hspace{0pt}1$,$\hspace{0pt}2$, ]or $\hspace{0pt}4$ (it can't be $<0$)
 

| $x^{2}+5y^{2}$ |                                                                                                          |                                                                                |
| -------------- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| 1              | $y=0$ (if $y\neq 0$, then $\left\| y \right\|\geq 1$, so $\left\| x^{2}+5y^{2} \right\|>1$)<br>$x=\pm 1$ | $x+y\sqrt{ -5 }=\pm 1$ which is a unit                                         |
| 2              | $y=0$, $x^{2}=2$, which is impossible as $x\in \mathbb{Z}$                                               |                                                                                |
| 4              | $y=0$,$x^{2}=4\implies x=\pm 2$                                                                          | $2=\pm 2(z+w\sqrt{ -5 })$<br>$\implies 1=\pm (z+w\sqrt{ -5) }$ which is a unit |

Hence $2$ is irriducible. But $2$ is not a prime element, as $2|(1-\sqrt{ -5 })(1+\sqrt{ -5 })=6$ but $2$ doesn't divide either factor $2 \nmid 1\pm \sqrt{ -5 }$, because if it did
$$
1\pm \sqrt{ -5 }=2(a+b\sqrt{ -5 })=2a+2b\sqrt{ -5 }
$$
Which would imply $1=2a$, which is not possible for $a\in \mathbb{Z}$.
In a sense, the failure here of irreducible elements being prime is due to the fact that $\mathbb{Z}[\sqrt{ -5 }]$ lacks unique factorisation :(( since, as we've seen $(1+\sqrt{ -5 })(1-\sqrt{ -5 })=6=2\cdot3$
Though to show that these are two genuinely different factorisations, we also need that none of the irreducible factors is a unit times another
