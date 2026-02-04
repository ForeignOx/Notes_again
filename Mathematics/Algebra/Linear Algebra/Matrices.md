An $m\times n$ matrix is a rectangular array of [[Real Numbers|real numbers]] with $m$ rows and $n$ columns
We call the [[Sets|set]] of all $m\times n$ matrices in some [[Fields|field]] $\mathbb{F}$ (mostly taken to be $\mathbb{R}$):
$$
M_{m\times n}(\mathbb{F})
$$
We call the entry in position $(i,j)$ the $(i,j)$th element
$$
A=\begin{pmatrix}
a_{11}&a_{12}&\dots&a_{1j}&\dots& a_{1n}\\a_{21}&a_{22}&\dots&a_{2j}&\dots& a_{2n}\\\vdots&\vdots&&\vdots& & \vdots\\a_{i1}&a_{i2}&\dots&a_{ij}&\dots& a_{in}\\\vdots&\vdots&&\vdots& & \vdots\\a_{n1}&a_{m2}&\dots&a_{mj}&\dots& a_{mn}
\end{pmatrix}
$$
## Example
$$
\begin{pmatrix}
1&5&10\\2&3&4
\end{pmatrix}\in M_{2\times 3}(\mathbb{R})
$$
and for example $4$ is the $(2,3)$ entry 
# 
___
If $A\in M_{m\times n}(\mathbb{R})$, we write $A_{ij}$ or $a_{ij}$ for the $(i,j)$th entry or element of $A$, and for shorthand, we write:
$$
A=(a_{ij})_{m\times n}
$$
## Column Vectors
We call $M_{n\times 1}(\mathbb{R})=\mathbb{R}^n$ a set of column vectors
## Row Vectors
We call $M_{1\times n}(\mathbb{R})=\mathbb{R}^n$ a set of row vectors
## Square Matrices
If we have matrices that are $n\times n$, or $M_{n\times n}(\mathbb{R})$, we denote these as $M_{n}(\mathbb{R})$, known as square matrices
## Matrix Addition
This is a [[Functions|function]]:
$$
M_{m\times n}(\mathbb{R})\times M_{m\times n}(\mathbb{R})\to M_{m\times n}(\mathbb{R})
$$
$$
 (X,Y)\mapsto X+Y
$$
Defined by:
$$
(X+Y)_{ij}=X_{ij}+Y_{ij}
$$
### Properties:
- There exists an additive identity: [[Zero Matrix|$0_{m\times n}\in M_{m\times n}(\mathbb{R})$]] such that
$$
0_{m\times n}+X=X=X+0_{m\times n},\,\forall X \in M_{m\times n}(\mathbb{R})
$$
- Commutativity:
$$
X+Y=Y+X,\forall X,Y\in M_{m\times n}(\mathbb{R})
$$
- Additive inverses:
$$
\forall X \in M_{m\times n}(\mathbb{R}),\exists-X\in M_{m\times n}(\mathbb{R}):X+(-X)=0_{m\times n}=(-X)+X
$$
- Associativity:
$$
(X+Y)+Z=X+(Y+Z),\forall X,Y,Z\in M_{m\times n}
$$
## Scalar Multiplication
This is a function:
$$
\mathbb{R}\times M_{n\times m}(\mathbb{R})\to M_{m\times n}(\mathbb{R})
$$
$$
(\lambda,X)\mapsto\lambda X
$$
Defined by:
$$
(\lambda X)_{ij}=\lambda X_{ij}
$$
### Properties:
- Multiplication by 0:
$$
0X=0_{m\times n},\forall X \in M_{m\times n}
$$
- Multiplication by 1:
$$
1X=X,\forall X \in M_{m\times n}
$$
- Associativity:
$$
\lambda(\mu X)=(\lambda\mu)X,\forall\lambda,\mu \in \mathbb{R},\forall X \in M_{m\times n}
$$
- Distributivity over matrix addition:
$$
(\lambda+\mu)X=\lambda X+\mu X
$$
$$
\lambda(X+Y)=\lambda X+\lambda Y,\forall\lambda,\mu \in \mathbb{R},\forall X,Y \in M_{m\times n}
$$
The fact that matrices have all these properties means that matrices are a [[Vectorspaces|vectorspace]]
## Matrix Multiplication
Matrix multiplication is a function:
$$
M_{m\times n}(\mathbb{R})\times M_{n\times p}(\mathbb{R})\to M_{m\times p}(\mathbb{R})
$$
$$
(X,Y)\mapsto XY
$$
Suppose $X=(x_{ij})$, $Y=(y_{ij})$, then:
$$
(XY)_{ij}=\sum_{k=1}^{n}x_{ik}y_{kj}=x_{i1}y_{1j}+x_{i2}y_{2j}+\dots+x_{in}y_{nj}
$$
### Properties of Matrix Multiplication
For $\forall X,X'\in M_{m\times n}(\mathbb{R}),Y,Y'\in M_{n\times p}(\mathbb{R}),Z\in M_{p\times r}(\mathbb{R})$, $\forall\lambda,\lambda'\in\mathbb{R}$ we have:
$$
0_{p\times m}X=0_{p\times n}=Z0_{r\times n}
$$
$$
I_{m}X=X=XI_{n}
$$
$$
\lambda(XY)=(\lambda X)Y=X(\lambda Y)
$$
$$
(XY)Z=X(YZ)
$$
$$
 (X+X')Y=XY+X'Y
$$
$$
X(Y+Y')=XY+XY'
$$
Note in general we don't have:
$$
XY=YX
$$
Partially because $XY$ and $YX$ might be of different sizes, unless they are both square matrices: $XY\in M_{m\times m}(\mathbb{R})$ and $YX \in M_{n\times n}(\mathbb{R})$, but even so, most often $XY\neq YX$ 
Note if $XY=0$, it doesn't follow that $X=0$ or $Y=0$ 
#### Proofs
Prove the first $\hspace{0pt}3$ and then also $\hspace{0pt}5$ to do pls
4th: 
For the two matrices to be equal, every entry of $(XY)Z$ must be equal to the respective entry of: $X(YZ)$
The $(i,k)$th entry of $XY$ is:
$$
(XY)_{ik}=\sum_{r=1}^nx_{ir}y_{rk}
$$
Then $(XY)Z$ has the $(i,j)$th entry of:
$$
((XY)Z)_{ij}=\sum_{k=1}^{p}\left(\sum_{r=1}^nx_{ir}y_{rk}\right)z_{kj}=*
$$
Now we can instead think of the $(r,j)$th entry of $YZ$ is:
$$
(YZ)_{rj}=\sum_{k=1}^{p}y_{rk}z_{kj}
$$
So the $(i,j)$th entry of $X(YZ)$ is:
$$
(X(YZ))_{ij}=\sum_{r=1}^{n}x_{ir}\left( \sum_{k=1}^{p}y_{rk}z_{kj} \right)=\sum_{r=1}^{n}\sum_{k=1}^{p}x_{ir}y_{rk}z_{kj}=*
$$



#Mathematics #LinAlg #Definition