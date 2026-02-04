This is the [[Groups|group]] that describes the all the [[Symmetry|symmetries]] of a regular $n$-gon, rotations and reflections. We write this $D_{n}$. Note this is not an [[Abelian Groups|abelian group]] in general
Note that $D_{n}$ is sometimes written as $D_{2n}$ :/
The order of the group is $\left| D_{n} \right|=2n$ 
## Examples
For $n=3$, we consider symmetries of an equalateral triangle
![[Dihedral Group 2025-11-10 15.08.08.excalidraw]]
We have the following symmetries:
- rotation by $\frac{2\pi}{3}=r$
- rotation by $\frac{4\pi}{3}=r^{2}$
- rotation by $0=e$
- reflections in lines $\mu_{1},\mu_{2},\mu_{3}$ which are written as $s_{1},s_{2},s_{3}$
So our set is
$$
D_{3}=\left\{ e,r,r^{2},s_{1},s_{2},s_{3} \right\}
$$
We can represent each of these as an [[Ordered Pairs|ordered triple]] by considering where each corner goes, for example, $r:(1,2,3)\to(2,3,1),s:(1,2,3)\to(1,3,2)$ 
If images of vertices are known, the symmetry is uniquely defined
The number of triples of $(1,2,3)$ is equal to $\hspace{0pt}6$, as it is $3!$ so there are no more than $\hspace{0pt}6$ elements in our group of symmetries of an equilateral triangle
This is a bit of a lame proof since we don't get any idea of the group structure
By some shenanigans we can find that we can generate this group from two elements e.g. $s_{1},s_{2}$:
$$
D_{3}=\left< s_{1},s_{2}:\middle|: s_{1}^{2}=e,s_{2}^{2}=e,(s_{1}s_{2})^{3}=e \right> 
$$
$$
=\left< r,s:\middle|: r^{3}=e,s^{2}=e,s rs=r^{-1} \right> 
$$
___
For $n=4$, 
$$
D_{4}=\left\{ M_{1},M_{2},M_{3},I,R_{1},R_{2},R_{3},R_{4} \right\}
$$
Where
$$
M_{1}=\begin{pmatrix}
0 & 1\\-1 & 0
\end{pmatrix},M_{2}=\begin{pmatrix}
-1 & 0 \\0 & -1 
\end{pmatrix},M_{3}=\begin{pmatrix}
0 & -1\\1 & 0
\end{pmatrix},I=\begin{pmatrix}
1 & 0\\0 & 1
\end{pmatrix}
$$
$$
R_{1}=\begin{pmatrix}
0 & -1\\-1 & 0
\end{pmatrix},R_{2}=\begin{pmatrix}
-1 & 0\\0 & 1
\end{pmatrix},R_{3}=\begin{pmatrix}
0 & 1\\1 & 0
\end{pmatrix},R_{4}=\begin{pmatrix}
1 & 0 \\0 & -1
\end{pmatrix}
$$
Note that all the $M$'s have [[Determinants|determinant]] $\hspace{0pt}1$, and all the $R$'s have determinant $-1$
The dihedral group is a [[Subgroups|subgoup]] of the [[Symmetric Groups|symmetric group]] 
___
For larger $n$, we have an $n$-gon with rotation element $r$ by $\frac{2\pi}{n}$ and for $n$ even, there are two types of reflection, from the edges and from the corners.
We write
$$
D_{n}=\left< r,s:\middle|: r^{n}=e,s^{2}=e,s rs=r^{-1} \right> 
$$
$$
= \left< s_{1},s_{2}:\middle|: s_{1}^{2}=e, s_{2}^{2}=e,(s_{1}s_{2})^{n}=e \right> 
$$
The order of $s$ is $\hspace{0pt}2$, the order of $r$ is $n$
If $n$ is even, the order of $r^{2}$ is $\frac{n}{2}$, if $n$ is odd, the order of $r^{2}$ is still $n$
## Lemma
For any element in $D_{n}$
$$
g=r ^{a_{1}}s ^{b_{1}} r^{a_{2}} s ^{b_{2}}\dots r ^{a_{k}} s ^{b_{k}}
$$
Can be written as $g=r ^{a}s ^{b}$, where $0\leq a\leq n-1$, $0\leq b\leq 1$
#### Proof
By induction on $m=\sum_{i=1}^{k}a_{i}+b_{i}$
For $m=1$, $g=r=r ^{1} s ^{0}$ or $g=s=r^{0}s ^{1}$
Assume we have proved the statement for $m$, we need to prove for $m+1$, so
$$
g=r ^{a_{1}}s ^{b_{1}}\dots r ^{a_{k}}s ^{b_{k}}
$$
Which was $m+1$ letters, we can say it is equal to either $g'r$ or $g's$, where $g'$ consists of $m$ letters, so we know that $g'=r ^{a}s ^{b}$
In the latter case,
$$
g=g's=r ^{a}s ^{b}s=r ^{a}s ^{b+1\mod 2}
$$
In the former case,
$$
g=g'r=r^{a}s ^{b}r=\begin{cases}
r ^{a+1\mod n} & \text{ if }b=0 \\
r ^{a}sr & \text{if }b=1
\end{cases}
$$
We recall $srs=r^{-1}\iff sr s s=r^{-1}s \iff s r=r^{-1}s$, so
$$
g=\begin{cases}
r ^{a+1\mod n} & \text{if }b=0 \\
r^{a-1}s & \text{if }b=1
\end{cases}
$$
Which was what we wanted, hence proved
___
Proof 2
We know that
$$
D_{n}=\left< r,s:\middle|: s^{2}=e,r^{n}=e,s rs=^{-1} \right> 
$$
Denote $t=sr\iff st=r$, so we can rewrite every element of $D_{n}$ in terms of $s$ and $t$, so our new conditions are:
$$
s ^{2}=e
$$
$$
 (st)^{n}=e
$$
$$
 t^{2}= srs r=r ^{-1} r=e
$$
Hence, 
$$
g=r^{a_{1}} s ^{b_{1}}\dots r ^{a_{k}}s ^{b_{k}}
$$
Can be rewritten in $s$ and $t$ and cancel neighbouring $ss$ and $tt$ terms:
$$
g=sts t s t s\dots \text{ or }g=ts ts ts \dots
$$
If $g=s ts ts ts\dots$, then $g=(st)^{c}$ or $g=(st)^{c}s$, which is the same as saying $g=r ^{c}$ or $g=r^{c}s$, and $c<n$, as $(st)^{n}=e$, so we can automatically modulo $n$
If $g=ts ts\dots$, then $g=(ts)^{c}$ or $g=(ts)^{c}t$, but $ts=t^{-1}s^{-1}= r^{-1}$, so $g=r ^{-i}=r^{n-i}=r^{-i \mod n}$, or $g=r ^{-i}t=r^{-i}sr=r ^{-i-1}s=r ^{-i-1\mod n}s$
So also proved...




