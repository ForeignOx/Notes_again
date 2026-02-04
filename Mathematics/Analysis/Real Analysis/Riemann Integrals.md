## Intro
Recall that a partition of an [[Intervals|interval]] $[a,b]$ is a finite [[Sequences|sequence]]
$$
a=x_{0}<x_{1}<x_{2}<\dots<x_{n}=b
$$
Each $[x_{i},x_{i+1}]$ is called a subinterval of the partition
The mesh of a partitiion is defined to be the length of the longest sub-interval $[x_{i},x_{i+1}]$, that is, $\max_{0\leq i\leq n-1}(x_{i+1}-x_{i})$
Let $f$ be a [[Real Functions|real]] [[Functions|function]] defined on the interval $[a,b]$. The [[Riemann Sums|Riemann sum]] of $f$ with respect to the partition $x_{0},\dots,x_{n}$ is  
$$
\sum_{i=0}^{n-1} f(x_{i}^{*})(x_{i+1}-x_{i})
$$
Where each $x_{i}^{*}$ is a fixed point in the subinterval $[x_{i},x_{i+1}]$
Notice that this is the sum of rectangles with heights $f(y_{i})$ and widths $x_{i+1}-x_{i}$
Loosely speaking, the Riemann integral of $f$ is the limit of Riemann sums of $f$ as the partitions get finer and finer (i.e. the mesh goes to zero)
Every function $f$ for which this limit doesn't depend on the approximating sequence is called integrable
## Definition
A function $f$ is called Riemann integrable if the limit of all Riemann sums exists as the mesh of the partition (the length of the largest sub-interval) goes to $\hspace{0pt}0$, if there exists a number $s$ (the integral of $f$) such that for all $\varepsilon>0$ there exists $\delta>0$ such that for all Riemann sums associated to a partition with mesh less that $\delta$, we have
$$
\left| s-\sum_{k=0}^{N-1}f(x_{k}^{*})(x_{k+1}-x_{k}) \right| <\varepsilon
$$
This is fairly difficult to practically impossible to deal with, and typically one considers the following concept which turns out to be equivalent to the definition of Riemann integrals, Darboux integrals
### Darboux Integration
A function $f$ is Darboux integrable, if for any partition $P$, one sets 
$$
m_{k}=\inf_{x\in [x_{k},x_{k+1}]}\left\{ f(x) \right\}
$$
$$
M_{k}=\sup_{x\in [x_{k},x_{k+1}]}\left\{ f(x) \right\}
$$
Here, one needs to assume $f$ is [[Boundedness|bounded]]
And defines the lower and upper Riemann sums as
$$
L(f,P)=\sum_{k=0}^{N-1}m_{k}(x_{k+1}-x_{k}),~U(f,P)=\sum_{k=0}^{N-1}M_{k}(x_{k+1}-x_{k})
$$
One then defines the lower and upper Riemann integrals by
$$
L_{f}=\sup_{P}L(f,P)=\underline{\int}_{P}f,~    U_{f}=\inf_{P}(f,P)=\overline{\int}_{P}f
$$
And calls $f$ Darboux-integrable if $U_{f}=L_{f}$
One can prove that this is the same as Riemann integrable
## Properties
- [[Linear|Linearity]]: If $f(x)$ and $g(x)$ are integrable functions and $a$ and $b$ are real constants, then $af(x)+bg(x)$ is integrable and
$$
\int af(x)+bg(x) \, dx =a\int f(x) \, dx +b\int g(x) \, dx 
$$
- Monotonicity: If $f(x)\leq g(x)$ for all $x$, then
$$
\int f(x) \, dx \leq \int g(x) \, dx 
$$
- Respect to limits: If $f_{n}(x)\to f(x)$ as $n\to \infty$, then
$$
\int f_{n}(x) \, dx \to \int f(x) \, dx \text{ as }n\to \infty
$$
By consturction, the Riemann integral is both linear and monotone. However it is difficult to define in spaces other than [[Real Numbers|$\mathbb{R}$]], and the Riemann integral does not respect all limits
## Example
For real $a$, let $\delta_{a}(x)$ be the [[Kronecker Delta Function|Kronecker delta-function]] 
$$
\delta_{a}(x)=\begin{cases}
1 & x=a \\
0 & x\neq a
\end{cases}
$$
It is immediate that the Riemann integral of $\delta_{a}$ vanishes, $\int \delta_{a} \, dx=0$
On the other hand the Dirichlet function $D(x)$, or the indicator function of the rational numbers,
$$
D(x)=\begin{cases}
1 & x\in \mathbb{Q} \\
0 & x\not\in \mathbb{Q}
\end{cases}

$$
Is clearly not Riemann-integrable.
At the same time, $D(x)$ can be written as a limit of point-wise increasing sequences of functions, each of which has zero Riemann integral on each fixed interval of finite length
Indeed, let $a$ and $b$ be any fixed real numbers such that $a<b$ for $m\in\mathbb{N}$, let $Q_{m}$ be the set of all rational nubers with denominator at most $m$:
$$
\mathbb{Q}_{m}:=\left\{ x\in \mathbb{R}\middle|kx\in \mathbb{Z}\text{ for some }k=1,\dots,m \right\}
$$
For example for $m=3$, we have $\mathbb{Q}_{3}\cap(0,1]=\left\{ \frac{1}{3},\frac{1}{2},\frac{2}{3},1 \right\}$
For each $m\geq 1$, let
$$
f_{m}(x):=\sum_{q\in \mathbb{Q}_{m}}\delta_{q}(x)
$$
Be the indicator function of the set $\mathbb{Q}_{m}$, so that $f_{m}(x)\in\left\{ 0,1 \right\}$ for each $x\in\mathbb{R}$
As the sets $\mathbb{Q}_{m}$ are increasing in $m$, for each fixed $x\in\mathbb{R}$, the sequence $(f_{m})_{m\in\mathbb{N}}$ is a non-decreasing sequence (of numbers in $\left\{ 0,1 \right\}$),
At the same time, for each $m\geq 1$, we have
$$
\int ^{b}_{a} f_{m}(x) \, dx =0
$$
and for each $x\in\mathbb{R}$, we have $f_{m}(x)\to D(x)$ as $m\to \infty$, while $\int ^{b}_{a} D(x) \, dx$ is not defined