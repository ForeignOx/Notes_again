A real function is a map, $f$, that associates a real number to every element of a [[Sets|set]] $S$. We call $S$ the domain of the function, and it can be any set: the real numbers, the unit [[Intervals|inverval]] $[0,1]$, and so on. For each number $x$ in $S$, we write $f(x)$ for the number assigned to $x$ by $f$.
For example, we can take $S$ to be tyhe [[Real Numbers|set of real numbers]], and $f(x)=2x^{2}+3$ for each $x \in\mathbb{R}$
Another example is to take $S=[0,4]$, and define $g$ in the following way:
$$
g(x)=\begin{cases}
x^{2}+3 &&\text{if } 0\leq x< 2\\
-x-2 &&\text{if } 2<x\leq 4\\
0&&\text{if }x=2
\end{cases}
$$
This is also a valid function: it defines a value for each $x\in[0,4]$. Note that we can't say what $g(5)$ is; it is not defined, because $\hspace{0pt}5$ is not in the domain of $g$
If we were to draw the graph of $g$, it would look like this:
![[Pasted image 20240925132418.png]]
If the domain of a function is not given, we take it to be the largest possible subset of $\mathbb{R}$
We call the set of values taken by the function its image. Using the notation of set theory, we say that the image is the set $I$ defined by:
$$
I=\{ y:y=f(x) \text{ for some }x\in S \}
$$
The image of our first function $f(x)=2x^{2}+3$ is the set of all $y$ such that $y\geq 3$. So we could write $I=\{ y : y\geq 3 \}$, or even $I=[3,\infty]$
The image of our second function is more complicated. Looking at the graph, the image of $g$ is $I=[-6,-4)\cup[3,7)\cup \{ 0 \}$

When we define a function, we often want to descrive the domain and image, as well as what the function does. We often use notation such as:
$$
f:S\to I
$$
$$
 x \mapsto 2x^{2}+3
$$
You should read this as "$f$ is defined as a function from $S$ to $I$, which assigns the value $2x^{2}+3$ to each $x$". This notation is helpful when we are defining more complicated functions: for example we could write
$$
f:\mathbb{R}^{2} \to \mathbb{R}
$$
$$
 (x,y)\mapsto x\sin(y)
$$
This defines a function which takes two real numbers as its inputs, $x$ and $y$, and produces $f(x,y)=x\sin (y)$

#Mathematics #Functions 