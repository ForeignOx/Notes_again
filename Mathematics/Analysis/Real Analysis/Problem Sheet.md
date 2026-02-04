

## Epiphany
![[Pasted image 20250207124207.png]]
Consider $f'(x)$ for $x\neq 0$,
$$
f'(x)=2x^{-3}e^{ -1/x^{2} }
$$
At $\hspace{0pt}0$,
$$
f'(0)=\lim_{ x \to 0 }  \frac{f(x)-f(0)}{x-0}=\lim_{ x \to 0 } \frac{e^{ -1/x^{2} }}{x}
$$
$$
= \lim_{ x \to \pm \infty }  \frac{e^{ -x^{2} }}{\frac{1}{x^{2}}}=\lim_{ x \to \pm \infty } x^{2}e^{ -x^{2} }=0
$$
Which is true since exponentials beat polynomials
For $n=0$, then $p_{n}(x)=1$, for $n=1$, it also works, with $p_{n}(x)=2x^{3}$ which corresponds with $f'(x)$ above...
Assume true for $n$, then we want to differentiate our expression:
$$
\frac{d }{dx} \left( p_{n}\left( \frac{1}{x} \right)e^{ -1/x^{2} } \right)=\underbrace{ \left( -\frac{1}{x^{2}}p'_{n}\left( \frac{1}{x} \right)+p_{n}\left( \frac{1}{x} \right)2x^{-3} \right) }_{ \text{polynomial in }  \frac{1}{x} }e^{ -1/x^{2} }
$$
Hence the first part is proved, we now want $f^{(n)}=0$, for $n=0,1$, it works, now by induction:
$$
f^{(n+1)}(0)=\lim_{ x \to 0 }  \frac{p_{n}\left( \frac{1}{x} \right)e^{ -1/x^{2} }-0}{x-0}=\lim_{ x \to \pm \infty } xp_{n}(x)e^{ -x^{2} }=0
$$
Since exponentials beat polynomials

![[Pasted image 20250207125151.png]]
We kow $\log x$ is differentiable since it is the inverse of $e^{ x }$ with derivative
$$
\log'(x)=\frac{1}{e^{ \log(x) }}=\frac{1}{x}
$$
Now by hand,
$$
\lim_{ h \to 0 } \frac{\log(x+h)-\log(x)}{h}=\lim_{ h \to 0 } \frac{\log\left( \frac{x+h}{h} \right)}{h}=\lim_{ h \to 0 }  \frac{\log\left( 1+\frac{h}{x} \right)}{h}
$$
If $h>0$, (same for $h<0$), we have
$$
 \frac{\frac{h}{x}}{1+\frac{h}{x}}\leq\frac{\log\left( 1+\frac{h}{x} \right)}{h}\leq \frac{\frac{h}{x}}{h}=\frac{1}{x}
$$
Both tend to $\frac{1}{x}$, so by squeeze theorem, we have proved it
___
We want to show using $\log'(x)=\frac{1}{x}$ that 
$$
\frac{x}{x+1}\leq \log(1+x)\leq x
$$
Using the growth theorem, take the deriavatives:
$$
\frac{1}{1+x^{2}}\leq \frac{1}{1+x}\leq 1
$$
