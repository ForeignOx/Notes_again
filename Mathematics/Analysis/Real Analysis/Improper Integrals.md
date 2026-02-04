Take a [[Continuity|continuous]] [[Functions|function]] $f:(a,b)\to \mathbb{R}$ with $a=-\infty,b=\infty$ allowed, then what is: $\int ^{b}_{a} f(t) \, dt$?
If $b$ is the problem:
$$
    \int ^{b}_{a} f(t) \, dt =\lim_{ c \to b^{-} } \int ^{c}_{a}  f(t)\, dt 
$$
If $a$ is the problem:
$$
\int ^{b}_{a} f(t) \, dt =\lim_{ c \to a^+ } \int_{c}^{b} f(t) \, dt 
$$
If the [[Limit|limit]] exists, we call the integral convergent, otherwise it is divergent.
### Examples
$$
\int_{1}^{\infty} x^{\alpha} \, dx=\lim_{ c \to \infty } \int_{1}^{c} x^{\alpha} \, dx  =\lim_{ c \to \infty } \left[ \frac{1}{\alpha+1}x^{\alpha+1}   \right]_{1}^{c}=\lim_{ c \to \infty } \frac{1}{\alpha+1}(c^{\alpha+1}-1)
$$
$$
= \begin{cases}
-\frac{1}{\alpha+1} & \alpha<-1\\\infty & \alpha \geq 1
\end{cases}

$$
___
$$
\int_{0}^{1} x^{\alpha} \, dx =\lim_{ c \to 0^+ } \int_{c}^{1} x^{\alpha} \, dx =\left[ \frac{1}{\alpha+1}x^{\alpha+1} \right]_{c}^{1}
$$
Will look back at what on earth this is saying later
___
$$
\int_{0}^{\infty} e^{ -x } \, dx =\lim_{ c \to \infty } [-e^{ -x }]_{0}^{c}=1
$$

## Comparison Test
If $0\leq f(x)\leq g(x)$ on $(a,b)$ then
- If $\int ^{b}_{a} g(x) \, dx$ converges, then $\int ^{b}_{a} f(x) \, dx$ also converges
- If $\int ^{b}_{a} f(x) \, dx$ diverges, then $\int ^{b}_{a} g(x) \, dx$ also diverges
### Proof
$$
0\leq \int_{a}^{c} f(x) \, dx \leq \int_{a}^{c} g(x) \, dx 
$$
Then [[Squeeze Theorem|squeeze]], and you have your result
### Examples
Consider the integrals:
$$
\int_{0}^{\infty} \frac{1}{1+e^{ x }} \, dx 
$$
$$
\int_{0}^{\infty} e^{ -x^{2} } \, dx 
$$
These do not have simple antiderivatives :( but we can do comparison, which is the continuous analogue to that for [[Series|series]], for the first,
$$
\int_{0}^{\infty} \frac{1}{1+e^{ x }} \, dx \leq \int_{0}^{\infty} \frac{1}{e^{ x }} \, dx <\infty
$$
So it converges
For the second:
$$
\int_{0}^{\infty} e^{ -x^{2} } \, dx =\underbrace{ \int_{0}^{1} e^{ -x^{2} } \, dx }_{ \text{finite} } +\int_{1}^{\infty} e^{ -x^{2} } \, dx <\int_{1}^{\infty} e^{ -x } \, dx<\infty 
$$
___
$$
\int_{1}^{\infty} \frac{\cos(x)}{x^{2}} \, dx 
$$
We consider that
$$
\left| \frac{\cos(x)}{x^{2}} \right|\leq \frac{1}{x^{2}} 
$$
And
$$
\int_{1}^{\infty} \frac{1}{x^{2}} \, dx =1<\infty
$$
Hence, we have [[Absolute Convergence|absolute]] convergence for $\int_{1}^{\infty} \frac{\cos(x)}{x^{2}} \, dx$
