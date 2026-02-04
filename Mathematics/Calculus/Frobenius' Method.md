Suppose you have an [[Linear Ordinary Differential Equations|ordinary differential equation]] with some number of [[Regular Points|singular points]], then the [[Cauchy-Hadamard Theorem|radius of convergence]] about some point is as large as the distance to the nearest singular point, for the [[Power Series|Power Series]] $y=\sum_{n=0}^{\infty} a_{n}(x-x_{0})^{n}$ with singular points $x_{1},x_{2},\dots$:
![[Frobenius' Method 2025-02-18 12.52.50.excalidraw]]
$$
R=\text{min}\left| x_{0}-x_{i} \right| 
$$
Frobenius tells us that if we have some regular singular point, we can still expand there by adding some $r$ to the power like so:
$$
y(x)=\sum_{n=0}^{\infty} a_{n}x^{n+r} 
$$
Where $r$ is a constant, not necessarily an integer
## Example
Consider the differential equation:
$$
2x(x+1)y''+(x+1)y'-3y=0
$$
Which can be re-written in canonical form:
$$
y''+\frac{y'}{2x}-\frac{3y}{2x(x+1)}=0
$$
So $p=\frac{1}{2x}$, $q=-\frac{3}{2x(x+1)}$
We get two singular points at $x=0,-1$, but at $x_{0}=0$, we can check if it is a regular singular point:
$$
p(x)x=\frac{1}{2},q(x)x^{2}=-\frac{3x}{2(x+1)}
$$
Both of which are analytic at $x_{0}=0$
We can then apply Frobenius' method:
$$
2x(x+1)\sum_{n=0}^{\infty} a_{n}(n+r)(n+r-1)x^{n+r-2}+(x+1)\sum_{n=0}^{\infty} a_{n}(n+r)x^{n+r-1}-3\sum_{n=0}^{\infty} a_{n}x^{n+r}=0
$$
$$
 \implies \sum_{n=0}^{\infty} a_{n}(n+r)(n+r-1)x^{n+r}+\sum_{n=0}^{\infty} 2a_{n}(n+r)(n+r-1)x^{n+r-1}+\sum_{n=0}^{\infty} a_{n}(n+r)x^{n+r}
$$
$$
 + \sum_{n=0}^{\infty} a_{n}(n+1)x^{n+r-1}-3\sum_{n=0}^{\infty} a_{n}x^{n+r}       =0 
$$
We want all the coefficients of a particular power of $x$ to match up to make a [[Recurrence Relations|recurrence relation]], so simply relable $n\to n+1$ when needed to get:
$$
\implies\sum_{n=-1}^{\infty} 2a_{n+1}(n+r+1)(n+r)x^{n+r}+\sum_{n=-1}^{\infty} a_{n+1}(n+r+1)x^{n+r}
$$
$$
 +\sum_{n=0}^{\infty} a_{n}x^{n+r}(2(n+r)(n+r-1)+(n+r)-3)  =0
$$

This has the lowest power of $x$ as $x^{r-1}$
$$
2a_{0}r(r-1)+a_{0}r=0=a_{0}r(2r-1)
$$
So $r=0,\frac{1}{2}$
At this point we can consider