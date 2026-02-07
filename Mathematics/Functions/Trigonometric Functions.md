We define the sine and cosine function by
$$
\sin(x):=\sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k+1)!}x^{2k+1}
$$
$$
 \cos(x):=\sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k)!}x^{2k}  
$$
By [[Ratio Test|ratio test]], (or [[Series#Comparison Test|comparison test]] with [[Exponential Functions|$\exp(x)$]]) we see that the [[Cauchy-Hadamard Theorem|radius of convergence]] is $R=\infty$
We have various properties:
## $f(0)$
$$
\sin(0)=\sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k+1)!}0^{2k+1}=0 
$$
$$
 \cos(0)=\sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k)!}0^{2k}=1+0+0+\dots=1 
$$
## Odd/Even
Since each term in $\sin$ is [[Odd Functions|odd]], $\sin$ is odd. Since each term in $\cos$ is [[Even Functions|even]], $\cos$ is even
## Differentiation
Sine and cosine are infinitely [[Differentiation|differentiable]] with
$$
\sin'(x)=\cos(x),\cos'(x)=-\sin(x)
$$
This can be obtained by differentiating term-wise

## Compound Angle Formulae
We want to show
$$
\sin(x+y)=\sin(x)\cos(y)+\cos(x)\sin(y)
$$
$$
 \cos(x+y)=\cos(x)\cos(y)-\sin(x)\sin(y)
$$
We consider a function
$$
f(t)=\sin(x+t)\cos(y-t)+\cos(x+t)\sin(y-t)
$$
$$
f(0)=\sin(x)\cos(y)+\cos(x)\sin(y)
$$
$$
f(y)=\sin(x+y)\cos(0)+\cos(x+y)\sin(0)=\sin(x+y)
$$
$$
f'(t)=\cos(x+t)\sin(y-t)-\sin(x+t)
$$
## [[Pythagoras' Theorem|Pythagoras' Theorem]]
We want to show:
$$
\sin ^{2}(x)+\cos ^{2}(x)=1
$$
In particular,
$$
\left| \sin(x) \right| \leq 1,\left| \cos(x) \right| \leq 1\forall x\in \mathbb{R}
$$
If we consider $x=0$
$$
\sin ^{2}(0)+\cos ^{2}(0)=0+1=1
$$
Next we differentiate $\sin ^{2}(x)+\cos ^{2}(x)$:
$$
2\sin(x)\cos(x)-2\cos(x)\sin(x)=0
$$
So by the [[Monotonic Functions#Growth Theorem|growth theorem]], $\sin ^{2}(x)+\cos ^{2}(x)$ is constant, and since at $x=0$, it is $1$, we have that it is $1$ for all $x\in\mathbb{R}$
The second part is trivially true considering $x^{2}\geq 0\forall x$
## The Equation $\cos(x)=0$ has a Smallest Positive Solution
Consider $\cos(2)$. We have:
$$
\sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k)!}2^{2k}=1-2+\frac{16}{24}+\sum_{k=3}^{\infty} \frac{(-1)^{k}}{(2k)!}2^{2k}=-\frac{2}{3}+\sum_{k=3}^{\infty} \frac{(-1)^{k}}{(2k)!}2^{2k}   
$$
The tail is an [[Alternating Series|alternating series]] with decreasing terms:
$$
\frac{2^{2(k+1)}}{(2(k+1))!}=\frac{4}{(2k+2)(2k+1)} \frac{2^{2k}}{(2k)!}< \frac{2^{2k}}{(2k)!}
$$
By the alternating series test, we see that its value must be a negative number, since $\cos(0)=1>0$, by the [[Intermediate Value Theorem|intermediate value theorem]], the cosine function has a [[Roots|root]] in the [[Intervals|interval]] $(0,2)$. Hence the set
$$
X:=\left\{ x>0|\cos(x)=0 \right\}
$$
Is non-[[Empty Set|empty]] and [[Boundedness|bounded]] below. Thus $x_{0}=\text{inf}(X)$ exists. Now take a sequence $x_{n}\in X$ with $\cos(x_{n})=0$
# [[Complex Functions|Complex]] Trigonometric Functions
Motivated by the identities
$$
\cos (x)=\frac{e^{ ix }+e^{ -ix }}{2},~\sin (x)=\frac{e^{ ix }-e^{ -ix }}{2i}
$$
From our definition and 
$$
\cosh( x)= \frac{e^{ x }+e^{ -x }}{2},~\sinh (x)= \frac{e^{ x }-e^{ -x }}{2}
$$
we define:
## Definition
$$
\cos (z):=\frac{e^{ iz }+e^{ -iz }}{2}  ,~\sin(z):=\frac{e^{ iz }-e^{ -iz }}{2i}
$$
$$
 \cosh( z) := \frac{e^{ z }+e^{ -z }}{2},~\sinh (z):= \frac{e^{ z }+e^{ -z }}{2}
$$
## Lemma
We have that for $z=x+iy$:
$$
\cos (z) = \cos (x)\cosh( y)-i\sin (x)\sinh(y)
$$
$$
 \sin(z)=\sin(x)\cosh(y)+i\cos(x)\sinh(y)
$$
$$
 \cosh(z)=\cos(iz)=\cosh(x)\cos(y)+i\sinh(x)\sin(y)
$$
$$
 \sinh(z)=-i\sin(iz)=\sinh(x)\cos(y)+i\cosh(x)\sin(y)
$$
In addition, we have that for all $z\in\mathbb{C}$,
$$
\sin ^{2}(z)+\cos ^{2}(z)=1,~\cosh ^{2}(z)-\sinh ^{2}(z)=1
$$
### Proof
A full proff is rather tedious, we just need to look to the definition of the functions, for example
$$
\sin(z)=\sin(x+iy)=\frac{e^{ i(x+iy) }-e^{ -i(x+iy) }}{2i}
$$
$$
= \frac{e^{ -y }e^{ ix }-e^{ y }e^{ -ix }}{2i}
$$
$$
= \frac{e^{ -y }(\cos (x)+i\sin(x))-e^{ y }(\cos(x)-i\sin(x))}{2i}
$$
$$
=   \frac{e^{ -y }-e^{ y }}{2i}\cos(x)+ \frac{e^{ -y }+e^{ y }}{2}\sin(x)
$$
$$
= \sin(x)\cosh(y)+i\cos(x)\sinh(y)
$$
## Mapping
Visualising these maps is quite complicated, but here is a summary
- The map $\sin(z)$ [[Injective Functions|injectively]] takes a segment of length $2\pi$ on the line $y=c$ which is open at one end and closed at the other when $c\neq 0$. When $=0$, we get the "squished ellipse" $[-1,1]\times \left\{ 0 \right\}$ and the map is injective for a segment of length $\pi$ on which the real map $\sin(x)$ is injective
- The map $\sin(z)$ injectively takes the line $x=c$ to a one-sided hyperbola when $c\neq k\pi$ and $c\neq \frac{\pi}{2}+k\pi$ for all $k\in \mathbb{Z}$. When $k\pi$, or $c=\frac{\pi}{2}+k\pi$ for some $k\in\mathbb{Z}$, we get the "squashed" hyperbolas:
    - $\left\{ 0 \right\}\times i\mathbb{R}$ if $c=\pi k$, the map is injective in this case
    - $[1,\infty)\times \left\{ 0 \right\}$ if $c=\frac{\pi}{2}+2\pi k$. The map is injective on $\left\{ z\in\mathbb{C}\mid z=\frac{\pi}{2}+2\pi k+iy,y\geq 0 \right\}$ and $\left\{ z\in\mathbb{C}\mid z=\frac{\pi}{2}+2\pi k+iy,y\leq 0 \right\}$
    - $(-\infty,1]\times \left\{ 0 \right\}$ if $c=-\frac{\pi}{2}+2\pi k$. The map is injective on $\left\{ z\in\mathbb{C}\mid z=-\frac{\pi}{2}+2\pi iy,y\geq 0 \right\}$ and $\left\{ z\in\mathbb{C}\mid z=-\frac{\pi}{2}+2\pi k+iy,y\leq 0 \right\}$
Similar statements can be made for $\cos(z)=\sin\left( z+\frac{\pi}{2} \right)$ (a shift by $\frac{\pi}{2}$ on the $x$ axis) and $\sinh(z)$ and $\cosh(z)$ using the identities
$$
\sinh(z)=-i\sin(iz),~\cosh(z)=\cos(iz)
$$
(rotations by $\pm \frac{\pi}{2}$ of the variable and image in the complex plane)