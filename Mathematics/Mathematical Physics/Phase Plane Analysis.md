The [[Hamiltonian|Hamiltonian]] analogue to [[Normal Modes|normal mode]] techniques is phase plane analysis and helps develop intuition for the behavior of dynamic systems
This generalises to arbitrary numbers of dimensions, but to aid visualisation, we'll consider systems with $\hspace{0pt}1$ degree of freedom where [[Phase Spaces|phase space]] is 2-dimensional and can be parametrised by a single coordinate $q$ with associated [[Generalised Momentum|generalised momentum]] $p$.
Recall that each point in space fully specifies all the data needed to determine the time evolution of the system. So if we know that at time $t=t_{0}$ the system is at $(q(t_{0}),p(t_{0}))$ in phase space, then we can fully determine the values of $(q(t),p(t))$ for all $t$, this is known as the [[State Trajectories|state trajectory]].
## Example
Consider a pendulum, its Lagrangian is given by
$$
L=\frac{1}{2}m\ell^{2}\dot{\theta}^{2}+mg\ell \cos\theta
$$
So the [[Hamiltonian|Hamiltonian]] is 
$$
H=\frac{1}{2m\ell^{2}}p_{\theta}^{2}-mg\ell \cos\theta
$$
Giving rise to Hamilton's equations:
$$
\dot{\theta}=\frac{ \partial H }{ \partial p_{\theta} } =\frac{1}{m\ell^{2}}p_{\theta}
$$
$$
 \dot{p}_{\theta}=-\frac{ \partial H }{ \partial \theta } =-mg\ell \sin\theta
$$
Clearly $\theta=p_{\theta}=0$ is an equilibrium point of this system
Computing the state trajectories amounts to solving Hamilton's equations for arbitrary initial condition, which is equivalent to solving the [[Euler-Lagrange Equations|Euler Lagrange equations]] for the system
In this case we still cannot find a solution in terms of elementary functions, but as we do when considering normal modes, we can understand the bahaviour around the equilibrium point for small oscillarions by linearising the problem
## Method
Consider a system with equilibrium point $(q,p)=(0,0)$ (One can always place any equilibrium point of interest at the origin by redefining coordinates if necessary)
The fact that there is an equilibrium point at the origin implies that when we expand $\frac{ \partial H }{ \partial q }$ and $\frac{ \partial H }{ \partial p }$ around the origin, we have no constant term in the [[Taylor Series|Taylor expansion]]:
$$
\frac{ \partial H }{ \partial p } =aq+bp+\dots ,~-\frac{ \partial H }{ \partial q } =cq+dp+\dots
$$
For some constant real numbers $a,b,c,d$, which in the case of Hamilton's equations,
$$
a=-d=\frac{ \partial^{2}H }{ \partial p\partial q }\Bigg{|}_{(0.0)} ,~b=\frac{ \partial^{2}H }{ \partial p^{2} }\Bigg{|}_{(0,0)}  ,~c=\frac{ \partial^{2}H }{ \partial q^{2} } \Bigg{|}_{(0,0)}  
$$
But phase plane analysis extends beyond Hamiltonian systems, so we'll leave them as generic numbers which we write in Matrix form
$$
\frac{d}{dt}\begin{pmatrix}
q \\
p
\end{pmatrix}=A\begin{pmatrix}
q \\
p
\end{pmatrix}
$$
Where
$$
A:=\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$
We can solve this system very similarly to how we solved normal modes problems; dente by $\lambda_{1}$ and $\lambda_{2}$ the two [[Eigenvalues|eigenvalues]] of $A$, which we will assume to be distinct for simplicity, and $\underline{v}_{1},\underline{v}_{2}$ to be corresponding [[eigenvectors|eigenvectors]]
Then the general solution of the linear system is
$$
\begin{pmatrix}
q(t) \\
p(t)
\end{pmatrix}=C_{1}e^{ \lambda_{1} t }\underline{v}_{1}+C_{2}e^{ \lambda_{2}t }\underline{v}_{2}
$$
Where $C_{1},C_{2}$ are constants that depend on the initial conditions
## Example
If we continue the pendulum example and study small oscillations around the equilibrium point, we have an effective [[Linear|linear]] Hamiltonian system given by
$$
\dot{\theta}=\frac{1}{m\ell^{2}}p_{\theta},~\dot{p}_{\theta}=-mg\ell\theta
$$
Using $\sin\theta \approx \theta$ for $\left| \theta \right|\ll 1$, our matrix $A$ is therefore
$$
A=\begin{pmatrix}
0 & \frac{1}{m\ell^{2}} \\
-mg\ell & 0
\end{pmatrix}
$$
This matrix has purely imaginary eigenvalues $\lambda_{1}=i\sqrt{ \frac{g}{\ell} },\lambda_{2}=-\\i\sqrt{ g\ell }$ with corresponding eige vectors
$$
\underline{v}_{1}=\begin{pmatrix}
1 \\
\text{im}(\sqrt{ \ell^{3} }g)
\end{pmatrix},~\underline{v}_{2}=\begin{pmatrix}
1 \\
-\text{im}(\sqrt{ \ell^{3}g })
\end{pmatrix}
$$
Since $\theta$ and $p_{{\theta}}$ are real, it is more consistent to write $e^{ \lambda_{1}t }$ and $e^{ \lambda_{2}t }$ in terms of sines and cosines:
$$
e^{ \lambda_{1}t }\underline{v}_{1}=\begin{pmatrix}
\cos(\omega t) \\
-m\ell^{2}\omega \sin(\omega t)
\end{pmatrix}+i\begin{pmatrix}
\sin(\omega t) \\
m\ell^{2}\omega \cos(\omega t)
\end{pmatrix}
$$
Where we have defined $\omega:=\sqrt{  \frac{g}{\ell} }$ and 
$$
e^{ \lambda_{2} t}\underline{v}_{2}=\overline{e^{ \lambda_{1}t }\underline{v}_{2}}=\begin{pmatrix}
\cos(\omega t) \\
-m\ell\omega \sin(\omega t)
\end{pmatrix}-i\begin{pmatrix}
\sin(\omega t) \\
m\ell^{2}\omega \cos(\omega t)
\end{pmatrix}
$$
Our system of differential equations is real and linear, so the real and imaginary components of these expressions are solutions of the equations of motion themselves and we finally find
$$
\begin{pmatrix}
q \\
p 
\end{pmatrix}=c_{1}\begin{pmatrix}
\cos(\omega t) \\
-m\ell^{2}\omega \sin(\omega t)
\end{pmatrix}+c_{2}\begin{pmatrix}
\sin(\omega t) \\
m\ell^{2}\omega \cos(\omega t)
\end{pmatrix}
$$
With $c_{1}$ and $c_{2}$ depending on the initial condition of the system, or in terms of amplitude $\mathcal{A}$ and a phase delay $\phi$
$$
\begin{pmatrix}
q \\
p 
\end{pmatrix}=\mathcal{A}\begin{pmatrix}
\cos(\omega t+\phi) \\
-m\ell^{2}\omega \sin(\omega t+\phi)
\end{pmatrix}
$$
With $c_{1}=\mathcal{A}\cos(\phi),c_{2}=\mathcal{A}\sin(\phi)$
So we see that the [[Phase Portrait|phase portrait]] of the pendulum, in the approximation of small oscillations is given by concentric ellipses in phase space
___
Note that similar to normal nodes, other possibilites exist depending on the eigenvalues of $$