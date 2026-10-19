## Definition
$f:A\to \mathbb{R}^{m}$ is said to be Lipschitz continuous on $A\subseteq \mathbb{R}^{m}$ if $\exists L>0$ such that
$$
\left| f(x)-f(y) \right| _{\mathbb{R}^{m}}\leq L\left| x-y \right| _{\mathbb{R}^{m}}
$$
## Remark
If $f$ is Lipschitz continuous, then it is [[Uniform Continuity|uniformly]] [[Continuity|continuous]]
___
The set of all Lipschitz constant functions will be denoted by $\mathrm{Lip}(A,\mathbb{R}^{m})$
## Definition#
$L>0$ is said to be the Lipschitz contant of $f\in \mathrm{Lip}(A,\mathbb{R}^{m})$ if $L$ is the smallest constant satisfying
$$
L=\inf\left\{ L>0s:\middle|:\left| f(x)-f(y) \right| \leq L\left| x-y \right| \text{ is satisfied }\forall x,y\in A \right\}
$$
## Local Lipschitz Continuity
$f:A\to \mathbb{R}^{m}$ is said to be locally Lipschitz continuous in $A$ if 
$$
\forall x_{0}\in A,\exists R>0,\exists L=L(x_{0},R)
$$
such that $f$ is locally Lipschitz in $B_{R}(x_{0})\cap A$
## Lemma
Let $A\subseteq \mathbb{R}^{n}$ and $\underline{f}:A\to \mathbb{R}^{m}$, writing $\underline{f}=(f_{1},\dots,f_{m})$, we have that
- $\underline{f}$ is Lipschitz on $A$ iff $f_{i}:\mathbb{R}^{n}\to \mathbb{R}$ is Lipschitz on $A$ for any $i=1,\dots,m$
- $\underline{f}$ is locally Lipschitz on $A$ iff $f_{i}:\mathbb{R}^{n}\to \mathbb{R}$ is locally Lipschitz on $A$ for any $i=1,\dots,m$
## Examples
Is $f:\mathbb{R}\to \mathbb{R}$ where $f(x)=x$, is there $L>0$ such that
$$
\left| f(x)-f(y) \right| \leq L\left| x-y \right| \forall x,y\in \mathbb{R}
$$
Yep, $f$ is 1-Lipschitz
___
Take $f:(0,\infty)\to \mathbb{R}$ given by $f(x)=\frac{1}{x}$, is thi?
$$
\left| \frac{1}{x}-\frac{1}{y} \right| =\frac{\left| x-y \right| }{xy}\leq L\left| x-y \right| 
$$
This cannot hold for all $x,y$, as for anu $L>0$, there exists $x,y>0$ such that $\frac{1}{xy}>L$
This function is however locally Lipschitz continuous, for $x_{0}\in(0,\infty)$, take $(x_{0}-R,x_{0}+R)\cap(0,\infty)$, taking $R=\frac{x_{0}}{2}$, 
$$
\left( x_{0}-\frac{x_{0}}{2},x_{0}+\frac{x_{0}}{2} \right)\cap(0,\infty)=\left( \frac{x_{0}}{2},\frac{3x_{0}}{2} \right)=B_{\frac{x_{0}}{2}}(x_{0})
$$
So the Lipschitz contant for $\frac{1}{x}$ on $B_{\frac{x_{0}}{2}}(x_{0})$ is $\frac{4}{x_{0}^{2}}$
___
Consider $f(x)=x^{2}$
$$
\left| f(x)-f(y) \right| =\left| x^{2}-y^{2} \right| =\left| x+y \right| \left| x-y \right| 
$$
This will explode, so cannot be Lipschitz, however it is again locally Lipschitz, clearly
## Proposition
$f:A\to \mathbb{R}^{m}$, with $A$ open is continuously differntiable, suppose that $A$ is [[Convex Sets|convex]] ($\forall x,y\in A$, $\theta x+(1-\theta)y\in A\forall\theta \in[0,1]$)
Then $f$ is $L$-Lipschitz iff $\lvert \lvert Df \rvert \rvert\leq L$
### Proof
$$
f(x)-f(y)=\int_{0}^{1} \partial_{\theta}(f(\theta x+(1-\theta)y)) \, d\theta  
$$
$$
= \int_{0}^{1}||\underbrace{ \underbrace{  Df(\theta x+(1-\theta)y) }_{ \in \mathbb{R}^{m\times n} }\underbrace{ (x-y)  }_{ \in \mathbb{R}^{n} }\, }_{ \in \mathbb{R}^{m} }|| d\theta 
$$
With norm given by
$$
\lvert \lvert B \rvert \rvert =\sup \frac{\left| B\alpha \right| }{\left| \alpha \right| }
$$

