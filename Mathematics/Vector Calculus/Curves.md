## Definition
A curve $C$ is a 1-[[Dimension|dimensional]] [[Subsets|subset]] of [[Vectorspace Rn|$\mathbb{R}^{n}$]], for $n>1$.
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
A curve in $\mathbb{C}$ is said to be continuously differentiable, or $C^{1}$ if its real and imagynary parts are continuouslly differentiable on $[0,1]$
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
It is straightforward to see that $C^{1}$ curves are harder to find that their nomrmal versions. Consequently, if a set is $C^{1}$ path connected or piecewise $C^{1}$ connected
## Examples
