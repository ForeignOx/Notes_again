## Definition
A subring $S$ of a [[Rings|ring]] $(R,+,\cdot)$ is a is a [[Subsets|subset]] $S\subseteq R$ such that:
- $0 \in S$, $1\in S$
- $a,b\in S\implies a+b\in S$
- $a,b\in S\implies ab\in S$
- $a\in S\implies -a\in S$
Note that a subring is a ring
### Examples
$\mathbb{Z}\subseteq \mathbb{Q}$, $\mathbb{R}\subseteq \mathbb{C}$, $\mathbb{Q}\subseteq \mathbb{Q}[x]$
___
Show that $\mathbb{Z} [\sqrt{ 2 }]=\left\{ a+b\sqrt{ 2 } \middle| a,b\in\mathbb{Z} \right\}$ is a ring.
A lengthy way of doing this is to check all the ring axioms. A quicker way is to check that it is a rubring of $\mathbb{R}$.
Property $\hspace{0pt}1$ is true since $0,1\in \mathbb{Z}[\sqrt{ 2 }]$, to show properties 2,$\hspace{0pt}3$,$\hspace{0pt}4$:
$$
(a+b\sqrt{ 2 })+(c+d\sqrt{ 2 })=a+c+(b+d)\sqrt{ 2 }
$$
$$
 (a+b\sqrt{ 2 })(c+d\sqrt{ 2 })=(ac+2bd)+(ad+bc)\sqrt{ 2 }
$$
$$
-(a+b\sqrt{ 2 })=-a-b\sqrt{ 2 }
$$
Since all of $a+c,b+d,ac+2bd,ad+bc,-a,-b\in \mathbb{Z}$ $\mathbb{Z} /2$ is thus a subring of $\mathbb{R}$. We don't have to check associativity or distributivity, as these follow from the corresponding known properties in $\mathbb{R}$.
___
Consider the ring $\mathbb{Z} /6$. It has $R=\left\{ \overline{0},\overline{2},\overline{4} \right\}$ as a subset? Is $R$ a subring? No, as $\overline{1} \not\in R$. Curiously however, it is still a ring: $\overline{4}$ functions as its multiplicative identity:
$$
\overline{4}\cdot \overline{0}=\overline{0}
$$
$$
 \overline{4}\cdot \overline{2}=\overline{8}=\overline{2}
$$
$$
 \overline{4}\cdot \overline{4}=\overline{16}=\overline{4}
$$
Actually $R$ is [[Isomorphisms|isomorphic]] to $\mathbb{Z} /3$. Indeed we set up a bijective map $R\to \mathbb{Z} /3$:
$$
[0]_{6}\mapsto [0]_{3}\in \mathbb{Z} /3
$$
$$
 [2]_{6}\mapsto [2]_{3}
$$
$$
 [4]_{6}\mapsto[1]_{3}
$$
It is a homomorphism since it is additive and multiplicative, which we can check directly, for example:
$$
[2]_{6}+[2]_{6}=[4]_{6}\mapsto [1]_{3}=[2]_{3}+[2]_{3}
$$
It is clearly a bijection by definition, since each of the three distinct elements are mapping to each of the other three distinct elements, thus $R\cong \mathbb{Z}/3$


