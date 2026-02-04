A function such that
$$
\frac{ \partial^{2}g(x,\xi) }{ \partial x^{2} } =\delta(x,\xi)
$$
Where
$$
\int_{a}^{b} \delta(x,\xi)f(\xi) \, d\xi=f(x) 
$$
Which acts a oike $\delta(x,\xi)=0$ unless $x=\xi$
## Definition
Essentially, we have a function that satisfies $\delta(x)=0$ for all $x\neq 0$, and which satisfies
$$
\int_{-\infty}^{\infty} \delta(x) \, dx =1
$$
Not actually allowed :(
Which is kinda wack (one can think of it as having infinite value at $x=0$)
The integral
$$
\int_{-\infty}^{x} \delta(x) \, dx=\begin{cases}
0& x<0 \\
1 & x>0
\end{cases} 
$$
Which is a [[Heaviside Step Function|Heaviside function]], a type of [[Step Functions|step function]]
The way we get around this is with analysis yippeee
Define some [[Sequences of Functions|sequence of functions]] $f_{n}(x)$ such that
$$
\int_{-\infty}^{\infty} f_{n}(x) \, dx=1\forall n
$$
With
$$
\lim_{ n \to \infty } f_{n}(x)=0\forall x\neq 0
$$
For example
$$
f_{n}(x)=\begin{cases}
0 & \left| x \right| >\frac{1}{n} \\
\frac{n}{2} & \left| x \right| \leq \frac{1}{n}
\end{cases}
$$
Which we can see fits the limits we want
This also shows why there is no actual $\delta(x)$ itself, but it's fine as long as it's in an integral
## Properties
### Sifting Property
Let $f(x)$ be a [[Continuity|continuous]] [[Functions|function]] and let $F(x)=\int_{-\infty}^{x} f(\xi) \, d\xi$, we want to show:
$$
\int_{-\infty}^{\infty} \delta(x-a)f(x) \, dx =\lim_{ n \to \infty } \int_{-\infty}^{\infty} f_{n}(x-a)f(x) \, dx =f(a)
$$
So if $f_{n}$ are hat functions (triangular things), then
$$
\lim_{ n \to \infty }\int_{a-\frac{1}{n}}^{a+\frac{1}{n}} \frac{n}{2}f(x) \, dx =\lim_{ n \to \infty } \frac{F\left( a+\frac{1}{n} \right)-F\left( a-\frac{1}{n} \right)}{2 /n}=f(a)
$$
Setting $s=\frac{1}{n}$ and using CoLT

We will limit ourselves to using just this sifting, so we don't need to do limits every time yippee


