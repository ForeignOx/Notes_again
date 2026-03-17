## Lemma
For $N\geq 0$, let $S_{N}$ be the square in $\mathbb{C}$ with vertices $(1+i)\left( N+\frac{1}{2} \right),(-1+i)\left( N+\frac{1}{2} \right),(-1-i)\left( N+\frac{1}{2} \right),(1-i)\left( N+\frac{1}{2} \right)$, then there exist real constants $C,D>0$ (independent of $N$) such that
$$
\left| \cot(\pi z) \right| := \left|  \frac{\cos(\pi z)}{\sin(\pi z)} \right| \leq C,  \left| \csc(\pi z) \right| := \frac{1}{\left| \sin(\pi z) \right| }\leq D
$$
For all $z\in S_N$, and 
## Basel Problem
Show that
$$
\sum_{n=1}^{\infty} \frac{1}{n^{2}}=\frac{\pi^{2}}{6}
$$
### Solution
Surprisingly, consider $f(z)= \frac{\cot(\pi z)}{z^{2}}$ and integrate it around the square contours $S_{N}$. The poles of $f(z)= \frac{\cos(\pi z)}{z^{2}\sin(\pi z)}= \frac{g(z)}{h(z)}$ are at zeros of $h$, so at $z=0$ or $z=n$
These are order $\hspace{0pt}1$ for $n\neq 0$ and order $\hspace{0pt}3$ for $n=0$
So by Cauchy's residue theorem,
$$
\oint_{S_{N}}f(z)~dz=2\pi i \sum_{n=-N}^{N} \mathrm{Res}_{z=n}(f)
$$
We claim that as $N\to \infty$, the integral tends to zero
By the ML inequality,
$$
\left| \oint_{S_{N}}f~dz \right| \leq L(S_{N})\sup_{z\in  S_{N}}\left| f(z) \right| 
$$
And $L(S_{N})=4\cdot (2N+1)=8N+4$
$$
\leq (8N+4)\sup \frac{\left| \cot(\pi z) \right| }{\left| z \right| ^{2}} \leq (8N+4) C \frac{1}{\left( N+\frac{1}{2} \right)^{2}}= \frac{C(8N+4)}{N^{2}+N+\frac{1}{4}}
$$
By the squares lemma which does tend to zero as $N\to \infty$
$$
0=\lim_{ N \to \infty }  2\pi i\sum_{n=-N}^{N} \mathrm{Res}_{z=n}(f)
$$
So by ruloe $\hspace{0pt}2$, for $n\neq 0$, 
$$
\mathrm{Res}_{z=n}(f) =\frac{g(n)}{h'(n)}= \frac{\cos(n\pi)}{\pi n^{2}(-1)^{n}}=\frac{1}{\pi n^{2}}
$$
Sooo
$$
0=\lim_{ N \to \infty }  2\pi i \sum_{n=-N}^{N}
$$