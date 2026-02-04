## Relations
The inverse $R^{-1}$ of a [[Relations|relation]] $R$ is the set of [[Ordered Pairs|ordered pairs]] obtained by reversing those of $R$:
$$
R^{-1} = \left\{ (x,y)\mid(y,x)\in  R \right\}
$$
## Functions
If $f$ is a [[Functions|function]], then $f^{-1}$ is of course a relation, but in general it is not a function.
If $f:A\to B$ and $g:B\to A$ is such that [[Identity Map|$g\circ f=I_{A}$]], then we say that $g$ is a left inverse of $f$, and $f$ is a right inverse of $g$
### Equality of Left and Right Inverses
If the mapping $f:A\to B$ has both a right inverse $h$ and a left inverse $g$, they must necessarily be equal
#### Proof
This is algebraic juggling and in fact works for any associative operation e.g. the [[Groups|group]] operation
$$
h=I_{A}\circ  h=(g\circ f)\circ h=g\circ (f\circ h)=g\circ I_{B}=g
$$
___
### Inverse iff Bijective
In this case we call the uniquely determined map $g:B\to A$ such that $f\circ g=I_{B}$ and $g\circ f=I_{A}$ the inverse of $f$
A mapping $f:A\to B$ has an inverse if and only if it is [[Bijective Functions|bijective]], in which case, its inversse is it relational inverse $f^{-1}$
#### Proof
If $f$ is bijective, then the relational inverse $f^{-1}$ is a function from $B$ to $A$ and the equations $f\circ f^{-1}=I_{B}$ and $f^{-1}\circ f =I_{A}$ are obvious
On the other hand, if $f\circ g=I_{B}$, then $f$ is [[Surjective Functions|surjective]], since every $y$ in $B$ can be written $y=f(g(y))$. And if $g\circ f=I_{A}$, then $f$ is injective, for the equation k$f(x)=f(y)$ implies that $x=g(f(x))=g(f(y))=y$, thus $f$ is bijective if it has an inverse
___


![[Inverses of Functions 2024-10-15 14.13.37.excalidraw]]
Note that $\text{Ran}f^{-1}=\text{Dom}f,\text{Dom}f^{-1}=\text{Ran}f$, equivalently, $i=f^{-1}(x)\iff f(y)=x$
### Examples
For example, if
$$
f(x)=\frac{1}{3x-4}
$$
(which has domain $S=\mathbb{R}\setminus \{ \frac{4}{3}\}$) then
The graph of the inverse of a function $f^{-1}(x)$ is found by reflecting the graph of $f(x)$ in the line $y=x$

$$
f^{-1}(y)=\frac{1+4y}{3y}
$$
Often, we can find the inverse function by writing 
$$
y=f(x)
$$
and then rearranging so that $x$ is the subject
We can't always find the inverse of a function over a given domain. For example, $f(x)=x^{2}$ does not have an inverse over the whole [[Real Numbers|real]] line, because there are two $x$-values for each $y$-value. On the other hand, if we only look at the positive part of the real line, we can find an inverse: $f^{-1}(x)=\sqrt{ x }$

#Mathematics #Functions #Set #Definition