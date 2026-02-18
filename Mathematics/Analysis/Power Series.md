## Definition
A (complex) power series is an expression of the form
$$
S(z):=\sum_{n=0}^{\infty}a_{n}(z-c)^{n}
$$
Where $\left\{ a_{n} \right\}_{n\in\mathbb{N}}$ is a sequence of complex numbers and $c\in \mathbb{C}$
## Theorem
A power series $\sum_{n=0}^{\infty}a_{n}(z-c)^{n}$ with radius of convergence $0<R\leq \infty$ converges uniformly on any ball $B_{r}(c)$ with $0<r<R$. This implies that the power series is [[Locally Uniform Convergence|locally uniform convergent]] on its disc of convergence
### Proof
We start by noticing that the disc of convergence is an open ball, so we can use the simplified version of local uniform convergence. Since for every $z_{0}\in B_{R}(c)$ we can find $0<r<R$ such that $z_{0}\in B_{r}(c)\subset B_{R}(c)$, we conclude that to how the local uniform convergence in $B_{R}(c)$, we only need to show the uniform convergence in $B_{r}(c)$ for any $0<r<R$
On $B_{r}(c)$, we have that
$$
\left| a_{n}(z-c)^{n} \right| \leq \left| a_{n} \right| \left| z-c \right| ^{n}\leq \left| a_{n} \right| r^{n}
$$
Since $\sum_{n=0}^{\infty}a_{n}(z-c)^{n}$ converges absolutely in $B_{R}(c)$, we find that as $z_{0}=c+r\in B_{R}(c)$, since $0<r<R$
$$
\sum_{n=0}^{\infty}\left| a_{n} \right| r^{n}=\sum_{n=1}^{\infty}\left| a_{n} \right| \left| z_{0}-c \right| ^{n}<\infty
$$
Using [[Weierstrass M-test|Weierstass' M-test]] on $B_{r}(c)$ with $M_{n}(B_{r}(c))=\left| a_{n} \right|r^{n}$ gives us the desired result
## Example
Show that the power series $\sum_{n=0}^{\infty} \frac{z^{n}}{n!}$ converges locally uniformly on $\mathbb{C}$
We will show that the radius of converges $R=\infty$ and conclude the result from the theorem.
Indeed, the expression is a power series with $a_{n}=\frac{1}{n!}$. We have that
$$
\frac{\left| a_{n} \right|}{\left| a_{n+1} \right| }=n+1\to \infty \text{ as }n\to\infty
$$
Which implies $R=\infty$ (this power actually converges to [[Exponential Functions|$e^{ z }$]])
## Formal Derivative & Antiderivative
Let $\sum_{n=0}^{\infty}a_{n}(z-c)^{n}$ be a power series with radius of convergence $0<R\leq \infty$, then the formal derivative obtained by differentiating term-wise:
$$
\sum_{k=1}^{\infty} ka_{k}(z-c)^{k-1}=\frac{1}{z-c}\sum_{k=1}^{\infty} ka_{k}(z-c)^{k}  
$$
The formal antiderivative is done by taking the antiderivative termwise:
$$
\sum_{k=1}^{\infty} \frac{1}{k+1}a_{k}(z-c)^{k+1}
$$
These have the same [[Cauchy-Hadamard Theorem|radius of convergence]]
### Proof
Consider the [[Root Test|root test]] for the formal derivative:
$$
\limsup_{ k \to \infty } \sqrt[k]{ k\left| a_{k} \right|  }=\lim_{ k \to \infty } \sqrt[k]{ k }\limsup_{ k \to \infty } \sqrt[k]{ \left| a_{k} \right|  }=1\times \limsup_{ k \to \infty } \sqrt[k]{ \left| a_{k} \right|  }
$$
So the radius of convergence is the same. The same applies for the antiderivative
## Power Series as Functions
Consider a [[Functions|function]] 
$$
f(x)=\lim_{ n \to \infty } f_{n}(x)=\sum_{k=0}^{\infty} a_{k}x^{k} 
$$
Where $f_{n}(x)=\sum_{ k=0} ^{ n} a_{k}x^{k}$
### Power Series are Continuous in Radius of Convergence
Power series are in fact locally Lipschitz [[Continuity|continuous]], that is, for any $0<r<R$, there exists a constant $M=M_{r}$ such that
$$
\left| f(x)-f(y) \right| \leq M_{r}\left| x-y \right| \forall x\in [-r,r]
$$
#### Proof
We have
$$
0\leq \left| f_{n}(x)-f_{n}(y) \right|=\left| \sum_{ k=1} ^{ n}  a_{k}(x^{k}-y^{k}) \right|  
$$
(The $a_{0}$ term vanishes)
$$
=\left| x-y \right| \left| \sum_{ k=1} ^{ n}  a_{k}(x^{k-1}+x^{k-2}y+\dots+xy^{k-2}+y^{k-1}) \right| 
$$
And since $\left| x \right|,\left| y \right|\leq r$, hence
$$
\leq \left| x-y \right| \sum_{ k=1} ^{ n}  \left| a_{k} \right| kr^{k-1}
$$
As $n\to \infty$, this tends to
$$
\to \left| x-y \right| \sum_{ k=1} ^{ \infty} \left| a_{k} \right| M_{r}  
$$
Which converges due to formal derivatives converging and this [[Cauchy-Hadamard Theorem#Corollary|corollary]] 
___
A further proof, since they converge [[Uniform Convergence|uniformly]] on compact subsets of $(-R,R)$:
Take a compact subset $[a,b]\subset[-r,r]\subset(-R,R)$, so $r<R$
Take $x\in[-r,r]$, then 
$$
\sum_{k=0}^{\infty} \underbrace{ \left| a_{k} x^{k} \right|  }_{ =f_{k}(x) }\leq \sum_{k=0}^{\infty} \left| a_{k} \right| r^{k}=\sum_{k=0}^{\infty} M_{k}  
$$
Since $r<R$
___
Warning typically $\sum_{k=0}^{\infty} a_{k}x^{k}$ is not Lipschitz on $(-R,R)$
### Power Series are Differentiable in Radius of Convergence
A power series $\sum_{k=0}^{\infty} a_{k}x^{k=f(x)}$ is [[Differentiation|differentiable]] in $(-R,R)$ with termwise derivative 
$$
f'(x)=\sum_{k=1}^{\infty} ka_{k}x^{k-1} 
$$
And
$$
f^{(n)}(0)=n!a_{n}
$$
#### Proof
Part 1:
Recall
$$
f(x)=f(c)+(x-c)\underbrace{ \sum_{k=1}^{\infty}a_{k}(x^{k-1}+x^{k-2}c+x^{k-3}c^{2}+\dots+xc^{k-2}+c^{k-1}) }_{ =f_{1}(x) }
$$
[[Taylor Series#First Order Taylor|First order taylor]] gives that $f(x)$ is differentiable at $c$ iff $f_{1}(x)$ is constant at $x=c$ and then
$$
f'(c)=f_{1}(c)=\sum_{k=1}^{\infty}a_{k}kc^{k-1}
$$
We can apply $M$-test to $f_{1}(x)$ in the compact interval $(-r,r)\subset[-R,R]$, where $c\in(-r,r)$, indeed
$$
\left| g_{k}(x) \right| =\left| a_{k}(x^{k-1}+x^{k-2}c+x^{x-3}c^{2}+\dots+xc^{k-2}+c^{k-1}) \right|
$$
$$
  \leq \left| a_{k} \right| (\left| x \right| ^{k-1}+\left| x \right| ^{k-2}\left| c \right| +\left| x \right| ^{k-3}\left| c \right|^{2}+\dots+\left| x \right| \left| c \right| ^{k-2}+\left| c \right| ^{k-1} )
$$
By [[Triangle Inequality|triangle inequality]], then substituting $x=c=r$
$$
\left| a_{k} \right| (r^{k-1}+r^{k-1}+\dots+r^{k-1})=\left| a_{k} \right| kr^{k-1}:=M_{k}
$$
Which is independent of $x$, so it must converge uniformly as the formal derivative of $f(x)$ evalueated at $x=r<R$, (so the radius of convergence is conserved)

Part 2:
Assuming part $\hspace{0pt}1$, we have
$$
f'(0)=\sum_{k=1}^{\infty} ka_{k}0^{k-1}=1\times a_{1}=a_{1} 
$$
$$
f''(0)=\sum_{k=2}^{\infty} k(k-1)a_{k}0^{k-2} =2(2-1)a_{2}=2!a_{2}
$$
$$
\vdots
$$
$$
 f^{(n)}(0)=\sum_{k=n}^{\infty} k(k-1)\dots(k-n+1)a_{k}0^{k-n}=n!a_{n} 
$$
