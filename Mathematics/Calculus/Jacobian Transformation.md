To convert axes we might want to change the variables to new variables $u$ and $v$ given in the relations $x=g(u,v),y=h(u,v)$, the change of $dA$ is a multiple of a Jacobian:
$$
J(u,v)=\frac{ \partial (x,y) }{ \partial (u,v) } =\det\left(
\begin{matrix}
\frac{ \partial x }{ \partial u } &\frac{ \partial x }{ \partial v } \\
\frac{ \partial y }{ \partial u } & \frac{ \partial y }{ \partial v } 
\end{matrix} \right)=\frac{ \partial x }{ \partial u } \cdot \frac{ \partial y }{ \partial v } -\frac{ \partial x }{ \partial v } \cdot \frac{ \partial y }{ \partial u } 
$$
Note that to then use this to integrate, one needs to make sure the region becomes either $u$-simple or $v$-simple to perform an iterated integral
## Converting to polar
It is often useful to use polar coordinates instead of cartesian coordinates, especially when the region of integration is rotationally symmetric
$x=r\cos\theta$, $y=r\sin\theta$, $r^{2}=x^{2}+y^{2}$, $\frac{ \partial x }{ \partial \theta }=-r\sin\theta$, $\frac{ \partial x }{ \partial r }=\cos\theta$, $\frac{ \partial y }{ \partial \theta }=r\cos\theta$, $\frac{ \partial y }{ \partial r }=\sin\theta$
$$
J(\theta,r)=r\sin ^{2}\theta +r\cos ^{2}\theta=r(\sin ^{2}\theta+\cos ^{2}\theta)=r
$$


#Mathematics #Calculus 