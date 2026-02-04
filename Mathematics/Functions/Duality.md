Let $F:A\times B\to C$ be any [[Functions|function]] of two variables. It is obviou that if $x$ is held fixed, then $F(x,y)$ is a function of one variable $y$ 
That is, for each fixed $x$, there is a function $h^{x}:B\to C$ defined by 
$$
h^{x}(y)=F(x,y)
$$
Then $x\mapsto h^{x}$ is a mapping $\varphi$ of $A$ into [[Product Sets|$C^{B}$]] 
Similarly, each $y\in B$ yields a function $g_{y}\in C^{A}$, where 
$$
g_{y}(x)=F(x,y)
$$
and $y\mapsto g_{y}$ is a mapping $\theta$ from $B$ to $C^{A}$
Now suppose that conversely that we are given a mapping $\varphi:A\to C^{B}$. For each $x\in A$, we designate the corresponding value of $\varphi$ in index notation as $h^{x}$, so that $h^{x}$ is a function from $B$ to $C$, and we define $F:A\times B\to C$ by $F(x,y)=h^{x}(y)$. We are now back where we started
Thus the mappings $\varphi:A\to C^{B}$, $F:A\times B\to C$, and $\theta:B\to C^{A}$ are equivalent, and can be thought of as three different ways of viewing the same phenomenon
The extreme mappings $\varphi$ and $\theta$ will be said to be dual to each other
___
The mapping $\varphi$ is the [[Sets of Indices|indexed]] family of functions 
$$
\left\{ h^{x}\mid x\in  A \right\}\subset C^{B}
$$
Now suppose that $\mathfrak{F}\subset C^{B}$ is an unindexed collection of functions on $B$ into $C$, and define $F:\mathfrak{F}\times B\to C$ by $F(f,y)=f(y)$
Then $\theta:B\to C^{\mathfrak{F}}$ is defined by $g_{y}(f)=f(y)$
What is happening here is simply that in the expression $f(y)$ we regard both symbols as variables, so that $f(y)$ is a function on $\mathfrak{F}\times B$
Then, when we hold $y$ fixed, we have a function on $\mathfrak{F}$ mapping $\mathfrak{F}$ into $C$
___
It is sometimes awkward to invent new notation for the 'partial' function obtained by holding a variable fixed in a function of several variables, as we did above when we set $g_{y}(x)=F(x,y)$, so we frequently put a $\cdot$ in the position of the varying variable
Thus $F(a,\cdot)$ is the function of one variable obtained from $F(x,y)$ by holding $x$ fixed at the value $a$, so that from our above way of writing, we have
$$
h^{x}=F(x,\cdot),g_{y}=F(\cdot,y)
$$
If $f$ is a function of one variable, we can then write $f=f(\cdot)$ and so express the above equations also as $h^{x}(\cdot)=F(x,\cdot),g_{y}(\cdot)=F(\cdot,y)$
The flaw in this notation is that we can't indicate substitution without losing meaning. Thus the value of the function $F(x,\cdot)$ at $b$ is $F(x,b)$, but from this evaluation we cannot read backward and tell which function was evaluated
We are therefore forced to use some combersome notatation such as $F(x,\cdot)|_{b}$, which can get out of hand
Nevertheless, the dot devidce is often helpful when it can be used without evaluation difficulties
In addition to eliminating the need for temporary notation, it can also be used in situations where it is strictly speaking superfluous and obvious which is the position of the variable
## Examples
There are many important applications of this duality principle. For example, a real $m\times n$ [[Matrices|matrix]] is a function $\underline{t}=\left\{ t_{ij} \right\}$ in $\mathbb{R}^{\overline{m}\times \overline{n}}$. We picture this matrix as a rectangular array of numbers, where $i$ is the row index and $j$ is the column index, so that $t_{ij}$ is the number at the intersection of the $i$th row and $j$th column
If we hold $i$ fixed, we get the $n$-tuple of column $m$-tuples
In the same vein, an $n$-tuple $(f_{1},\dots,f_{n})$ of functions from $A$ to $B$ can be regarded as a single $n$-tuple-valued function from $A$ to $B^{\overline{n}}$,
$$
a\mapsto (f_{1}(a),\dots,f_{n}(a))
$$
___
In a somewhat different application, duality will allow us to regard a finite [[Dimension|dimensional]] [[Vectorspaces|vectorspace]] as being its own second conjugate space $(V^{*})^{*}$
___
It is instructive to look at elementary Euclidean geometry from this point of view; today we regard a straight line as being a set of geometric points; an older and more neutral view is to take points and lines to b two diffferent kinds of primitive objects
Accordingly, let $A$ be the set of all points (so that $A$ is the Euclidean plane as we view it in modern mathematics), and let $B$ be the set of all straight lines
Let $F$ be the incidence function: $F(p,l)=1$ if $p$ and $l$ are incident ($p$ lies on $l$, $l$ is on $p$) and $F(p,l)=0$ otherwise
Thus $F:A\times B\to \left\{ 0,1 \right\}$. Then for each $l\in B$, the function $g_{l}(p)=F(p,l)$ is the characteristic function of the set of points that we think of as being the line $l$ ($g_{l}(p)$ has the value $1$ if $p$ is on $l$)
But, dually, each point $p$ determines the set of lines $l$ on it, through its characteristic function $h^{p}(l)$. Thus, in complese duality, we can regard a line as being a set of points and a point as being a set of lines. This duality aspect of geometry is basic in projective geometry



#Mathematics #Set #Functions 