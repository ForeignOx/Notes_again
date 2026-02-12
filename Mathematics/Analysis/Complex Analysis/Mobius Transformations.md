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
## Fixed Point Theorem for Mobius Transformations
Let $M:\hat{\mathbb{C}}\to \hat{\mathbb{C}}$ be a Mobius transformation that is not the identity map. Then $M$ has at most $\hspace{0pt}2$ [[Fixed Points|fixed points]] in $\hat{ \mathbb{C}}$. In other words, if a Mobius transformation has three fixed points in $\hat{\mathbb{C}}$, then it is the identity
## Proof
Let $a,b,c,d\in\mathbb{C}$ be such that $ad-bc\neq 0$ and
$$
M(z)=\frac{az+b}{cz+d}
$$
We have that $M(z)=z$ for $z\in\mathbb{C}$ iff $az+b=z(cz+d)$ i.e.
$$
cz^{2}+(d-a)z-b=0
$$
We have three options:
- $c\neq 0$: in this case we have a quadratic equation which has at most two solutions
- $c=0$ and $d\neq a$: in this case we have the unique solution $z=\frac{b}{d-a}$
- $c=0$ and $d=a$, in that case $b=0$ and our map is
$$
M(\xi)=\frac{a\xi}{a}=\xi
$$
    which contradicts our initial assumption
Lastly, we notice that $M(\infty)=\infty$ only when $c=0$, adding another fixed point to the second (and third) cases above
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
To prove the uniqueness we assue that there exist two Mobius transformations $M_{1},M_{2}$ that take $\left\{ z_{1},z_{2},z_{3} \right\}$ to $\left\{ w_{1},w_{2},w_{3} \right\}$, then $M_{1}\circ M_{2}^{-1}$ is also a Mobius transformation is also a Mobius transformation that takes the ordered distinct points $\left\{ z_{1},z_{2},z_{3} \right\}$ to themselves. According to the fixed point theorem for Mobius transformations, this is possible only if
$$
M_{1}\circ M_{2}^{-1}=I \iff M_{1}=M_{2}
$$
# Geometric Properties
## Building Blocks of Mobius Transformations
Any Mobius transformation is compositions of the following $\hspace{0pt}4$ types of maps:
- Shift: $z\to z+b$ for some $b\in\mathbb{C}$
- Dilation: $z\to\lambda z$ for some $\lambda \in\mathbb{R}_{>0}$
- Rotation: $z\to e^{ i\theta }$ for some $\theta \in(-\pi,\pi]$
- Inversion: $z\to \frac{1}{z}$
### Proof
We start by noticing that for any $a,b\in\mathbb{C}$, with $a\neq 0$,
$$
f(z)=az+b=\left| a \right| e^{ i\mathrm{Arg}(a) }z+b
$$
Which is a composition of a rotation, dilation and shift
Following on this, we see that for any $\alpha,\beta,c,d\in\mathbb{C}$ with $\beta,c\neq 0$, the map
$$
g(z)=\alpha+\frac{\beta}{cz+d}=\beta\left( \frac{1}{cz+d} \right)+\alpha
$$
Is a composition of rotation, dilation, shift, inversion and then rotation, dilation and shift again
Given $a,b,c,d\in\mathbb{C}$ with $ad-bc\neq 0$, we have that $M(z)=\frac{az+b}{cz+d}$ satisfies:
$$
M(z)=\begin{cases}
\frac{\frac{a(cz+d)}{c}-\frac{ad}{c}+b}{cz+d}=\frac{a}{c}+\frac{bc-ad}{c^{2}z+cd} & c\neq 0 \\
\frac{a}{d}z+\frac{b}{d} & c=0
\end{cases}
$$
Consequently, $M(z)$ is always of the forms we previously discussed, as such is a composition of the four geometric maps
## Corollary
Any Mobius transformation is compositions of the following two maps:
- $z\to az+b$ for some $a\in\mathbb{C}^{*},b\in\mathbb{C}$
- $z\to \frac{1}{z}$
___
The three points theorem is more than an abstract mathematical theorem; its proof is constructive, giving us a recipe to build the unique Mobius tranformation that takes $\left\{ z_{1},z_{2},z_{3} \right\}$ to $\left\{ w_{1},w_{2},w_{3} \right\}$. This recipe involves the cross ratio, emphasising its geometric importtance in the world of Mobius transformations. The following observation shows that the cross ratio is not only useful in constructing a Mobius transformation, it is also invariant under them:
## Lemma
The cross ratio is invariant under Mobius transformation. In other words, if $M:\hat{\mathbb{C}}\to \hat{\mathbb{C}}$ is a Mobius transformation, then
$$
(M(z_{0}),M(z_{1});M(z_{2}),M(z_{3}))=(z_{0},z_{1};z_{2},z_{3})
$$
### Proof
From the Corollary of the building blocks of the Mobius transform we see that it is enough to show that the cross ratio is preserved under the maps $f_{1}(z)=az+b$ with $a\in\mathbb{C}^{*},b\in\mathbb{C}$ and $f_{2}(z)=\frac{1}{z}$ since every Mobius transformation is a composition of these maps/
Since
$$
f_{1}(z)-f_{1}(w)=a(z-w)
$$
We see that
$$
\frac{f_{1}(z_{0})-f_{1}(z_{2})}{f_{1}(z_{0})-f_{1}(z_{3})}=\frac{z_{0}-z_{2}}{z_{0}-z_{3}}
$$
And similarly
$$
\frac{f_{1}(z_{1})-f_{1}(z_{2})}{f_{1}(z_{1})-f_{1}(z_{3})}= \frac{z_{1}-z_{2}}{z_{1}-z_{3}}
$$
Which shows the desired invariance (including the case where one of the $z$'s is infinite since the corresponding $f_{1}(z)$ is also infinity in this case)
Let us consider $f_{2}$ and assume, to begin with that $z_{i}\neq 0$ for $i\in\overline{3}_{0}$. We have that
$$
\frac{f_{1}(z_{0})-f_{1}(z_{2})}{f_{1}(z_{0})-f_{1}(z_{3})}=\frac{\frac{1}{z_{0}}-\frac{1}{z_{2}}}{\frac{1}{z_{0}}-\frac{1}{z_{3}}}=\frac{z_{3}}{z_{2}} \frac{z_{2}-z_{0}}{z_{3}-z_{0}}
$$
Similarly
$$
\frac{f_{2}(z_{1})-f_{2}(z_{2})}{f_{2}(z_{1})-f_{2}(z_{3})}=\frac{z_{3}}{z_{2}} \frac{z_{2}-z_{1}}{z_{3}-z_{1}}
$$
Dividing the two gives us:
$$
(f_{2}(z_{0}),f_{2}(z_{1});f_{2}(z_{2}),f_{2}(z_{3}))=\frac{\frac{f_{1}(z_{0})-f_{1}(z_{2})}{f_{1}(z_{0})-f_{2}(z_{3})}}{\frac{f_{2}(z_{1})-f_{2}(z_{2})}{f_{2}(z_{1})-f_{2}(z_{3})}}=\frac{z_{2}-z_{0}}{z_{3}-z_{0}} \frac{z_{3}-z_{1}}{z_{2}-z_{1}}=\frac{(z_{0}-z_{2})(z_{1}-z_{3})}{(z_{0}-z_{3})(z_{1}-z_{2})}=(z_{0},z_{1};z_{2},z_{3})
$$
Next we consider the case where one of the $z$'s, say $z_{0}$ without loss of generality, is zero. In that case, $f_{2}(z_{0})=\infty$ and
$$
(f_{2}(z_{0}),f_{2}(z_{1});f_{2}(z_{2}),f_{2}(z_{3}))=(\infty,f_{2}(z_{1});f_{2}(z_{2}),f_{2}(z_{3}))=\frac{f_{2}(z_{1})-f_{2}(z_{3})}{f_{2}(z_{1})-f_{2}(z_{3})}
$$
$$
= \frac{z_{2}}{z_{3}} \frac{z_{1}-z_{3}}{z_{1}-z_{2}}=(0,z_{1};z_{2},z_{3})=(z_{0},z_{1};z_{2},z_{3})
$$
Yay
___
The invariance of the cross ratio allows us to explicitly find a Mobius transfomation that takes $\hspace{0pt}3$ distinct points $\left\{ z_{1},z_{2},z_{3} \right\}$ to three other distinct points $\left\{ w_{1},w_{2},w_{3} \right\}$
For any $z\in\mathbb{C}$, the Mobius tranformation $M$ must satisfy
$$
(M(z),w_{1};w_{2},w_{3})=(z,z_{1};z_{2},z_{3}) 
$$
or
$$
\frac{M(z)-w_{2}}{M(z)-w_{3}} \frac{w_{1}-w_{3}}{w_{1}-w_{2}}=\frac{z-z_{2}}{z-z_{3}} \frac{z_{1}-z_{3}}{z_{1}-z_{2}}
$$
Rearranging this gives us a way to find $M(z)$
Notice that if we know that one of the points goes to infinity, the ratio on the left becomes simpler
## Example
FInd the Mobius transformation that takes the points $\left\{ 1,-1,i \right\}$ to $\left\{ 0,1,\infty \right\}$ respectively
We remove the terms that have $w_{2}=\infty$ in them to find that
$$
\frac{0-1}{M(z)-1}= \frac{z+1}{z-i} \frac{1-i}{1+i}
$$
which is equivalent to
$$
M(z)-1=\frac{2}{1-i}  \frac{i-z}{z+1}=(1+i) \frac{i-z}{z+1}
$$
So we conclude that
$$
M(z)= \frac{-iz+i}{z+1}
$$
## Lemma
Let $M:\hat{\mathbb{C}}\to \hat{\mathbb{C}}$ be a Mobiuis transformation. For any open set $D\subseteq \mathbb{C}$ we have that
$$
M\left( \partial D\setminus \left\{ -\frac{d}{c} \right\} \right)=\partial M(D)\setminus \left\{ \infty \right\}
$$
When $c=0$, we consider $-\frac{d}{c}$ as $\infty$, which is outside of $\mathbb{C}$ and consequently, $A\setminus \left\{ \infty  \right\}=A$ for any $A\subseteq \mathbb{C}$
## Remark
We can extend the above to $\hat{\mathbb{C}}$ by including $-\frac{d}{c}$ and $\infty$
## Image of Special Domains under Mobius Transformations
Since any Mobius transformation is a biholomorphism from $\hat{\mathbb{C}}$ to itself, we would like to find particular domains that are biholomorphic under such transformations. Towards that end, we use the lemma above.
An immediate application is the following strategy to understand the image of a given (general) domain $D\subseteq \mathbb{C}$ by a Mobius transformation $M$
1. Find the image $M(\partial D)$ of the boundary of $D$
2. Find the image $M(z_{0})$ of a point $z_{0}\in D$
3. $M(D)$ is the set whose boundary is $M(\partial D)$ and contains $M(z_{0})$. Moreover,
$$
M:D \tilde{\to}M(D)
$$
The general strategy relies on being able to map the boundary of a omain with a Mobius tranformation
A remarkable feature of Mobius transformations is the following:
### Proposition
Mobius transformations map circles and lines in $\hat{\mathbb{C}}$ to circles and lines in $\hat{\mathbb{C}}$, where we consider any line to pass through infinity and where circ les in $\hat{\mathbb{C}}$ simply mean circles in $\mathbb{C}$. Moreover, a circle or a line would be mapped to a line iff there is a point on it that is mapped to $\infty$
#### Proof
Using the fact that every Mobius transformation is a composition of shifts, dilations, rotations, and inversions, we see that we only need to show that the claim is true for each such map (while being careful with the point $-\frac{d}{c}$)
The claim is straightforward and intuitive for shifts, dilations and rotations. Moreover, in that case, se see that a line will go to a line if and only if there is a point on it that goes to infinity
To conclude the proof we only need to consider inversions.
We that we can write the general equation of a [[Circles|circle]] in the complex plane as
$$
\gamma z\overline{z}-\alpha \overline{z}-\overline{\alpha}z+\beta=0
$$
With $\gamma,\beta \in\mathbb{R},\alpha \in\mathbb{C}$ and $\left| \alpha \right|^{2}-\beta\gamma>0$. Defining $w=\frac{1}{z}$, we see that when $z\neq 0$, the above equation becomes
$$
\frac{\gamma}{w\overline{w}}-\frac{\alpha}{\overline{w}}-\frac{\overline{\alpha}}{w}+\beta=0
$$
Which is equivalent to 
$$
\beta w \overline{w}-\alpha w-\overline{\alpha}\overline{w}+\gamma=0
$$
This is again an equation of a circle or a line, we have two options:
- $\beta=0$, in this case since $\left| \alpha \right|^{2}-\beta\gamma>0$, we must have that $\alpha \neq 0$, and a such the image of the circle under the inversion is a line
- $\beta \neq 0$: in this case we define $\gamma'=\beta,\alpha'=\overline{\alpha}$ and $\beta'=\gamma$ and notice that
$$
\gamma'w\overline{w}-\alpha'\overline{w}-\overline{\alpha'}w+\beta'-\beta w\overline{w}-\overline{\alpha}w-\alpha \overline{w}+\gamma=0
$$
and
$$
\left| \alpha' \right| ^{2}-\beta'\gamma'=\left| \alpha \right| ^{2}-\beta\gamma>0
$$
Showing that the image of the circle under the inverion is a circle
We now turn our attention to the general form of a [[Lines|line]] which we know can be written in the complex plane as
$$
-\alpha \overline{z}-\overline{\alpha}z+\beta=0
$$
With $\alpha \in\mathbb{C}^{*}$. Defining $w=\frac{1}{z}$ as before, we find that the equation of the line becomes
$$
-\overline{\alpha}\overline{w}-\alpha w+\beta w\overline{w}=0
$$
Which is again the equation for a circle or a line. We have two options:
- $\beta=0$: in this case, the equation becomes $-\overline{\alpha}\overline{w}-\alpha w=0$ which is a line as $\alpha \neq 0$
- $\beta \neq 0$: in this case, we define $\gamma'=\beta$, $\alpha'=\overline{\alpha}$ and $\beta'=0$ and notice that
$$
\gamma'w\overline{w}-\alpha'\overline{w}-\overline{\alpha'}=-\overline{\alpha}\overline{w}-\alpha w+\beta w \overline{w}=0
$$
And
$$
\left| \alpha' \right| ^{2}-\beta'\gamma'=\left| \alpha \right| ^{2}>0
$$
Showing that the image of the line under the inversion is a circle
To prove the last statement, we notice that a circle or a line go to a line iff $\beta=0$. This only happens if $z=0$ on the curve is derfined by
$$
\gamma z\overline{z}-\overline{\alpha}z-\alpha \overline{z}+\beta=0
$$
Which is equivalent to the fact that the circle or line pass through th point that the map $\frac{1}{z}$ takes to infinity
### Remark
Any three distinct non-colinear points $z_{1},z_{2},z_{3}\in\mathbb{C}$ uniquely determine a circle in $\mathbb{C}$ passing through these points. Any two distinct points uniquely determine a line passing through them
This means to find out where a circle is mapped under a Mobius transformation, we only need to check where three points on the circle go
### Proposition: Mobius Transformations that Preserve the Upper Plane (H2H)
Every Mobius transformation mapping $\mathbb{H}$ to $\mathbb{H}$ is of the form $M_{T}$ with $T$ in the [[General Linear Group|special linear group]]:
$$
SL_{2}(\mathbb{R}):=\left\{ T=\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}:\middle|:a,b,c,d\in \mathbb{R},\det T=ad-bc=1 \right\}
$$
Conversely, every such Mobius transformation maps $\mathbb{H}$ to $\mathbb{H}$ and hence gives a biholomorphism from $\mathbb{H}$ to $\mathbb{H}$
#### Proof
Assume that the Mobius transformation $M$ takes $\mathbb{H}$ to itself.
Since the boundary of $\mathbb{H}$ must be mapped to the boundary of $\mathbb{H}$ under $M$, we find that we need $M$ to take the real axis to itself
Consequently, there exists $x_{1},x_{2},x_{3}\in\mathbb{R}\cup \left\{ \infty \right\}$ such that
$$
M(x_{1})=1,~M(x_{2})=0,~M(x_{3})=\infty
$$
If none of $x_{1},x_{2},x_{3}$ is $\infty$, we use the cross ratio to conclude that
$$
\frac{M(z)-0}{1-0}=\frac{z-x_{2}}{z-x_{3}} \frac{x_{1}-x_{3}}{x_{1}-x_{2}}
$$
Or
$$
M(z)=\frac{(x_{1}-x_{3})z-x_{2}(x_{1}-x_{3})}{(x_{1}-x_{2})z-x_{3}(x_{1}-x_{2})}
$$
