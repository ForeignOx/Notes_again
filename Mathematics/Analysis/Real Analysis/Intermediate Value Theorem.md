This is often abbreviated to IVT, and states that if I have a [[Functions|function]] $f(x)$ which is [[Continuity|continuous]] on the [[Intervals|interval]] $[a,b]$ with $f(a)<f(b)$ (but works both ways...) pick $d\in[f(a),f(b)]$, then ther exists some number $c\in(a,b)$ such that $f(c)=d$
![[Intermediate Value Theorem 2024-10-22 14.24.01.excalidraw]]
One important application of the IVT is finding the zeros (roots) of a function. If $f$ is continuous on $[a,b]$ and $f(a)<0<f(b)$ then by the IVT it must go through zero somewhere in the interval there is at least one root such that $f(x)=0$
## Proof
Pick $d$, assume $d<f(b)$ (otherwice pick $c=b$) Define the [[Sets|set]]
$$
X:=\{ x\in [a,b]|f(x)\leq d \}
$$
So the set of all the points in $[a,b]$ that have $x$ coordinate of a point where $f(x)$ is less than $d$
$X\neq \emptyset$ since $a\in X$ and sibounded as is a subset of $[a,b]$. Hence by the [[Real Numbers#Completeness Axiom|completeness axiom]], has a [[Supremum and Infimum|supremum]], $c$. So there exists a [[Sequences|sequence]] $x_{n}\in X$ such that it [[Convergence|converges]] to $c$; $\lim_{ n \to \infty }x_{n}=c$. Hence, the limit also lies in this interval, so $c\in[a,b]$
By continuity,
$$
\lim_{ n \to \infty } f(x_{n})=f(\lim_{ n \to \infty } x_{n})=f(c)
$$
We claim $f(c)=d$
Assume not; i.e. $f(c)<d$ since $f(c)=\lim_{ n \to \infty }f(x_{n})$, and all $x_{n}\leq d$, then there exist a neighbourhood around $c$, $(c-\delta,c+\delta)\subset(a,b)$ such that $f(x)<d\forall x\in(x-\delta,c+\delta)$
![[Intermediate Value Theorem 2025-01-23 11.24.10.excalidraw]]
So in particular, $f\left( c+\frac{\delta}{2} \right)<d$, so $c+\frac{\delta}{2}\in X$, but $c+\frac{\delta}{2}>c$, but $c$ is the supremum of $X$, so $c+\frac{\delta}{2}$ cannot exist, we have a contradiction and the proof is proved yay!
## Corollary
$f:I\to \mathbb{R}$ is continuous on an interval $I$, then the [[Image|image]] of $f(I)$ is also an interval
### Proof
What is an interval? An interval $J$ is a set such that when $x<y\in J$, then all numbers in between are also in $y$, by that logic, applying the intermediate value theorem, letting $x=f(a),y=f(b)$, then we get that all numbers inbetween exist
## Examples
For example $f(x)=\sin x$ is continuous on $\left[ 0, \frac{\pi}{2} \right]$ and $f(0)<\frac{1}{2}<1=f\left( \frac{\pi}{2} \right)$, so by the intermediate value theorem there exists at least one $x\in\left( 0, \frac{\pi}{2} \right)$ such that $\sin x=\frac{1}{2}$
___
Note: we do require continuity for the IVT to apply, otherwise we might end up with something like this, consider the [[Sign Function|$y=\text{sign}(x)$]] 
$$
\text{sign}(x)=\begin{cases}
1&\text{if }x>0\\0&\text{if }x=0\\-1&\text{if }x<0
\end{cases}
$$
Then $f(x)=\frac{\text{sign}x}{1+x^{2}}$ has $f(-1)=-\frac{1}{2}$ and $f(1)=\frac{1}{2}$, but $\not \exists x\in(-1,1)$ such that $f(x)=\frac{1}{5}$ The IVT does not apply, as $f$ has a jump discontinuity at $x=0$
$$
L^-\lim_{ x \to 0^- }f(x) =-1
$$
$$
L^+\lim_{ x \to 0^+ } =1
$$
So $L^+\neq L^-$
___
$f(x)=x^{2}-2$ is continuous on $[1,2]$ with $f(1)=-1<0$ and $f(2)=2>0$ so the IVT tells me that there is at least one root of $x^{2}-2$ in $(1,2)$, iterating this, leads to the bisection method to find roots to arbitrary accuracy
___
$$
f(x)=\frac{x^{7}-25}{x(x-39)}
$$
This function is defined and continuous in $(0,39)$, $\lim_{ x \to 39^- }f(x)=-\infty$, $\lim_{ x \to 0^+ }f(x)=\infty$, so $f((0,39))=(-\infty,\infty)=\mathbb{R}$ by the corollary

#Mathematics #Analysis #Theorem