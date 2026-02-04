Given a set of data, how does one "fit" a smooth function to it?
## Polynomial Interpolation
The classical problem of polynomial interpolation is to find a polynomial
$$
p_{n}(x)=a_{0}+a_{1}x+\dots+a_{n}x^{n}=\sum_{ k=0} ^{ n}  a_{k}x^{k}
$$
That interpolates our function $f$ at a finite set of nodes $\left\{ x_{0},x_{1},\dots,x_{m} \right\}$. In other words, $p_{n}(x_{i})=f(x_{i})$ at each of the nodes $x_{i}$. SInce the polynomial has $n+1$ unknown coefficients, we expect to need $n+1$ distinct nodes, so let us assume that $m=n$.
Here we have two nodes $x_{0},x_{1}$, ande seek a polynomial $p_{1}(x)=a_{0}+a_{1}x$. Then the interpolation would require that:
$$
\begin{cases}
p_{1}(x_{0})=a_{0}+a_{1}x_{0}=f(x_{0}) \\
p_{1}(x_{1})=a_{0}+a_{1}x_{1}=f(x_{1})
\end{cases}
$$
$$
\implies p_{1}(x)=\frac{x_{1}f(x_{0})-x_{0}f(x_{1})}{x_{1}-x_{0}}+\frac{f(x_{1})-f(x_{0})}{x_{1}-x_{0}}x
$$
For general $n$, the interpolation conditions require:
$$
a_{0}+a_{1}x_{0}+a_{2}x_{0}^{2}+\dots+a_{n}x_{0}^{n}=f(x_{0})
$$
$$
 a_{0}+a_{1}x_{1}+a_{2}x_{1}^{2}+\dots+a_{n}x_{1}^{n}=f(x_{1})
$$
$$
\vdots
$$
$$
 a_{0}+a_{1}x_{n}+a_{2}x_{n}^{2}+\dots+a_{n}x^{n}_{n}=f(x_{n})
$$
So we have to solve
$$
\begin{pmatrix}
1 & x_{0} & x_{0}^{2} & \dots & x_{0}^{n} \\
1 & x_{1} & x_{1}^{2} & \dots & x_{1}^{n} \\
\vdots & \vdots & \vdots &  & \vdots \\
1 & x_{n} & x_{n}^{2} & \dots & x_{n}^{n}
\end{pmatrix}
\begin{pmatrix}
a_{0} \\
a_{1} \\
\vdots \\
a_{n}
\end{pmatrix}=\begin{pmatrix}
f(x_{0}) \\
f(x_{1}) \\
\vdots \\
f(x_{n})
\end{pmatrix}
$$
Which is called a Vandermonde [[Matrices|matrix]]. The [[Determinants|determinant]] of this matrix is
$$
\det(A)=\prod_{0\le i\leq j\leq n}(x_{j}-x_{i})
$$
Which is non-zero provided the nodes are all distinct. This establishes an important result, where $\mathbb{R}[x]_n$ denotes the space of all real polynomials of degree $\leq n$.
### Existence/Uniqueness Theorem
Given $n+1$ distinct nodes $x_{0},x_{1},\dots,x_{n}$, there is a unique polynomial $p_{n}\in \mathbb{R}[x]_n$ that interpolates $f(x)$ at these nodes.
#### Proof of Uniqueness
Suppose that in addition to $p_{n}$, there is another interpolating polynomial $q_{n}\in \mathbb{R}[x]_n$. Then the difference $r_{n}=p_{n}-q_{n}$ is also a polynomial with degree $\le n$; but we have 
$$
r_{n}(x_{i})=p_{n}(x_{i})-q_{n}(x_{i})=f(x_{i})-f(x_{i})=0
$$
So $r_{n}$ has $n+1$ roots. From the fundamental theorem of algebra, this is possible only if $r_{n}(x)\equiv 0$, which implies $p_{n}=q_{n}$
___
One way to compute the interpolating polynomial would be to solve the Vandermonde system by [[Gauss-Jordan Elimination|Gauss-Jordan elimination]]. However, this is not recommended. In practice, we choose a different [[Basis|basis]] for $p_{n}$: there are two common and effective choices
### Lagrange Polynomials
This uses a special basis of polynomials $\left\{ \ell_{k} \right\}$ in which the interpolation equations reduce to the identity matrix. In other words, the coefficientss in this basis are just the funcgtion values,
$$
p_{n}(x)=\sum_{ k=0} ^{ n}f(x_{k})\ell_{k}(x)  
$$
For general $n$, the $n+1$ lagrange polynoials are defined as a product:
$$
\ell_{k}(x)=\prod_{j=0,j\neq k}^{n} \frac{x-x_{j}}{x_{k}-x_{j}}
$$
Which by construction have the property that
$$
\ell_{k}(x_{i})=\begin{cases}
1 & \text{if }i=k  \\
0 & \text{otherwise}
\end{cases}
$$
The Lagrange form of the interpolating polynomial is easy to write down, but expensive to evaluate since all of the $\ell_{k}$ must be computed. Moreover, changing any of the nodes means that the $\ell_{k}$ must all be recomputed from scratch, and similarly for adding a new node (moving to a higher degree)
### Newton/Divided Difference Polynomials
It would be easy to increase the degree of $p_{n}$ if
$$
p_{n+1}(x)=p_{n}(x)+g_{n+1}(x)
$$
Where $g_{n+1}\in \mathbb{R}[x]_{n+1}$.
From the interpolation conditions, we know that
$$
g_{n+1}(x_{i})=p_{n+1}(x_{i})-p_{n}(x_{i})=f(x_{i})-f(x_{i})=0
$$
$$
\implies g_{n+1}(x)=a_{n+1}(x-x_{0})\dots(x-x_{n})
$$
The coefficient $a_{n+1}$ is determined by the remaining interpolation condition at $x_{n+1}$, so
$$
p_{n}(x_{n+1})+g_{n+1}(x_{n+1})=f(x_{n+1})
$$
$$
\implies a_{n+1}=\frac{f(x_{n+1})-p_{n}(x_{n+1})}{(x_{n+1}-x_{0})\dots(x_{n+1}-x_{n})}
$$
The polynomial $(x-x_{0})(x-x_{1})\dots(x-x_{n})$ is called a Newton polynomial. These form a new basis
$$
n_{0}(x)=1,n_{k}(x)=\prod_{j=0}^{k-1}(x-x_{j})\text{ for }k>0
$$
Notice that $a_{k}$ depends only on $x_{0},\dots,x_{k}$, so we can construct first $a_{0}$, then $a_{1}$ etc
It turns out that the $a_{k}$ are easy to compute, but it will take a little work to derive the method
#### Definition
We define the divided difference $f[x_{0},x_{1},\dots,x_{k}]$ to be the coefficient of $x^{k}$ in the polynomial in the polynomial interpolating $f$ at nodes $x_{0},x_{1},\dots,x_{k}$. It follows that
$$
f[x_{0},x_{1},\dots,x_{k}]=a_{k}
$$
Where $a_{k}$ is the coefficient in the Newton form above
Divided differences are actually approximations of [[Differentiation|derivatives]] of $f$. In the limit that the nodes all coincide, the Newton form of $p_{n}(x)$ becomes the [[Taylor Series|Taylor polynomial]]
#### Theorem
For $k>0$, the divided differences satisfy
$$
f[x_{i},x_{i+1},\dots,x_{i+k}]=\frac{f[x_{i+1},\dots,x_{i+k}]-f[x_{i},\dots,x_{i+k-1}]}{x_{i+k}-x_{i}}
$$
##### Proof
WLOG, we relable the nodes so that $i=0$. So we want to prove that
$$
f[x_{0},x_{1},\dots,x_{k}]=\frac{f[x_{1},\dots,x_{k}]-f[x_{0},\dots,x_{k-1}]}{x_{k}-x_{0}}
$$
The trick is to write the interpolant with nodes $x_{0},\dots,x_{k}$ in the form
$$
p_{k}(x)=\frac{(x_{k}-x)q_{k-1}(x)+(x-x_{0})\tilde{q}_{k-1}(x)}{x_{k}-x_{0}}
$$
Where $q_{k-1}\in\mathbb{R}[x]_{k-1}$ interpolates $f$ at the subset of nodes $x_{0},x_{1},\dots,x_{k-1}$ and $\tilde{q}_{k-1}\in \mathbb{R}[x]_{k-1}$ interpolates $f$ at the subset $x_{1},x_{2},\dots,x_{k}$. If this holds, then matching the coefficient of $x^{k}$ on each side will give the divided difference formua, since, for example, the leading coefficient of $q_{k-1}$ is $f[x_{0},\dots,x_{k-1}]$. To see that $p_{k}$ may really be written this way, note that
$$
p_{k}(x_{0})=q_{k-1}(x_{0})=f(x_{0})
$$
$$
 p_{k}(x_{k})=\tilde{q}_{k-1}(x_{k})=f(x_{k})
$$
$$
 p_{k}(x_{i})=\frac{(x_{k}-x_{i})q_{k-1}(x_{i})+(x_{i}-x_{0})\tilde{q}_{k-1}(x_{i})}{x_{k}-x_{0}}=f(x_{i})
$$
For $i=1,\dots,k-1$
Since $p_{k}$ agrees with $f$ at the $k+1$ nodes, it is the unique interpolant in $\mathbb{R}[x]_{k}$
### Interpolation Error
The goal here is to estimate the error $\left| f(x)-p_{n}(x) \right|$ when we approximate a function $f$ by a polynomial interpolant $p_{n}$. Clearly this will depend on $x$
#### Cauchy's Interpolation Error Theorem
Let $p_{n}\in \mathbb{R}[x]_{n}$ be the unique polynomial interpolating $f(x)$ at the $n+1$ distinct nodes $x_{0},x_{1},\dots,x_{n}\in[a,b]$, and let $f$ be continuous on $[a,b]$ with $n+1$ continuous derivatives on $(a,b)$. Then for each $x\in[a,b]$ there exists $\xi \in(a,b)$ such that
$$
f(x)-p_{n}(x)=\frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_{0})(x-x_{1})\dots(x-x_{n})
$$
Which looks similar to the error formula for Taylor polynomials, but now the error vanishes at multiple nodes, rather than just at $x_{0}$.
From the formula, you can see that the error will be larger for a more curvacious function, where the derivative $f^{(n+1)}$ is larger. It might also appear that the error will go down as the number of nodes $n$ increases; we will see that this is not always true
### Node Placement
You might expect polynomial interpolation to [[Convergence|converge]] as $n\to \infty$. Surprisingly, this is not the case if you take equally spaced nodes $x_{i}$, this is called the Runge phenomenon.
The problem is largely coming from the interpolating polynomial
$$
w(x)=\prod_{i=0}^{n}(x-x_{i})
$$
We can avoid the Runge phenomenon by choosing different nodes $x_{i}$ that are not uniformly spaced
Since the problems usually occur near the ends of the interval, it would be logical to put more nodes there. A good choice is given by taking equally-spaced points on the unit circle $\left| z \right|=1$ and projecting to the real line;
![[Pasted image 20251016193320.png]]
The points around the circle are
$$
\phi_{j}=\frac{(2j+1)\pi}{2(n+1)},j=0,\dots,n
$$
So the corresponding Chebyshev nodes are
$$
x_{j}=\cos\left( \frac{(2j+1)\pi}{2(n+1)} \right)
$$
In fact, the Chebyshev nodes are, in one sense, an optimal choice. To see this, we first note that they are zeroes of the [[Chebyshev Polynomials|Chebyshev polynomial]]:
$$
T_{n+1}(t):=\cos((n+1)\arccos(t))
$$
So in choosing Chebyshev nodes, we are choosing the error polynomial $w(x):=\prod_{i=0}^{n}(x-x_{i})$ to be $\frac{T_{n+1}(x)}{2^{n}}$ (this normalisation makes the leading coefficient 1). This is a good choice because of the following result
#### Theorem
Let $x_{0},x_{1},\dots,x_{n}\in[-1,1]$ be distinct. Then $\max_{[-1,1]}\left| w(x) \right|$ is minimized if
$$
w(x)=\frac{1}{2^{n}}T_{n+1}(x)
$$
Where $T_{n+1}(x)$ is the $n+1$th Chebyshev polynomial.
___
Having established that the Chebyshev polynomial minimises the maximum error, we can see convergence as $n\to \infty$ from the fact that
$$
\left| f(x)-p_{n}(x) \right| =\frac{\left| f^{(n+1)}(\xi) \right| }{(n+1)!}\left| w(x) \right| =\frac{\left| f^{(n+1)}(\xi) \right| }{2^{n}(n+1)!}\left| T_{n+1}(x) \right| \le \frac{\left| f^{(n+1)}(\xi) \right| }{2^{n}(n+1)!}
$$
If the function is well-behaved enough that $\left| f^{(n+1)(x)} \right|<M$ for some constant whenever $x\in [-1,1]$, then the error will tend to zero as $n\to \infty$