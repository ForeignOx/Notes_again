If [[Functions|$f(x)$]] is a [[Periodic Functions|periodic function]] with period $2L$ with [[Fourier Series#Fourier Coefficients|Fourier coefficients]] $a_{n},b_{n}$, then
$$
\frac{1}{2L}\int _{-L}^{L}(f(x))^{2} \, dx =\frac{1}{4}a_{0}^{2}+\frac{1}{2}\sum_{ n=1} ^{\infty}  (a_{n}^{2}+b_{n}^{2})
$$
## Proof
$$
\frac{1}{L}\int _{-L}^{L}(f(x))^{2} \, dx =\frac{1}{L}\int _{-L}^{L}\left( \frac{a_{0}}{2}+\sum_{ n=1} ^{\infty} \left(  a_{n}\cos\left( \frac{n\pi x}{L} \right)  +b_{n}\sin\left( \frac{n\pi x}{L} \right)\right)\right)^{2} \, dx 
$$
We can take out the first term squared, then we have all the terms that are the first term multiplied by either a $\cos$ or a $\sin$, then also the terms which are $\cos$ terms multiplied by $\sin$ terms, which are all equal to $\hspace{0pt}0$ from our [[Fourier Series#Identities )|identities]], so are left with the $\cos$ terms multiplied by $\cos$ terms and the $\sin$ terms multiplied by $\sin$ terms which we have as an identity using the [[Kronecker Delta Function|Kronecker delta function]]:
$$
= \frac{a_{0}^{2}}{2}+\sum_{ n=1} ^{\infty}  \sum_{ m=1} ^{\infty} ( a_{n}a_{m}\delta_{mn}+b_{n}b_{m}\delta_{mn})
$$
Which we can then simplify due to knowing how the Kronecker delta function works:
$$
=\frac{a_{0}^{2}}{2}+\sum_{ n=1} ^{\infty}  (a_{n}^{2}+b_{n}^{2})
$$
## Usefulness??
Parseval's theorem can allow us to find the value of certain infinite sums
### Example
Calculate $\sum_{ n=1} ^{\infty} \frac{1}{n^{2}}=\zeta(2)$ by applying Parleval's theorem to $f(x)=x$ for $x\in(-\pi,\pi)$
From [[Fourier Series#Examples|these examples]], one shows that $f(x)$ has Fourier coefficients $a_{n}=0$ and $b_{n}=\frac{2(-1)^{n+1}}{n}$
We have
$$
\frac{1}{2\pi}\int _{-\pi}^{\pi}x^{2} \, dx =\frac{1}{2\pi}\left[ \frac{x^{3}}{3} \right]_{-\pi}^{\pi}=\frac{\pi^{2}}{3}
$$
And hence by Parseval's theorem
$$
\frac{1}{2\pi}\int x^{2} \, dx =\frac{\pi^{2}}{3}=\frac{1}{2}\sum_{ n=1} ^{\infty}  \frac{4}{n^{2}}
$$
$$
\implies \sum_{ n=1} ^{\infty}  \frac{1}{n^{2}}=\frac{\pi^{2}}{6}
$$

#Mathematics #Calculus #Theorem 