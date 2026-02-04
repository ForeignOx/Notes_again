Let [[Functions|$f(x)$]] be a [[Periodic Functions|periodic]] function with period $2L$, such that on the [[Intervals|interval]] $(-L,L)$ it has a finite number of extrema, a finite number of [[Continuity#Jump Discontinuity|jump discontinuities]], and $\left| f(x) \right|$ is integrable on $(-L,L)$, then its [[Fourier Series|Fourier series]] [[Series|converges]] for all $x$. Furthermore, it converges to $f(x)$ at all points where $f$ is continuous and if $x=a$, is a jump discontinuity, then the Fourier series converges to $\frac{1}{2}(\lim_{ x \to a^{-} }f(x)+\lim_{ x \to a^{+} }f(x))$ 
This means certain infinite sums can be calculated by evaluating the Fourier series at a particular $x$
## Example
Calculate $\sum_{ n=1} ^{\infty} \frac{1}{(2n-1)^{2}}$ by evaluating the Fourier series of $f(x)=\left| x \right|$ for $x\in(-1,1)$ at $x=0$
In one of [[Fourier Series#Examples|these examples]] we calculated the Fourier series of $f(x)$ as:
$$
f(x)=\frac{1}{2}-\frac{4}{\pi^{2}}\sum_{ n=1} ^{\infty}  \frac{\cos((2n-1)\pi x)}{(2n-1)^{2}}
$$
Since $f$ satisfies Dirichlet's theorem, and since $f$ is continuous at $0$, the value of the Fourier series at $x=0$ is $f(0)=0$, hence:
$$
0=\frac{1}{2}-\frac{4}{\pi^{2}}\sum_{ n=1} ^{\infty}  \frac{1}{(2n-1)^{2}}
$$
$$
\implies \sum_{ n=1} ^{\infty}  \frac{1}{(2n-1)^{2}}=\frac{\pi^{2}}{8}
$$

#Mathematics #Calculus #Theorem 