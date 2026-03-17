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
\oint_{S_{N}}f(z)~dz=2\pi i \sum_{n=-N}^{N} \mathrm{Res}
$$
