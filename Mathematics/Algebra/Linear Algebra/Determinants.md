A determinant is a [[Functions|funciton]]:
$$
\det:M_{n}(\mathbb{R})\to \mathbb{R}
$$
$$
 A\mapsto \det(A)=|A|
$$
This determines whether a [[Matrices|matrix]] is [[Matrix Inverses|invertible]]:
$A$ is invertible "non-singular" iff $\det(A)\neq 0$
## Guess the Definition :)
If $n=1$, we can guess:
$$
\det((a))=a
$$
___
$n=2$ we can show that if
$$
A=\begin{pmatrix}
a&b\\c&d
\end{pmatrix}
$$
is invertible iff $ad-bc\neq 0$
So:
$$
\det \begin{pmatrix}
a&b\\c&d
\end{pmatrix}=ad-bc
$$
___
$n=3$, suppose we write:
$$
A=\begin{pmatrix}
a_{1}&a_{2}&a_{3}\\b_{1}&b_{2}&b_{3}\\c_{1}&c_{2}&c_{3}
\end{pmatrix}
$$
Say we have:
$$
\underline{a}=\begin{pmatrix}
a_{1}\\a_{2}\\a_{3}
\end{pmatrix},\underline{b}=\begin{pmatrix}
b_{1}\\b_{2}\\b_{3}
\end{pmatrix},\underline{c}=\begin{pmatrix}
c_{1}\\c_{2}\\c_{3}
\end{pmatrix}
$$
$A$ is invertible iff $A\underline{x}=\underline{0}$ as shown in this [[Gauss-Jordan Elimination#Theorem|theorem]], so it is invertible iff:
$$
a_{1}x+a_{2}y+a_{3}z=0
$$
$$
 b_{1}x+b_{2}y+b_{3}z=0
$$
$$
c_{1}x+c_{2}y+c_{3}z=0
$$
Have a unique solution iff the [[Scalar Triple Product|scalar triple product]] is non-zero from what we know about [[Points in R3|points in $\mathbb{R}^3$]], so iff
$$
\begin{pmatrix}
a_{1}\\a_{2}\\a_{3}
\end{pmatrix}\cdot \begin{pmatrix}
b_{2}c_{3}-b_{3}c_{2}\\b_{3}c_{1}-b_{1}c_{3}\\b_{1}c_{2}-b_{2}c_{1}
\end{pmatrix}\neq 0
$$
$$
 \iff a_{1}\det \begin{pmatrix}
b_{2}&b_{3}\\c_{2}&c_{3}
\end{pmatrix}-a_{2}\det \begin{pmatrix}
b_{1}&b_{3}\\c_{1}&c_{3}
\end{pmatrix}+a_{3}\det \begin{pmatrix}
b_{1}&b_{2}\\c_{1}&c_{2}
\end{pmatrix}\neq 0
$$
___
## Recursive Definition
We can see that these are sort of following a pattern, that for the first row, you multiply the first element by the determinant of the matrix you obtain by ignoring the row and column of that element, then alternate negatives and positives
Based on this, we can give an inductive definition of a determinant:
Let $A=(a_{ij})\in M_{n}(\mathbb{R})$
For $1\leq r,s\leq n$, we let $A_{r,s}$ be the $(r,s)$th [[Matrix Minor|minor]] of $A$, which is the $(n-1)\times (n-1)$ matrix obtained by deleting the $r$th row and $s$th column of $A$
Let $\det(A_{r,s})$ be the $(r,s)$th unsigned cofactor of $A$, then $(-1)^{r+s}\det(A_{r,s})$ is the signed cofactor
Using this we can inductively define $\det A$ by setting:
$$
\det A=\sum_{ j=1} ^{ n} (-1)^{1+j} a_{1j}\det(A_{1,j})
$$
### Proposition
If $A\in M_{n}(\mathbb{R})$ and $1\leq i\leq n$, then we can in fact expand on any row (not just the first)
$$
\det(A)=\sum_{ j=1} ^{ n}  (-1)^{i+j}a_{ij}\det(A_{i,j})
$$
#### Proof
This proof is via [[Proof by Mathematical Induction!!!!!|induction]] on $n$. For notational convenience, let
$$
\det_{i}(A):=\sum_{ k=1} ^{ n}  (-1)^{i+k}a_{ik}\det(A_{i,k})
$$
We wish to show $\det_{i}(A)=\det (A)$. In the case $n=2$, it is easy to chec k we have $\det_{2}=\det$, indeed
$$
\det_{2}(A)=\sum_{k=1}^{2}(-1)^{2+k}a_{2k}\det(A_{2,k})=-a_{21}\det(a_{12})+a_{22}\det(a_{11})=a_{11}a_{22}-a_{12}a_{21}=\det(A)
$$
This is the base case
So let's assume that we know for any $(n-1)\times(n-1)$ matrix, we have $\det_{i}=\det$ for $1\leq i\leq n-1$. Let $A$ be an $n\times n$ matrix and suppose $2\leq i\leq n$. For integers $k$ and $l$ between $1$ and $n$, notice (by thinking about what it means to be a minor) that the minors of the minors satisfy:
- if $l<k$, then we have $(A_{i,k})_{1,l}=(A_{1,l})_{i-1,k-1}$
- if $k<l$, then we have $(A_{i,k})_{1,l-1}$ 
## Columns
If we had tried to develop the theory of determinants by expanding along columns rather than rows, we would have arrived at a function:
$$
\text{coldet}:M_{n}(\mathbb{R})\to \mathbb{R}
$$
It turns out that we would get $\text{coldet}=\det$
Equivalently we have:
$$
\det(A^{\top})=\det (A)
$$
For all square matrices
### Proof
Apply EROs $E_{1},E_{2},\dots,E_{r}$ to $A$ to get RREF $A'$:
$$
A'=E_{r}\dots E_{2}E_{1}A
$$
Then
$$
A=E_{1}^{-1}E_{2}^{-1}\dots E_{r}^{-1}A'
$$
Recall each $E_{i}^{-1}$ is also elementary, then
$$
\det(A^{\top})=\det((A')^{\top}(E_{r}^{-1})^{\top}\dots(E_{2}^{-1})^{\top}(E_{1}^{-1})^{\top})
$$
$$
=\det((E_{r}^{-1})^{\top}\dots(E_{2}^{-1})^{\top}(E_{1}^{-1})^{\top})
$$
If $A$ is invertible, since then $A'=I_{n}$, so $(A')^{\top}=I_{n}$
$$
\det(E_{r}^{-1})\dots \det(E_{2}^{-1})\det( E_{1}^{-1})=\det(E_{1}^{-1}E_{2}^{-1}\dots E_{r}^{-1}A')=\det (A)
$$
Since $\det(E^{\top})=\det(E)$ can be checked for $E$ elementary, so $E^{\top}$ is elementary if $E$ is elementary
If $A$ is not invertible, then neither is $A^{\top}$, so $\det(A)=0=\det(A^{\top})$
## Fundamental Poperties of the Determinant
The determinant is the unique function that satisfies these properties
Let $A\in M_{n}(\mathbb{R})$, let $\underline{a}_{r}$ be the $r$th row vector of $A$:
$$
\underline{a}_{r}=\begin{pmatrix}
a_{r_{1}}&a_{r_{2}}&\dots&a_{r_{n}}
\end{pmatrix}
$$
So
$$
A=\begin{pmatrix}
\underline{a}_{1}\\\underline{a}_{2}\\\vdots\\\underline{a}_{n}
\end{pmatrix}
$$
The properties are:
- $\det(I_{n})=1$
- $\det(M_{r}(\lambda)A)=\lambda \det(A)$, where $M_{r}(\lambda)$ is the [[Gauss-Jordan Elimination|ERO]] 
 $$
\det(M_{r}(\lambda)A)=\det \begin{pmatrix}
\underline{a}_{1}\\\vdots\\\lambda\underline{a}_{r}\\\vdots\\\underline{a}_{n}
\end{pmatrix}=\lambda \det\begin{pmatrix}
\underline{a}_{1}\\\vdots\\\underline{a}_{r}\\\vdots\\\underline{a}_{n}
\end{pmatrix}=\lambda \det(A)
$$
- For any vector $\underline{b}_{r}$, we have
$$
\det\begin{pmatrix}
\underline{a}_{1}\\\vdots\\\underline{a}_{r}+\underline{b}_{r}\\\vdots\\\underline{a}_{n}
\end{pmatrix}=\det\begin{pmatrix}
\underline{a}_{1}\\\vdots\\\underline{a}_{r}\\\vdots\\\underline{a}_{n}
\end{pmatrix}+\det\begin{pmatrix}
\underline{a}_{1}\\\vdots\\\underline{b}_{r}\\\vdots\\\underline{a}_{n}
\end{pmatrix}
$$
    Combining this with the previous one we have linearity in each row
- $\det(P_{rs}A)=-\det A$ where $P_{rs}$ is the ERO swapping $r$th and $s$th rows of $A$
- If $A$ has two equal (or even collinear) rows then $\det (A)=0$
- $\det(A)=0$ if $A$ has a row of zeroes
- $\det(A_{rs}(\lambda)A)=\det A$:
$$
\det(A_{rs}(\lambda)A)=\det\begin{pmatrix}
\underline{a}_{1}\\\vdots\\\underline{a}_{r}\\\vdots\\\underline{a}_{s}+\lambda  \underline{a}_{r}\\\vdots\\\underline{a}_{n}
\end{pmatrix}=\det\begin{pmatrix}
\underline{a}_{1}\\\vdots\\\underline{a}_{r}\\\vdots\\\underline{a}_{s}\\\vdots\\\underline{a}_{n}
\end{pmatrix}=\det(A)
$$
### Proof
#### First Property:
Induction on $n$
Let $n=1$, $\det(1)=1$ so base case is true
Also, expanding $\det(I_{n})$ along the top row gives:
$$
\det(I_{n})=(I_{n})_{11}(-1)^{1+1}\det(I_{n-1})=\det(I_{n-1})
$$
Since all other terms are $\hspace{0pt}0$, so proved by induction
#### Second Property
Expand along $r$th row:
$$
\det(M_{r}(\lambda)A)=\sum_{ j=1} ^{ n}  (-1)^{r+j}\lambda a_{rj}\det(A_{r,j})
$$
And note that deleting the $r$th row of the matrix $M_{r}(\lambda)A$ gives the same matrix as doing the same to $A$, so:
$$
\det(M_{r}(\lambda)A)=\lambda \sum_{ j=1} ^{ n}  (-1)^{r+j}\det(A_{r,j})=\lambda \det A
$$
#### Third Property
Expand along $r$th row
#### Fourth Property
H/W
#### Fifth Property
First note that if row $r$ is collinear to row $s$, then by $M_{r}(\lambda)$, for some $\lambda$, we obtain a matrix with two equal rows. If the $r$th row of $A$ equals the $s$th row of $A$, then
$$
\det(A)=\det(P_{rs}(A))=-\det(A)
$$
$$
\implies \det(A)=0
$$
#### Sixth Property
Expand along the $\hspace{0pt}0$ row, giving each term is zero, so the determinant is 0
#### Seventh Property
Write $B$ for the matrix that I get by replacing the $s$th row of $A$ with another copy of the $r$th row of $A$. Then $\det(B)=0$ by the 5th property, so:
$$
\det(A_{rs}(\lambda)A)=\det(A)+\det(M_{r}(\lambda)B)=\det (A)+\lambda \det(B)=\det(A)
$$
## If a Function Satisfies the Above Properties, then the Function must be the Determinant
Let $f:M_{n}(\mathbb{R})\to \mathbb{R}$ that satisfies this list of properties, then $f(A)=\det (A)$, in other words these properties characterise $\det$
### Proof
Let $A\in M_{n}(\mathbb{R})$, we can run the Gauss-Jordan algorithm to get the RREF $B$, As $f$ and $\det$ satisfy properties $\hspace{0pt}2$,$\hspace{0pt}4$,$\hspace{0pt}5$,$\hspace{0pt}7$ as we apply EROs, $f$ and $\det$ change in the same way, so:
$$
\det (A)=\lambda_{1}\lambda_{2}\dots\lambda_{k}\det(B)
$$
$$
f(A)=\lambda_{1}\lambda_{2}\dots\lambda_{k}f(B)
$$
where $\lambda_{i}\neq 0$
Then either $B=I_{n}$ in which case $\det (A)=f(A)$ or $B$ has a row of 0's so $\det(B)=0$ and $f(B)=0$, by the 4th property
Hence $\det (A)=f(A)$
___
## Calculations
We know how $\det$ changes under EROs:
- $A_{rs}(\lambda)$ doesn't change $\det$
- $M_{r}(\lambda)$: $\det(M_{r}(\lambda)A)=\lambda \det(A)$
- $P_{rs}$: $\det(P_{rs}A)=-\det(A)$

Note EROs change $\det$ by non-zero multiples, so if we apply some EROs to $A$, including $M_{r_{i}}(\lambda_{i})$ for $i=1,\dots,s$ and $t$ occurences of $P_{ab}$ resulting in $A'$, then
$$
\det(A')=\lambda_{1}\lambda_{2}\dots\lambda_{s}(-1)^{t}\det(A)
$$
If $A'$ is in RREF (for example), then $\det(A')=1$ if $A'=I_{n}$ and $\det(A)=0$ otherwise, so then we can read off $\det(A)$
### Proposition
If $A\in M_{n}(\mathbb{R})$ which is upper-triangular (i.e. $A_{ij}=0$ for $i>j$, so only has entries on or above the leading diagonal), then $\det(A)=\prod_{ i=1} ^{ n}a_{ii}=a_{11}a_{22}\dots a_{nn}$
#### Proof
induct :)
#### Use
We now only want to put $A'$ in upper triangular form to find $\det (A)$
#### Examples
![[Determinants 2024-11-11 11.22.40.excalidraw]]
So $\det(A')=1\times 1\times 2=2$, so:
$$
\det(A)=(-1)\det(A')=-2
$$
Since we only did one $P_{rs}$ and no $M_{r}(\lambda)$
___
![[Determinants 2024-11-11 11.45.31.excalidraw]]
Obtained by taking factors $a,b,c$ out of each column
![[Determinants 2024-11-11 11.47.01.excalidraw]]
By performing column operations $\text{col}A_{12}(-1)$ and $\text{col}A_{13}(-1)$
![[Determinants 2024-11-11 11.48.48.excalidraw]]
By expanding along row 1
![[Determinants 2024-11-11 11.49.51.excalidraw]]
By taking factors $(b-a),(c-a)$ out of each column
$$
=abc(b-a)(c-a)(c^{2}+ca+a^{2}-b^{2}-ab-a^{2})=abc(b-a)(c-a)(c^{2}+ac-ab-b^{2})
$$
$$
= abc(b-a)(c-a)(c-b)(a+b+c)
$$
## Areas and Volumes
### $n=2$
Consider [[Vectorspace Rn|$\mathbb{R}^2$]], 
![[Determinants 2024-11-12 11.43.48.excalidraw]]
We have a parallelogram with vertices $0,\underline{v},\underline{w},\underline{v}+\underline{w}$, it has an area we can obtain by considering two equal triangles of:
$$
\text{Area}(P)=|\underline{v}||\underline{w}|\sin\theta
$$
Now imagine $\mathbb{R}^{2}\times \{ 0 \}\subseteq \mathbb{R}^3$:
![[Determinants 2024-11-12 11.47.05.excalidraw]]
So this is that same parallelogram, but with one coordinate $\hspace{0pt}0$
$$
\underline{v}=\begin{pmatrix}
a\\c\\0
\end{pmatrix},\underline{w}=\begin{pmatrix}
b\\d\\0
\end{pmatrix}
$$
So,
$$
\text{Area}(P)=|\underline{v}| |\underline{w}|\sin\theta=|\underline{v} \times \underline{w}|
$$
$$
=\left|\begin{pmatrix}
a\\c\\0
\end{pmatrix}\times \begin{pmatrix}
b\\d\\0
\end{pmatrix}\right|=\left| \begin{pmatrix}
0\\0\\ad-bc
\end{pmatrix}\right|=|ad-bc|=|\det(\underline{v}\underline{w})=\left|\det \begin{pmatrix}
a&b\\c&d
\end{pmatrix}\right|
$$
Note that, by considering where you put the second triangle to construct the parallelogram,
$$
|\det \begin{pmatrix}
\underline{v}&\underline{w}
\end{pmatrix}|=|\det \begin{pmatrix}
\underline{v}&\underline{v}+\underline{w}
\end{pmatrix}|=|\det \begin{pmatrix}
\underline{w}&\underline{v}+\underline{w}
\end{pmatrix}|
$$
#### Example
Find the area of the trianle $T\subseteq \mathbb{R}^{2}$ with vertices:
$$
\underline{a}=\begin{pmatrix}
2\\5
\end{pmatrix},\underline{b}=\begin{pmatrix}
-1\\3
\end{pmatrix},\underline{c}=\begin{pmatrix}
1\\2
\end{pmatrix}
$$
![[Determinants 2024-11-12 11.52.56.excalidraw]]
So
$$
T=\frac{1}{2}\text{Area}(\text{Parallelogram})=\frac{1}{2}\left|\det \begin{pmatrix}
\underline{b}-\underline{a}&\underline{c}-\underline{a}
\end{pmatrix}\right|
$$
$$
= \frac{1}{2}\left| \det \begin{pmatrix}
-3&-1\\-2&-3
\end{pmatrix}\right|=\frac{1}{2}|9-2|=\frac{7}{2}
$$
Note we can change where we put the triangle to get the same area in different ways, as above
### $n=3$
Consider the parallelopiped formed by $\hspace{0pt}3$ non collinear vectors $\underline{u},\underline{v},\underline{w}$:
![[Determinants 2024-11-14 18.44.56.excalidraw]]
Let $P'$ be a pivot unit vector perpendicular to the base, $\theta$ is the angle between $P'$ and $\underline{w}$
$$
\text{Volume}(P)=|\underline{v}\times \underline{u}||\underline{u}| |\cos\theta|=|\underline{v}\times \underline{u}| |\underline{u}|\left| \frac{\underline{u}\cdot(\underline{v}\times \underline{w})}{|\underline{u}| |\underline{v}\times \underline{w}|}\right|=|\underline{u}\cdot(\underline{v}\times \underline{w})|
$$
$$
=| \det \begin{pmatrix}
\underline{u}&\underline{v}&\underline{w}
\end{pmatrix}|
$$
Similarly to when $n=2$, we can form equivalent expressions by icking any $\hspace{0pt}3$ non-zero vertices of $P$, 
$$
\{ \underline{a},\underline{b},\underline{c} \}\subseteq \{ \underline{u},\underline{v},\underline{w},\underline{u}+\underline{v},\underline{u}+\underline{w},\underline{v}+\underline{w},\underline{u}+\underline{v}+\underline{w} \}
$$
Then
$$
\left|\det \begin{pmatrix}
\underline{a}&\underline{b}&\underline{c}
\end{pmatrix}\right|
$$
Is either $\text{Volume}(P)$ when $\underline{a},\underline{b},\underline{c}$ are not coplanar or $0$ when $\underline{a},\underline{b},\underline{c}$  are the vertices of a face of $P$, in fact 
$$
\det \begin{pmatrix}
\underline{a}&\underline{b}&\underline{c}
\end{pmatrix}=0
$$
When $\underline{a},\underline{b},\underline{c}$ are coplanar as the parallelopiped they span would have no volume
## Higher $n$
This generalises for higher $n$, so one can find the volume of the shape 'spanned' by $\underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k}\in\mathbb{R}$ to be
$$
|\det \begin{pmatrix}
\underline{u}_{1}&\underline{u}_{2}&\dots&\underline{u}_{k}
\end{pmatrix}|
$$



#Mathematics #LinAlg #Functions #Definition #Theorem 
