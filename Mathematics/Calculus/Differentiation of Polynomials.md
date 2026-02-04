Consider the derivative of $f(x)=x^{n}$, from [[Differentiation|first principles]]:
$$
f'(x)=\lim_{ h \to 0 } \frac{(x+h)^{n}-x^{n}}{h}
$$
For $n \in \mathbb{N}$:
$$
f'(x)=\lim_{ h \to 0 } \frac{-x^{n}+x^{n}+ ^nC_{1}hx^{n-1}+^{n}C_{2}h^{2}x^{n-1}+\dots}{h}
$$
$$
= \lim_{ h \to 0 } \frac{nhx^{n-1}+^{n}C_{2}h^{2}x^{n-2}+\dots}{h}
$$
$$
=\lim_{ h \to 0 } nx^{n-1}+^{n}C_{2}hx^{n-2}+\dots
$$
$$
=nx^{n-1}
$$
Hence $f'(x)=nx^{n-1}$, from this we can extend to a general polynomial:
$$
f(x)=a_{0}+a_{1}x+a_{2}x^{2}+\dots+a_{n}x^{n}
$$
$$
f'(x) = a_{1}+2a_{2}x+\dots+na_{n}x^{n-1}
$$
#Mathematics #Calculus