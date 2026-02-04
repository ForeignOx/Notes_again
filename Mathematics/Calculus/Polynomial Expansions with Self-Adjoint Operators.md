We postulate that we can write a [[Functions|function]] $y(x)$ as:
$$
y(x)=\sum_{k=0}^{\infty} b_{k}p_{k}(x) 
$$
Which is an $n$th order [[Legendre's Equation|Legendre polynomial]]
We also have:
$$
\mathcal{L}_{L}p_{n}=\left[ (x^{2}-1)\frac{d }{dx^{2}}+2x\frac{d }{dx}   \right]p_{n}=n(n+1)p_{n}
$$
$$
 p_{n}(x)=\frac{1}{2^{n}n!}\frac{d ^{n}}{dx^{n}} [(x^{2}-1)^{n}]
$$

Where $p_{n}(x)$ are the [[Basis|basis]] [[Vectors|vectors]], and we write functions as a [[Linear Combinations|linear combination]] of them
This is similar to [[Fourier Series|Fourier series]];
$$
y(x)=\frac{a_{0}}{2}+\sum_{n=1}^{\infty} a_{n}\cos(nx)+\sum_{n=1}^{\infty} b_{n}\sin(nx)  
$$
And we essentially have $\cos(nx)$ and $\sin(nx)$ as a basis for [[Periodic Functions|periodic functions]]
We want to know given $y(x)$, how do we determine the coefficients in these sorts of expansions?
The result relies on two key observations:
## Observation $\hspace{0pt}1$
It is easy to find components if your basis vectors are [[Orthogonality|orthogonal]]
### Example
Let $V$ be a 3-[[Dimension|dimensional]] [[Vectorspaces|vectorspace]] with orthogonal basis $\underline{x}_{1}\underline{x}_{2},\underline{x}_{3}$
If $\underline{v}\in V$, I can write $\underline{v}=b_{1}\underline{x}_{1}+b_{2}\underline{x}_{2}+b_{3}\underline{x}_{3}$, to calculate $b_{2}$, we simply take the [[Dot Product|dot product]] of this equation with $\underline{x}_{2}$:
$$
\underline{v}\cdot \underline{x}_{2}=(b_{1}\underline{x}_{1}+b_{2}\underline{x}_{2}+b_{3}\underline{x}_{3})\cdot \underline{x}_{2}=b_{1}\underline{x}_{1}\cdot \underline{x}_{2}+b_{2}\underline{x}_{2}\cdot \underline{x}_{2}+b_{3}\underline{x}_{3}\cdot \underline{x}_{2}=b_{2}\underline{x}_{2}\cdot \underline{x}_{2}
$$
So
$$
b_{2}=\frac{\underline{v}\cdot \underline{x}_{2}}{\underline{x}_{2}\cdot \underline{x}_{2}}
$$
___
Find components of $\underline{v}={-1 \choose -7 }$ in the basis $\underline{x}_{1}={2 \choose -1 },\underline{x}_{2}={1 \choose 2 }$,
$$
\underline{v}=b_{1}\underline{x}_{1}+b_{2}\underline{x}_{2}
$$
So
$$
b_{1}= \frac{\underline{v}\cdot \underline{x}_{1}}{\underline{x}_{1}\cdot \underline{x}_{1}}=\frac{5}{5}=1
$$
$$
b_{2}=\frac{\underline{v}\cdot \underline{x}_{2}}{\underline{x}_{2}\cdot \underline{x}_{2}}=-\frac{15}{3}=-3
$$
So
$$
\begin{pmatrix}
-1\\-7
\end{pmatrix}=\begin{pmatrix}
2\\-1
\end{pmatrix}-3\begin{pmatrix}
1\\2
\end{pmatrix}
$$
## Observation 2
The [[Eigenvectors|eigenvectors]]/[[Eigenfunctions|eigenfunctions]] of a [[Self-Adjoint|self-adjoint]] [[Matrices|matrix]]/operator are orthogonal
### Proof
Let $\underline{v}_{1},\underline{v}_{2}$ be eigenvectors of $\mathcal{L}$:
$$
\mathcal{L}\underline{v}_{1}=\lambda_{1}\underline{v}_{1}
$$
$$
\mathcal{L}\underline{v}_{2}=\lambda_{2}\underline{v}_{2}
$$
Consider
$$
(\underline{v}_{1},\mathcal{L}\underline{v}_{2})=(\underline{v}_{1},\lambda_{2}\underline{v}_{2})=\overline{\lambda_{2}}
$$
$$
(\mathcal{L}_{1}\underline{v}_{1},\underline{v}_{2})=(\lambda_{1}\underline{v}_{1},\underline{v}_{2})=\overline{\lambda_{1}}(\underline{v}_{1},\underline{v}_{2})
$$
So
$$
(\lambda_{1}-\lambda_{2})(\underline{v}_{1},\underline{v}_{2})=0
$$
If $\lambda_{1}\neq\lambda_{2}$, then $(\underline{v}_{1},\underline{v}_{2})$ are orthogonal. If $\lambda_{1}=\lambda_{2}$, we can pick $\underline{v}_{1},\underline{v}_{2}$ that are orthogonal using [[Gram-Schmidt Procedure|Gram-Schmidt]]
___
For example using the Legendre expansion $y=\sum_{n=0}^{\infty} b_{n}p_{n}$, where $p_{n}$ are eigenvectors of $\mathcal{L}_{L}$. If $\mathcal{L}_{L}$ is self-adjoint, then $p_{n}$ are orthogonal to each other, so it is easy to find components $b_{n}$
 So we need to find an inner product for which $\mathcal{L}_{L}$ is self-adjoint, we choose
 $$
(f(x),g(x))=\int _{-1}^{1}f(x)g(x) \, dx 
$$
(recall how $-1$ and $1$ are the points where Legendre's has singular points)
The Legendre differential operator can be written:
$$
\mathcal{L}_{L}y=\left[ (x^{2}-1)\frac{d ^{2}y}{dx^{2}} +2x\frac{d y}{dx}  \right]=\frac{d }{dx} \left[ (x^{2}-1)\frac{d y}{dx}  \right]
$$
So
$$
(\mathcal{L}_{L_{1}f,g})=\left( \frac{d }{dx} \left[ (x^{2}-1)\frac{d f}{dx}  \right],g \right)=\int_{-1}^{1} \frac{d }{dx} \left[ (x^{2}-1)\frac{d f}{dx}  \right]g(x) \, dx 
$$
Here we [[Integration by Parts|integrate by parts]]:
$$
=\left[ (x^{2}-1)\frac{d f}{dx} g \right]_{-1}^{1}-\int_{-1}^{1} (x^{2}-1)\frac{d f}{dx} \frac{d g}{dx}  \, dx 
$$
Here we insist $f,g$ are [[Differentiation|differentiable]] and $f,f'$ are finite at $x=\pm 1$, so the first term is $\hspace{0pt}0$. Then we integrate by parts agian:
$$
=-\left[ (x^{2}-1)f\frac{d g}{dx}  \right]^{1}_{-1}+\int _{-1}^{1}f\frac{d }{dx} \left[ (x^{2}-1)\frac{d g}{dx}  \right] \, dx 
$$
Again the first term vanishes, and the second term is what we wanted, so
$$
=\int_{_1}^{1} f\mathcal{L}_{L}g \, dx =(f,\mathcal{L}_{L}g)
$$
So $\mathcal{L}_{L}$ is self-adjoint with that inner product
So the eigenfunctions of $\mathcal{L}_{L}$ are orthogonal, so
$$
(P_{n},P_{m})=\int_{-1}^{1} p_{n}p_{m} \, dx =0,n\neq m
$$
So we have the Legendre expansion $y(x)=\sum_{n=0}^{\infty} b_{n}p_{n}(x)$, so find $b_{m}$, so we can take the inner product of the equation with $p_{m}(x)$:
$$
(y,p_{m})=\left( \sum_{n=0}^{\infty} b_{n}p_{n} ,p_{m} \right)=\sum_{n=0}^{\infty} b_{n}(p_{n},p_{m})=b_{m}(p_{m},p_{n})
$$
$$
\therefore  b_{m}= \frac{(y,p_{m})}{(p_{m},p_{m})}
$$
And we have
$$
(p_{m},p_{m})=\int _{-1}^{1}p_{m}^{2}(x) \, dx =\frac{2}{2m+1}
$$
$$
\therefore b_{m}=\frac{2m+1}{2}(y,p_{m})=\frac{(2m+1)}{2}\int_{-1}^{1} y(x)p_{m}(x) \, dx 
$$
If $y(x)$ is even/odd, then $b_{m}=0$ for $m$ even/odd, since it will be the integral of an odd function as $p_{m}(x)$ is odd/even for odd/even $m$
### Example
Find the first non-vanishing term in the Legendre expansion of
$$
\cos(\pi x)=\sum_{k=0}^{\infty} b_{k}P_{k}(x) 
$$
$$
b_{0}=\frac{1}{2}\int_{-1}^{1} y(x)P_{0}(x) \, dx =\frac{1}{2}\int_{-1}^{1} \cos(\pi x) \, dx =\frac{1}{2\pi}[\sin(\pi x)]=0
$$
$$
b_{1}=\frac{3}{2}\int_{-1}^{1} y(x)P_{1}(x) \, dx =\frac{3}{2}\int_{-1}^{1} \underbrace{ x\cos(\pi x) }_{ \text{odd}\times \text{even}=\text{odd} } \, dx =0
$$
We can extend this logic and say that for odd $n$, since $\cos$ is even, will integrate an odd function, so will vanish
$$
b_{2}=\frac{5}{2}\int_{-1}^{1} y(x)P_{2}(x) \, dx =\frac{5}{4}\int_{-1}^{1} \cos(\pi x)(3x^{2}-1) \, dx 
$$
$$
= \frac{5}{4\pi}\underbrace{ [\sin(\pi x)(3x^{2}-1)]_{-1}^{1} }_{ =0 }-\frac{15}{2\pi}\int_{-1}^{1} \sin(\pi x)x \, dx =\frac{15}{2\pi^{2}}[\cos(\pi x)x]_{-1}^{1}-\frac{15}{\pi^{2}}\int_{-1}^{1} \cos(\pi x) \, dx =-\frac{15}{\pi^{2}}
$$
So the first non-vanishing term is $\cos(\pi x)\approx-\frac{15}{2\pi^{2}}(3x^{2}-1)$ 