If we consider data in maths, we are referring to a finite set $X\subseteq \mathbb{R}^{n}$ and one thing we are looking for is to find the dimension of the data.
In the real world, data are things like videos on youtube, people on facebook, students at durham etc. and the process of going from this to maths is called vectorisation
If you think about it, $\mathbb{R}^{n}$ is a really bad space for data

Consider a computer network with computers A,B,C, and between A and B has speed $s_{1}$ and between B and C there is speed $s_{2}$, then the speed between A and C has speed at least $\min(s_{1},s_{2})$
Which is not a Euclidean space as distances might not add up. This type of data is called heierachical. It can never be faithfully embedded into $\mathbb{R}^{n}$
The way LLMs work is that it does this with words, which are inherantly non-archimedian, so what it does is give each word its own dimension

The $p$-adic valuation and norm on $\mathbb{Q}$ is:
$$
\text{val}_{p}\left( p^{k}  \frac{a}{b} \right):=k
$$
If $p\nmid a,b$,
$$
\left\lvert  \left\lvert  p^{k} \frac{a}{b}  \right\rvert  \right\rvert_{p} := p^{-k}
$$
The following theorem from Ostrauski says that the standard absolute value and the $p$-adic norm are the only norms that exist on $\mathbb{Q}$ (up to equivalent multiples)
The completion of the absolute value leads to $\mathbb{R}$, and the completion of the $p$-adic norm leads to $\mathbb{Q}_{p}$, the $p$-adic numbers:
$$
\mathbb{Q}_{p}=\left\{ \sum_{h\geq h_{0}} a_{k}p^{k}:\middle| : h_{0}\in \mathbb{Z},a_{k}\in \left\{ 0,\dots,p-1 \right\} \right\}
$$
This is a nice theorem with a yucky proof :/
consider for example $\text{val}_{3}(18)=\text{val}_{3}(3^{2}\cdot2)=2$, $\lvert \lvert 18 \rvert \rvert_{3}=3^{-2}$
$$
\text{val}_{3}(27)=\text{val}_{3}(3^{3}\cdot 1)=3,\lvert \lvert 27 \rvert \rvert _{3}=3^{-3}
$$
$$
 \text{val}_{3}(18+27)=\text{val}_{3}(3^{2}(2+3))=2,\lvert \lvert 18+27 \rvert \rvert =3^{-2}=\max\left\{ \lvert \lvert 18 \rvert \rvert _{3},\lvert \lvert 27 \rvert \rvert_{3}  \right\}
$$
$\mathbb{Q}_{p}$ is a non-archimedean space. And in $\mathbb{Q}_{p}$ we have the strong triangle inequality, where 
$$
\lvert \lvert a+b \rvert \rvert \leq \max\left\{ \lvert \lvert a \rvert \rvert ,\lvert \lvert b \rvert \rvert  \right\}
$$
A consequence of this, is that if you consider a ball of radius $\hspace{0pt}1$, while disks have unique centres in $\mathbb{R}$, every point in $\mathbb{Q}_{p}$ is a valid centre
Lemma 1:
Let $b\in B(a,r):=\left\{ c\in k\mid \left| c-a \right|\leq r \right\}$, I claim that $B(a,r)=B(b,r)$
Proof:
Let $c\in B(a,r)$, then $\left| c-b \right|=\left| c-a+a-b \right|\leq \max\left\{ \left| c-a \right|,\left| a-b \right| \right\}\leq r$, and $\left| c-a \right|<r$, and $\left| r-a \right|<r$ since $c$ and $b$ are in the ball, which means that $c\in B(b,r)$
Let $c\in B(b,r)$, then $\left| c-a \right|=\left| c-b+b-a \right|\leq\max\left\{ \left| c-b \right|,\left| b-a \right| \right\}\leq r$, i.e. $c\in B(a,r)$
In $\mathbb{R}$, discs can intersect, but in $\mathbb{Q}_{p}$, discs are either disjoint or nested
Lemma 2:
Let $B_{1}=B(a_{1},r_{1})$ and $B_{2}=B(a_{2},r_{2})$, then $B_{1}\cap B_{2}\neq 0 \iff B_{1}\subseteq B_{2}$ or $B_{2}\subseteq B_{1}$
Proof:
The proof fo the backwards direction is clear, For the other way:
Let $c\in B_{1}\cap B_{2}$, then either $B_{1}\subseteq B_{2},(r_{1}\leq r_{2})$ or vice versa.