## Definition
A [[Transformations of Configuration Spaces|transformation]] $q_{i}\to \phi_{i}$ is a symmetry if there exists some [[Functions|function]] $F(\underline{q},t)$ such that
$$
\delta L=L'(\phi_{1},\dots,\phi_{N})-L(q_{1},\dots,q_{N})=\varepsilon \frac{d F(\underline{q},t)}{dt} +\mathcal{O}(\varepsilon^{2})
$$
## Remark
If some $F(\underline{q},t)$ exists such that the transformation is a symmetry, then $F+c$ with $c$ a constant also makes the transformation a symmetry, in fact, for the transformation to be a symmetry, this has to hold without the equations of motion
## Example
Any system with [[Ignorable Coordinates|ignorable coordinates]] is a symmetry, for instance a mass on a spring:
$$
L=\frac{1}{2}m(\dot{r}^{2}+r^{2}\dot{\theta}^{2})-\frac{1}{2}\kappa r^{2}
$$
Here we have that $\theta$ is ignorable, so the system has a symmetry:
$$
r\to r'=r,~ \dot{r}\to  \dot{r}'= \dot{r}
$$
$$
 \theta \to\theta'=\theta+\varepsilon,~ \dot{\theta}\to \dot{\theta}'=\dot{\theta}
$$
This means
$$
L\to L'(\dot{r}',\dot{\theta}',r',\theta')=L(\dot{r},\dot{\theta},r,\theta+\varepsilon)=L(\dot{r},\dot{\theta},r,\theta)
$$
We can also do this in Cartesian coordinates:
$$
L=\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2})-\frac{1}{2}\kappa (x^{2}+y^{2})\to L'(\dot{x}',\dot{y}',x',y')
$$
$$
\begin{pmatrix}
x \\
y 
\end{pmatrix}\to \begin{pmatrix}
x' \\
y'
\end{pmatrix}=\begin{pmatrix}
\cos\varepsilon & -\sin\varepsilon \\
\sin\varepsilon & \cos\varepsilon
\end{pmatrix}\begin{pmatrix}
x \\
y
\end{pmatrix}
$$
$$
\implies x'=\cos\varepsilon x-\sin\varepsilon y = x-\varepsilon y+\dots ,~ y'=\sin\varepsilon x+\cos\varepsilon y=\varepsilon x+y+\dots

$$
$$
\dot{x}'=\dot{x}-\varepsilon \dot{y}+\dots,~\dot{y}'=\varepsilon \dot{x}+\dot{y}+\dots
$$
Sooo
$$
L'=\frac{1}{2}m(\dot{x}'^{2}+\dot{y}'^{2})-\frac{1}{2}\kappa(x'^{2}+y'^{2})
$$
$$
= \frac{1}{2}m((\dot{x}-\varepsilon \dot{y})^{2}+(\dot{y}+\varepsilon \dot{x})^{2})-\frac{1}{2}\kappa((x-\varepsilon y)^{2}+(y+\varepsilon x)^{2})
$$
$$
= \frac{1}{2} m(\dot{x}^{2}-2\dot{x}\dot{y}\varepsilon+\varepsilon^{2}\dot{x}^{2}+\dot{y}^{2}+2\dot{x}\dot{y}\varepsilon+\varepsilon^{2}\dot{y}^{2})-\frac{1}{2}\kappa(x^{2}-2xy\varepsilon+\varepsilon^{2}x+y^{2}+2xy\varepsilon+\varepsilon^{2}y^{2})
$$
$$
= \frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2}+\mathcal{O}(\varepsilon^{2}))-\frac{1}{2}\kappa(x^{2}+y^{2}+\mathcal{O}(\varepsilon^{2}))
$$
___
Consider the lagrangian:
$$
L=\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2})-y\dot{x}-\frac{1}{2}x^{2}
$$
We claim $x\to x'=x,y\to y'=y+\varepsilon$ is a symmetry:
$$
L\to \frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2})-(y+\varepsilon)\dot{x}-\frac{1}{2}x^{2}=L-\varepsilon \dot{x}=L+\varepsilon \frac{d F(x,y,t)}{dt} 
$$
With for example $F=-x$