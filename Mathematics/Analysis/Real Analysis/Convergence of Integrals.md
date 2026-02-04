Say we have $f_{n}:[a,b]\to \mathbb{R}$ is a [[Sequences of Functions|sequence]] of [[Regulated Functions|regulated]] [[Functions|functions]] on an [[Intervals|interval]] such that $f_{n}\to f$ converges [[Uniform Convergence|uniformly]], then:
- $f$ is regulated,
- $\int ^{b}_{a} f(t) \, dt=\lim_{ n \to \infty }\int ^{b}_{a} f_{n}(t) \, dt$ 
## Proof
$f_{n}\to f$ uniformly, so given $\varepsilon>0$, 
$$
\left| f_{n}(x)-f(x) \right| <\varepsilon \forall x\in [a,b]\forall n\geq N
$$
Such that $f_{n}$ is regulated, so there exists a [[Step Functions|step function]] $g_{n}(x)$ such that
$$
\left| f_{n}(x)-g_{n}(x) \right| <\varepsilon
$$
We claim that $g_{n}\to f$ uniformly, so $f$ is regulated.
$$
\left| f(x)-g_{n}(x) \right| =\left| f(x)-f_{n}(x)+f_{n}(x)-g_{n}(x) \right| \leq \left| f(x)-f_{n}(x) \right| +\left| f_{n}(x)-g_{n}(x) \right| <\varepsilon+\varepsilon=2\varepsilon
$$
Which is true $\forall x\in[a,b],\forall n\geq N$, fo $f$ is regulated as required
For the second part we really only need the first part to show that $f$ is integrable, then use the [[Convergence|limit of sequences]] and [[Integration|integral]] properties:
$$
\left| \int ^{b}_{a} f(t) \, dt -\int ^{b}_{a}  f_{n}(t)\, dt  \right| =\left| \int ^{b}_{a} f(t)-f_{n}(t) \, dt \right| \leq \int ^{b}_{a} \left| f(t)-f_{n}(t) \right|  \, dt 
$$
$$
 \leq \int ^{b}_{a} \varepsilon \, dt =(b-a)\varepsilon
$$
## Example
The [[Weierstrass Monster|Weierstrass monster]]:
$$
f(x)=\sum_{k=0}^{\infty} \frac{1}{2^{k}}\cos(15^{k}\pi x) 
$$
Converges uniformly by the [[Weierstrass M-test|Weierstrass M-test]], so it is [[Continuity|continuous]], so it is regulated, so the integral $\int_{0}^{\frac{1}{2}} f(t) \, dt$ exists:
$$
\int_{0}^{\frac{1}{2}} f(t) \, dt =\sum_{k=0}^{\infty}\int_{0}^{\frac{1}{2}} \frac{1}{2^{k}}\cos(15^{k}\pi t) \, dt=\sum_{k=0}^{\infty} \frac{1}{2^{k}} \frac{1}{15^{k}\pi}\sin\left( 15^{k}\pi \frac{1}{2} \right)
$$
$$
= \frac{1}{\pi}\sum_{k=0}^{\infty}  \frac{1}{30^{k}}(-1)^{k}=\frac{1}{\pi}  \frac{1}{1+\frac{1}{30}}=\frac{30}{31\pi}
$$
## [[Pointwise Limit|Pointwise Convergence]]
If $f_{n}$'s converge only pointwise, there might be issues, for example, consider the function:
$$
f_{n}(x)=\begin{cases}
n-n^{2}x & x\in \left[ 0,\frac{1}{n} \right]\\0 & \text{otherwise}
\end{cases}
$$
![[Convergence of Integrals 2025-03-17 16.45.54.excalidraw]]
$$
\int_{0}^{1} f_{n}(x) \, dx =\frac{1}{2}
$$
But $f_{n}\to f(x)=0$ and
$$
\int_{0}^{1} 0 \, dx =0
$$
This is because $f_{n}(x)$ doesn't converge uniformly (pick $x_{n}=\frac{1}{2n}$)
___
However, consider $f_{n}(x)=x^{n}$ for $x\in[0,1]$, which converges to:
$$
f(x)=\begin{cases}
0 & x\in [0,1)\\1 & x=1
\end{cases}
$$
It is not uniform on $[0,1]$, but it is uniform on compact subsets of $(0,1)$ and
$$
\int_{0}^{1} f(x) \, dx =0
$$
$$
 \int_{0}^{1} f_{n}(x) \, dx =\frac{1}{n+1}\to0
$$
So it does work sometimes, since all the functions are bounded