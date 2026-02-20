While having the [[Cauchy-Goursat theorem|Cauchy-Goursat theorem]] is nice, a natural question to ask is how might one deal with a [[domains|domain]] that is not [[Starlike Domains|starlike]]. We have seen the important example by explicitly calculating the [[integration|integral]] that for $r>0$, we have
$$
\int _{\left| z-a \right| =r} \frac{1}{z-a} \, dz=2\pi i 
$$
In order to generalise this, we observe the compatibility of [[Contour Integration|contour integrals]] and [[Uniform Convergence|uniformly converging sequences]]. Recall that if $g,f_{n}:U\to \mathbb{C}$ are continuous and $f_{n}\to f$ [[Pointwise Convergence|pointwise]] on $U$, then for each $z\in U$, we have
$$
\lim_{ n \to \infty } f_{n}(z)g(z)=f(z)g(z)
$$
If the convergence is uniform, we can go further
## Lemma: Exchange of Integral and Uniform Limit
Let $f_{n}:U\to \mathbb{C}$ be a sequence of continuous functions on an open set and let $\gamma$ be a contour in $U$, if
$$
f_{n}\to f
$$
Uniformly on $\gamma$, then
$$
\lim_{ n \to \infty } \int _{\gamma}f_{n}(z) \, dz=\int_{\gamma} \lim_{ n \to \infty } f_{n}(z) \, dz=\int _{\gamma}f(z) \, dz 
$$
In particular, if $g:U\to \mathbb{C}$ is continuous, then
$$
\lim_{ n \to \infty } \int _{\gamma}f_{n}(z)g(z) \, dz=\int _{\gamma}f(z)g(z) \, dz  
$$
### Proof
Fix $\varepsilon>0$ and let $L(\gamma)$ be the length of $\gamma$
Since $f_{n}\to f$ uniformly on $\gamma$, there exists $N>0$ such that for all $z\in \gamma$, we have 
$$
\left| f_{n}(z)-f(z) \right| < \frac{\varepsilon}{2L(\gamma)}
$$
Whenever $n>N$
Recall that the limit definition $f$ is also continuous, and so the integral of $f$ along $\gamma$ is defined. In particular, by the [[ML inequality|ML inequality]] we have that for $n>N$:
$$
\left| \int _{\gamma}f_{n}(z) \, dz -\int _{\gamma}f(z) \, dz   \right|=\left| \int _{\gamma}f_{n}(z)-f(z) \, dz  \right|
$$
$$
  \leq L(\gamma)\sup_{z\in  \gamma} \left| f_{n}(z)-f(z) \right| \leq L(\gamma) \frac{\varepsilon}{2L(\gamma)}<\varepsilon 
$$
For the final statement, note that the image of $\gamma$ is a compact set, so $g$ must attain a maximum absolute value on $\gamma$, by the [[Extreme Value Theorem|extreme value theorem]]. Thus, there exists $K>0$ such that $\sup_{z\in \gamma}\left| g(z) \right|\leq K$
We then follow the argument the same way as above
## Example
A clasic example of power series is $\sum_{n=0}^{\infty}z^{n}$ which converges locally uniformly on $\left| z \right|<1$, and in fact
$$
\lim_{ N \to \infty } f_{N}(z)=\lim_{ N \to \infty } \sum_{n=0}^{N}z^{n}=\lim_{ N \to \infty }  \frac{1-z^{N+1}}{1-z}=\frac{1}{1-z}
$$
In particular, for any contour $\gamma$ in the unit disc,
$$
\int _{\gamma}\sum_{n=0}^{\infty}z^{n} \, dz=\sum_{n=0}^{\infty}\int _{\gamma}z^{n} \, dz 
$$
## Proposition: Integral of Cauchy Kernel
Let $a\in\mathbb{C}$ and $r>0$. If $w\in B_{r}(a)\subset \mathbb{C}$, then
$$
\int _{\left| z-a \right| =r} \frac{1}{z-w} \, dz=2\pi i 
$$
The function $\frac{1}{z-w}$ is often known as the Cauchy kernel
### Proof
For $w\in B_{r}(a)$ and pick $z$ on $\left| z-a \right|=r$, then
$$
\frac{1}{z-w}=\frac{1}{z-a+a-w}=\frac{1}{z-a} \frac{1}{1- \frac{w-a}{z-a}}=\frac{1}{z-a} \sum_{n=0}^{\infty} \left( \frac{w-a}{z-a} \right)^{n}
$$
Which we can justify as $\left| z-a \right|=r$ and so since $w\in B_{r}(a)$, $\left| w-a \right|<r$
Note that $M(z)= \frac{w-a}{z-a}$ is a Mobius transform, $[a,w,\infty]\to[\infty,1,0]$
![[Pasted image 20260220162122.png]]
If we use the contour $\gamma(t)=a+re^{ i\theta }$ with $\theta \in[0,2\pi]$, let
$$
\delta=M(\gamma)=\frac{w-a}{r}e^{ -it }
$$
Where $\frac{\left| w-a \right|}{r}<1$, note $\delta'(t)=-i\delta(t)$,
$$
    \int _{\gamma} \frac{1}{z-w} \, dz=\int _{\gamma}  \frac{1}{z-a}\sum_{n=0}^{\infty} \left( \frac{w-a}{z-a} \right)^{n} \, dz 
$$
$$
    = \int_{0}^{2\pi} \frac{\gamma'(t)}{\gamma(t)-a}\sum_{n=0}^{\infty} \left( \frac{w-a}{\gamma(t)-a} \right)^{n} \, dt =\int_{0}^{2\pi}  \frac{ire^{ it }}{re^{ it }}\sum_{n=0}^{\infty} \left( \frac{w-a}{re^{ it }} \right)^{n} \, dt 
$$
$$
    = \int_{0}^{2\pi} -\frac{\delta'(t)}{\delta(t)} \sum_{n=0}^{\infty} (\delta(t))^{n} \, dt = \int _{\delta} -\frac{1}{z}\sum_{n=0}^{\infty}z^{n} \, dz = \sum_{n=0}^{\infty} \int _{\delta} -\frac{1}{z} z^{n} \, dz=2\pi i  
$$
## Remark
Knowing the integral of the Cauchy kernel allows us to prove the following remarkable fact: the values of a holomorphic function in an open ball are determined by the values of the function on its boundary, in other words, we can reconstruct the whole function in a two dimensional disc by just knowing the function on the one dimensional circle that bounds the disc
## Theorem: Cauchy's Integral Formula
If $f$ is holomorphic on some ball $B_{r}(a)$ and $\gamma$ is the contour $\left| z-a \right|=\rho$, then for every $w\in B_{\rho}(a)$, we have
$$
f(w)=\frac{1}{2\pi i} \int _{\gamma} \frac{f(z)}{z-w} \, dz 
$$
### Proof
Assume $w\in B_{\rho}(a)$, so that $w$ lies inside the circle $\left| z-a \right|=\rho$. We know that the [[difference quotient function|difference quotient function]] is holomorphic on $B_{r}(a)\setminus \left\{ w \right\}$, so by the more generalised form of [[Cauchy-Goursat Theorem|Cauchy-Goursat]], we have that
$$
\int _{\gamma} g(z) \, dz=0 
$$
Since the point $w$ does not lie on the circle $\left| z-a \right|=\rho$, this means
$$
    \int _{\gamma} \frac{f(z)-f(w)}{z-w} \, dz=0 
$$
$$
 \iff \int _{\gamma} \frac{f(z)}{z-w} \, dz= \int _{\gamma} \frac{f(w)}{z-w} \, dz=f(w)\int _{\gamma} \frac{1}{z-w} \, dz=f(w)2\pi i
$$
## Example
$\sin z$ is holomorphic on $\mathbb{C}$ as it is starlike soo
$$
\int _{\left| z \right| =1}\sin z \, dz=0
$$
And
$$
    \int \frac{\sin z}{z} \, dz=2\pi i \sin(0)=0
$$
$$
\int _{\left| z \right|  } \frac{\sin z}{z-\frac{\pi}{2}} \, dz=  2\pi i \sin\left( \frac{\pi}{2} \right) =2\pi i
$$
