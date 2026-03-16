## Definition
The charge continuity is a universal law, so it must hold for all observers, it is
$$
\frac{ \partial \rho }{ \partial t } +\underline{\nabla} \cdot \underline{J} =0
$$
And has to be frame independent
We can express this as a [[tensors|tensor]] equation to make it compatable with [[special relativity|special relativity]] 
We know $x^{0}=ct$, so
$$
\frac{ \partial c\rho }{ \partial ct } +\underline{\nabla} \cdot \underline{J} =0 
$$
$$
\implies \frac{ \partial  }{ \partial x^{0} } c\rho+ \frac{ \partial  }{ \partial x^{1} } J^{1}+\frac{ \partial  }{ \partial x^{2} } J^{2}+\frac{ \partial  }{ \partial x^{3} } J^{3}=0
$$
Which kinda looks like the 4d divergence for a new quantity, so it is natural to define the space-time current:
$$
J^{\mu}=\begin{pmatrix}
c\rho \\
\underline{J}
\end{pmatrix}
$$
And thus the continuity equation reads as
$$
\partial_{\mu}J^{\mu}=0
$$
Since it holds in all frames, $J^{\mu}$ has to transform as a vector
## Physical Consequennes
There is a frame where we have no current in $R$:
$$
J^{\mu}=\begin{pmatrix}
c\rho \\
\overline{0}
\end{pmatrix}
$$
How does it look from a frame $R'$ moving with velocity $v_{x}$ along the $x$-axis:
$$
\Lambda_{x}(v)=\begin{pmatrix}
\gamma & -\frac{v_{x}}{c}\gamma & 0 & 0 \\
-\frac{v_{x}}{c}\gamma & \gamma & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix}
$$
So
$$
J^{\mu'}=(\Lambda_{x}(v))^{\mu}\,_{\nu}J^{\nu}=\begin{pmatrix}
\gamma c\rho \\
-\gamma \rho v_{x} \\
0 \\
0
\end{pmatrix}
$$
As usual with $\gamma=\frac{1}{\sqrt{ 1-\frac{v_{x}^{2}}{c^{2}} }}$
By comparison we could say that the moving observer $R'$ see a different density, $\rho'=\gamma \rho$ and $J_{x}$