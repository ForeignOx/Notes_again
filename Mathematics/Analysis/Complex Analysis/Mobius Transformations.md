## Definition
Let $a,b,c,d\in\mathbb{C}$ be such that $ad-bc\neq 0$. The map
$$
M(z):= \frac{az+b}{cz+d}
$$
defined on $\mathbb{C}\setminus \left\{ -\frac{d}{c} \right\}$ when $c\neq 0$ and $\mathbb{C}$ when $c=0$ is called a Mobius transformation
Any Mobius transformation can be represented by a [[Matrices|matrix]] 
$$
T=\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}\in GL_{2}(\mathbb{C})
$$
Where $GL_{2}(\mathbb{C})$ is the [[General Linear Group|general linear group]] of $2\times 2$ complex matrices
In that case we write $M=M_{T}$
## Remark
The reason we want the [[Determinants|determinant]] to be nonzero is since if it is zero and the map is defined (i.e. we don't have $d=c=0$) we can find a scalar $\alpha \in\mathbb{C}$ such that
$$
a=\alpha c,b=\alpha d
$$
And in that case $M(z)=\alpha$ which is a constant map
___
The representation of a Mobius transformation by a matrix is not unique. Indeed, for any $a,b,c,d\in\mathbb{C}$ such that $ad-bc\neq 0$ and any $k\in\mathbb{C}^{*}$, we have that
$$
M_{kT}(z)=\frac{(ka)z+(kb)}{(kc)z+(kd)}=\frac{az+b}{cz+d}=M_{T}(z)
$$
One advantage of using the matrix representation is that it helps bring out the structure of the set of Mobius transformations
## Lemma
The let of Mobius transformations form a [[Groups|group]] under [[Composition of Functions|composition]]. Furthermore,
- $M_{T_{1}}\circ M_{T_{2}}=M_{T_{1}T_{2}}$
- Any Mobius transformation is invertible with $(M_{T})^{-1}=M_{T^{-1}}$
- For any $k\in\mathbb{C}^{*}$, we have that $M_{kT}=M_{T}$, so we conclude that $M_{T}=I$ iff 
$$
T=k\begin{pmatrix}
1 & 0 \\
0  & 1
\end{pmatrix}
$$
    For some $k\in\mathbb{C}^{*}$
### Proof
Kinda obvious man
## Remark
An immediate consequence of the above and that fact that if $T \in GL_{2}(\mathbb{C})$, then
$$
T^{-1}=\frac{1}{ad-bc}\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}\in GL_{2}(\mathbb{C})
$$
And $M_{T}$ is invertible on $\mathbb{C}\setminus \left\{ -\frac{d}{c} \right\}$ when $c\neq 0$ and $\mathbb{C}$ when $c=0$ with an inverse $M_{T^{-1}}$
To be more precise:
- When $c\neq 0$:
$$
M_{T}:\mathbb{C}\setminus \left\{ -\frac{d}{c} \right\}\to \mathbb{C}\setminus \left\{ \frac{a}{c} \right\}
$$
    is a [[Bijective Functions|bijection]] with an inverse $M_{T^{-1}}$
- When $c=0$:
$$
M_{T}:\mathbb{C}\to \mathbb{C}
$$
    is a bijection with inverse $M_{T^{-1}}$
Recalling that we use the [[Riemann Sphere|Riemann sphere]] denoted y $\hat{\mathbb{C}}=\mathbb{C}\cup \left\{ \infty \right\}$ where $\infty$ is understood to be an infinite circle, we notice that when $c\neq 0$,
$$
\lim_{ z \to \frac{d}{c} } \left| \frac{az+b}{cz+d} \right| =\infty 
$$
$$
 \lim_{ \left| z \right|  \to \infty }  \frac{az+b}{cz+d}=\frac{a}{c}
$$
We can conclude the following:
We can extend the definition of Mobius transformation to bijections from $\hat{\mathbb{C}}$ to $\hat{\mathbb{C}}$:
Given $a,b,c,d\in\mathbb{C}$ such that $ad-bc \neq 0$, we define $M:\hat{\mathbb{C}}\to \hat{\mathbb{C}}$ by
$$
M(z)=\begin{cases}
 \frac{az+b}{cz+d} & z\neq -\frac{d}{c},\infty  \\
\infty & z=-\frac{d}{c} \\
\frac{a}{c} & z=000
\end{cases}
$$
When $c\neq 0$, and
$$
M(z):=\begin{cases}
 \frac{az+b}{d} & z\neq \infty \\
\infty & z=\infty
\end{cases}

$$
When $c=0$
## Example
The map $f(z)=\frac{1}{z}$ corresponds to $T=\begin{pmatrix}0&1\\1&0 \end{pmatrix}$. Using polar coordinates, we see that
$$
f(z)=\frac{1}{r}e^{ -i\theta }
$$
The map, thus inverrts the distance from the origin and reflects it with respect to the real axis. We see that, much line $z^{n}$, the map takes segments of circles centred at the origin to segments of circle centred at the origin but going in an opposite direction
