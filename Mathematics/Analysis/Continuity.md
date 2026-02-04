## $\hspace{0pt}1$ Variable
### Example
If we change the value of $f(a)$ in an [[Exponential Functions|exponential]] [[Functions|function]]
![[Continuity 2024-10-15 14.48.21.excalidraw]]
Then [[limits|$\lim_{ x \to a }f(x)$]] still exists, and is still $L$, but we would no longer consider $f(x)$ as a continuous function; it has a discontinuity
In words continuity is saying that I can make the change in $f$ $\delta f=\left| f(x)-f(x_{0}) \right|$ as small as I lilke by choosing $x$ close to $x_{0}$
### Definition
A [[Functions|function]] is continuous at the point $a$ if:
- $f(a)$ exists
- $\lim_{ x \to a }f(x)$ exists
- $f(a)=\lim_{ x \to a }f(x)$
Or:
$$
\forall\varepsilon>0\exists\delta>0:\left| x-a \right| <\delta\implies\delta f=\left| f(x)-f(a) \right| <\varepsilon
$$
A function $f(x)$ is continuous on a [[Subsets|subset]] of its domain if it is continuous at all points in $S$
A function $f(x)$ is continuous if it is continuous at every point in its domain


### Remarks
Continuity is a "local" property only depending on the behavious of $f(x)$ in a (small) neighbourhood of $c$
we can define left and right continuity like before, which gives us a notion of continuity on a closed interval $[a,b]$
### Proposition
We get for free
$f(x)$ is continuous at $x=c\iff \lim_{ n \to \infty }f(x_{n})=f(\lim_{ n \to \infty }x_{n})=f(c)$
using the link to sequences

### Classification of Discontinuities
#### Right-Sided Limits
$f(x)$ has a right-sided limit $L^+$ as $x$ tends to $a$ from above:
$$
\lim_{ x \to a^+ } =L^+\iff \forall\varepsilon>0\exists\delta>0:|f(x)-L^+|<\varepsilon \forall x:0<x-a<\delta
$$
Note the lack of absolute value on the $0<x-a<\delta$
#### Left-Sided Limits
Similarly, $f(x)$ has a left-sided limit $L^-$ as $x$ tends to $a$ from below:
$$
\lim_{ x \to a^- } =L^+\iff \forall\varepsilon>0\exists\delta>0:|f(x)-L^-|<\varepsilon \forall x:0<a-x<\delta
$$
Note $L=\lim_{ x \to a }f(x)$ exists iff $L^+$ and $L^-$ both exist and $L^+=L^-$, thus $L=L^+=L^-$
Note that at the edge of an interval, one must perform a one-sided limit to show that the function is continuous over the interval
Using these definitions, there are three types of discontinuity:
###' Removable Discontinuity
$L$ exists but i$f(a)\neq L$. We can always "remove" the discontinuity in order to make a continuous function
$$
g(x)=\begin{cases}
f(x)&&\text{if }x\neq a\\L&&\text{if x=a}
\end{cases}
$$
#### Jump Discontinuity
$L^+$ and $L^-$ exist, but $L^+\neq L^-$
#### Infinite (Essential) Discontinuity
At least one of $L^+$ and $L^-$ don't exist 
### Facts about Continuity
- If $f$ and $g$ are continuous, then so are $(f+g)$, $(fg)$, $\left( \frac{f}{g} \right)$ and $|f|$
- All polynomial, rational, trigonometric and hyperbolic functions are continuous
- If $\lim_{ x \to a }g(x)=L$ and $f(x)$ is continuous at $x=L$, then $\lim_{ x \to a }(f(g(x)))=f(L)$
### Examples
$f(x)=L$; the constant function is continous as for a given $\varepsilon$, we can take $\delta$ to be anything, since
$$
\left| f(x)-L \right|=\left| L-L \right|=0<\delta \forall\delta>0
$$
___
$f(x)=x$ is continuous on $\mathbb{R}$. Given $\varepsilon>0$ can take $\delta=\varepsilon$, so if 
$$
\left| x-c \right| <\delta=\varepsilon
$$
Then
$$
\left| f(x)-f(c) \right| =\left| x-c \right| <\epsilon
$$
As required
___
Using $CoLT$ any $p(x)$ is a polynomial is continuous on $\mathbb{R}$, and similarly $\frac{p(x)}{q(x)}$ is continuous in the domain for $q(x)\neq 0$ 


___
Let:
$$
f(x)=\begin{cases}
x^{2}&&\text{if }-1\leq x<0\\1&&\text{if }x=0\\x^{2}&&\text{if }0< x\leq 1
\end{cases}
$$
![[Continuity 2024-10-17 14.10.59.excalidraw]]
Then $f(x)$ is continuous on $[-1,1]\setminus \{ 0 \}$, but not continuous at $x=0$ as $\lim_{ x \to 0 }f(x)=0\neq f(0)=1$
Thus this has a removable discontinuity at $x=0$, removing this gives the continuous function $g(x)=x^{2}$
___
$$
f(x)=\begin{cases}
1&&\text{if }x\leq 0\\x^{2}&&\text{if }x>0
\end{cases}
$$
![[Continuity 2024-10-17 14.14.30.excalidraw]]
is not continuous at $x=0$ as $\lim_{ x \to 0 }f(x)$ doesn't exist, as here $L^+=0$, $L^-=1$, so $L^+\neq L^-$ and no limit exists
___
$f(x)=\frac{1}{x}$ 
![[Continuity 2024-10-17 14.36.16.excalidraw]]
has an infinite discontinuity at $x=0$, in theis case, neither $L^+$ nor $L^{-}$ exists
___
$f(x)=\sin\left( \frac{1}{x} \right)$
![[Pasted image 20241018150942.png]]
Has an infinite discontinuity at $x=0$. Neither at $x=0$. Neither $L^{+}$ nor $L^{-}$ exists
The following are continuous:
$$
f(x)=2x^{3}+x+7,g(x)=\frac{3x}{x-1}
$$
even though $g(x)$ seems to have a discontinuity at $x=1$, but it is still considered continuous as $x=1$ is not in the domain of the function, similarly:
$$
h(x)=\left| \frac{1+x^{2}}{\sin x}\right|
$$
Is continuous
## Continuity for Functions of Many Variables
### Two Variables
For $f(x,y)$, where $f:D\to \mathbb{R}$, $D\subseteq \mathbb{R}^{2}$. $f(x,y)$ is continuous at $(x_{0},y_{0})$ iff
In words: I can make a change in $f$, $\delta f=\left| f(\underline{x})-f(\underline{x}_{0}) \right|$ as small as I like by choosing $\underline{x}$ to lie close enough to $\underline{x}_{0}$. Here we define what is close to be the [[Distance Between two Points|distance between two points]] as we might imagine: $\left| \underline{x}-\underline{x}_{0} \right|=\left| (x,y)-(x_{0},y_{0}) \right|=\sqrt{ (x-x_{0})^{2}+(y-y_{0})^{2} }$, what this does is essentially means there is a circle of radius $\delta$ of points around $x_{0}$ where the heights are within $\pm\varepsilon$ of $f(\underline{x}_{0})$
The proper definitions is:
$$
\forall\varepsilon>0,\exists\delta>0:\left| \underline{x}-\underline{x}_{0} \right| <\delta\implies\delta f=\left| f(\underline{x})-f(\underline{x}_{0}) \right| <\varepsilon
$$
#### Example
Show that $f(x,y)=x^{2}+y^{2}$ is continuous at $\underline{x}_{0}=(0,0)$
$$
\delta f=\left| f(\underline{x})-f(\underline{x}_{0}) \right| =\left| x^{2}+y^{2}-0 \right| =\left| \underline{x} \right| ^{2}=\left| \underline{x}-\underline{x}_{0} \right| ^{2}
$$
So if I choose $\left| \underline{x}-\underline{x}_{0} \right|<\delta\implies \left| f(\underline{x})-f(\underline{x}_{0}) \right|<\delta^{2}<\varepsilon$, so we choose $\delta^{2}<\varepsilon$
## Complex Continuity
Let $A\subseteq \mathbb{C}$. A map $f:A\to \mathbb{C}$ is called continuous at $z_{0}\in A$ if 
$$
(\forall\varepsilon>0)(\exists \delta>0):\left| z-z_{0} \right| <z,z\in  A\implies \left| f(z)-f(z_{0}) \right| <\varepsilon
$$
We say a function $f$ is continuous on a set $A\subseteq \mathbb{C}$ if it is continuou at every point in $A$
### Remark
We can recast the above in term of open balls:
A function $f:A\to \mathbb{C}$ is continuous at $z_{0}$ if
$$
(\forall\varepsilon>0)(\exists\delta>0): \forall z\in  B_{\delta}(z_{0})\cap A\implies f(z)\in B_{\varepsilon}(f(z_{0}))
$$
is automatically in $A$
Consequently, continuity at $z_{0}$ is equivalent to
$$
(\forall\varepsilon>0)(\exists\delta>0):\left| z-z_{0} \right| <\delta\implies \left| f(z)-f(z_{0}) \right| <\varepsilon
$$
While the condition $\left| z-z_{0} \right|<\delta$ and $z\in A$ feels clunky, it allows us to consider points in the set $A$ that do not lie in the interior of $A$
For instance the point $z=1$ which is not inthe interior of $A=\overline{B}_{1}(0)$. Thi is similar to us discussing the continuity of a real function on the interval $[a,b]$ at the point $a$ or $b$. This demonstrates that in complex analysis there can be no sense of left and right continuity
___
### Continuity via Sequences
Similarly for real numbers we define continuity by sequences
A function $f:A\to \mathbb{C}$ is continuous at $z_{0}\in A$ iff
$$
\lim_{ n \to \infty } f(z_{n})=f(z_{0})
$$
for every sequence $\left\{ z_{n} \right\}_{n\in\mathbb{N}}$ in $A$ such that $\lim_{ n \to \infty }z_{n}=z_{0}$
___
We usually use this to show lack of continuity (and in fact, lack of limit)
If we find $\left\{ z_{n} \right\},\left\{ w_{n} \right\}$ which converge to $z_{0}$, but such that $f(z_{n})\to l_{1}$ and $f(w_{n})\to l_{2}$ and $l_{1}\neq l_{2}$, then $f$ is not continuous at $z_{0}$
### Examples
The following functions are continuous on $\mathbb{C}$:
- $f(z)=z$
- $f(z)=c,c\in\mathbb{C}$
- $f(z)=\mathfrak{R}(z),f(z)=\mathfrak{I}(z),f(z)=\left| z \right|$
- $f(z)=\overline{z}$
- $f(z)=z^{n}$, consequently polynomials are continuous
- $f(z)=e^{ z }$ and consequently $\sin z,\cos z,\sinh z,\cosh z$
For any $\theta_{1}<\theta_{2}$ such that $\theta_{2}-\theta_{1}=2\pi$, the argument associated to $(\theta_{1},\theta_{2}]$ is not continuous on $\mathbb{C}^{*}=\mathbb{C}\setminus \left\{ 0 \right\}$ this is due to a jump discontinuity at $R_{\theta_{1}}$, the [[Rays|ray]] at $\theta_{1}$. It is continuous on $\mathbb{C}\setminus R_{\theta_{1}}$
Similarly any branch of $\log z$ is continuous on $\mathbb{C}\setminus R_{\theta_{1}}$, the branch cut
___
Much like sequences, we can frame continuity in a topological sense:
### Continuity via Open Sets
Let $A\subseteq \mathbb{C}$ be an [[Open Sets|open set]] and let $f:A\to \mathbb{C}$ be a given map. Then the following are equivalent
- $f$ is continuous
- $f^{-1}(U)$ is an open set for every open set $U\subseteq \mathbb{C}$
- $f^{-1}(F)$ is a closed set for every closed set $F\subseteq \mathbb{C}$
### Remark
It might seem odd that the set we investivgate, $A$, is open. This is to avoid issues where the [[Image|preimage]] of a set omehow lands on the boundary of $A$. It is possible to define being open relative to $A$, at which the above theorem holds
We can use this theorem to classify sets!
- For any $z_{0}\in\mathbb{C}$, $\left\{ z_{0} \right\}$ is closed, so if $f$ is continuous, then $f^{-1}(\left\{ z_{0} \right\})$ is closed
For example
$$
\left\{ z\in \mathbb{C}:\middle|: \left| z \right| =1 \right\}
$$
ehh
stuff
### Remark
SImilarly to the above statement, we can find a criterion to continuity at a point that is given completely by open sets:
Let 



#Mathematics #Analysis #Definition