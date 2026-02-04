A function $f:D\to C$ is a map ($f$) from a [[Sets|set]] $D$ called the domain ($\text{Dom}f$), to a set $C$ called the codomain $\text{Codom}$f
For every $x\in D$, there is a unique $f(x)\in C$ called the [[Image|image]] of $x$ under $f$
Let $X$, $Y$ be sets, a function $f$ from $X$ to $Y$ is a [[Subsets|subset]] $f\subset X\times Y$ such that for every $x\in X$ there exists exactly one $y\in Y$ with $(x,y)\in f$
A way of expressing this is as follows:
$$
(x,y)\in  f\text{ and }(x,z)\in  f \implies y=z
$$
The $y$ which is thus uniquely determined by $f$ and $x$ is designated $f(x)$:
$$
y=f(x) \iff (x,y)\in  f
$$
We write $f:X\to Y$ for a function and write $f(x)$ for the unique element of $Y$ with $(x,f(x))\in f$

![[Functions 2024-10-08 14.39.36.excalidraw]]
We sometimes write:
$$
f:D\to C
$$
$$
x\mapsto f(x)
$$
Since we take $x$ and apply $f$ to it, we often call a function an operator
## Functions of a Single Real Variable
These are functions where the domain is $\mathbb{R}$, or a subset
## Real-Valued Functions
Real valued functions are functions where the codomain is $\mathbb{R}$ or a subset
## Examples
Consider a function $f:\mathbb{R}\to \mathbb{R}$ given by $f(x)=x^{2},\,\forall x\in\mathbb{R}$, so $\text{Dom}f=\mathbb{R}$, $\text{Codom}f=\mathbb{R}$, but $\text{Ran}f=[0,\infty)$ 
Here the codomain was a choice that could have been more restrictive, but having the codomain be $\mathbb{R}$, we can compose this function with other functions with domain $\mathbb{R}$
## Formal Dirichlet-Bourbaki Definition
A function $f:X\to Y$ is a subset of $X\times Y$ such that $(x,y_{1})\in f$ and $(x,y_{2})\in f$ implies $y_{1}=y_{2}$

#Mathematics #Functions #Definition
