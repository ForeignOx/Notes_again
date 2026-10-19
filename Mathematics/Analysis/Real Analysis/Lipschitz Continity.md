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
\forall x_{0}\in A,\forall R>0,\exists L=L(x_{0},R)
$$
such that $f$ is locally Lipschitz in $B_{R}(x_{0})\cap A$
## Examples
Is $f:\mathbb{R}\to \mathbb{R}$ where $f(x)=x$, is there $L>0$ such that
$$
\left| f(x)-f(y) \right| \leq L\left| x-y \right| \forall x,y\in \mathbb{R}
$$
Yep, 