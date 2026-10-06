## Definition
A regular curve $C$ is a 1-[[Dimension|dimensional]] [[Subsets|subset]] of [[Vectorspace Rn|$\mathbb{R}^{n}$]], for $n>1$.
![[Curves 2025-10-07 11.21.35.excalidraw]]
We usually describe them by a parametrisation $\underline{x}(t)$:
$$
\underline{x}(t)=x_{1}(t)\underline{e}_{1}+x_{2}(t)\underline{e}_{2}+\dots+x_{n}(t)\underline{e}_{n}
$$
Which maps an [[Intervals|interval]] $[t_{0},t_{1}]$ to $\mathbb{R}^{n}$.
One can think of $\underline{x}(t)$ as the trajectory of a particle where $t$ is time.
A curve is closed if $\underline{x}(t_{1})=\underline{x}(t_{0})$.
A curve is simple if it doesn't intersect itself.
A curve is regular if it has at least one [[Differentiation#Remark|regular parametarisation]] 
An oriented curve is a curve together with a specified (consistent) choice of [[Unit Tangent Vectors|unit tangent vector]].
A curve is [[Smooth Functions|smooth]] if it is infinitely many times differentiable 
If a curve is a map $f:U\to \mathbb{R}^{n}$ with $U\subset \mathbb{R}^{m}$, then the restriction of the map $f$ to a subset $V\subset U$ is denoted by $f|_{V}:V\to \mathbb{R}^{n}$
## Examples
Find a parametrisation $\underline{x}(t)$ for the circle $x^{2}+y^{2}=a^{2}$ in $\mathbb{R}^{2}$.
![[Curves 2025-10-07 11.21.45.excalidraw]]
We can recall [[Polar Coordinates|polar coordinates]] which say that $x=r\cos\theta,y=r\sin\theta$, so 
$$
x^{2}+y^{2}=a^{2}\implies r^{2}(\cos ^{2}\theta+\sin ^{2}\theta)=a^{2}\implies r=a
$$
So we can set $t=\theta$ and obtain $\underline{x}(t)=a\cos t \underline{e}_{1}+a\sin t \underline{e}_{2}$ for $t\in[0,2\pi]$
___
Is the helix $\underline{x}(t)=\cos t \underline{e}_{1}+\sin t \underline{e}_{2}+t\underline{e}_{3}$ for $t\in[0,6\pi]$ closed? Or simple?
![[Curves 2025-10-07 11.27.40.excalidraw]]
$\underline{x}(0)=\underline{e}_{1},\underline{x}(6\pi)=\underline{e}_{1}+6\pi \underline{e}_{3}$, so it is not closed. It has no self-intersections, since the $z$-component is always different as $t$ varies, so the curve is simple.
___
Is the clover $\underline{x}(t)=\cos3t\cos t \underline{e}_{1}+\cos 3t \sin t \underline{e}_{2}$ for $t\in[0,\pi]$ closed? or simple?
![[Curves 2025-10-07 11.32.20.excalidraw]]
$\underline{x}(0)=\underline{e}_{1}$, $\underline{x}(\pi)=(-1)^{2}\underline{e}_{1}=\underline{e}_{1}$, so it is closed. It is not simple as there is a triple intersection at $\underline{x}= \underline{0}$ at $t=\frac{\pi}{6},\frac{\pi}{2},\frac{5\pi}{6}$
## Complex things
A curve in $\mathbb{C}$, sometimes described as a path is a [[Continuity|continuous]] function $\gamma:[0,1]\to \mathbb{C}$
We say that the curve starts at $z\in\mathbb{C}$ and ends at $w\in\mathbb{C}$ if $\gamma(0)=z,\gamma(1)=w$
A path $\gamma:[0,1]\to \mathbb{C}$ can be thought of as two functions from $[0,1]\to \mathbb{R}$, indeed:
$$
\gamma(t)=\mathfrak{R}(\gamma(t))+\mathfrak{I}(\gamma(t))
$$
## Definition
A curve in $\mathbb{C}$ is said to be continuously differentiable, or $C^{1}$ if its real and imaginary parts are continuouslly differentiable on $[0,1]$
At the end point $0$ and $1$, this means that real and imaginary parts have right-sided derivatives at $0$ and left-sided derivatives at $1$, and the derivatives are continuous from the right at $\hspace{0pt}0$ and from the left at 1
In that case, we define
$$
\gamma'(t):= (\mathfrak{R}(\gamma(t)))'+i(\mathfrak{I}(\gamma(t))')
$$
___
A curve in $\mathbb{C}$ is said to be a piecewise $C^{1}$ curve or a contour, if there exist
$$
0=a_{0}<a_{1}<\dots<a_{n-1}<a_{n}=1
$$
Such that the paths $\gamma_{i}:[a_{i-1},a_{i}]\to \mathbb{C}$ with $i=1,2,\dots,n$ defined by
$$
\gamma_{i}(t):=\gamma(t)\text{ for }i\in [a_{i-1},a_{i}]
$$
Are $C^{1}$ ($\gamma$ also has to be $C^{1}$ on every interval)
___
We say a subset $A\subseteq \mathbb{C}$ is $C^{1}$ [[Path Connectedness|path connected]] if for every pair of points $z,w\in A$ there exists a $C^{1}$ path that starts at $z$ and ends at $w$ such that $\gamma(t)\in A$ for all $t\in[0,1]$
___
We say that $A$ is piecewise $C^{1}$ path connected if for every pair of points $z,w\in A$ there exists a contour that starts at $z$ and ends at $w$ such that $\gamma(t)\in A$ for all $t\in[0,1]$
## Remark
It is straightforward to see that $C^{1}$ curves are harder to find that their normal versions. Consequently, if a set is $C^{1}$ path connected or piecewise $C^{1}$ connected
## Theorem
Let $\gamma:[a,b]\to \mathbb{C}$ be a path, and let $w\not\in \gamma$, then let $r(t)=\left| \gamma(t)-w \right|>0$ be the continuous function representing the distance from $\gamma(t)$ to $w$, then there exists a continuous function $\theta:[a,b]\to \mathbb{R}$ such that
$$
\gamma(t)=w+r(t)e^{ i\theta(t) }
$$
## Definition
A closed path $\gamma$ is simple if $\gamma(t_{1})=\gamma(t_{2})$ for some $t_{1}<t_{2}$ then $t_{1}=a,t_{2}=b$
(i.e. no self-crossing or backtracking allowed)
## Definition 
Let $I$ be an open interval and $\underline{\alpha}:I\to \mathbb{R}^{n}$ be a map. ($I$ can include $(a,b),(a,\infty),(-\infty,b),(-\infty,\infty)$) 
- We can write:
$$
\underline{\alpha}(u)=(\alpha_{1}(u),\alpha_{2}(u),\dots,\alpha_{n}(u))
$$
    Where $\alpha_{i}$ are the [[coordinates|coordinates]] in a given [[basis|basis]]. We call $\underline{\alpha}$ smooth if all component functions $\alpha_{i}$ are smooth maps
- The image $\underline{\alpha}(I)\subset \mathbb{R}^{n}$ of the interval $I$ under $\underline{\alpha}$ is called the trace of $\underline{\alpha}$
- We call the vector
$$
\underline{\alpha}'(u)=(\alpha_{1}'(u),\alpha_{2}'(u),\dots,\alpha_{n}'(u))\in \mathbb{R}^{n}
$$
    the tangent vector of $\underline{\alpha}$ at $u$ (where $'$ is derivative with respect to $u$)
- The curve $\underline{\alpha}$ is called regular if we have $\underline{\alpha}'(u)\neq 0$ $\forall u\in I$. The curve is singular at $u$ if $\underline{\alpha}'(u)=0$, the tangent vector of a the curve $\underline{\alpha}$ vanishes precisely at the singular points
- If $\underline{\alpha}$ is a regular curve, the unit tangent vector of $\underline{\alpha}$ at $u$ is defined as:
$$
\underline{t}_{\underline{\alpha}}(u)=\frac{\underline{\alpha}'(u)}{\lvert \lvert \underline{\alpha}'(u) \rvert \rvert }
$$
- If $\lvert \lvert \underline{\alpha}'(u) \rvert \rvert=1$ for all $u \in I$, we say that $\underline{\alpha}$ is a unit speed curve. Generally if $\lvert \lvert \underline{\alpha}'(u) \rvert \rvert=c$ for all $u\in I$, we say that $\underline{\alpha}$ is a constant speed curve
## Example
The unit circle $\underline{\alpha}:\mathbb{R}\to \mathbb{R}^{2}$, $\underline{\alpha}(u)=(\cos u,\sin u)$, the curve $\alpha$ is regular and unit speed. The trace of $\underline{\alpha}$ can be described as follows:
$$
\underline{\alpha}(\mathbb{R})=\underline{\alpha}([0,2\pi))=\left\{ \underline{x}\in \mathbb{R}:\middle|:\lvert \lvert \underline{x} \rvert \rvert =1 \right\}
$$
___
The helix $\underline{\alpha}:\mathbb{R}\to \mathbb{R}^{3}$ given by $\underline{\alpha}(u)=(\cos u,\sin  u,u)$, in this case we have $\underline{\alpha}'(u)=(-\sin u, \cos u,1)$, and therefore
$$
\lvert \lvert \underline{\alpha}'(u) \rvert \rvert =\sqrt{ \sin ^{2}u+\cos ^{2}u+1^{2} }=\sqrt{ 2 }
$$
Therefore $\underline{\alpha}$ is a constant speed wiith unit tangent vector
$$
\underline{t}(u)=\frac{\underline{\alpha}'(u)}{\lvert \lvert \underline{\alpha}'(u) \rvert \rvert }=\left( -\frac{\sin u}{\sqrt{ 2 }},\frac{\cos u}{\sqrt{ 2 }},\frac{1}{\sqrt{ 2 }} \right)
$$
___
The cusp $\underline{\alpha}:\mathbb{R}\to \mathbb{R}^{2},\underline{\alpha}(u)=(u^{3},u^{2})$, then $\underline{\alpha}$ is a smooth curve with $\underline{\alpha}'(u)=(3u^{2},2u)$. We have that $\underline{\alpha}'(u)=0$ iff $u=0$ and therefore $\underline{\alpha}$ is singular at $u=0$, so $\underline{\alpha}$ is smooth, but not regular
___
The node $\underline{\alpha}:\mathbb{R}\to \mathbb{R}^{2}$, $\underline{\alpha}(u)=(u^{3}-u,u^{2}-1)$, then $\underline{\alpha}(-1)=\underline{\alpha}(1)=(0,0)$, and $\underline{\alpha}'(u)=(3u^{2}-1,2u)$, which is never $\underline{0}$ for any value of $u\in \mathbb{R}$, so it is regular
These look like:
```desmos-graph
(t^3,t^2)|-10<t<10
(t^3-t,t^2-1)|-10<t<10

```



