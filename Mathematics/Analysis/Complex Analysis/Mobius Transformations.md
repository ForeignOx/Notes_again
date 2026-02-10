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
![[Pasted image 20260209232413.png]]
Similarly, segments of [[rays|rays]] of angle $\theta$, without the origin, become segments of rays of angle $-\theta$, though the length gets inverted
![[Pasted image 20260209232531.png]]
Using the above, we can conclude the following:
## Lemma
- The map $\frac{1}{z}$ [[Injective Functions|injectively]] takes the set $\mathbb{D}\setminus \left\{ 0 \right\}=\left\{ z\in\mathbb{C}:\middle|:0<\left| z \right|<1 \right\}$ to $\mathbb{D}^{c}=\left\{ z\in\mathbb{C}:\middle|:\left| z \right|>1 \right\}$. When considering $\frac{1}{z}$ over $\hat{\mathbb{C}}$, we find that it injectively takes $\mathbb{D}$ to $\mathbb{D}\cup \left\{ \infty \right\}$. Similarly, $\frac{1}{z}$ injectively takes the set $\mathbb{D}^{c}$ to $\mathbb{D}\setminus \left\{ 0 \right\}$ and on $\hat{\mathbb{C}}$ it takes $\mathbb{D}^{c}\cup \infty$ to $\mathbb{D}$
- The map $\frac{1}{z}$ injectively takes the ray at angle $\theta$ (without the origin) to the ray at angle $-\theta$ (without the origin). On $\hat{\mathbb{C}}$, the statement remains the same by adding the origin and $\infty$ to the rays
![[Pasted image 20260209233033.png]]
## Differentiability :o
## Lemma
Let $M$ be a mobius transformation which is represented by the matrix $T=\begin{pmatrix}a & b\\c & d\end{pmatrix}\in GL_{2}(\mathbb{C})$. If $c\neq 0$, then the Mobius transformation $M=M_{T}$ is a [[Biholomorphic Maps|biholomorphism]]:
$$
M:\mathbb{C} \setminus \left\{ -\frac{d}{c}\right\}\tilde{\to}\mathbb{C}\setminus \left\{ \frac{a}{c} \right\}
$$
And when $c=0$, the Mobiius transformation is a biholomorphism:
$$
M:\mathbb{C} \tilde{\to}\mathbb{C}
$$
### Proof
If $c\neq 0$, we dee that for any $z\neq -\frac{d}{c}$
$$
M'(z)=\frac{a(cz+d)-c(az+b)}{(cz+d)^{2}}=\frac{ad-bc}{(cz+d)^{2}}=\frac{\det T}{(cz+d)^{2}}
$$
Where we have used the [[Leibniz Rule|quotient rule]] for the [[Differentiation|derivative]]
Consequently, $M$ is complex differentiable on $\mathbb{C}\setminus \left\{ -\frac{d}{c} \right\}$ i.e. it is [[Holomorphicity|holomorphic]] in this [[Domains|domain]]
Since $M^{-1}=(M_{T})^{-1}=M_{T^{-1}}$ which is a Mobius transformation defined on $\mathbb{C}\setminus \left\{ \frac{a}{c} \right\}$, we find that the inverse is also holomorphic and conclude the result in this case.
For the case $c=0$, we see that from the condition $ad-bc\neq 0$ we must have that $a\neq 0$ and $d\neq 0$, consequently,
$$
M(z)=\frac{az+b}{d}=\frac{a}{d}z+\frac{b}{d}
$$
And both $M$ and its inverse are holomorphic on $\mathbb{C}$ showing the desired result
___ 
## Derivative of Mobius Transforom
In the above proof we've shown that
$$
M_{T}'(z)=\begin{cases}
\frac{\det T}{(cz+d)^{2}} & c\neq 0 \\
\frac{a}{d} & c=0
\end{cases}
$$
Which is never zero in its domain of definition. We conclude that
## Corollary
A Mobius transformation $M$ is [[Conformal Maps|conformal]] at all $z\in\mathbb{C}$ with $M(z)\neq \infty$
In fact, we can extend the notion of holomorphicity to $\hat{\mathbb{C}}$ and find that
## Proposition
A Mobius transformation $M$ is a biholomorphism of $\hat{\mathbb{C}}$ to itself. Moreover, any biholomorphism between $\hat{ \mathbb{C}}$ and itself must be a Mobiius transformation
# Three Points Theorem
The fact that any Mobius transformation can be represented by a $2\times 2$ matrix $T\in GL_{2}(\mathbb{C})$ and the fact that $M_{kT}=M_{T}$ for any $k\in\mathbb{C}^{*}$, implies that we can fix one of the entries of $T$ to be, for example $\hspace{0pt}1$ (for instance, if $a\neq 0$, then the matrix $T'=\frac{1}{a}T$ satisfies $M_{T}=M_{T'}$)
Consequently, any Mobius transformation requires only three complex numbers to be determined uniquely
It turns out that these numbers can be determined by three points in the image of $M$
## Theorem
Let $\left\{ z_{1},z_{2},z_{3} \right\}$ and $\left\{ w_{1},w_{2},w_{3} \right\}$ be two [[sets|sets]] of three [[Ordered Pairs|ordered]] distinct points in $\hat{\mathbb{C}}$. Then there exists a unique Mobius transformation $M$ such that $M(z_{i})=w_{i}$ for $i\in\overline{ 3}$
### Proof
For a given distinct $\left\{ z_{1},z_{2},z_{3} \right\}$, we use the [[Cross Ratio|cross ratio]] to define the map
$$
F(z)=(z,z_{1};z_{2},z_{3})=\frac{z-z_{2}}{z-z_{3}} \frac{z_{1}-z_{3}}{z_{1}-z_{2}}
$$
$F(z)$ is a Mobius transformation. moreover, $F(z_{1})=1,F(z_{2})=0,F(z_{3})=\infty$
Given the associated numbers $\left\{ w_{1},w_{2},w_{3} \right\}$, we see that
$$
G(w)=(w,w_{1};w_{2},w_{3})
$$
Is another Mobius transformation such that $G(z_{1})=1,G(z_{2})=0,G(z_{3})=\infty$
The map $M=G^{-1}\circ F$, which is well defined, is a Mobius transformation that satisfies 
$$
M(z_{1})=G^{-1}(1)=w_{1},M(z_{2})=G^{-1}(0)=w_{2},M(z_{3})=G^{-1}(\infty)=w_{3}
$$
To prove the uniqueness
