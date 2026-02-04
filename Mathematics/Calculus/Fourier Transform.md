The Fourier Transform is a tool that does “[[Frequency|frequency]] analysis” similar to [[Fourier Series|fourier series]], but for non-[[Periodic Functions|periodic]] [[Functions|functions]]
If we consider a fourier series of a function of periodicity $2\pi M$, for $M\in\mathbb{N}$
![[Fourier Transform 2025-03-11 14.18.25.excalidraw]]
Then this has a fourier series:
$$
f(x)=\frac{a_{0}}{2}+{\sum_{n=1}^{\infty}}a_{n}\cos\left( \frac{nx}{M} \right)+\sum_{n=1}^{\infty}b_{n}\sin\left( \frac{nx}{M} \right)=\sum_{n=-\infty}^{\infty}d_{n}e^{ inx/M }
$$
Which needs angular frequencies $\frac{1}{M},\frac{2}{M},\frac{3}{M},\dots$
As $M\to \infty$, the function becomes non-periodic, but we need all angular frequencies to describe it, so the equation becomes:
$$
f(x)=\frac{1}{2\pi}\int_{-\infty}^{\infty} \tilde{f}(p)  e^{ ipx } \, dp 
$$
Which is the Fourier transform
___
Let $f(x)$ be a (non)-periodic function on $\mathbb{R}$:
![[Fourier Transform 2025-03-11 14.31.17.excalidraw]]
For each integer $M>0$, construct a function $f_{M}(x)$ or periodicity $2\pi M$ as follows, $f_{M}(x)=f(x)$ for $-\pi M\leq x\leq \pi M$, $f_{M}(x+2\pi M)=f_{M}(x)$, so we can construct the fourer series as follows:
$$
f_{M}(x)=\sum_{n=-\infty}^{\infty}d_{n}e^{ inx/M }
$$
Where
$$
d_{n}=\frac{1}{2\pi M}\int_{-\pi M}^{\pi M} f_{M}(x)e^{ -inx/M } \, dx =\frac{1}{2\pi M}\int_{-\pi M}^{\pi M} f(x)e^{ -inx/M } \, dx 
$$
But $d_{n}$ is not a good thing to use, since the label $n$ is no longer the same as the angular frequency $\frac{n}{M}$, and $d_{n}\to0$ as $M\to \infty$ as it is roughly proportional to $\frac{1}{M}$
Instead we will define
$$
\tilde{f}\left( \frac{n}{M} \right)=d_{n}2\pi M=\int_{-\pi M}^{\pi M} f(x)e^{ -inx/M } \, dx 
$$
So the Fourier series becomes:
$$
f_{M}(x)=\sum_{n=-\infty}^{\infty}d_{n}e^{ inx/M }=\sum_{n=-\infty}^{\infty} \frac{1}{2\pi M}\tilde{f}\left( \frac{n}{M} \right)e^{ inx/M }=\frac{1}{2\pi}\sum_{n=-\infty}^{\infty}\Delta p\tilde{f}(p)e^{ ipx }
$$
Where $p=\frac{n}{M},\Delta p=\frac{1}{M}$, and $\Delta p$ is the difference between neighbouring values of angular frequency in series
We can represent this graphically:
![[Fourier Transform 2025-03-11 14.43.11.excalidraw]]
In the limit as $M\to \infty,\Delta p\to  0$ and the [[Riemann Sums|riemann sum]] of the rectangles tends to an [[Integration|integral]], so
$$
f_{M}(x)\to f(x)=\frac{1}{2\pi}\int_{-\infty}^{\infty} \tilde{f}(p)e^{ ipx } \, dx 
$$
Where
$$
\tilde{f}(p)=\int_{-\infty}^{\infty} f(x)e^{ -ipx } \, dx
$$
Note that $\tilde{f}(p)$ is the fourier transform of $f(x)$
## Example
Find the Fourier transform of
$$
F(x)=\begin{cases}
1 & \left| x \right| <1\\0 & \text{otherwise}
\end{cases}
$$
![[Fourier Transform 2025-03-11 14.49.37.excalidraw]]
$$
\tilde{F}(p)=\int_{-\infty}^{\infty} F(x)e^{ -ipx } \, dx =\int_{-1}^{1} e^{ -ipx } \, dx=\left[ \frac{e^{ -ipx }}{-ip} \right]_{-1}^{1}=\frac{2(e^{ ip }-e^{ -ip })}{2ip}=\frac{2\sin(p)}{p} 
$$
Which looks like:
![[Fourier Transform 2025-03-11 14.52.10.excalidraw]]
## Properties
### Taking Fourier Transform is a [[Linear|Linear]] Operation
If $f_{1}(x),f_{2}(x)$ have fourier transforms $\tilde{f}_{1}(p),\tilde{f}_{2}(p)$ respectively, then $F(x)=\alpha f_{1}(x)+\beta f_{2}(x)$ has fourier transform 
$$
\tilde{F}(p)=\alpha \tilde{f}_{1}(p)+\beta \tilde{f}_{2}(p)
$$
#### Proof
$$
\tilde{F}(p)=\int_{-\infty}^{\infty} F(x)e^{ -ipx } \, dx=\int_{-\infty}^{\infty} (\alpha f_{1}(x)+\beta f_{2}(x))e^{ -ipx } \, dx 
$$
$$
 =\alpha \int_{-\infty}^{\infty} f_{1}(x)e^{ -ipx } \, dx +\beta \int_{-\infty}^{\infty} f_{2}(x)e^{ -ipx } \, dx =\alpha \tilde{f}_{1}(p)+\beta \tilde{f}_{2}(p)
$$
### Shift Theorem
Let $f(x)$ have fourier trnasform $\tilde{f}(p)$, and $g(x)=f(x+a)$, then 
$$
\tilde{g}(p)=e^{ ipa }\tilde{f}(p)
$$
You can think of this as if you move in $x$ space, then you multiply by a shift factor in $p$ space
#### Proof
$$
    \tilde{g}(p)=\int_{-\infty}^{\infty} g(x)e^{ -ipx } \, dx =\int_{-\infty}^{\infty} f(x+a)e^{ -ipx } \, dx 
$$
Let $u=x+a,du=dx$, bounds are equal,
$$
    =\int_{-\infty}^{\infty} f(u)e^{ -ip(u-a) } \, du =e^{ ipa }\int_{-\infty}^{\infty} f(u)e^{ -ipu } \, du =e^{ ipa }\tilde{f}(p)
$$
#### Example
What is the Fourier transform of
$$
g(x)=\begin{cases}
1 & 0\leq x\leq 2\\0 & \text{otherwise}
\end{cases}
$$
Note that we know the fourier transform above of 
$$
f(x)=\begin{cases}
1 & -1\leq x\leq 1\\0 & \text{otherwise}
\end{cases}

$$
So since $g(x)=f(x-1)$, by shift theorem, 
$$
\tilde{g}(p)=\tilde{f}(p)e^{ -ip }=\frac{2\sin(p)e^{ -ip }}{p}
$$
### Scaling Theorem
Let $f(x)$ have fourier transform $\tilde{f}(p)$, then if $g(x)=f(bx)$ with $b\neq 0$, then
 $$
\tilde{g}(p)=\frac{1}{\left| b \right| }\tilde{f}\left( \frac{p}{b} \right)
$$
We can think of this as stretching all the waves' wavelengths by $b$, hence their frequency scales with $\frac{1}{b}$ as well as shifting the height of the graph
#### Proof
$$
\tilde{g}(p)=\int_{-\infty}^{\infty} g(x)e^{ -ipx } \, dx =\int_{-\infty}^{\infty} f(bx)e^{ -ipx } \, dx 
$$
Let $u=bx,du=bdx$, if $b<0$, bounds swap
$$
=\int_{-\infty \times \text{sign} (b)}^{\infty \times\text{sign} (b)} \frac{f(u)}{b}e^{ -ipu/b } \, du=\frac{1}{b\times \text{sign} (b)}\int_{-\infty}^{\infty} f(u)e^{ -i\frac{p}{b} u} \, du=\frac{1}{\left| b \right| }\tilde{f}\left( \frac{p}{b} \right)
$$
### [[Odd Functions|Odd]]/[[Even Functions|Even]] Functions
The fourier transform of an even/odd function $f(x)$ is $\tilde{f}(p)$ which is even/odd
#### Proof
Consider $g(x)=f(-x)=f(bx)$, using the scaing theorem with $b=-1$
$$
\tilde{g}(p)=\frac{1}{\left| -1 \right| }\tilde{f}\left( \frac{p}{-1} \right)=\tilde{f}(-p)
$$
Let $f(x)$ be even, then
$$
f(x)=f(-x)=g(x)\implies \tilde{f}(p)=\tilde{g}(p)=\tilde{f}(-p)
$$
So $\tilde{f}$ is even
Let $f(x)$ be odd, then
$$
f(x)=-f(-x)=-g(x)\implies \tilde{f}(p)=-\tilde{g}(p)=-\tilde{f}(-p)
$$
So $\tilde{f}$ is odd
## [[Differentiation|Derivative]] Theorem
Let $f(x)$ have fourier transform $\tilde{f}(p)$, then if $g(x)=\frac{d f}{dx}(x)$, then
$$
\tilde{g}(p)=ip\tilde{f}(p)
$$
This is useful, since it is saying that differetiating in $x$-space is the same as multiplying by $ip$ in $p$-space
#### Proof
$$
\tilde{g}(p)=\int_{-\infty}^{\infty} g(x)e^{ -ipx } \, dx =\int_{-\infty}^{\infty} \frac{d f}{dx} e^{ -ipx } \, dx 
$$
Integrating by [[Integration by Parts|parts]] gives:
$$
=[fe^{ -ipx }]_{-\infty}^{\infty}-\int_{-\infty}^{\infty} f(x)(-ip)e^{ -ipx } \, dx 
$$
We assume $\lim_{ \left| x \right| \to \infty }f(x)=0$ which is necessary for these improper integrals to converge, so the first term vanishes
$$
=ip \int_{-\infty}^{\infty} f(x)e^{ -ipx } \, dx =ip \tilde{f}(p)
$$
### [[Convolution of Functions|Convolution]] Thorem
Let $f(x)$ have fourier transform $\tilde{f}(p)$ and $g(x)$ have fourier transform $\tilde{g}(p)$, then if $F(x)=(f*g)(x)$, then
$$
\tilde{F}(p)=\tilde{f}(p)\tilde{g}(p)
$$
#### Proof
$$
\tilde{F}(p)=\int_{-\infty}^{\infty} F(x)e^{ -ipx } \, dx =\int_{-\infty}^{\infty} (f*g) e^{ -ipx } \, dx 
$$
$$
= \int_{-\infty}^{\infty} \left( \int_{-\infty}^{\infty} f(t)g(x-t) \, dt \right) e^{  -ipx} \, dx 
$$
$$
= \int_{-\infty}^{\infty} f(t)\left( \int_{-\infty}^{\infty} g(x-t)e^{ -ipx } \, dx  \right) \, dt 
$$
The inner integral is the fourier transform of $g(x-t)$ by shift theorem it is equal to $\tilde{g}(p)e^{ -ipt }$
$$
=\int_{-\infty}^{\infty} f(t)\tilde{g}(p)e^{ -ipt } \, dt=\tilde{g}(p)\int_{-\infty}^{\infty} f(t)e^{ -ipt } \, dt =\tilde{f}(p)\tilde{g}(p)
$$

## Example
$$
f(x)=\begin{cases}
e^{ -ax } & x\geq 0\\0 & x<0
\end{cases}
$$
$$
\tilde{f}(p)=\int_{-\infty}^{\infty} f(x)e^{ ipx } \, dx =\int_{0}^{\infty} e^{ -ax }e^{ -ipx } \, dx =\int_{0}^{\infty} e^{ -(ip+a)x } \, dx =\left[ -\frac{1}{ip+a}e^{ -(ip+a)x } \right]^{\infty}_{0}=\frac{1}{ip+a}
$$
___
$$
g(x)=e^{ -a\left| x \right|  }
$$
$$
\implies \tilde{g}(p)=\int_{-\infty}^{\infty} g(x)e^{ -ipx } \, dx =\int_{-\infty}^{0} e^{ ax }e^{ -ipx } \, dx +\int_{0}^{\infty} e^{ -ax }e^{ -ipx } \, dx 
$$
$$
= \int_{-\infty}^{0} e^{ (a-ip)x } \, dx +\int_{0}^{\infty} e^{ -(ip+a)x } \, dx=\left[ \frac{1}{a-ip}e^{ (a-ip)x } \right]_{-\infty}^{0}-\left[ \frac{1}{ip+a}e^{ -(ip+a)x } \right]_{0}^{\infty}
$$
$$
= \frac{1}{a-ip}+\frac{1}{ip+a}=\frac{2a}{a^{2}+p^{2}} 
$$
___
$$
f(x)=e^{ -x^{2} }
$$
$$
 \tilde{f}(p)=\int_{-\infty}^{\infty} f(x)e^{ -ipx } \, dx=\int_{-\infty}^{\infty} e^{ -x^{2} }e^{ -ipx } \, dx =\int_{-\infty}^{\infty} e^{ -(x+ip/2)^{2} }e^{ (ip/2)^{2} } \, dx  
$$
$$
= e^{ -p^{2}/4 }\int_{-\infty}^{\infty} e^{ -(x+ip/2)^{2} } \, dx =e^{ -p^{2}/4 }\int_{-\infty}^{\infty} e^{ -x'^{2} } \, dx' =\sqrt{ \pi }e^{ -p^{2}/4 }
$$
Where we made the substitution $x'=x+\frac{ip}{2}$
We can then do other quadratics
$$
F(x)=e^{ -bx^{2}-cx }=e^{ -(\sqrt{ b }x+c/2\sqrt{ b })^{2} }e^{ c^{2}/4b }=e^{ c^{2}/4b }f\left( \sqrt{ bx }+\frac{c}{2\sqrt{ b }} \right)
$$
So let $h(x)=f\left( \sqrt{ b }x+\frac{c}{2\sqrt{ b }} \right)$, $g(x)=h\left( \frac{x}{\sqrt{ b }} \right)=f\left( x+\frac{c}{2\sqrt{ b }} \right)$, so by the shift theorem:
$$
\tilde{g}(p)=\tilde{f}(p)e^{ ipc/2\sqrt{ b } }=\sqrt{ \pi }e^{ -p^{2}/4 }e^{ ipc/2\sqrt{ b } }
$$
Then $h(x)=g(\sqrt{ b }x)$, so by scaling theorem:
$$
\tilde{h}(p)=\frac{1}{\sqrt{ b }}\tilde{g}\left( \frac{p}{\sqrt{ b }} \right)=\sqrt{ \frac{\pi}{b} }e^{ -\frac{p^{2}}{4b} }e^{ \frac{ic}{2\sqrt{ b }}p }
$$
Finally $F(x)=e^{ \frac{c^{2}}{4b} }h(x)$, so
$$
\tilde{F}(p)=\sqrt{ \frac{\pi}{b} }e^{ \frac{c^{2}}{4b} }e^{ -\frac{p^{2}}{4b} }e^{ \frac{icp}{2b} }=\sqrt{ \frac{\pi}{b} }e^{ -\frac{1}{4b}(p-ic)^{2} }
$$

