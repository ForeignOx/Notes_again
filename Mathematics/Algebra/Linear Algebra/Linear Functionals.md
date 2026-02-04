## Definition
A [[Linear Maps|linear transformation]] from a [[Vectorspaces|vectorspace]] $V$ to the [[Scalar Fields|scalar field]] [[Fields|$\mathbb{F}$]] is called a linear functional on $V$
## Example
Thus $f\mapsto \int ^{b}_{a} f(t) \, dt$ is a linear functional on $V=\mathcal{C}([a,b])$, the [[Sets|set]] of [[Continuity|continuous]] [[Functions|functions]]
___
[[Linear Maps#Linear Combination Mapping Theorem|This theorem]] is particularly simple for a linear functional $F$, since $W=\mathbb{R}$, each vector $\beta_{i}=F(\delta^{i})$ is simply a number $b_{i}$, and the [[Skeletons of Linear Maps|skeleton]] $\left\{ b_{i} \right\}_{1}^{n}$ is thus an element of [[Vectorspace Rn|$\mathbb{R}^{n}$]]
In this case we would write
$$
F(\underline{x})=\sum_{n=1}^{n}b_{i}x_{i}
$$
Putting the numerical coefficient $b_{i}$ before the variable $x_{i}$. Thus $F(\underline{x})=3x_{1}-x_{2}+4x_{3}$ is the linear functional on $\mathbb{R}^{3}$ with skeleton $(3,-1,4 )$
The set of all linear functionals on $\mathbb{R}^{n}$ is a natural one to one correspondence with $\mathbb{R}^{n}$ itself; we bet $\underline{b}$ from $F$ by $b_{i}=F(\delta^{i})$ for all $i$, and we get $F$ from $\underline{b}$ by $F(\underline{x})=\sum_{ i=1} ^{ n} b_{i}x_{i}$ for all $\underline{x}\in \mathbb{R}^{n}$
## As Matrices/Vectors
A linear functional $F$ on $\mathbb{R}^{n}$ is a linear mapping from $\mathbb{R}^{n}$ to $\mathbb{R}^{1}$, so it must be expressed by a $1\times n$ [[Matrices|matrix]], that is, the $n$-tuple $\underline{b}$ in $\mathbb{R}^{n}$ which is the skeleton of $F$ is viewed as a matrix of one row and $n$ comumns


#Mathematics #LinAlg #Definition