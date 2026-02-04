We want to simplify the method of showing that a [[Functions|function]] is [[Complex Functions|complex]] [[Differentiation|differentiable]] 
Recall we can write
$$
f(z)=\mathfrak{R}(f(z))+i\mathfrak{I}(f(z))
$$
Where $\mathfrak{R}(f(z))$ and $\mathfrak{I}(f(z))$ are functions from $\mathbb{C}$ to $\mathbb{R}$
Writing $z=x+iy$, the above can be reformulated as
$$
f(z)=f(x+iy)=u(x,y)+iv(x,y)
$$
We call $u$ the real part of $f$ and $v$ the imaginary part of $f$
Since $u$ and $v$ are functions from $\mathbb{R}^{2}$ to $\mathbb{R}$, we have a notion of partial derivatives and differentiability for them
Recall we define the partial derivatives as
$$
u_{x}(x,y)=\frac{ \partial u } { \partial x } (x,y)
$$
Where $h$ is a real number this time, is there a connection between differentiability of $u$ and $v$ and complex differentiability of $f$?
## Proposition
Let $f=u+iv$ be complex differentiable at $z_{0}=x_{0}+iy_{0}$. Then the real partial derivatives $u_{x},u_{y},v_{x},v_{y}$ exist at $(x_{0},y_{0})$ and satisfy the Cauchy-RIemann equations:
$$
u_{x}(x_{0},y_{0})=v_{y}(x_{0},y_{0}),~u_{y}(x_{0},y_{0})=-v_{x}(x_{0},y_{0})
$$
Furthermore, the derivative of $f$ at $z_{0}$ can be written as
$$
f'(z_{0})=u_{x}(z_{0})+iv_{x}(z_{0})=v_{y}(z_{0})-iu_{y}(z_{0})
$$
$$
= u_{x}(z_{0})-iu_{y}(z_{0})=v_{y}(z_{0})+iv_{x}(z_{0})
$$
Where we have used the shorthand notation $w(z_{0})=w(x_{0},y_{0})$ for functions from $\mathbb{R}^{2}$ to $\mathbb{R}$
### Proof
The proof relies on the realisation that since $\lim_{ h_{c} \to 0 } \frac{f(z_{0}+h_{c})-f(z_{0})}{h_{c}}$
$h_{c}$ can go to $\hspace{0pt}0$ in any complex way. Let's consider $\hspace{0pt}2$ ways, along $x$-axis and along the $y$-axis, we have that
$$
f'(z_{0})=\lim_{ h \to 0 }  \frac{f(z_{0}+ih)-f(z_{0})}{ih}=\lim_{ h \to 0 }  \frac{(u(x_{0},y_{0}+h)+iv(x_{0},y_{0}+h))-(u(x_{0},y_{0})+iv(x_{0},y_{0}))}{ih}
$$
$$
= \lim_{ h \to 0 } \left( -i \frac{u(x_{0},y_{0}+h)-u(x_{0},y_{0})}{h}+ \frac{v(x_{0},y_{0}+h)-v(x_{0},y_{0})}{h} \right)
$$
Since the limit exists, we have that
$$
\mathfrak{R}(f'(z_{0}))=\lim_{ h \to 0 }  \frac{v(x_{0},y_{0}+h)-v(x_{0},y_{0})}{h}
$$
$$
 \mathfrak{I}(f'(z_{0}))=-\lim_{ h \to 0 }  \frac{v(x_{0},y_{0}+h)-v(x_{0},y_{0})}{h}
$$
We conclude that the partial derivatives with repect to $y$ exist at $(x_{0},y_{0})$, and
$$
v_{y}(x_{0},y_{0})=\mathfrak{R}(f'(z_{0})),~u_{y}(x_{0},y_{0})=-\mathfrak{I}(f'(z_{0}))
$$
We can do the same sort of thing along the $x$-axis to get other stuff
___
Note that the proposition doesn't tell us when $f$ is complex differentiable, it tells us that if the equations do not hold, $f$ is not complex differentiable, so we want some converse to check whether things are complex differentiable
## Theorem
Let $f=u+iv$ be defined on an open subset $U$ of $\mathbb{C}$. Then $f$ is complex differentiable  at $z_{0}=x_{0}+iy_{0}\in U$ iff $u$ and $v$ are real differentiable at $(x_{0},y_{0})$ and the Cauchy Riemann equations are satisfied at this point.
Note that in the above, we have considered the set $U$ is a subset of $\mathbb{C}$ for $f$, and a subset of $\mathbb{R}^{2}$ for $u$ and $v$ at the same time. This has no ambiguity in it and we will continue to do so from now on
## Corollary
Let $f=u+iv$ be defined on an open subset $U$ of $\mathbb{C}$. Assume the patial derivatives $u_{x},u_{y},v_{x},v_{y}$ exist and are continuous, and satisfy the Cauchy-Riemann equations at $z_{0}\in U$, then $f$ is complex differentiable at $z_{0}$
## Examples
Let $f(z)=e^{ z }=e^{ x }\cos y+ie^{ x }\sin y$. Then
$$
u_{x}=e^{ x }\cos y,v_{y}=e^{ x }\cos y,~ u_{y}=-e^{ x }\sin y,v_{x}=e^{ x }\sin y
$$
Hence our Cauchy Riemann equations hold at every point and $e^{ z }$ is complex differentiable at any $z\in\mathbb{C}$
Moreover,
$$
f'(z)=u_{x}(z)+iv_{x}(z)=e^{ x }\cos y+ie^{ x }\sin y=e^{ x }+e^{ iy }=e^{ z }
$$
___
$f(z)=e^{ iz }$ is complex differentiable and $f'(z)=ie^{ iz }$. Consequently, by using COLT for derivatives, we find that the functions $\sin,\cos,\sinh,\cosh$ are differentiable everywhere in $\mathbb{C}$ and
$$
\sin'(z)=\cos(z),\cos'(z)=-\sin (z),\sinh'(z)=\cosh(z),\cosh'(z)=\sinh(z)
$$
___
Polynomials are complex differentiable on $\mathbb{C}$ with 
$$
(a_{n}z^{n}+\dots+a_{1}z+a_{0})'=na_{n}z^{n-1}+\dots+a_{1}
$$
___
Any beranch of $\log z$ on $\mathbb{C}\setminus \mathbb{R}_{\theta_{1}}$ is complex differentiable on $\mathbb{C}\setminus \mathbb{R}_{\theta}$ and 
$$
(\log z)'=\frac{1}{z}
$$
___






