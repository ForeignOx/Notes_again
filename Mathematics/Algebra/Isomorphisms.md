# Linear Algebra
## Definition
If $T:V\to W$ is a [[Bijective Functions|bijective]] [[Linear Maps|linear map]] (onto and 1-1), then we call $T$ an isomorphism and we call $V$ and $W$ isomorphic. We write $V\cong W$
## Lemma
If $T:V\to W$ is an isomorphism, then so is $T^{-1}:W\to V$ 
For the linear map $T:\mathbb{R}^{n}\to \mathbb{R}^m$ given by [[Matrices|$A\in M_{m\times n}(\mathbb{R})$]], we have $T$ is an isomorphism iff $A$ is invertible and then $T^{-1}(\underline{y})=A^{-1}\underline{y}$
### Proof
We essentially need to check that $T^{-1}$ is also a linear map
Let $\underline{w}_{1},\underline{w}_{2}\in W,\lambda \in\mathbb{R}$, then there exist unique $\underline{v}_{1},\underline{v}_{2}\in V$ such that $T(\underline{v}_{1})=\underline{w}_{1},T(\underline{v}_{2})=\underline{w}_{2}$, since $T$ is a bijection
Then
$$
\underline{w}_{1}+\underline{w}_{2}=T(\underline{v}_{1})+T(\underline{v}_{2})=T(\underline{v}_{1}+\underline{v}_{2})
$$
To which we apply $T^{-1}$:
$$
T^{-1}(\underline{w}_{1}+\underline{w}_{2})=\underline{v}_{1}+\underline{v}_{2}=T^{-1}(\underline{w}_{1})+T^{-1}(\underline{w}_{2})
$$
$$
\lambda \underline{w}_{1}=\lambda T(\underline{v}_{1})=T(\lambda \underline{v}_{1})
$$
Applying $T^{-1}$:
$$
T^{-1}(\lambda \underline{w}_{1})=\lambda \underline{v}_{1}=\lambda T^{-1}(\underline{w}_{1})
$$
Prove the second part here :)
## Fundamental Example
If $B$ is a [[Basis|basis]] for [[Vectorspaces|$V$]], $\{ \underline{v}_{1},\dots,\underline{v}_{n} \}$, then we have a [[Coordinates|coordinate]] map
$$
\Phi_{B}:V\to \mathbb{R}^{n}
$$
Where $\dim(V)=n$, $\Phi_{B}$ is an isomorphism:
$$
\lambda_{1}\underline{v}_{1}+\dots+\lambda_{n}\underline{v}_{n}\mapsto \begin{pmatrix}
\lambda_{1}\\\vdots\\\lambda_{n}
\end{pmatrix}
$$
### Proof
We have seen that $\Phi_{B}$ is linear, is it a bijection?
Check 1$\hspace{0pt}-1$, if
$$
\underline{v}=\lambda_{1}\underline{v}_{1}+\dots+\lambda_{n}\underline{v}_{1}
$$
$$
 \underline{w}=\mu_{1}\underline{v}_{1}+\dots+\mu_{n}\underline{v}_{n}
$$
Then $\Phi_{B}(\underline{v})=\Phi_{B}(\underline{w})$
$$
\implies \begin{pmatrix}
\lambda_{1}\\\vdots\\\lambda_{n}
\end{pmatrix}=\begin{pmatrix}
\mu_{1}\\\vdots\\ \mu_{n}
\end{pmatrix}
$$
$$
\implies \lambda_{i}=\mu_{i}
$$
$$
\implies \underline{v}=\underline{w}
$$
Now check onto, if
$$
\begin{pmatrix}
\lambda_{1}\\\vdots\\\lambda_{n}
\end{pmatrix}\in \mathbb{R}^{n}
$$
Then
$$
\Phi_{B}(\lambda_{1}\underline{v}_{1}+\dots+\lambda_{n}\underline{v}_{n})=\begin{pmatrix}
\lambda_{1}\\ \vdots\\\lambda_{n}
\end{pmatrix}
$$
Hence onto
## Matrix Representing Isomorphism
Suppose $V,W$ are finite dimensional with $\dim V=n,\dim W=m$, and we have bases $B$ for $V$ and $C$ for $W$, and suppose $T:V\to W$ is linear
We define the matrix $A\in M_{m\times n}(\mathbb{R})$ that represents $T$ with respect to $B$ and $C$ in the following way:
![[Isomorphisms 2024-12-10 11.21.07.excalidraw]]
We want this diagram to commute, so we want $A$ such that you can follow the arrows in either way to get to the same vectorspace, so
$$
A:\mathbb{R}^{n}\to \mathbb{R}^{n}
$$
Satistfying  
$$
\Phi_{C}\circ T=A\circ \Phi_{B}:V \to \mathbb{R}^{n}
$$
So we set:
$$
A=\Phi_{C}\circ T\circ \Phi_{B}^{-1}
$$
Note one can recover $T$ from $A$, as
$$
T=\Phi_{C}^{-1} \circ A \circ \Phi_{B}
$$
### Examples
What is the matrix representing
$$
\frac{d }{dx} :\mathbb{R}[x]_{4}\to \mathbb{R}[x]_{3}
$$
With respect to the standard bases
Consider the two maps:
$$
\Phi_{4}:a_{0}+a_{1}x+a_{2}x^{2}+a_{3}x^{3}+a_{4}x^{4}\mapsto \begin{pmatrix}
a_{0}\\a_{1}\\a_{2}\\a_{3}\\a_{4}
\end{pmatrix}
$$
$$
\Phi_{3}:a_{0}+a_{1}x+a_{2}x^{2}+a_{3}x^{3}\mapsto \begin{pmatrix}
a_{0}\\a_{1}\\a_{2}\\a_{3}
\end{pmatrix}
$$
$$
\left( \Phi_{3}\circ \frac{d }{dx} \circ \Phi_{4}^{-1} \right)\begin{pmatrix}
a_{0}\\a_{1}\\a_{2}\\a_{3}\\a_{4}
\end{pmatrix}=\left( \Phi_{3}\circ \frac{d }{dx}  \right)(a_{0}+a_{1}x+a_{2}x^{2}+a_{3}x^{3}+a_{4}x^{4})
$$
$$
= \Phi_{3}(a_{1}+2a_{2}x+3a_{3}x^{2}+4a_{4}x^{3})=\begin{pmatrix}
a_{1}\\2a_{2}\\3a_{3}\\4a_{4}
\end{pmatrix}
$$
So what is $A\in M_{4\times 5}(\mathbb{R})$?
$$
\begin{pmatrix}
A\underline{e}_{1}&\dots&A\underline{e}_{5}
\end{pmatrix}=\begin{pmatrix}
0&1&0&0&0\\0&0&2&0&0\\0&0&0&3&0\\0&0&0&0&4
\end{pmatrix}
$$
___
What is the matrix representing 
$$
F:M_{2}(\mathbb{R})\to M_{2}(\mathbb{R})
$$
$$
 F:A\mapsto A^{t}
$$
With respect to the standard bases?
$$
A\begin{pmatrix}
a\\b\\c\\d
\end{pmatrix}=\Phi\circ F\circ \Phi ^{-1} \begin{pmatrix}
a\\b\\c\\d
\end{pmatrix}
$$
$$
= \Phi\circ F\begin{pmatrix}
a&b\\c&d
\end{pmatrix}=\Phi \begin{pmatrix}
a&c\\b&d
\end{pmatrix}=\begin{pmatrix}
a\\c\\b\\d
\end{pmatrix}
$$
So 
$$
A=\begin{pmatrix}
1&0&0&0\\0&0&1&0\\0&1&0&0\\0&0&0&1
\end{pmatrix}
$$
### "Shortcut"
$$
A=\Phi_{B}\circ T\circ \Phi_{C}^{-1}
$$
$$
 A\underline{e}_{i}=(\Phi_{B} \circ T\circ \Phi_{C}^{-1})(\underline{e}_{i})=\Phi _{B}\circ T(\underline{v}_{i})
$$
Where $\underline{v}_{i}$ is the $i$th basis element of $e$, so
$$
A=\begin{pmatrix}
A\underline{e}_{1}&\dots&A\underline{e}_{n}
\end{pmatrix}=\begin{pmatrix}
\Phi_{B}T(\underline{v}_{1})&\Phi_{b}T(\underline{v}_{n})
\end{pmatrix}
$$
## Proposition
Suppose $T:V\to W$ is linear and $\phi:V'\to V$ and $\psi:W\to W'$ are isomorphisms, then we know the following about the [[Kernel|nullity]] and the [[Image|rank]]: 
$$
\text{rk}(\psi \circ T\circ \phi)=\text{rk}(T)
$$
$$
\text{null}(\psi \circ T\circ \phi)=\text{null}(T)
$$
### Proof
Since $\phi$ is onto, $\text{im}(\psi \circ T\circ \phi)=\text{im}(\psi \circ T)=\psi(\text{im}(T))$, but since $\psi$ is an isomorphism, it has the same dimension as $\text{im}(T)$, so since it is injective, by this [[Linear Maps#Corollary|this corollary]], it is equal
$\psi$ is 1$\hspace{0pt}-1$ so $\text{ker}(\psi \circ T\circ \phi)=\text{ker}(T\circ \phi)$, but $\text{ker}(T \circ \phi)=\phi ^{-1}(\text{ker}(T))$ which has the same dimension as $\text{ker}(T)$ by the corollary again
## Example
The map $(c_{1},c_{2},\dots ,c_{n})\to \sum_{i=0}^{n-1}c_{i+1}x^{i}$ is an isomorphism $\mathbb{R}^{n}\cong \mathbb{R}[x]_{n-1}$ 
# Group Theory
## Definition
Two [[Groups|groups]] are isomorphic ($G_{1} \cong G_{2}$) if there is a one-to-one mapping (isomorphism) that preserves the structure of the group. An isomorphism is a bijective [[Homomorphisms|homomorphism]] 
## Remarks
Two isomorphic groups are either both finite and of the same order or both infinite
Two isomorphic groups are either both [[Abelian Groups|abelian]] or both non-abelian
The identity elements of isomorphic groups are mapped to each other by the isomorphism
The inverses of corresponding elements are mapped to each other by the isomorphism
The inverses of the corresponding elements are mapped to each other by the isomorphism
The order of an element is preserved by isomorphism

# Ring Theory
We say two [[Rings|rings]] $R$ and $S$ are isomorphic if there exists a bijective homomorphism (called an isomorphism) between them, and we write $R\cong S$
### Lemma
A homomorphism $f:S\to R$ is injective iff $\text{ker}(f)=\left\{ 0 \right\}$
#### Proof
Assume $f$ is injective, this means that
$$
f(x)=f(y)\implies x=y,\,\forall x,y\in \mathbb{R}
$$
Choosing $y=0,$ we get $f(x)=0\implies x=0$, so $x\in \text{ker}(f)\implies \text{ker}(f)= \left\{ 0 \right\}$.
Conversely, assume $\text{ker}(f)=0$, then 
$$
f(x)=f(y)\implies f(x-y)=0\implies x-y\in \text{ker}(f)\implies x-y=0\implies x=y
$$
### Observations
Let $f:R \to S$ be a homomorphism of rings, then the [[Image|image]] $\text{im}(f)$ is always a [[Subrings|subring]] or $S$, since the 
- identity $f(1)\in S$, 
- they are closed under addtition and multiplication as if $x,y\in \text{im}(f)$, then $f(a)=x,f(b)=y$ for some $a,b\in R$ which implies $f(a+b)=f(a)+f(b)\in \text{im}(f)$, and the same goes for multiplication.
- They must also be closed under negations as if $x\in \text{im}(f)$, then $f(a)=x$, which implies $f(-a)=-x$ which implies $-x\in \text{im}(f)$.
However the [[Kernel|kernel]] $\text{ker}(f)$ is almost never a subring of $R$, because it usually doesn't contain the identity of $R$ (the exception being the unit ring), but they are still very special subsets, they satisfy:
 - closed under addition:
$$
x,y\in \text{ker}(f)\implies f(x+y)=f(x)+f(y)=0+0=0\implies x+y\in \text{ker}(f)
$$
 - closed under multiplication from $R$ (absorption property)
$$
r\in  R,x \in  \text{ker}(f)\implies rx\in  \text{ker}(f)
$$

#Mathematics #LinAlg #Definition #Theorem 