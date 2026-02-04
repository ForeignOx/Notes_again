We consider a [[Systems of Linear Equations|system of linear equations]] with $m$ equations in $n$ unkowns ($x_{i}$'s are the unknowns)
$$
a_{11}x_{1}+a_{12}x_{2}+\dots+a_{1n}x_{n}=b_{1}
$$
$$
a_{21}x_{1}+a_{22}x_{2}+\dots+a_{2n}x_{n}=b_{2}
$$
$$
\vdots
$$
$$
a_{m1}x_{1}+a_{m2}x_{2}+\dots+a_{mn}x_{n}=b_{m}
$$
Which can be written:
$$
\sum_{ j=1} ^{ n}   a_{ij}x_{j}=b_{i}
$$
For $i=1,\dots,m$
The way to solve this is to epress the system as an [[Augmented Matrices|augmented matrix]], then perform operations known as ERO's (Elementary Row Operations) to the matrix without changing the solution set, which will turn the augmented matrix into RREF (Row Reduced Echolon Form) using the Gauss-Jordan algorithm, which allows us to then read off the solution set
Note that non-leading 1's correspond to free variables
If $A=(a_{ij})_{m\times n}$, then $A$ is known as the matrix of coefficients:
$$
A=\begin{pmatrix}
a_{11}&a_{12}&\dots&a_{1j}&\dots& a_{1n}\\a_{21}&a_{22}&\dots&a_{2j}&\dots& a_{2n}\\\vdots&\vdots&&\vdots& & \vdots\\a_{i1}&a_{i2}&\dots&a_{ij}&\dots& a_{in}\\\vdots&\vdots&&\vdots& & \vdots\\a_{n1}&a_{m2}&\dots&a_{mj}&\dots& a_{mn}
\end{pmatrix}
$$
$$
\underline{x}=\begin{pmatrix}
x_{1}\\x_{2}\\\vdots\\x_{i}\\\vdots\\x_{n}
\end{pmatrix},\underline{b}=\begin{pmatrix}
b_{1}\\b_{2}\\\vdots\\b_{i}\\\vdots\\b_{n}
\end{pmatrix}
$$
The system of equations is:
$$
A\underline{x}=\underline{b} 
$$
We are thus looking for 
$$
\{ \underline{x}\in \mathbb{R}^{n}\mid A\underline{x}=\underline{b} \}
$$
If $\underline{b}=\underline{0}$, we call the system homogeneous, if $\underline{b}\neq  \underline{0}$, we call it inhomogeneous, if $\underline{b}$ is homogeneous, there is always a solution $\underline{x}=0$
So we make the augmented matrix of the system is $(A|\underline{b})$:
$$
(A|\underline{b})=\left(\begin{array}{cccccc|c}
a_{11}&a_{12}&\dots&a_{1j}&\dots& a_{1n}&b_{1}\\a_{21}&a_{22}&\dots&a_{2j}&\dots& a_{2n}&b_{2}\\\vdots&\vdots&&\vdots& & \vdots&\vdots\\a_{i1}&a_{i2}&\dots&a_{ij}&\dots& a_{in}&b_{i}\\\vdots&\vdots&&\vdots& & \vdots&\vdots\\a_{n1}&a_{m2}&\dots&a_{mj}&\dots& a_{mn}&b_{n}
\end{array}\right)
$$
## Example
$$
x+y+w=1
$$
$$
x-w=0
$$
$$
x+y+z-w=2
$$
$$
x+z+w=3
$$
Is a system of equations which can be written as:
$$
1\times x+1\times y+0\times z+1\times w=1
$$
$$
1\times x+0\times y+0\times z+(-1)\times w=0
$$
$$
1\times x+1\times y+1\times z+(-1)\times w=2
$$
$$
1\times x+0\times y+1\times z+1\times w=3
$$
Which can be written as the augmented matrix:
$$
\left(
\begin{array}{cccc|c}
1&1&0&1&1\\
1&0&0&-1&0\\
1&1&1&-1&2\\
1&0&1&1&3
\end{array}
\right)
$$
## Lemma
Let $A\in M_{n}(\mathbb{R})$ and $\underline{v}\in\mathbb{R}^{n},\underline{v}\neq 0$ such that $A\underline{v}=\underline{0}$, then $A$ is not [[Matrix Inverses|invertible]] i.e. is singular
If $A\in M_{n}(\mathbb{R})$ is invertible, then the system $A\underline{x}=\underline{b}$ has a unique solution
### Proof
Assume $A^{-1}$ exists, then:
$$
\underline{v}=I_{n}\underline{v}=A^{-1}(A\underline{v})=A^{-1}\underline{0}=\underline{0}
$$
Which is a contradiction to $\underline{v}\neq  \underline{0}$
$$
A\underline{x}=\underline{b}\iff A^{-1}A\underline{x}=A^{-1}\underline{b}\iff \underline{x}=A^{-1}\underline{b}
$$
And $A^{-1}\underline{b}$ exists and is unique
## Gauss-Jordan Algorithm
### EROs
Each ERO is a function:
$$
M_{m\times n}(\mathbb{R})\to M_{m\times n}(\mathbb{R})
$$
They are:
- $P_{rs}$ interchanges row $r$ with row $s$ (the $P$ stands for 'permute')
- $M_{r}(\lambda)$ multiplies the elements in the $r$th row by $\lambda \neq 0$
- $A_{rs}(\lambda)$ adds $\lambda \in\mathbb{R}$ times the $r$th row to the $s$th row
## More Stuff
### Lemma
If $B\in M_{m}(\mathbb{R})$ is invertible, then the system $A\underline{x}=\underline{b}$ has the same solution set as:
$$
(BA)\underline{x}=B\underline{b}
$$
#### Proof
First note that if $A\underline{x}=\underline{b}$, then
$$
(BA)\underline{x}=B(A\underline{x})=B(\underline{b})=B\underline{b}
$$
Also if $(BA)\underline{x}=B\underline{b}$:
$$
A\underline{x}=(B^{-1}B)A\underline{x}=B^{-1}(BA)\underline{x}=B^{-1}(B\underline{b})=\underline{b}
$$
$w^{5}$
### ERO's do not change the solution set
This lemma is why performing ERO's in the [[Gauss-Jordan Elimination|Gauss-Jordan algorithm]] does not change the solution set
#### Proof
By the Lemma, it is enough to see that ERO's can be performed by left multiplication by invertible matrices, so we want to find invertible matrices corresponding to the ERO's
- The ERO $P_{rs}$ can be performed by left multiplication by the matrix denoted $P_{rs}$ (which is a bit of an abuse of notation but oh well) which is obtained from $I_{m}$ by exchanging the $r$th and $s$th rows
$$
(P_{rs})_{ij}=\begin{cases}
1&\text{if }i=j,i\neq r,s\\1&\text{if }i=r,j=s\\1&\text{if }i=s,j=r\\0&\text{otherwise}
\end{cases}
$$
    one can check that $(P_{rs})^{-1}=P(rs)$
- The matrix $M_{r}(\lambda)$ is given by 
$$
(M_{r}(\lambda))_{ij}=\begin{cases}
1&\text{if }i=j\neq r\\\lambda&\text{if }i=j=r\\0&\text{otherwise}
\end{cases}
$$
    similarly one can check that $(M_{r}(\lambda))^{-1}=M_{r}\left( \frac{1}{\lambda} \right)$
- The matrix $A_{rs}(\lambda)$ is given by
$$
(A_{rs}(\lambda))_{ij}=\begin{cases}
1&\text{if } i=j\\\lambda&\text{if }i=s,j=r\\0&\text{otherwise}
\end{cases}
$$
    one can check that $(A_{rs}(\lambda))^{-1}=A_{rs}(-\lambda)$
### Lemma
Let $A\in M_{n}(\mathbb{R})$ be a square matrix, then the following statements are each equivalent to one another
- In each column of the [[Row Reduced Echelon Form|RREF]] of $A$, there is a leading 1
- The RREF of $A$ is $I_{n}$
- The only solution to $A\underline{x}=\underline{0}$ is $\underline{x}=\underline{0}$
#### Proof
Statement $\hspace{0pt}2$ implies $\hspace{0pt}1$ clearly, also $\hspace{0pt}1$ implies $\hspace{0pt}2$ since all non-leading $\hspace{0pt}1$ entries in columns with leading 1's are $\hspace{0pt}0$ (and the leading 1's are arranged left to right and top to bottom)
$2\implies3$ Assume 2: the solution set to $A\underline{x}=\underline{0}$ agrees with the solution set to $I_{n}\underline{x}=\underline{0}$, i.e. $\underline{x}=\underline{0}$
$3 \implies 1$ If not each column had a leading $\hspace{0pt}1$, then the solution set would have free variables, so i.e. more than one solution
### Theorem
A square matrix $A\in M_{n}(\mathbb{R})$ is invertible iff any one of the conditions of this above lemma hold
#### Proof
Backwards direction:
If $A^{-1}$ exists, then:
$$
A\underline{x} =\underline{0}
$$
$$
\implies \underline{x}=A^{-1}(A\underline{x})=A^{-1}\underline{0}=\underline{0}
$$
So $\underline{x}=\underline{0}$ is the unique solution to $A\underline{x}=\underline{0}$
Forwards direction:
If the RREF of $A$ is $I_{n}$, then there exists a sequence of elementary matrices (which form the elementary row operations) $E_{1},E_{2},\dots,E_{r}$ such that:
$$
E_{r}\dots E_{2}E_{1}A=I_{n}
$$
From this we see that $B=E_{r}\dots E_{2}E_{1}$ is a left inverse for $A$, so we try to show that $AB=I_{n}$:
$$
AB=AE_{r}\dots E_{2}E_{1}
$$
$$
= (E_{1}^{-1}E_{2}^{-1}\dots E_{r}^{-1})\underbrace{ (E_{r}\dots E_{2}E_{1})A }_{ I_{n} }(E_{r}\dots E_{2}E_{1})
$$
$$
=(E_{1}^{-1}E_{2}^{-1}\dots E_{r}^{-1})(E_{r}\dots E_{2}E_{1})=I_{n}
$$
So $A^{-1}=B$
#### Corollary
Any invertivle matrix is a product of elementary matrices
##### Proof
Suppose $A\in M_{n}(\mathbb{R})$ is invertible and $A^{-1}=E_{r}\dots E_{2}E_{1}$ as above, then 
$$
A=(A^{-1})^{-1}=(E_{r}\dots E_{2}E_{1})^{-1}=E_{1}^{-1}E_{2}^{-1}\dots E_{r}^{-1}
$$
And inverses of elementary matrices are elementary
#### Corollary
If $BA=I_{n}$, then $AB=I_{n}$ ($A,B \in M_{n}(\mathbb{R})$)
##### Proof
Suppose $A\underline{x}=\underline{0}$, then:
$$
\underline{x}=BA\underline{x}=B \underline{0}=\underline{0}
$$
So by the theorem, we have that $A$ is invertible, so
$$
AB=AB(AA^{-1})=A(BA)A^{-1}=A A^{-1}=I_{n}
$$



#Mathematics #LinAlg 