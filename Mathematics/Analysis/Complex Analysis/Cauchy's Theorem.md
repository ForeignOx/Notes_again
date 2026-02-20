 To prove a vesion of Cauchy's theorem, Goursat observed:


## Theorem: Cauchy-Goursat's Theorem (for Starlike Domains)

## Lemma: Exchange of Integral and Uniform Limit
Let $f_{n}:U\to \mathbb{C}$ be a sequence fo continuous functions on an open set and let $\gamma$ be a contour in $U$, if
$$
f_{n}\to f
$$
Uniformly on $\gamma$, then
$$
\lim_{ n \to \infty } \int _{\gamma}f_{n}(z) \, dz=\int_{\gamma} \lim_{ n \to \infty } f_{n}(z) \, dz=\int _{\gamma}f(z) \, dz 
$$
### Proof
By the [[ML Inequality|ML inequality]],
$$
\left| \int _{\gamma}f_{n}(z) \, dz-\int _{\gamma}f(z) \, dz   \right| =\left| \int _{\gamma}f_{n}(z)-f(z) \, dz  \right| \leq L(\gamma)\sup_{z\in  \gamma}\left| f_{n}(z)-f(z) \right| 
$$
Which must tend to zero since $f_{n}\to f$ uniformly
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
Let $w\in B_{r}(a)\subset \mathbb{C}$, then
$$
\int _{\left| z-a \right| =r} \frac{1}{z-w} \, dz=2\pi i 
$$
### Proof
For $w\in B_{r}(a)$ and pick $z$ on $\left| z-a \right|=r$, then
$$
\frac{1}{z-w}=\frac{1}{z-a+a-w}=\frac{1}{z-a} \frac{1}{1- \frac{w-a}{z-a}}=\frac{1}{z-a} \sum_{n=0}^{\infty} \left( \frac{w-a}{z-a} \right)^{n}
$$
Which we can justify as $\left| z-a \right|=r$ and so since $w\in B_{r}(a)$, $\left| w-a \right|<r$
Note that $M(z)= \frac{w-a}{z-a}$ is a Mobius transform, $[a,w,\infty]\to[\infty,1,0]$
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
## Theorem: Cauchy's Integral Formula
If $f$ is holomorphic on some ball $B_{r}(a)$ and $\gamma$ is the contour $\left| z-a \right|=\rho$, then for every $w\in B_{\rho}(a)$, we have
$$
f(w)=\frac{1}{2\pi i} \int _{\gamma} \frac{f(z)}{z-w} \, dz 
$$
### Proof
By secret remark, we have
$$
\int _{\gamma} g(z) \, dz=0 
$$
Where $g(z)$ is the difference quotient function, so
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
C
