You can approximate [[Periodic Functions|periodic]] [[Functions|functions]] using trigonometric functions such as $\sin$ and $\cos$ using the following method
The fourier series for a function $f(x)$ [[Convergence|converges]] is $f(x)$ is [[Square-Integrable|square-integrable]] .
# 1D
Consider a function $f(x)$ of period $2L$ ($f(x+2L)=f(x)$) given on the interval $(-L,L)$ The functions $\cos\left( \frac{n\pi x}{L} \right),\sin\left( \frac{n\pi x}{L} \right)$, for $n\in\mathbb{N}$ are also periodic with period $2L$, so we can try to write $f(x)$ in terms of these functions
Since any constant is periodic (for any period), we can include a constant term
We therefore aim to express $f(x)$ as:
$$
f(x)=\frac{a_{0}}{2}+\sum_{ n=1} ^{\infty}  \left( a_{n}\cos\left( \frac{n\pi x}{L} \right)+b_{n}\sin\left( \frac{n\pi x}{L} \right) \right)
$$
where $a_{0},a_{n},b_{n}$ are constants labelled by the positive integer $n$, and are called the Fourier coefficients of $f(x)$
If the constants are such that the series converges, then it is called the Fourier Series of $f(x)$
___
Fourier Series can be thought of as "frequency analysis of periodic functions" and $a_{n}$ and $b_{n}$ tell you how much frequency $n$ is in $f(x)$. If we consider the graph of $\sin(nx)$, we can get various properties from it:
![[Fourier Series 2025-03-11 14.14.21.excalidraw]]
So we find that [[Wavelength|wavelength]] is $\lambda=\frac{2\pi}{n}$, the [[Frequency|frequency]] is $\frac{1}{\lambda}=\frac{n}{2\pi}$ and the angular frequency is $2\pi f=n$
This is very useful for example it is how our brains analyse sound and so on
## Example
$$
f(x)=2\cos ^{2}\left( \frac{\pi x}{L} \right)+3\sin\left( \frac{\pi x}{L} \right)
$$
Has period $2L$
Since $\cos(2x)=2\cos ^{2}x-1$,
$$
f(x)=1+\cos\left( \frac{2\pi x}{L} \right)+3\sin\left( \frac{\pi x}{L} \right)
$$
Is the Fourier Series of $f(x)$ containing only a finite number of terms with $a_{0}=2$, $a_{2}=1$, $b_{1}=3$, and all the other coefficients are $\hspace{0pt}0$
In general, an infinite number of coefficients may be non-zero, so we need a method to find them for a given $f(x)$
## Identities :)
Let $m$ and $n$ be positive integers, then:
$$
\frac{1}{L}\int _{-L}^{L}\cos\left( \frac{n\pi x}{L} \right) \, dx =0
$$
$$
\frac{1}{L}\int _{-L}^{L}\sin\left( \frac{n\pi x}{L} \right) \, dx =0
$$
$$
\frac{1}{L}\int _{-L}^{L} \sin\left( \frac{n\pi x}{L} \right)\cos\left( \frac{n\pi x}{L} \right) \, dx =0
$$
$$
 \frac{1}{L}\int _{-L}^{L} \cos\left( \frac{n\pi x}{L} \right)\cos\left( \frac{m\pi x}{L} \right) \, dx =\begin{cases}
0&\text{if }m\neq n\\1&\text{if }m=n
\end{cases}
$$
$$
\frac{1}{L}\int _{-L}^{L}\sin\left( \frac{n\pi x}{L} \right)\sin\left( \frac{m\pi x}{L} \right) \, dx =\begin{cases}
0&\text{if }m\neq n\\1&\text{if }m=n
\end{cases}
$$
It is convenient to use the [[Kronecker Delta Function|Kronecker Delta function]] to rewrite the last two:
$$
 \frac{1}{L}\int _{-L}^{L} \cos\left( \frac{n\pi x}{L} \right)\cos\left( \frac{m\pi x}{L} \right) \, dx =\delta_{mn}
$$
$$
\frac{1}{L}\int _{-L}^{L}\sin\left( \frac{n\pi x}{L} \right)\sin\left( \frac{m\pi x}{L} \right) \, dx =\delta_{mn}
$$
### Proof
For the first:
$$
\frac{1}{L}\int _{-L}^{L}\cos\left( \frac{n\pi x}{L} \right) \, dx =\frac{1}{L}\left[ \frac{L}{n\pi}\sin\left( \frac{n\pi x}{L} \right) \right]_{-L}^{L}=0
$$
For the second and third, these are immediate as they are integrals of [[Odd Functions|odd functions]] over symmetric intervals
For the fourth, recall $\cos(x\pm y)=\cos(x)\cos(y)\mp \sin(x)\sin(y)$, which can be used to obtain $\cos(x+y)+\cos(x-y)=2\cos(x)\cos(y)$
Then, first assuming $m\neq n$,
$$
\frac{1}{L}\int _{-L}^{L}\cos\left( \frac{m\pi x}{L} \right)\cos\left( \frac{n\pi x}{L} \right) \, dx =\frac{1}{L}\int _{-L}^{L} \cos\left( \frac{(m+n)\pi x}{L} \right)+\cos\left( \frac{(m-n)\pi x}{L} \right)\, dx 
$$
$$
= \frac{1}{2L}\left[ \frac{L}{(m+n)\pi}\sin\left( \frac{(m+n)\pi x}{L} \right)+\frac{L}{(m-n)\pi}\sin\left( \frac{(m-n)\pi x}{L} \right) \right]_{-L}^{L}=0
$$
If $m=n$,
$$
\frac{1}{L}\int _{-L}^{L}\cos\left( \frac{m\pi x}{L} \right)\cos\left( \frac{n\pi x}{L} \right) \, dx =\frac{1}{L}\int _{-L}^{L}\cos ^{2}\left( \frac{n\pi x}{L} \right) \, dx
$$
$$
= \frac{1}{2L}\int _{-L}^{L}1+\cos\left( \frac{2n\pi x}{L} \right) \, dx =\frac{1}{2L}\left[ x+\frac{L}{2n\pi}\sin\left( \frac{2n\pi x}{L} \right) \right]^{L}_{-L}=\frac{1}{2L}(L--L)=1 
$$
For the fifth, the method is similar to above (pls do here)

In general if $f(x)$ is even on $(-L,L)$, then all $b_{n}=0$ and the Fourier series contains only $\cos$ terms (plus a constant term) we call such a series a cosine series
## Fourier Coefficients
We say that the [[Sets|set]] of functions $\left\{  1,\cos\left( \frac{n\pi x}{L} \right),\sin\left( \frac{n\pi x}{L} \right)  \right\}$ form an orthogonal (or [[Orthonormal Vectors|orthonormal]]) set on $[-L,L]$, because if $\phi,\psi$ are different elements of the set, then 
$$
\frac{1}{L}\int _{-L}^{L}\phi \psi \, dx =0
$$
We can now use these identities to determine the Fourier Coefficients, firstly by integrating the original series:
$$
\frac{1}{L}\int _{-L}^{L}f(x) \, dx =\frac{1}{L}\int _{-L}^{L} \frac{a_{0}}{2}+\sum_{n=1}^{\infty} \left[ a_{n}\cos \left( \frac{n\pi x}{L} \right)+b_{n}\sin\left( \frac{n\pi x}{L} \right) \right]  \, dx 
$$
$$
= \frac{1}{L}\left[ \frac{a_{0}x}{2} \right]_{-L}^{L}=a_{0}
$$
By idendities $\hspace{0pt}1$ and $\hspace{0pt}2$, therefore:
$$
a_{0}=\frac{1}{L}\int_{-L}^{L}f(x)  \, dx 
$$
Or $a_{0}=<1,f(x)>$ where $<f,g> =\frac{1}{L}\int _{-L}^{L}fg \, dx$
Now letting $m$ be a positive integer, and multiplying the fourier series by $\cos\left( \frac{m\pi x}{L} \right)$ and integrating,
$$
\frac{1}{L}\int _{-L}^{L}f(x)\cos\left( \frac{m\pi x}{L} \right) \, dx 
$$
$$
 =\frac{1}{L}\int _{-L}^{L} \left( \frac{a_{0}}{2}+\sum_{n=1}^{\infty}\left( a_{n}\cos\left( \frac{n\pi x}{L} \right) \right)+b_{n} \sin\left( \frac{n\pi x}{L} \right)  \right)\cos\left( \frac{n\pi x}{L} \right) \, dx =\sum_{n=1}^{\infty} a_{n}\delta_{mn}=a_{m} 
$$
By identities $1,3,4$, so
$$
a_{n}=\frac{1}{L}\int _{-L}^{L}f(x)\cos\left( \frac{n\pi x}{L} \right) \, dx 
$$
Or $a_{n}= <f,\cos\left( \frac{n\pi x}{L} \right)>$
Note that with $n=0$, this also gives the correct expression for $a_{0}$
Similarly multiplying the fourier series by $\sin\left( \frac{m\pi x}{L} \right)$ and integrating gives
$$
\frac{1}{L}\int _{-L}^{L}f(x)\sin\left( \frac{m\pi x}{L} \right) \, dx=\frac{1}{L}\int _{-L}^{L}\left( \frac{a_{0}}{2}+\sum_{n=1}^{\infty} a_{n}\cos\left( \frac{n\pi x}{L} \right) +b_{n}\sin\left( \frac{n\pi x}{L} \right)\right) \, dx 
$$
pls finish :)


In order to see how the Fourier series apporaches $f(x)$ we can define the partial sum:
$$
S_{m}(x)=\frac{a_{0}}{2}+\sum_{n=1}^{m}a_{n}\cos\left( \frac{n\pi x}{L} \right)+b_{n}\sin\left( \frac{n\pi x}{L} \right)
$$
In general the partial sum $S_{m}$ is an approximation to $f(x)$ which improves as $m\to \infty$
In general we want to know what happens to the partial sum $S_{m}(x)$ for all $x$ as $m\to \infty$ and how this relates to the original function
## Linear Algebra Derivation
If $y(x)$ is a function of periodicity $2L$, we can write
$$
y(x)=\frac{a_{0}}{2}+\sum_{n=1}^{\infty} a_{n}\cos\left( \frac{n\pi x}{L} \right)+\sum_{n=1}^{\infty} b_{n}\sin\left( \frac{n\pi x}{L} \right)  
$$
So we have the [[Basis|basis]] [[Eigenfunctions|eigenfunctions]] of some [[Linear Differential Operators|differential operator]] $\mathcal{L}_{F}$. We know that these coefficients satisfy:
$$
a_{n}=\frac{1}{L}\int _{-L}^{L}y(x)\cos\left( \frac{n\pi x}{L} \right) \, dx =\frac{\left( y,\cos\left( \frac{n\pi x}{L} \right) \right)}{\left( \cos\left( \frac{n\pi x}{L} \right),\cos\left( \frac{n\pi x}{L} \right) \right)}
$$
For some [[Inner Product|inner product]], so we will take the inner product to be:
$$
(f,g)=\int _{-L}^{L}f(x)g(x) \, dx 
$$
We know that $\sin (nx),\cos(nx)$ satisfy [[Simple Harmonic Motion|simple harmonic motion]] differential equations: $y''+n^{2}y=0$, so 
$$
\mathcal{L}_{F}=\frac{d ^{2}}{dx^{2}} 
$$
Now we must check whether $\mathcal{L}_{F}$ is [[Self-Adjoint|self-adjoint]] with respect to the inner product, so we need to show
$$
(\mathcal{L}_{F}f,g)=(f,\mathcal{L}_{F}g)
$$
$$
 (\mathcal{L}_{F}f,g)=       (f'',g)=\int_{-L}^{L}f''g  \, dx =[f'g]_{-L}^{L}-\int_{-L}^{L}f'g'  \, dx =[f'g]_{-L}^{L}-[fg']_{-L}^{L}+\int_{-L}^{L}fg'  \, dx 
$$
$$
 =[f'g-fg']_{-L}^{L}+(f,\mathcal{L}_{F}g)
$$
So we need $[f'g-g'f]_{-L}^{L}=0$, which is true if $f,g$ are periodic with period $2L$ 
So what are the eigenfunctions of $\mathcal{L}_{F}=\frac{d ^{2}}{dx^{2}}$ which are periodic with period $2L$. 
We want to solve $y''=\lambda y$, so let 
$\lambda=n^{2}>0$, then $y''=n^{2}y$ gives $y(x)=Ae^{ nx }+Be^{ -nx }$ which has no non-vanishing periodic functions
$\lambda=0$, then $y''=0$ which gives $y(x)=Ax+B$, so $y=1$ is periodic and no others
$\lambda=-n^{2}<0$, then $y(x)=A\sin(nx)+B\cos(nx)$ which has periodicity $2\pi$ when $n$ is a positive integer, so we can scale this to find $n$ periodic with period $2L$
So the eigenfunctions of $\mathcal{L}_{F}$ with period $2\pi$ are $\left\{ 1,\cos(nx),\sin(nx) \right\}$, so
$$
y(x)=\frac{a_{0}}{2}+\sum_{n=1}^{\infty} a_{n}\cos\left( \frac{nx\pi}{L} \right)+\sum_{n=1}^{\infty} b_{n}\sin\left( \frac{n\pi x}{L} \right)  
$$
And $\left\{ \cos(nx),\sin(nx) \right\},1$ are orthogonal since $\mathcal{L}_{F}$ is self-adjoint
### Example
Find $b_{7}$ in the expansion, i.e. the coefficient of $\sin(7x)$: 
$$
(y(x),\sin(7x))=\left( \frac{a_{0}}{2}+\sum_{n=1}^{\infty} a_{n}\cos\left( \frac{nx\pi}{L} \right)+\sum_{n=1}^{\infty} b_{n}\sin\left( \frac{n\pi x}{L} \right), \sin(7x)  \right)
$$
$$
= a_{0}\left( \frac{1}{2},\sin(7x) \right)+\sum_{n=1}^{\infty} a_{n}\left( \cos \left( \frac{n\pi x}{L} \right),\sin(7x) \right)+\sum_{n=1}^{\infty} b_{n} \left( \sin\left( \frac{n\pi x}{L} \right),\sin(7x) \right) 
$$
Which are all $0$, except the coefficient of $\sin(7x)$
## Cosine Series
If $f(x)$ is [[Even Functions|even]] on $(-L,L)$, then all $b_{n}=0$ and the Fourier series contains only cosine terms (plus a constant), such a series is called a cosine series
## Sine Series
If $f(x)$ is [[Odd Functions|odd]] on $(-L,L)$, then all $a_{n}=0$ and the Fourier series contains only sine terms, such a series is called a sine series
## Half-Range Fourier Series
Given a function $f(x)$ defined on $(0,L)$, we can find different Fourier series which converge to $f(x)$ on $(0,L)$
Given $f(x)$ on $(0,L)$, we obtain it's half range sine series by calculating the Fourier sine series of its odd extension:
$$
f_{o}(x)=\begin{cases}
f(x)&x\in (0,L)\\-f(-x)&x\in (-L,0)
\end{cases}
$$
The Fourier coefficients of $f_{o}(x)$ are $a_{n}=0$ and 
$$
b_{n}=\frac{1}{L}\int _{-L}^{L}f_{o}(x)\sin\left( \frac{n\pi x}{L} \right) \, dx=\frac{2}{L}\int _{0}^{L}f(x)\sin\left( \frac{n\pi x}{L} \right) \, dx 
$$
The half range sine series for $f(x)$ on $(0,L)$ is then
$$
f(x)=\sum_{ n=1} ^{\infty}  b_{n}\sin\left( \frac{n\pi x}{L} \right)
$$
Similarly, given $f(x)$ on $(0,L)$, we obtain it's half range cosine series by calculating the Fourier series of its even extension
$$
f_{e}(x)=\begin{cases}
f(x)&x\in (0,L)\\f(-x)&x\in (-L,0)
\end{cases}
$$
The Fourier coefficients of $f_{e}(x)$ are $b_{n}=0$ and
$$
    a_{n}=\frac{1}{L}\int _{-L}^{L}f_{e}(x)\cos\left( \frac{n\pi x}{L} \right) \, dx =\frac{2}{L}\int_{0}^{L}f(x)\cos\left( \frac{n\pi x}{L} \right) \, dx 
$$
This gives the half range cosine series for $f(x)$ on $(0,L)$ as
$$
f(x)=\frac{a_{0}}{2}+\sum_{ n=1} ^{\infty}  a_{n}\cos\left( \frac{n\pi x}{L} \right)
$$
So we have two different ways of writing different Fourier series that converge to the same function on the interval $(0,L)$
For a given problem on $(0,L)$, it is usually the boundary conditions which determine whether a half range sine or cosine series is appropriate
## Fourier Series in Complex Form
Fourier series can be written in a more compact simple form if written in terms of complex variables. Given the Fourier series
$$
f(x)=\frac{a_{0}}{2}+\sum_{ n=1} ^{\infty}  \left( a_{n}\cos\left( \frac{n\pi x}{L} \right)+b_{n}\sin\left( \frac{n\pi x}{L} \right) \right)
$$
We can use the identities 
$$
\cos\left( \frac{n\pi x}{L} \right)=\frac{1}{2}(e^{ in\pi x/L }+e^{ -in\pi x/L })
$$
$$
 \sin\left( \frac{n\pi x}{L} \right)=\frac{1}{2i}(e^{ in\pi x/L }-e^{ -in\pi x/L })
$$
To rewrite this as:
$$
f(x)=\frac{a_{0}}{2}+\frac{1}{2}\sum_{ n=1} ^{\infty}  (a_{n}-ib_{n})e^{ in\pi x/L }+(a_{n}+ib_{n})e^{ -in\pi x/L }
$$
$$
=\sum_{ n=-\infty} ^{\infty}  c_{n}e^{ in\pi x/L }
$$
Where we define 
$$
c_{0}=\frac{a_{0}}{2}=\frac{1}{2L}\int _{-L}^{L}f(x) \, dx 
$$
For $n>0$:
$$
c_{n}=\frac{1}{2}(a_{n}-ib_{n})=\frac{1}{2L}\int_{-L}^{L}f(x)\cos\left( \frac{n\pi x}{L} \right)-i\sin\left( \frac{n\pi x}{L} \right) \, dx 
$$
$$
= \frac{1}{2L}\int _{-L}^{L}f(x)e^{ -in\pi x/L } \, dx 
$$
For $n<0$:
$$
c_{n}=\frac{1}{2}(a_{-n}+ib_{-n})=\frac{1}{2L}\int _{-L}^{L}f(x)\cos\left( -\frac{n\pi x}{L} \right)+i\sin\left( -\frac{n\pi x}{L} \right) \, dx 
$$
$$
= \frac{1}{2L}\int _{-L}^{L}f(x)e^{ -in\pi x/L } \, dx 
$$
Which is the same formula for all three cases which can be written as a single formula:
$$
c_{n}=\frac{1}{2L}\int _{-L}^{L}f(x)e^{ -in\pi x/L } \, dx 
$$
With Fourier series
$$
f(x)=\sum_{ n=-\infty} ^{\infty}  c_{n}e^{ in\pi x/L }
$$
## Examples
The function $f(x)$ has period $\hspace{0pt}2$ i.e. $f(x+2)=f(x)$ and is given by $f(x)=|x|$ for $-1<x<1$, so looks like:
![[Fourier Series 2024-12-10 14.40.53.excalidraw]]
To calculate the Fourier series of $f(x)$, we compute the Fourier coefficients using our previous results with $L=1$
$$
a_{0}=\int _{-1}^{1}f(x) \, dx =\int _{-1}^{1}\left| x \right|  \, dx =2\int _{0}^{1}x \, dx =[x^{2}]_{0}^{1}=1
$$
For $n>0$:
$$
a_{n}=\int _{-1}^{1}f(x)\cos(n\pi x) \, dx =\int _{-1}^{1}\left| x \right| \cos(n\pi x) \, dx 
$$
$$
= 2\int _{0}^{1}x\cos(n\pi x) \, dx =2\left( \underbrace{ \left[ \frac{1}{n\pi}\sin(n\pi x) \right]_{0}^{1} }_{ =0 }-\int _{0}^{1} \frac{1}{n\pi}\sin (n\pi x) \, dx  \right)
$$
$$
= \frac{2}{n^{2}\pi^{2}}[\cos(n\pi x)]_{0}^{1}=\frac{2}{n^{2}\pi^{2}}(\cos(n\pi)-1=\frac{2}{n^{2}\pi^{2}}((-1)^{n}-1)
$$
$$
b_{n}=\int _{-1}^{1}\left| x \right| \sin(n\pi x) \, dx =0
$$
Since this is the integral of an odd function over a symmetric interval
Putting the above together, we have the Fourier cosine series for $f(x)$
$$
f(x)=\frac{a_{0}}{2}+\sum_{n=1}^{\infty} a_{n}\cos\left( \frac{n\pi x}{L} \right)+b_{n}\left( \frac{n\pi x}{L} \right) 
$$
$$
=\frac{1}{2}+\sum_{n=1}^{\infty} \frac{2((-1)^{n}-1)}{n^{2}\pi^{2}}\cos(n\pi x)
$$
$$
= \frac{1}{2}-\frac{4}{\pi^{2}}\left( \cos(\pi x)+\frac{1}{9}\cos(3\pi x)+\dots \right)
$$
Note that in this example $a_{2n}=0$, and $a_{2n-1}=-\frac{4}{(2n-1)^{2}\pi^{2}}$
So we can also write the Fourier series as:
$$
f(x)=\frac{1}{2}-\frac{4}{\pi^{2}}\sum_{ n=1} ^{\infty}  \frac{\cos((2n-1)\pi x)}{(2n-1)^{2}}
$$
In this example
$$
S_{1}=\frac{1}{2}-\frac{4}{\pi^{2}}\cos(\pi x)=S_{2}
$$
$$
S_{3}=\frac{1}{2}-\frac{4}{\pi^{2}}\left( \cos(\pi x)+\frac{1}{9}\cos(3\pi x) \right)=S_{4}
$$
___
Let $f(x)$ have period $2\pi$ and be iven by $f(x)=x$ for $-\pi<x<\pi$, calculate the Fourier series of $f(x)$. This time the function looks like
![[Fourier Series 2024-12-31 15.18.32.excalidraw]]
Note this function has jump discontinuities at $x=(2p+1)\pi$ for $p \in\mathbb{Z}$
We use our previous results with $L=\pi$. For $n\geq 0$:
$$
a_{n}=\frac{1}{\pi}\int _{-\pi}^{\pi}x\cos(nx) \, dx =0
$$
Since this is the integral of an odd function function over a symmetric interval
For $n>0$,
$$
b_{n}=\frac{1}{\pi}\int _{-\pi}^{\pi}x\sin(nx) \, dx =\frac{1}{\pi}\left( \left[ -\frac{x}{n}\cos(nx) \right]^{\pi}_{-\pi}-\frac{1}{n}\int _{-\pi}^{\pi}\cos(nx) \, dx  \right)
$$
$$
= \frac{1}{\pi}\left( -\frac{\pi}{n}\cos(n\pi)-\frac{\pi}{n}\cos(n\pi) +\underbrace{ \left[ \frac{1}{n^{2}}\sin(nx) \right]_{-\pi}^{\pi} }_{ =0 } \right)
$$
$$
= -\frac{2}{n}\cos(n\pi)=-\frac{2}{n}(-1)^{n}=\frac{2}{n}(-1)^{n+1}
$$
We therefore have the Fourier sine series
$$
f(x)=\sum_{ n=1} ^{\infty}  \frac{2(-1)^{n+1}}{n}\sin(nx)
$$
$$
= 2\left( \sin (x)-\frac{1}{2}\sin(2x)+\frac{1}{3}\sin(3x)+\dots \right)
$$
As we include more terms in the partial sum, the Fourier series becomes an increasingly accurate approximation to $f(x)$ on $(-\pi,\pi)$, however at the points $x=(2p+1)\pi$, $p \in\mathbb{Z}$, where $f(x)$ is not [[Continuity|continuous]], the Fourier series converges to $0$, the midpoint of the jump
___
Let $f(x)$ have period $2\pi$ and be given as 
$$
f(x)=\begin{cases}
1&0\leq x< \pi\\
-1&-\pi<x<0
\end{cases}
$$
Then we can use the complex form
$$
c_{n}=\frac{1}{2\pi}\int _{-\pi}^{\pi}f(x)e^{ -inx } \, dx 
$$
$$
= -\frac{1}{2\pi}\int _{-\pi}^{0}e^{ -inx } \, dx +\frac{1}{2\pi}\int _{0}^{\pi}e^{ -inx } \, dx 
$$
For $n=0$, 
$$
c_{0}=-\frac{1}{2\pi}\int _{\pi}^{0}1 \, dx+\frac{1}{2\pi}\int _{0}^{\pi}1 \, dx =-\frac{1}{2}+\frac{1}{2}=0
$$
For $n\neq 0$,
$$
c_{n}=\left[ \frac{1}{2\pi in}e^{ -inx } \right]_{-\pi}^{0}-\left[ \frac{1}{2\pi in}e^{ -inx } \right]_{0}^{\pi}=\frac{1}{2\pi in}(1-e^{ in\pi }-e^{ -in\pi }+1)
$$
$$
= \frac{i}{\pi n}(e^{ in\pi }-1)=\frac{i}{\pi n}((-1)^{n}-1)
$$
So $c_{2m}=0$ and $c_{2m+1}=-\frac{2i}{\pi(2m+1)}$, so
$$
f(x)=\sum_{ n=-\infty} ^{\infty}  -\frac{2i}{\pi(2n+1)}e^{ i(2n+1)x }
$$
This can be converted back to the real form, since $f(x)=\overline{f(x)}$,
$$
2f(x)=\sum_{ n=-\infty} ^{\infty}  -\frac{2i}{\pi(2n+1)}e^{ i(2n+1)x }+\sum_{ n=-\infty} ^{\infty}  \frac{2i}{\pi(2n+1)}e^{ -i(2n+1)x }
$$
Hence
$$
f(x)=\sum_{ n=-\infty} ^{\infty}  -\frac{i}{\pi(2n+1)}(e^{ i(2n+1)x }-e^{ -i(2n+1)x })
$$
$$
= \sum_{ n=-\infty} ^{\infty}  \frac{2}{\pi(2n+1)}\sin((2n+1)x)
$$
$$
= \sum_{ n=0} ^{\infty}  \frac{4}{\pi(2n+1)}\sin((2n+1)x)
$$
# 2D
In 2D it is similar, except we have to consider every possible combination for $x$ and $y$:
If $x\in[0,Lx]$,$y\in[0,Ly]$
$$
f(x,y) = \sum_{n=0}^{\infty}\sum_{m=0}^{\infty}\left(a_{mn}\cos\left( \frac{n\pi x}{Lx} \right)\cos\left( \frac{m\pi y}{Ly} \right)\right|
$$
$$
 +b_{nm}\cos\left( \frac{n\pi x}{Lx} \right)\sin\left( \frac{m\pi x}{Ly} \right)
$$
$$
 +c_{nm}\sin\left( \frac{n\pi x}{Lx} \right)\cos\left( \frac{m\pi y}{Ly} \right)
$$
$$
\left| +d_{nm}\sin\left( \frac{n\pi x}{Lx} \right)\sin\left( \frac{m\pi y}{Ly} \right)\right)
$$
And we can find the coefficients:
$$
a_{nm}=\frac{4}{LxLy}\int _{0}^{Lx}\int_{0}^{Ly} f(x,y)\cos\left( \frac{n\pi x}{Lx} \right)\cos\left( \frac{m\pi y}{Ly} \right) \, dy  \, dx 
$$
And similar for the other coeffs...
These again rely on the integral making them orthogonal

#Mathematics #Calculus 