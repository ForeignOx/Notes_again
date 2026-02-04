# For Rings
## Theorem
Let $\varphi:R\to S$ be a [[Rings|ring]] [[Homomorphisms|homomorphism]], then the map 
$$
\overline{\varphi}:R/ \text{ker}(\varphi)\to \text{im}(\varphi),\overline{x}\mapsto \varphi(x)
$$
is a well-defined [[Isomorphisms|isomorphism]], i.e. $R /\text{ker}(\varphi)\cong \text{im}( \varphi)=S$ 
### Proof
$\overline{\varphi}$ is well-defined. Let $x,x'\in R$ be two equivalent elements, i.e. $\overline{x}=\overline{x'}$, $x\equiv x' \mod \text{ker}(\varphi)$, then $x-x'\in \text{ker}(\varphi)$, so
$$
\varphi(x-x')=\varphi(x)-\varphi(x')=0
$$
So $\varphi(x)=\varphi(x')$, hence
$$
\overline{\varphi}(\overline{x})=\varphi(x)=\varphi(x')=\overline{\varphi}(\overline{x'})
$$
So it is well defined.
$\overline{\varphi}$ can easily be checked to be a homomorphism, we claim that $\text{ker}(\overline{\varphi})=0$. Indeed, 
$$
\overline{x}\in \text{ker}(\overline{\varphi})\iff \overline{\varphi}(\overline{x})=0 \iff \varphi(x)=0 \iff x\in  \text{ker}(\varphi) \iff \overline{x}=\overline{0}
$$
Thus $\overline{\varphi}$ is injective. Finally $\overline{\varphi}$ is surjective becaue for all $y\in \text{im}(\varphi)$, $\exists x\in R$ such that $\varphi(x)=y$, so $\overline{\varphi}(\overline{x})=y$
## Example
Let $\varphi:\mathbb{R}[x]\to \mathbb{C}$, $\varphi(f(x))=f(i)$, (where $i^{2}=-1$)
If $f(i)=0$, then $i$ is a root, so its conjugate $-i$ is also a root, then $f(x)$ has a factor $(x-i)(x+i)=x^{2}+1$
Thus $\text{ker}(\varphi)=(x^{2}+1)$. By the first isomorphism theorem, 
$$
\mathbb{R}[x] /(x^{2}+1)\cong \text{im}(\varphi)=\mathbb{C}=\mathbb{R}[i]
$$
Similarly, $(\mathbb{Z} /2)[x] /(x^{2}+1)$ also adjoins $i$ to $\mathbb{Z} /2$, and this works with many a field
# For Groups
## Theorem
Let $\varphi:G\to H$, be a [[Groups|group]] homomorphism, then
$$
G /\text{ker}(\varphi)\cong \text{im}(\varphi)
$$
### Proof
We know elements in $G /\text{ker}(\varphi)$ take the form $g\text{ker}(\varphi)$,
$$
g\text{ker}(\varphi)\mapsto \varphi(g)
$$
Which is an isomorphism
## Example
Consider $\varphi:D_{n}\to \mathbb{Z} /2$, where $\varphi(r^{a})=\overline{0},\varphi(r ^{a}s)=\overline{1}$, which is a homomorphism, clearly
$$
\text{ker}(\varphi)=\left<  r \right>,\text{im}(\varphi)=\mathbb{Z} /2 
$$
So by the first isomorphism theorem,
$$
D_{n} /\left< r \right> \cong \mathbb{Z}/2
$$
___
Consider $\varphi:\mathbb{Z}/6\to S_{3}$ defined by $\varphi(\overline{a})=\begin{pmatrix}1 & 2 & 3\end{pmatrix}^{a}$,
$$
\text{ker}(\varphi)=\left\{ \overline{0},\overline{3} \right\},\text{im}(\varphi)=\left< \begin{pmatrix}
1 & 2 & 3
\end{pmatrix} \right> \cong \mathbb{Z} /3
$$
So by the first isomorphism theorem,
$$
\mathbb{Z} /6 /\left\{ \overline{0},\overline{3} \right\}\cong \left< \begin{pmatrix}
1 & 2 & 3
\end{pmatrix} \right> 
$$
$$
 \iff \mathbb{Z} /6 /\mathbb{Z} /2\cong \mathbb{Z} /3
$$



