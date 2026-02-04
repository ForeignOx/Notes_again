[[Differentiation|Differentiability]] at one point is nice, but usually not enough. Most theorems in real analysis want differentiability on [[Intervals|intervals]]
A good candidate to replace the interval with is an open ball, or in general and open set
## Definition
A function $f:U\to \mathbb{C}$ defined on an open set $U\subseteq \mathbb{C}$ is holomorphic on $U$ if it is complex differentiable at every point in $U$
We say $f$ is holomorphic at $z_{0}$ if it is holomorphic in an [[Open Sets|open ball]] $B_{\varepsilon}(z_{0})$ around $z_{0}$ for some $\varepsilon>0$
A function that is holomorphic on $\mathbb{C}$ is called an entire function
## Examples
$e^{ x },\sin x,\cos x,\sinh x,\cosh x,\log x,$ polynomials are all entire (on respective branches for $\log$)
## Zero Derivative Theorem
Let $f:D\to \mathbb{C}$ be holomorphic on a domain $D\subseteq \mathbb{C}$. If $f'(z)=0$ for every $z\in D$, then $f$ is constant
### Proof
We claim that it is enough to show that for any $z_{1},z_{2}\in D$, $f(z_{1})=f(z_{2})$ since $D$ is a domain
We can find a contour $\gamma:[0,1]\implies \mathbb{C}$ such that

finish ths plzzz
___
The beauty of complex analysis is that to have a constant holomorphic function, we only need that $f$ "doesn't fill" the space i.e.