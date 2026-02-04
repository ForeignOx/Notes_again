# Of Relations
## Definition
If $R$ is a [[Relations|relation]] and $A$ is any [[Sets|set]], then the image of $A$ under $R$, $R[A]$, is the set of second elements of [[Ordered Pairs|ordered pairs]] in $R$ whose first elements are in $A$:
$$
R[A] = \left\{ y\mid(\exists x)(x\in A\text{ and }(x,y)\in  R) \right\}
$$
Thus [[Restrictions|$R[A]=\text{range}(R\restriction A)$]]  
# Of Functions
## Definition
Let $f:X\to Y$ be a [[Functions|function]] between [[Sets|sets]] $X,Y$
If $A\subset X$, we define the image of $A$ as:
$$
f(A)=\{ f(a)\in Y|a\in A \}
$$
For $B\subset Y$ we define the pre-image of $B$ as:
$$
f^{-1}(B)=\{ x\in X|f(x)\in B \}
$$
Note this is not the same as the [[Inverses|inverse function]], it is a notion only in set theory
## Proposition
Let $f:X\to Y$ be a function, and assume that $A,B\subset X$ Then
- $f(A\cap B)\subset f(A)\cap f(B)$
- $f(A\cup B)=f(A)\cup f(B)$
- $f(X\setminus A) \supset f(X)\setminus f(A)$

Assume that $C,D\subset Y$. Then:
- $f^{-1}(C\cup D)=f^{-1}(C)\cap f^{-1}(D)$
- $f^{-1}(C\cup D)=f^{-1}(C)\cup f^{-1}(D)$
- $f(Y\setminus C) \supset f(Y)\setminus f(C)$
### Proof
Look at $f(A\cap B)\subset f(A)\cap f(B)$ 
Take $y\in f(A\cap B)$ then there is $x\in A\cap B$ with $f(x)=y$ Then $x\in A$ and $x\in B$. Then $y=f(x)\in f(A)$ and $y= f(x)\in f(B)$ so $y\in f(A)\cap f(B)$
Look now at $f^{-1}(C\cap D)=f^{-1}(C)\cap f^{-1}(D)$
To prove this, we want to show both $f^{-1}(C\cap D)\subseteq f^{-1}(C)\cap f^{-1}(D)$ and $f^{-1}(C\cap D)\supseteq f^{-1}(C)\cap f^{-1}(D)$
Take $x\in f^{-1}(C\cap D)$. Then $f(x)\in C\cap D$. So $f(x)\in C$ and $f(x)\in D$. So $x\in f^{-1}(C)$ and $x\in f^{-1}(D)$
Hence $x \in f^{-1}(C)\cap f^{-1}(D)$ so $f^{-1}(C\cap D)\subseteq f^{-1}(C)\cap f^{-1}(D)$ is true
Take $x\in f^{-1}(C)\cap f^{-1}(D)$. So $x\in f^{-1}(C)$ and $x\in f^{-1}(D)$ so $f(x)\in C$ and $f(x)\in D$. So $f(x)\in C\cap D$ so $x\in f^{-1}(C\cap D)$, $x$ is in the pre-image by definition, so we have, $f^{-1}(C\cap D)\supseteq f^{-1}(C)\cap f^{-1}(D)$ thus we have equality
# Of Linear Maps
If [[Linear Maps|$T:V\to W$]], we define the image of $T$ by:
$$
\text{im}(T):=\{ T(\underline{v})\mid\underline{v}\in  V \}\subseteq W
$$
$\text{im}(T)$ is a subspace of $W$
Other notations include calling it the range of $T$ and denoting it $R(T)$ or $\mathfrak{R}(T)$ 
## Proof
Suppose $\underline{u},\underline{w}\in \text{im}(T),\lambda \in\mathbb{R}$, then $\exists \underline{x},\underline{y}\in V$ such that
$$
T(\underline{x})=\underline{u},T(\underline{y})=\underline{w}
$$
So
$$
\underline{u}+\underline{w}=T(\underline{x})+T(\underline{y})=T(\underline{x}+\underline{y})\in  \text{im}(T)
$$
## [[Columnspace and Rowspace|Rank]]
The rank of $T$ is the [[Dimension|dimension]] of the image of $T$
$$
\text{rk}(T):=\dim(\text{im}(T))
$$
## Example
If [[Matrices|$A\in M_{m\times n}(\mathbb{R})$]], $A:\mathbb{R}^{n}\to \mathbb{R}^{n}$, 
$$
\text{im}(A)=\{ A\underline{v}\mid \underline{v}\in \mathbb{R}^{n} \}=\text{colspace(A)}\subseteq \mathbb{R}^{n}
$$
### Subexample
$$
A=\begin{pmatrix}
3&1\\12&4
\end{pmatrix}:\mathbb{R}^{2}\to \mathbb{R}^{2}
$$
So
$$
\text{im}(A)=\left< \begin{pmatrix}
3\\12
\end{pmatrix},\begin{pmatrix}
1\\4
\end{pmatrix} \right> =\left< \begin{pmatrix}
1\\4
\end{pmatrix} \right> \subseteq \mathbb{R}^{2}
$$
Hence $\text{rk}(A)=1$
___
$$
\frac{d }{dx} :\mathbb{R}[x]_{n}\to \mathbb{R}[x]_{n}
$$
Consider what the map is doing:
$$
\frac{d }{dx} (a_{0}+a_{1}x+\dots+a_{n}x^{n})=a_{1}+2a_{2}x+\dots+na_{n}x^{n-1}
$$
So
$$
\text{im}\left( \frac{d }{dx}  \right)=\mathbb{R}[x]_{n-1}\subseteq \mathbb{R}[x]_{n}
$$
$$
 \text{rk}\left( \frac{d }{dx}  \right)=n=\dim(\mathbb{R}[x]_{n-1})
$$
## Lemma
Let $T:V\to W$ be linear and $\{ \underline{v}_{1},\dots,\underline{v}_{n} \}$ be a [[Linear Span|spanning set]] for $V$ (eg. a [[Basis|basis]]), then $\{ T(\underline{v}_{1},\dots,T(\underline{v}_{n})) \}$ is a spanning set for $\text{im}(T)$
### Proof
Suppose $\underline{w}\in\text{im}(T)$, then $\exists \underline{v}\in V:T(\underline{v})=\underline{w}$, we have $\underline{v}=\lambda_{1}\underline{v}_{1}+\dots+\lambda_{n}\underline{v}_{n}$ for some $\lambda_{i}$'s. So 
$$
\underline{w}=T(\underline{v})=T(\lambda_{1}\underline{v}_{1}+\dots+\lambda_{n}\underline{v}_{n})=\lambda_{1}T(\underline{v}_{1})+\dots+\lambda_{n}T(\underline{v}_{n})
$$
Hence proved

#Mathematics #LinAlg #Definition 