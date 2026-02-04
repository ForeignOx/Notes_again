## Definition
Take a [[Rings|commutative ring]], [[Natural Numbers|$n\in\mathbb{N}$]], then the general [[Linear|Linear]] [[Groups|group]] $GL_{n}(R)$ is defined as:
$$
GL_{n}(R)=\left\{ A\in M_{n}(R)\mid \det(A)\in R^{\times} \right\}
$$
## Remark
If we have some [[Fields|field]] $\mathbb{F}$, then $\mathbb{F}^{\times}=\mathbb{F}\setminus \left\{ 0 \right\}$, so 
$$
GL_{n}(\mathbb{F})=\left\{ A\in M_{n}(\mathbb{F})\mid \det(A)\neq 0 \right\}
$$
So the [[Real Numbers|real]] general linear [[Groups|group]] is the set of [[Matrix Inverses|invertible]] real [[Matrices|matrices]] under matrix multiplication and is denoted $GL_{n}(\mathbb{R})$
## Showing it is a Group
We have that $\det:GL_{n}(R)\to R$ is a [[Homomorphisms|homomorphism]] of goups, in particular, $\text{ker}(\det)=SL_{n}(R)$, so by the [[First Isomorphism Theorem|first isomorphism theorem]]:
$$
GL_{n}(R) /SL_{n}(R)\cong R^{\times}
$$
## Example
If $R=\mathbb{R},\mathbb{C}$ these are Lie groups
If $R=\mathbb{Z}$, then $\mathbb{Z}^{\times}=\left\{ \pm 1 \right\}$, so [[Index of Groups|$[GL_{n}(\mathbb{Z}):SL_{n}(\mathbb{Z})]=2$]]
For a finite field $F_{q},\left| F_{q} \right|=q$, then what is $\left| GL_{2}(F_{q}) \right|$ and $\left| SL_{2}(F_{q}) \right|$?
If $A\in GL_{2}(F_{q})$, then
$$
A=\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$
Then consider the rows as vectors $\underline{v}_{1}=(a,b)\in F_{q}^{2},\underline{v}_{2}=(c,d)\in F_{q}^{2}$
Then $\det A=0 \iff$ $\underline{v}_{1}$ and $\underline{v}_{2}$ are [[Linear Independence|linearly dependent]] $\iff \underline{v}_{1}=\lambda \underline{v}_{2}$
Our possible choices for $\underline{v}_{1}$ is $q^{2}-1$ as it is all except $(0,0)$ and for $\underline{v}_{2}$ the choices are $q^{2}-q$ which are multiples of $v_{1}$
Soo
$$
\left| GL_{2}(F_{q}) \right| =(q^{2}-1)(q^{2}-q)
$$
$$
 \left| SL_{2}(F_{q}) \right| =\frac{\left| GL_{2}(F_{q}) \right| }{q-1}=q(q^{2}-1)
$$
As
$$
GL_{2}(F_{q}) /SL_{2}(F_{q})\cong F_{q}^{\times}
$$
by the FIT
Now, we can compute $\left| GL_{n}(F_{q}) \right|,\left| SL_{n}(F_{q}) \right|$ using the same method, the rows are elements of $F_{q}^{n}$, the number of choices is then
- First row: $q^{n}-1$
- Second row: $q^{n}-q$
- Third row: $q^{n}-q^{2}$
- $n$th row: $q^{n}-q^{n-1}$
