# Group Homomorphism
## Definition
Let $(G,*)$ and $(H,\circ)$ be [[Groups]]. A group homomorphism is a [[Functions|function]] $\varphi:G\to H$ that preserves the group structure. That is, a function for which $\varphi(g_{1}*g_{2})=\varphi(g_{1})\circ \varphi(g_{2}), \forall g_{1},g_{2} \in G$ 
## Remark
$\varphi:G\to H$ is a homomorphism, then $\varphi(e)=e$
If $x^{m}=e$, then $\varphi(x)^{m}=e$
## Examples
Let $\left| G \right|=2$, so $G=\left\{ e,x \right\},\text{ord}(x)=2$
We can make a homomorphism from $G$ to [[Cyclic Groups|$\mathbb{Z}/2$]]: $\varphi:G\to \mathbb{Z} /2$, $\varphi(e)=\overline{0},\varphi(x)=\overline{1}$;
$$
\varphi(e\cdot x)=\varphi(x)=\overline{1}=\overline{0}+\overline{1}=\varphi(e)+\varphi(x)
$$
$$
 \varphi(x\cdot x)=\varphi(e)=\overline{0}=\overline{1}+\overline{1}=\varphi(x)+\varphi(x)
$$
So any group of order $\hspace{0pt}2$ is [[Isomorphisms|isomorphic]] to $\mathbb{Z} /2$
___
Let $\left|  G \right|=3$, so $G=\left\{ e,x,y \right\}$ where $\text{ord}(x)=\text{ord}(y)=3$, let $\varphi:G\to \mathbb{Z} /3$ where 
$$
\varphi(e)=\overline{0},\varphi(x)=\overline{1},\varphi(y)=\overline{2}
$$
We can see this is again an isomorphism, so we have shown that all groups of order $\hspace{0pt}3$ are iomorphic to $\mathbb{Z}/3$
___
Now we make a homomorphism from [[Dihedral Groups|$D_{n}$]], let $\varphi :D_{n}\to \mathbb{Z}/2$ where
$$
\varphi(r^{a})=\overline{0}, \varphi(r^{a}s)=\overline{1},\forall a=0,1,\dots,n-1
$$
So $\varphi(r^{a}s ^{b})=\overline{b}$
Why is this a homomorphism?
If we consider $\varphi(r^{a_{1}} s ^{b_{1}} \cdot r^{a_{2}}s ^{b_{2}})$ if $b_{1}=0$:
$$
\varphi(r ^{a_{1}}r ^{a_{2}}s ^{b_{2}})=\varphi(r ^{a_{1}+a_{2}}s ^{b_{2}})=\overline{b_{2}}
$$
$$
\varphi(r^{a_{1}})+\varphi(r^{a_{2}}s ^{b_{2}})=\overline{0}+\overline{b_{2}}=\overline{b_{2}}
$$
If $b_{1}=1$, then
$$
\varphi(r ^{a_{1}}sr^{a_{2}}s ^{b_{2}})=\varphi(r ^{a_{1}}s r^{a_{2}}sss ^{b_{2}})=\varphi(r^{a_{1}}r ^{-a_{2}}s ^{b_{2}+1})=\overline{b_{2}+1}=\overline{b_{2}}+\overline{1}
$$
$$
\varphi(r ^{a_{1}}s)+\varphi(r ^{a_{2}}s ^{b_{2}})=\overline{1}+\overline{b_{2}}
$$
So it is a homomorphism. It is not, however, an isomorphism as it is not injective, for example $\varphi(r ^{a})$ is the same for all $a$. It is however surjective
___
Take $G= \mathbb{Z} /6\to S_{3}$:
$$
\varphi(\overline{1})=\begin{pmatrix}
1 & 2 & 3
\end{pmatrix}\implies \varphi(\overline{a})=\begin{pmatrix}
1 & 2 & 3
\end{pmatrix}^{a}
$$
Why is this well-defined? We need to check $\begin{pmatrix}1 & 2 & 3\end{pmatrix}^{a+6m}=\begin{pmatrix}1 & 2 & 3\end{pmatrix}^{a}$, indeed
$$
\begin{pmatrix}1 & 2 & 3\end{pmatrix}^{a+6m}=\begin{pmatrix}
1 & 2 & 3 
\end{pmatrix}^{a}\cdot (\begin{pmatrix}
1 & 2 & 3
\end{pmatrix}^{3})^{2m}=\begin{pmatrix}
1 & 2 & 3
\end{pmatrix}^{a}
$$
$$
\varphi(\overline{a}+\overline{b})=\begin{pmatrix}
1 & 2 & 3 
\end{pmatrix}^{a+b}=\begin{pmatrix}
1 & 2 & 3 
\end{pmatrix}^{a}\begin{pmatrix}
1 & 2 & 3
\end{pmatrix}^{b}=\varphi(\overline{a})\varphi(\overline{b})
$$
It i not surjective (e.g. $\begin{pmatrix}1 & 2\end{pmatrix}\not\in \varphi(\overline{a})\forall \overline{a}\in \mathbb{Z} /6$)
It is also not injective as $\varphi(\overline{0})=\varphi(\overline{3})=e$
## Kernel and Image
Just like for linear maps, homomorphisms have kernels and images
$$
\text{ker}(\varphi)=\left\{ g\in  G\mid \varphi(g)=e \right\}
$$
$$
 \text{im}(\varphi)=\left\{ h\in  H\mid h=\varphi(g)\text{ for some }g\in  G \right\}
$$
### Remark
$\varphi: G\to H$ is injective iff $\text{ker}(\varphi)=\left\{ e \right\}$
# [[Rings|Ring]] Homomorphism
## Definition
If $R$ and $S$ are rings, a function $f:R\to S$ is called a (ring) homomorphism if for all $a,b\in R$, we have:
- $f(\underbrace{ 1 }_{ \in R })=\underbrace{ 1 }_{ \in S }$ 
- $f(a+b)=f(a)+f(b)$
- $f(ab)=f(a)f(b)$
## Kernel and Image
Just like for [[Linear Maps|linear maps]], homomorphisms have [[Kernel|kernels]] and [[Image|images]]:
$$
\text{ker}(f):= \left\{ a\in  R\mid f(a)=0 \right\}\subseteq R
$$
$$
 \text{im}(f):=\left\{ f(a)\mid a\in  R \right\}\subseteq S
$$
## Lemma
Let $f:R\to S$ be a homomorphism of rings, then
- $f(0)=0$
- $\forall a\in R,f(-a)=-f(a)$
### Proof
- $f(0)=f(0+0)=f(0)+f(0)\implies f(0)=0$ by additive cancellation
- This is true iff $f(-a)+f(a)=0\iff f(a+ -a)=0 \iff f(0)=0$ which we showed above :)
## Examples
Consider $f:\mathbb{Z}\to \mathbb{Z} /n$, such that $f(a)=\overline{a}$. This is additive and multiplicative by the definition of [[Integers Modulo n|$\overline{a}$]], giving $\overline{a}+\overline{b}$ and $\overline{a}\overline{b}=\overline{ab}$, and also note that $f(1)=\overline{1}$, the identity in $\mathbb{Z} /n$
___
[[Complex Numbers|Complex]] conjugation, $\mathbb{C}\to \mathbb{C},x\mapsto \overline{x}$. This is also additive and multiplicative, for example $\overline{x+y}=\overline{x}+\overline{y}$ (this was used to define the norm map $N:\mathbb{Z}[\sqrt{ -5 }]\to \mathbb{Z}$, which itself is multiplicative, but not additive)
___
$f:\mathbb{Z}[\sqrt{ 2 }]\to \mathbb{Z}[\sqrt{ 2 }]$, $f(m+n\sqrt{ 2 })=m-n\sqrt{ 2 }$, which is similar, but not the same as complex conjugation. $f$ is additive and multiplicative and clearly $f(1)=1$
___
Let 
$$
S=\left\{ \begin{pmatrix}
a & -b\\b&a
\end{pmatrix}\middle|a,b\in \mathbb{R}  \right\}
$$
This is a subring of $M_{2}(\mathbb{R}):0,1\in S$, and it being closed under addition, multiplication, and taking negatives are straightforward to check. We find that actually $S$ is a commutative ring
We will link $S$ with the ring of complex numbers by means of a homomorphism
We can check that it is a ring:
$$
\begin{pmatrix}
a & -b \\
b & a 
\end{pmatrix}\begin{pmatrix}
c & -d  \\
d & c
\end{pmatrix}=\begin{pmatrix}
ac-bd & bc+ad \\
-ad-bc & ac-bd
\end{pmatrix}
$$
Which we can see is a member of $S$. We can also swap the order to show that multiplication will be commutative.
We defnine a map $f:\mathbb{C}\to S$ by 
$$
f(a+bi)=\begin{pmatrix}
a & -b \\
b & a
\end{pmatrix}
$$
We claim $f$ is a homomorphism. 
Additivity: 
$$
f(a+bi+c+di)=f(a+c+(b+d)i)=\begin{pmatrix}
a+c & -(b+d) \\
b+d & a+c
\end{pmatrix}
$$
$$
= \begin{pmatrix}
a & -b  \\
b & a 
\end{pmatrix}+\begin{pmatrix}
c & -d \\
d & c
\end{pmatrix}=f(a+bi)+f(c+di)
$$
Multiplicity:
$$
f((a+bi)(c+di))=f(ac-bd+(ad+bc)i)=\begin{pmatrix}
ac-bd & -(ad+bc) \\
ad+bc & ac-bd
\end{pmatrix}
$$
$$
= \begin{pmatrix}
a & -b \\
b & a
\end{pmatrix}\begin{pmatrix}
c & -d \\
d & c
\end{pmatrix}=f(a+bi)f(c+di)
$$
Identity:
$$
f(1)=\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$
Which is the what we want.
It happens that $f$ is bijective. This can be shown by finding an inverse $f^{-1}$ of $f$:
$$
f^{-1}\begin{pmatrix}
 a & -b \\
b & a
\end{pmatrix}=a+bi
$$
So we have shown that $f$ is a 1-$\hspace{0pt}1$ map between $\mathbb{C}$ and $S$ that preserves the binary operations, so $\mathbb{C} \cong S$, they are [[Isomorphisms|isomorphic]] (as rings)
Since $\mathbb{C}$ is a field, then $S$ must also be


#Mathematics #Group #Ring #Definition 