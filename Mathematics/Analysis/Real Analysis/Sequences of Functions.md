Many [[Functions|functions]] cannot be obtained in an 'elementary' way, but rather arise by a [[Limit|limit]] process, for example $e^{ x }=\lim_{ n \to \infty }\left( 1+\frac{x}{n} \right)^{n}$. Particularly attractive are infinite [[Series|series]] of functions $\sum_{k=0}^{\infty} g_{k}(x)$, viewed as the limit of partial sums $f_{n}(x)=\sum_{ k=0} ^{ n} g_{k}(x)$. For example [[Power Series|power series]] are of this type
Given a function $f$, one can also seek to represent by an infinite series of (simpler) functions for example its [[Taylor Series|Taylor Series]] or for [[Periodic Functions|periodic functions]] its [[Fourier Series|fourier series]]
We can use step functions to approximate [[Continuity|continuous]] functions on a more compact [[Intervals|interval]] uniformly to arbitrary precision and use this then to extend the notion of [[Integration|integration]] for step functions to the one for continuous functions
One fundamental question in this process is under which circumstances the limit function $f$ inherits the properties of the functions $f_{n}$, say continuity or differentiability
If we have
$$
f_{n}(x):I\to \mathbb{R}
$$
Is a sequence of functions
## Examples
Let $f(x)=\sum_{k=0}^{\infty} x^{k}$ for $\left| x \right|<1$, then
$$
f(x)=\lim_{ n \to \infty } \sum_{k=0}^{n}x^{k}=\lim_{ n \to \infty } f_{n}(x)=\frac{1}{1-x}
$$
So pointwise convergent
We can check whether this is [[Uniform Convergence|uniformly convergent]]:
$$
\left| f(x)=f_{n}(x) \right|=\left| \sum_{k=n+1}^{\infty} x^{k}  \right|=\left| \frac{x^{n+1}}{1-x} \right|   
$$
This quite clearly looks like it won't work, so we want to contradict, pick $x_{n}=\sqrt[n+1]{ \frac{1}{2} }$, and $\lim_{ n \to \infty }x_{n}=1$, so
$$
\left| f(x_{n})-f_{n}(x_{n}) \right| =\left|  \frac{x_{n}^{n+1}}{1-x_{n}} \right| =\left| \frac{\left( \sqrt[n+1]{ \frac{1}{2} } \right)^{n+1}}{1-\sqrt[n+1]{ \frac{1}{2} }} \right| =\frac{\frac{1}{2}}{1-\sqrt[n+1]{ \frac{1}{2} }}
$$
Which is unbounded as $n\to \infty$, so any $\varepsilon$ will work, so pick, for example $\varepsilon=1$, then for large $n$, we have
$$
\left| f(x_{n})-f_{n}(x_{n}) \right| \geq\varepsilon
$$
So we have a contradiction. We can however check for uniformity on all compact subsets $[a,b]\in(-1,1)$, for convenience take $r\in(0,1)$, such that $[a,b]\subseteq[-r,r]\subset(-1,1)$, then
$$
\left| f(x)-f_{n}(x) \right| =\left| \frac{x^{n+1}}{1-x} \right| \leq \frac{r^{n+1}}{1-r}
$$
And
$$
\lim_{ n \to \infty }  \frac{r^{n+1}}{1-r}=0
$$
As $\left| r \right|<1$. Now we have $\frac{r^{n+1}}{1-r}$ which is independent of $x$, so we can pick $\varepsilon>0$, find $N$ such that $\forall N\geq n$, $\frac{r^{n+1}}{1-r}<\varepsilon$, (which we can as it tends to $0$), so we'll have $\left| f(x)-f_{n}(x) \right|<\varepsilon$
___
Consider $f_{n}(x)=\left( 1+\frac{x}{n} \right)^{n}\to e^{ x }=f(x)$ for $x\in\mathbb{R}$, we have shown pointwise convergence, we believe that this doesn't converge uniformly on $\mathbb{R}$, so we need to find a sequence to tend to infinity, so we can pick, for example $x_{n}=n$, then
$$
\left| f_{n}(x_{n})-f(x_{n}) \right| =\left| 2^{n}-e^{ n } \right| =e^{ n }-2^{n}=e^{n}\left( 1-\left( \frac{2}{e} \right)^{n} \right)
$$
Which is unbounded, so will be greater than $\varepsilon$
But it is uniform on compact subsets