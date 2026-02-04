We say that two square [[Matrices|matrices]] $A$ and $B$ are similar, written $A\sim B$, if there exists an [[Matrix Inverses|invertible matrix]] $M$ such that $A=MBM^{-1}$
## Similarity is an [[Equivalence Relation|Equivalence Relation]]
We can think of this as saying that $A$ and $B$ represent the same transformation
### Proof
- Reflexive?
Yes we can take $M=I$, and then $A=A$
- Symmetric?
Yes, since if $A=MBM^{-1}\implies M^{-1}AM=B$, so we take $N=M^{-1}$, and then we have what we want
- Transitive?
If $A=M^{-1}BM$, and $B=N^{-1}CN$, then $A=M^{-1}N^{-1}CNM$, and hence we havve triansitivity with $C=MN$, as the product of invertible matrices is invertible
___
So the [[Sets|set]] of all $n\times n$ matrices gets partitioned into equivalence classes (or for matrices similarity classes):
$$
[A]=\{ B|B\sim A\iff B=MAM^{-1}\text{ for some }M\in GL(n,\mathbb{R}) \}
$$
Where $GL(n,\mathbb{R})$ simply denotes the [[Groups|group]] of invertible $n\times n$ matrices with real coefficients;
$$
GL(n,\mathbb{R})=\{ M\in M_{n}(\mathbb{R})|\det(M)\neq 0 \}
$$
# 
___
## Similar Matrices have the same [[Eigenvalues|Eigenvalues]]
### Proof
Suppose $A=MBM^{-1}$, then the characteristic polynomial of $A$ is 
$$
p_{A}(t)=\det(A-tI)=\det(M(B-tI)M^{-1})=\det (M)\det(B-tI)\det (M^{-1})
$$
$$
= \det(M)\det(B-tI)\det(M)^{-1}=\det(B-tI)
$$
So their characteristic polynomials are the same, so must have the same roots and thus the same eigenvalues