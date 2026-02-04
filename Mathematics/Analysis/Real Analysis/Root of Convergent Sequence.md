Let $(x_{n})_{n\in\mathbb{N}}$ be a [[Convergence|convergent]] [[Sequences|sequence]] with each $x_{n}\geq 0$. Then $(\sqrt{ x_{n} })_{n\in\mathbb{N}}$ is a convergent sequence with:
$$
\lim_{ n \to \infty } \sqrt{ x_{n} }=\sqrt{ \lim_{ n \to \infty } x_{n} }
$$
## Proof
Denote $x=\lim_{ n \to \infty }x_{n}\geq 0$
Distinguish between the cases $x=0$ and $x>0$
Assume $x>0$:
$$
|\sqrt{ x_{n} }-\sqrt{ x }|=\left|\frac{(\sqrt{ x_{n} }-\sqrt{ x })(\sqrt{ x_{n} }+\sqrt{ x })}{\sqrt{ x_{n} }+\sqrt{ x }}\right|=\frac{|x_{n}-x|}{\sqrt{ x_{n} }+\sqrt{ x }}\leq \frac{|x_{n}-x|}{\sqrt{ x }}
$$
The numerator converges to $\hspace{0pt}0$, so by the [[Squeeze Theorem|squeeze theorem]], 
$$
\sqrt{ x_{n} }-\sqrt{ x }\to0
$$
So by [[Calculus of Limits Theorem|CoLT]], $\sqrt{ x_{n} }\to \sqrt{ x }$
## Examples

$$
y_{n}=\frac{n^{2}-n(-1)^{n}}{\sqrt{ n^{4}+1 }}=\frac{n^{2}\left( 1-\frac{(-1)^{n}}{n} \right)}{n^{2}\sqrt{ 1+\frac{1}{n^{4}} }}=\frac{1-\frac{(-1)^{n}}{n}}{\sqrt{ 1+\frac{1}{n^{4}} }}
$$
By CoLT, 
$$
y_{n}\to \frac{1-0}{\sqrt{ 1+0 }}=1
$$
___
$$
x_{n}=\sqrt{ n }(\sqrt{ n+1 }-\sqrt{ n })=\frac{\sqrt{ n }(\sqrt{ n+1 }-\sqrt{ n })(\sqrt{ n+1 }+\sqrt{ n })}{\sqrt{ n+1 }+\sqrt{ n }}=\frac{\sqrt{ n }}{\sqrt{ n+1 }+\sqrt{ n }}=\frac{\sqrt{ n }}{\sqrt{ n }\left( \sqrt{ \frac{n+1}{n} }+1 \right)}
$$
$$
=\frac{1}{\underbrace{ \sqrt{ \frac{n+1}{n} } }_{ \to 1 }+1}
$$
So this converges to $\frac{1}{2}$

#Mathematics #Analysis #Theorem 