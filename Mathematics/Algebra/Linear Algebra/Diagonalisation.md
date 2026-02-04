Let $T:\mathbb{R}^{n}\to \mathbb{R}^{n}$ be a [[Linear Maps|linear mapping]], to represent it using an $n\times n$ [[Matrices|matrix]] $M$, we need to make a choice of [[Basis|basis]] for $\mathbb{R}^{n}$, usually weith standard basis [[Standard Basis Vectors|$\underline{e}_{1},\underline{e}_{2},\dots,\underline{e}_{n}$]], in a different basis, $M$ changes
## Lemma
Suppose $\underline{x}\in\mathbb{R}^{n}$ is given with respect to a standard basis as 
$$
\underline{x}=\begin{pmatrix}
x_{1}\\x_{2}\\\vdots\\x_{n}
\end{pmatrix}=x_{1}\underline{e}_{1}+x_{2}\underline{e}_{2}+\dots+x_{n}\underline{e}_{n}
$$
And $M$ is the matrix representing a linear transformation $T$ in this basis,
$$
T(\underline{x})=M\begin{pmatrix}
x_{1}\\\vdots\\x_{n}
\end{pmatrix}
$$
Suppose we instead have a different basis $\{ \underline{v}_{1},\dots,\underline{v}_{n} \}$ is a different basis, then we could write
$$
\underline{x}=\tilde{x}_{1}\underline{v}_{1}+\tilde{x}_{2}\underline{v}_{2}+\dots+\tilde{x}_{n}\underline{v}_{n}
$$
Where $\tilde{x}_{1},\tilde{x}_{2},\dots \tilde{x}_{n}\in\mathbb{R}$ such that
$$
\begin{pmatrix}
x_{1}\\ \vdots\\x_{n}
\end{pmatrix}=P\begin{pmatrix}
\tilde{x}_{1}\\\vdots\\\tilde{x}_{n}
\end{pmatrix}
$$
And $P$ is an $n\times n$ invertible "changed basis matrix", then the matrix $N$ representing the same linear map in the new basis is $N=P^{-1}MP$
Key question: is there a basis in which the matrix representation of $T$ looks as simple as possible; the best situation would be a diagonal matrix
## Diagonalisability
$A$ is said to be diagonalisable if [[Similarity Relation|$A\sim B$]], i.e. 
$$
\exists M:M^{-1}AM=D=\begin{pmatrix}
d_{1}&0&\dots&0\\0&d_{2}&\dots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\dots&d_{n}
\end{pmatrix}
$$
Given $A$, is it diagnoalisable? More generally, given $A$ and $B$, it $A\sim B$, now 
$$
A\sim B\implies p_{A}(t)=p_{B}(t)
$$
so similarity matrices hae the same eigenvalues, but importantly, the converse is not necessarily true:
$$
p_{A}(t)=p_{B}(t)\nRightarrow A\sim B
$$
### Example
Say $A=I$ (e.g. in $\mathbb{R}^{2}$), then $[I]=\{ I \}$ since $M^{-1}IM=I\forall M$, now consider
$$
B=\begin{pmatrix}
1&1\\0&1
\end{pmatrix}\neq I
$$
So $B\not\in[I]$, but $p_{A}(t)=(1-t)^{2}=p_{B}(t)$
### Facts about Diagonalisation
- For $A$ and $B$ to be similar, they must have the same [[Eigenvalues|eigenvalues]]
- If $A$ and $B$ have the same eigenvalues, and both are diagonalisable, then $A\sim B$. Being diagonalisable means that $A=MD_{1}M^{-1}$ and $B=ND_{2}N^{-1}$ for some diagonal matrices $D_{1},D_{2}$. But since they have the same eigenvalues, it means that $D_{1}\sim D_{2}$, so by the transitivity of $\sim$, it follows that $A\sim B$
- If $A$ is diagonalisable, but $B$ is not, then they cannot be similar. Diagonalisability of $A$ means that $A\sim D$ for some diagonal matrix $D$; if $A$ were to be similar to $B$, this would mean, by the transitivity of $\sim$, that $B\sim D$, contradicting our hypothesis
- Not all square matrices are diagonalisable; the matrix $B$ above is an example; if it was diagonalisable, it would be similar to the identity matrix, but it wasn't
- If the eigenvalues of $A$ are distinct, then $A$ is diagonalisable
- If $A$ is a real symmetric matrix, [[Transpose|$A=A^{\top}$]], then $A$ is diagonalisable
___
Key Idea: find a "smart" basis, i.e. a basis of eigenvectors
### The $n\times n$ Matrix $A$ is Diagonalisable iff it has $n$ [[Linear Independence|Linearly Independent]] [[Eigenvectors|Eigenvectors]]
#### Proof
$\impliedby$:
Suppse $\{ \lambda_{1},\dots,\lambda_{n} \}$ are the eigenvalues (not distinct) and $\{ \underline{v}_{1},\dots,\underline{v}_{n} \}$ are a set of linearly independent eigenvectors for $A$. Can we diagonalise $A$?
Consider 
$$
M=\begin{pmatrix}
\underline{v}_{1}&\dots&\underline{v}_{n}
\end{pmatrix}
$$
So an $n\times n$ matrix with the eigenvectors as its columns, and let 
$$
D=\begin{pmatrix}
\lambda_{1}&0&\dots&0\\0&\lambda_{2}&\dots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\dots&\lambda_{n}
\end{pmatrix}
$$
We know $A\underline{v}_{1}=\lambda_{1}\underline{v}_{1},A\underline{v}_{2}=\lambda_{2}\underline{v}_{2},\dots,A\underline{v}_{n}=\lambda_{n}\underline{v}_{n}$, so computing $AM$ we get:
$$
AM=\begin{pmatrix}
A\underline{v}_{1}&A\underline{v}_{2}&\dots&A\underline{v}_{n}
\end{pmatrix}=\begin{pmatrix}
\lambda_{1}\underline{v}_{1}&\lambda_{2}\underline{v}_{2}&\dots&\lambda_{n}\underline{v}_{n}
\end{pmatrix}
$$
$$
= \begin{pmatrix}
\underline{v}_{1}&\underline{v}_{2}&\dots&\underline{v}_{n}
\end{pmatrix}\begin{pmatrix}
\lambda_{1}&0&\dots&0\\0&\lambda_{2}&\dots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\dots&\lambda_{n}
\end{pmatrix}=MD
$$
So $AM=MD\implies A=MDM^{-1}$ so $A\sim D$, so $A$ is diagonalisable. We know $M^{-1}$ exists since when you form a matrix out of linearly independent vectors, then its [[Determinants|determinant]] will be non-zero
$\implies$ Suppose $M^{-1}AM=D$, then $AM=MD$. Think of $M$ column by column as 
$$
M=\begin{pmatrix}
\underline{v}_{1}&\dots&\underline{v}_{n}
\end{pmatrix}
$$
So they must be linearly independent since $M$ is [[Matrix Inverses|invertible]]
## Procedure
This is an algorigthm that we can use in general
Fix the eigenvalues using the characteristic polynomial:
$$
p_{A}(t)=\underbrace{ a }_{ \neq 0 }(t-\lambda_{1})^{k_{1}}(t-\lambda_{2})^{k_{2}}\dots(t-\lambda_{p})^{k_{p}}
$$
Where $\lambda_{i}\neq\lambda_{j}$ if $i\neq j$ and the $k_{i}$'s are the algebraic multiplicities of the eigenvalues. If $A$ is $N\times N$, then $\sum_{i=1}^{p}k_{i}=N$, and $k_{i}\geq 1$
Then you work eigenspace by [[Eigenspaces|eigenspace]]: pick $\lambda \in\{ \lambda_{1},\dots,\lambda_{p} \}$ and find $V_{\lambda}=\text{ker}(A-\lambda I)=\{ \underline{v}|(A-\lambda I)\underline{v}=\underline{0} \}$, and $\dim(V_{\lambda})=p_{\lambda}$ i.e. the geometric multiplicity of $\lambda$ $1\leq p_{i}\leq k_{i}$, then go on to the next until you have run out
___
The crucial fact that is working behind the scene is that eigenvectors corresponding to different eigenvalues are linearly independent
### Proof (for $\hspace{0pt}2$ eigenvectors/eigenvalues)
Supple $\lambda_{1}\neq\lambda_{2}$ and $A\underline{v}_{1}\lambda_{1}\underline{v}_{1}$, $A\underline{v}_{2}=\lambda_{2}\underline{v}_{2}$, and $\underline{v}_{1},\underline{v}_{2}\neq  \underline{0}$
Suppose they were linearly dependent, then $\underline{0}=c_{1}\underline{v}_{1}+c_{2}\underline{v}_{2},c_{1},c_{2}\in\mathbb{C}$ i.e. $\underline{v}_{2}=\alpha \underline{v}_{1}$ for some $\alpha \neq 0$, then
$$
A\underline{v}_{2}=\lambda_{2}\underline{v}_{2}=\lambda_{2}\alpha \underline{v}_{1}=\alpha A\underline{v}_{1}=\alpha\lambda_{1}\underline{v}_{1}=\lambda_{1}\underline{v}_{2}
$$
So
$$
\lambda_{2}\underline{v}_{2}=\lambda_{1}\underline{v}_{2}\implies(\lambda_{2}-\lambda_{1})\underline{v}_{2}=\underline{0}
$$
Which is impossible
For generalisation to $> 2$ eigenvalues is In notes pls dooooo
# 
___
So the number of linearly independent eigenvectors is
$$
\dim(V_{\lambda_{1}})+\dim(V_{\lambda_{2}})+\dots+\dim(V_{\lambda_{p}})
$$
So
$$
p\leq\dim(V_{\lambda_{1}})+\dim(V_{\lambda_{2}})+\dots+\dim(V_{\lambda_{p}})\leq \sum_{i=1}^{p}k_{i}=N
$$
So for $A$ to be diagonalisable we need $N$ linearly independent eigenvectors which is only possible if $\dim(V_{\lambda_{i}})=p_{i}=k_{i}\forall i=1,\dots ,p$ 
## $A$ is Diagonalisable if Geometric Multiplicity is equal to Algebraic Multiplicity
some nonsense here maychance?

## Example
Consider a Predator-Prey model in discrete time. Let $x_{n}$ be the number of owls at the end of year $n$ and $y_{n}$ be the number of mice at the end of year $n$. Owls are predators, mice are prey
A possible equation could be:
$$
x_{n+1}=0.6x_{n}+0.5y_{n}
$$
If $y_{n}$ was $\hspace{0pt}0$, then the number of owls would decrease to $0.6$ times the previous year, so they are starving
$$
y_{n+1}=-0.1x_{n}+1.2y_{n}
$$
The negative $x_{n}$ is for the mice being eaten by owls, and the $\hspace{0pt}1.2$ $y_{n}$ is for the general growth of the population
We can represent these as a matrix equation
$$
\begin{pmatrix}
x_{n+1}\\y_{n+1}
\end{pmatrix}=\begin{pmatrix}
0.6&0.5\\-0.1&1.2
\end{pmatrix}\begin{pmatrix}
x_{n}\\y_{n}
\end{pmatrix}
$$
Which can be rewritten as
$$
\underline{v}_{n+1}=M\underline{v}_{n}
$$
What we want to find is the population after $n$ years given a starting population $\underline{v}_{0}$, 
$$
\underline{v}_{1}=M\underline{v}_{0}
$$
$$
 \underline{v}_{2}=M\underline{v}_{1}=M^{2}\underline{v}_{0}
$$
Which can be extended to
$$
M^{n}\underline{v}_{n}
$$
But if $M$ were diagonal, that is easy since 
$$
M^{n}=\begin{pmatrix}
a^{n}&0\\0&b^{n}
\end{pmatrix}
$$
___
We want to solve a system of ODEs
$$
\dot{x}(t)=-x(t)+4y(t)
$$
$$
 \dot{y}(t)=-2x(t)+5y(t)
$$
Which we can write as a matrix equation:
$$
\frac{d }{dx} \begin{pmatrix}
x\\y
\end{pmatrix}=\begin{pmatrix}
-1&4\\-2&5
\end{pmatrix}\begin{pmatrix}
x\\y
\end{pmatrix}
$$
If $A$ were instead diagonal, say 
$$
A=\begin{pmatrix}
-2&0\\0&3
\end{pmatrix}
$$
The system is 
$$
\dot{x}=-2x
$$
$$
 \dot{y}=3y
$$
The solution is de-coupled and the solution is pretty easy to find as $x(t)=x_{0}e^{-2t}$, $y(t)=y_{0}e^{ 3t }$
___
If $A$ is diagonal, 
$$
A=\begin{pmatrix}
a_{1}&0&\dots&0\\0&a_{2}&\dots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\dots&a_{n}
\end{pmatrix}
$$
Then
$$
A\begin{pmatrix}
1\\0\\\vdots\\0
\end{pmatrix}=\begin{pmatrix}
a_{1}\\0\\\vdots\\0
\end{pmatrix}=a_{1}\begin{pmatrix}
1\\0\\\vdots\\0
\end{pmatrix}
$$
$$
A\begin{pmatrix}
0\\1\\\vdots\\0
\end{pmatrix}=\begin{pmatrix}
0\\a_{2}\\\vdots\\0
\end{pmatrix}=a_{2}\begin{pmatrix}
0\\1\\\vdots\\0
\end{pmatrix}
$$
___
If possible, diagonalise 
$$
A=\begin{pmatrix}
-1&4\\-2&5
\end{pmatrix}
$$
$$
p_{A}(t)=\det \begin{pmatrix}
-1-t&4\\-2&5-t
\end{pmatrix}=(-1-t)(5-t)+8
$$
$$
= t^{2}-4t+3=(t-1)^{1}(t-3)^{1}
$$
So $t=1$ and $t=3$ are our eigenvalues:
$$
\lambda_{1}=1,k_{1}=1
$$
$$
 \lambda_{2}=3,k_{2}=1
$$
Since the geometric multiplicities satisfy $1\leq p_{i}\leq k_{i}$, each $p_{i}$ must also be $\hspace{0pt}1$. We can also check this normally:
$$
p_{1}=\dim(V_{\lambda_{1}})=\dim(\text{ker}(A-\lambda_{1}I))=1
$$
$$
p_{2}=\dim(V_{\lambda_{2}})=\dim(\text{ker}(A-\lambda_{2}I))=1
$$
Note that this links to the [[Sums and Intersections of Vectorspaces#Direct Sums|direct sum]]:
$$
\dim(V_{\lambda_{1}})+\dim(V_{\lambda_{2}})=2=\dim(\mathbb{R}^{2})
$$
$$
\mathbb{R}^{2}=V_{\lambda_{1}}\oplus V_{\lambda_{2}}
$$
We find the eigenvectors one-by-one. Take $\lambda_{1}=1$:
$$
(A-I)\underline{v}_{1}=\underline{0}
$$
$$
\implies \begin{pmatrix}
-2&4\\-2&4
\end{pmatrix}\begin{pmatrix}
a\\b
\end{pmatrix}=\begin{pmatrix}
0\\0
\end{pmatrix}
$$
$$
\implies -2a+4b=0
$$
So we can pick 
$$
\underline{v}_{1}=\begin{pmatrix}
2\\1
\end{pmatrix}
$$
But this is not the only choice
$$
V_{\lambda_{1}=1}=\text{ker}(A-I)=\left< \begin{pmatrix}
2\\1
\end{pmatrix} \right> 
$$
Now for the next eigenvector, take $\lambda_{2}=3$:
$$
(A-3I)\underline{v}_{2}=\underline{0}
$$
$$
\implies \begin{pmatrix}
-4&4\\-2&2
\end{pmatrix}\begin{pmatrix}
a\\b
\end{pmatrix}=\begin{pmatrix}
0\\0
\end{pmatrix}
$$
$$
\implies -4a+4b=0
$$
So we can pick:
$$
\underline{v}_{2}=\begin{pmatrix}
1\\1
\end{pmatrix}
$$
$$
V_{\lambda_{2}=3}=\text{ker}(A-3I)=\left< \begin{pmatrix}
1\\1
\end{pmatrix} \right> 
$$
Low and behold the eigenvectors are linearly independent :)
Now we diagnoalise, set
$$
M=\begin{pmatrix}
\underline{v}_{1}&\underline{v}_{2}
\end{pmatrix}=\begin{pmatrix}
2&1\\1&1
\end{pmatrix}
$$
$$
\implies M^{-1}=\begin{pmatrix}
1&-1\\-1&2
\end{pmatrix}
$$
And now we can check
$$
M^{-1}AM=\begin{pmatrix}
1&0\\0&3
\end{pmatrix}
$$
___
Solve the system of ODEs:
$$
\dot{x}=-x+4y
$$
$$
 \dot{y}=-2x+5y
$$
$$
\begin{pmatrix}
\dot{x}\\\dot{y}
\end{pmatrix}=\begin{pmatrix}
-1&4\\-2&5
\end{pmatrix}\begin{pmatrix}
x\\y
\end{pmatrix}=A\begin{pmatrix}
x\\y
\end{pmatrix}
$$
This is the same matrix as above. so let's say
$$
\begin{pmatrix}
w_{1}\\w_{2}
\end{pmatrix}=M^{-1}\begin{pmatrix}
x\\y
\end{pmatrix}
$$
$$
\implies \begin{pmatrix}
x\\y
\end{pmatrix}=M\begin{pmatrix}
w_{1}\\w_{2}
\end{pmatrix}
$$
So we are shifting to a basis of eigenvectors of $A$
$$
\underline{x}=x\begin{pmatrix}
1\\0
\end{pmatrix}+y\begin{pmatrix}
0\\1
\end{pmatrix}=w_{1}\underline{v}_{1}+w_{2}\underline{v}_{2}
$$
Then
$$
\begin{pmatrix}
\dot{w}_{1}\\\dot{w}_{2}
\end{pmatrix}=M^{-1}\begin{pmatrix}
\dot{x}\\\dot{y}
\end{pmatrix}=MA\begin{pmatrix}
x\\y
\end{pmatrix}=M^{-1}AMM^{-1}\begin{pmatrix}
x\\y
\end{pmatrix}
$$
$$
= D\begin{pmatrix}
w_{1}\\w_{2}
\end{pmatrix}
$$
So our ODE has decoupled, i.e.
$$
\begin{pmatrix}
\dot{w}_{1}\\\dot{w}_{2}
\end{pmatrix}=\begin{pmatrix}
1&0\\0&3
\end{pmatrix}\begin{pmatrix}
w_{1}\\w_{2}
\end{pmatrix}
$$
$$
\implies \dot{w}_{1}=w_{1},\dot{w}_{2}=3w_{2}
$$
$$
 \implies w_{1}(t)=c_{1}e^{ t },w_{2}(t)=c_{2}e^{ 3t },c_{1},c_{2}\in \mathbb{R}
$$
Back to $x$ and $y$:
$$
\begin{pmatrix}
x\\y
\end{pmatrix}=M\begin{pmatrix}
w_{1}\\w_{2}
\end{pmatrix}=\begin{pmatrix}
\underline{v}_{1}&\underline{v}_{2}
\end{pmatrix}\begin{pmatrix}
w_{1}\\w_{2}
\end{pmatrix}
$$
$$
\implies x(t)=2c_{1}e^{ t }+c_{2}e^{ 3t },y(t)=c_{1}e^{ t }+c_{2}e^{ 3t }
$$
## Orthogonal Diagonalisation
We say that $A$ is orthogonally diagonalisable if $\exists M\in O(n):M^{\top}AM=D$ where $D$ is a diagonal matrix
### Proposition
Suppose $A$ is real symmetric, $A=A^{\top}$, then the eigenvalues of $A$ are real
#### Proof like below
yay
### Proposition
If $A$ is orthogonally diagonalisable, then $A$ is symmetric
#### Proof
If $P^{\top}AP=D$ with $D$ diagonal, $P$ orthogonal, then $A=PDP^{\top}$ which is clearly symmetric
### Example
If possible, find $P \in O(2)$ such that $P^{\top}AP=D$ where $D$ is diagonal and 
$$
A=\begin{pmatrix}
2&-2\\-2&5
\end{pmatrix}
$$
This is possible, since $A=A^{\top}$
$$
p_{A}(t)=\det(A-tI)=\det \begin{pmatrix}
2-t&-2\\-2&5-t
\end{pmatrix}=(2-t)(5-t)-4=t^{2}-7t+6=(t-1)(t-6)
$$
So we have eigenvalues $\lambda_{1}=1,\lambda_{2}=6$, now we find the eigenvectors
Starting with $\lambda_{1}$:
$$
(A-I)\begin{pmatrix}
a\\b
\end{pmatrix}=\begin{pmatrix}
1&-2\\-2&4
\end{pmatrix}\begin{pmatrix}
a\\b
\end{pmatrix}=\begin{pmatrix}
0\\0
\end{pmatrix}
$$
$$
\implies \underline{v}_{1}=\begin{pmatrix}
2\\1
\end{pmatrix}
$$
$$
\lvert \lvert \underline{v}_{1} \rvert \rvert ^{2}=5
$$
$$
\implies \underline{u}_{1}= \frac{\underline{v}_{1}}{\lvert \lvert \underline{v}_{1} \rvert \rvert }=\frac{1}{\sqrt{ 5 }}\begin{pmatrix}
2\\1
\end{pmatrix}
$$
Now
$$
U_{1}=\text{span}\left\{ \frac{1}{\sqrt{ 5 }}\begin{pmatrix}
2\\1
\end{pmatrix} \right\}
$$
$$
\implies U_{1}^{\bot}:\underline{u}_{1}\cdot \begin{pmatrix}
a\\b
\end{pmatrix}=\begin{pmatrix}
0\\0
\end{pmatrix}
$$
$$
\implies 2a+b=0
$$
So
$$
U_{1}^{\bot}=\text{span}\left\{ \begin{pmatrix}
1\\-2
\end{pmatrix} \right\}
$$
So take
$$
\underline{u}_{2}=\frac{1}{\sqrt{ 5 }}\begin{pmatrix}
1\\-2
\end{pmatrix}
$$
We can do a sanity chack to see if $\underline{u}_{2}$ is in fact an eigenvector for $\lambda_{2}=6$:
$$
A\underline{u}_{2}=\frac{1}{\sqrt{ 5 }}\begin{pmatrix}
2&-2\\-2&5
\end{pmatrix}\begin{pmatrix}
1\\-2
\end{pmatrix}=\frac{1}{\sqrt{ 5 }}\begin{pmatrix}
6\\-12
\end{pmatrix}=6\underline{u}_{2}
$$
Which is what we wanted (we could have instead just done it normally, but this is cooler)
So
$$
P=\begin{pmatrix}
\underline{u}_{1}&\underline{u}_{2}
\end{pmatrix}=\frac{1}{\sqrt{ 5 }}\begin{pmatrix}
2&1\\1&-2
\end{pmatrix}
$$
$P$ is equal to its transpose, but this is a fluke, we can then check:
$$
P^{\top}P=\frac{1}{5}  \begin{pmatrix}
2&1\\1&-2
\end{pmatrix} \begin{pmatrix}
2&1\\1&-2
\end{pmatrix}=\begin{pmatrix}
1&0\\0&1
\end{pmatrix}
$$
Which is cool :)
## Unitary Diagonalisation
We say that $B$ is unitarily diagonalisable if $\exists P\in U(n):P^{*}AP=D$, where $D$ is a diagonal matrix
### Proposition
Suppose $A$ is complex hermitian, $A=A^{*}$, then the eigenvalues of $A$ are real
#### Proof
Suppose $A\underline{x}=\lambda \underline{x}$ for some $\underline{x}\neq 0$, then 
$$
\underline{x}^{*}A\underline{x}=\lambda \underline{x}^{*}\underline{x}
$$
Since $\underline{x}^{*}\underline{x}=\left< \underline{x},\underline{x} \right>$, we then take "$*$" of both sides:
$$
\underline{x}^{*}A^{*}\underline{x}=\overline{\lambda}\underline{x}^{*}\underline{x}
$$
$$
\implies \underline{x}^{*}A\underline{x}=\overline{\lambda}\underline{x}^{*}\underline{x}
$$
Since $A=A^{*}$
$$
\implies \lambda \underline{x}^{*}\underline{x}=\overline{\lambda}\underline{x}^{*}\underline{x}
$$
$$
\implies \lambda=\overline{\lambda}\implies \lambda \in \mathbb{R}
$$
If $A$ is real symmetric, then the eigenvectors can be taken to be real as well since they solve $(A-\lambda I)\underline{v}=\underline{0}$
### Proposition
Let $A$ be complex hermitian, then the eigenvectors of $A$ corresponding to different eigenvalues are [[Mutually Orthogonal Vectors|mutually orthogonal]] using the [[Dot Product|standard]] [[Hermitian Inner Product|inner produc]] on $\mathbb{C}^{n}$
#### Proof
Suppose the eigenvalues are $\lambda$ and $\mu$, both are in $\mathbb{R}$, from above proof, then
$$
A\underline{x}=\lambda \underline{x},\underline{x}\neq 0
$$
$$
 A\underline{y}=\mu \underline{y},\underline{y}\neq 0
$$
So
$$
\underline{x}^{*}A\underline{y}=\mu \underline{x}^{*}\underline{y}
$$
$$
 \underline{y}^{*}A\underline{x}=\lambda \underline{y}^{*}\underline{x}
$$
By taking "$*$ of both sides we get:
$$
\underline{x}^{*}A^{*}\underline{y}=\overline{\lambda}\underline{x}^{*}\underline{y}
$$
Since $A=A^{*},\lambda \in\mathbb{R}$
$$
\implies \underline{x}^{*}A\underline{y}=\lambda \underline{x}^{*}\underline{y}
$$
Combined with the equation for $\mu$, we have
$$
\lambda \underline{x}\underline{y}^{*}=\mu \underline{x}^{*}\underline{y}
$$
$$
\implies (\lambda-\mu)\underline{x}^{*}\underline{y}=0
$$
$$
\implies x^{*}\underline{y}=0
$$
Since $\lambda \neq \mu$, so $\underline{x}\bot\underline{y}$
So if all eigenvalues of $A$ are different, have $n$ orthogonal eigenvectors, so we can diagonalise $A$ with a unitary matrix $P$ (after rescaling eigenvectors to unit length)
### Proposition
If $A$ is complex hermitian, then $\exists P \in U(n):P^{*}AP=D$ where $D$ is a diagonal (real) matrix
In each case, the columns of $P$ are an [[Orthonormal Vectors|orthonormal]] basis
#### Proof
Pick an eigenvalue $\lambda_{1}$ and associated unit eigenvector $\underline{u}_{1}:A\underline{u}_{1}=\lambda_{1}\underline{u}_{1}$, and write
$$
U_{1}=\text{span}\left\{ \underline{u}_{1} \right\}
$$
And construct the [[Orthogonal Complement|orthogonal complement]] $U_{1}^{\bot}$ using the [[Dot Product|standard inner product]] on $\mathbb{C}^{n}$, then we know from the [[Sums and Intersections of Vectorspaces#Direct Sums|direct sum]] that:
$$
\mathbb{C}^{n}=U_{1}\oplus U_{1}^{\bot}
$$
Now note that $A$ acting on any $\underline{v}\in U_{1}^{\bot}$ gives another element of $U_{1}^{\bot}$ since:
$$
\left< A\underline{v},\underline{u}_{1} \right> = \underline{u}_{1}^{*}A\underline{v}=(A\underline{u}_{1})^{*}\underline{v}
$$
Using $A=A^{*}$
$$
=(\lambda_{1}\underline{u}_{1})^{*}\underline{v}=\overline{\lambda}_{1}\underline{u}_{1}^{*}\underline{v}=\overline{\lambda}_{1}\left< \underline{u}_{1},\underline{v} \right> =0
$$
Since $\underline{v}\in U^{\bot}$, hence $A\underline{v}\in U_{1}^{\bot}$
So we can talk about the restriction of $A$ to $U_{1}^{\bot}$, denoted 
$$
A|_{U_{1}^{\bot}}:U_{1}^{\bot}\to U_{1}^{\bot}
$$
This is a Hermitian operator operating on $U_{1}^{\bot}\cong\mathbb{C}^{n-1}$ (one dimension less)
Now we repeat, so we pick $\underline{u}_{1}\in U_{1}^{\bot}$ with $A\underline{u}_{2}=\lambda_{2}\underline{u}_{2}$, set $U_{2}=\text{span}\left\{ \underline{u}_{2} \right\}$, and $U_{1}=U_{2}\oplus U_{2}^{\bot}$ and so on
In th end, we get to
$$
\mathbb{C}^{n}=U_{1}\oplus U_{2}\oplus\dots \oplus U_{n}
$$
Where each $U_{i}=\text{span}\left\{ \underline{u}_{i} \right\}$ where all $\underline{u}_{i}$'s are orthogonal and unit length, which is what we wanted
___
It works the other way too:
### Proposition
If $A$ is unitarily diagonalisable, then $A$ is hermitian
#### Proof
If $P^{*}AP=D$ with $D$ diagonal, $P$ orthogonal, then $A=PDP^{*}$ which is true iff the eigenvalues of $D$ are all real, which thankfully is the case



#Mathematics #LinAlg 