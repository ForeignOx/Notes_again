Let [[Matrices|$A\in M_{n}(\mathbb{R})$]], we say that $A$ is invertible iff there exists $B\in M_{m}(\mathbb{R})$ such that:
$$
AB=I=BA
$$
If such a $B$ exists, we call it the inverse of $A$, and denote it $A^{-1}$
## Properties
- A matrix has at most $\hspace{0pt}1$ inverse, so if an inverse exists, it must be unique
### Proof
Suppose $B,C$ are inverrses for a matrix $A\in M_{n}(\mathbb{R})$, so
$$
B=BI_{n}=B(AC)=(BA)C=I_{n}C=C
$$
So $B$ and $C$ must be equal
# 
___
- If $A,B \in M_{n}(\mathbb{R})$ are invertible, then $AB$ is also invertible: $(AB)^{-1}=B^{-1}A^{-1}$
- If $A\in M_{n}(\mathbb{R})$ is invertible, then so is [[Transpose|$A^{\top}$]]: $(A^{\top})^{-1}=(A^{-1})^{\top}$
### Proof
$$
A^{\top}(A^{-1})^{\top}=(A^{-1}A)^{\top}=(I_{n})^{\top}=I_{n}
$$
And
$$
(A^{-1})^{\top}A^{\top}=(AA^{-1})^{\top}=(I_{n})^{\top}=I_{n}
$$
So $(A^{-1})^{\top}=(A^{\top})^{-1}$
# 
___
- If $A,B\in M_{n}(\mathbb{R})$ and $AB=I_{n}$, then $BA=I_{n}$, $B=A^{-1}$ and $A=B^{-1}$

## Computing the Inverse
Consider a matrix $A\in M_{n}(\mathbb{R})$, we perform the following steps:
- First form an [[Augmented Matrices|augmented matrix]] $(A|I_{n})$
- Second run the [[Gauss-Jordan Elimination|Gauss-Jordan algorithm]], i.e. left multiply by a sequence of elementary matrices $E_{1},E_{2},\dots,E_{r}(=I_{n})$
- If $A$ is invertible, it will become $I_{n}$ by [[Gauss-Jordan Elimination#Theorem|this theorem]] 
So we have:
$$
E_{r}\dots E_{2}E_{1}(A|I_{n})
$$
$$
= (E_{r}\dots E_{2}E_{1}A|E_{r}\dots E_{2}E_{1})
$$
$$
= (I_{n}|E_{r}\dots E_{2}E_{1})
$$
$$
= (I_{n}|A^{-1})
$$
Note that if $A$ was not invertivle, then LHS would not become $I_{n}$ (RREF of $A$ is not $I_{n}$)
## [[Determinants|Determinants]]
$A\in M_{n}(\mathbb{R})$ then $A$ is invertible iff $\det(A)\neq 0$
### Proof
We apply EROs $E_{1},E_{2},\dots ,E_{r}$ to $A$ so that $A'=E_{r}\dots E_{2}E_{1}A$ is in RREF so there exists non-zero factors $M_{1},M_{2},\dots,M_{r}$ such that
$$
\det(A')=M_{r}\dots M_{2}M_{1}\det(A)
$$
Since EROs change $\det$ by non-zero factors
A is invertible iff $A'=I_{n}$ iff $\det(A')\neq 0$, since $A'$ is in RREF (and if it is not $I_{n}$, then it must have a row of zeros) iff $\det(A)\neq 0$ by the observation above

#Mathematics #LinAlg #Definition