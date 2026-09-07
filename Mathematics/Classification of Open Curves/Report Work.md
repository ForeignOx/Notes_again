# Abstract

# Mathematical Background
## Haar Wavelet Transform
Suppose we have a discrete [[Spacecurves|spacecurve]] with vertices
$$
x_{0},x_{1},\dots,x_{n}\in  \mathbb{R}^{3}
$$
and edge vectors
$$
e_{i}=x_{i+1}-x_{i}~~i=1,\dots,n-1
$$
Group the edges in pairs $(e_{1},e_{2}),(e_{2},e_{3}),\dots,(e_{n-1},e_{n})$ then for each pair define an average vector and a detail vector:
$$
a_{j}^{(1)}=\frac{1}{2}(e_{2j-1}+e_{2j})
$$
$$
 d_{j}^{(1)}=\frac{1}{2}(e_{2j-1}-e_{2j})
$$
For $j\in\left\{ 1,2,\dots,\frac{n}{2} \right\}$. So $a_{j}^{(1)}$ records the mean direction of the two edges, while $d_{j}^{(1)}$ records the direction that the average has deviated.
Equivalently we can write this in matrix form, 
$$
\begin{pmatrix}
a_{j}^{(1)} \\
d_{j}^{(1)} 
\end{pmatrix}=\begin{pmatrix}
1 & 1  \\
1 & -1 
\end{pmatrix}\begin{pmatrix}
e_{2j-1} \\
e_{2j}
\end{pmatrix}
$$
We can then repeat this process for our new edge set to get a second level of decomposition, and so on.
___
Suppose we have a sequence of curves $C(t_{1}),C(t_{2}),\dots,C(t_{T})$, with vertices at time $t_{\ell}$
$$
x_{0}(t_{\ell}),x_{1}(t_{\ell}),\dots,x_{n}(t_{\ell})
$$
$$
 e_{i}(t_{\ell})=x_{i}(t_{\ell})-x_{i-1}(t_{\ell})
$$Applying the Haar tranform to each frame give time-dependent detail coefficients coefficients:
$$
d_{j}^{(k)}(t_{\ell})
$$
These coefficients contain both the static hape of the molecule and its motion
The changes relative to a reference state are given by
$$
\Delta d_{j}^{(k)}(t)=d_{j}^{(k)}(t)-d_{j}^{(k)}(t_{0})
$$
Which measures the accumulated deformation relative to the starting frame,
Alternatively, for instantaneous motion, we can use coefficient velocities:
$$
\dot{d}_{j}^{(k)}(t_{\ell})\approx \frac{d_{j}^{(k)}(t_{\ell+1})-d_{j}^{(k)}(t_{\ell})}{t_{\ell+1}-t_{\ell}}
$$
        Which measure how the multiscale shape is changing at each time

# Findings
