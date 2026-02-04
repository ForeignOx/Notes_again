## Canonical Kintic Terms
Assuming to start that we have a Lagrangian
$$
L=\left( \frac{1}{2}\sum_{i=1}^{N}\dot{q}_{i}^{2} \right)-V(\underline{q})
$$
We want to expand around an extremum of $V(\underline{q})$
$$
\frac{ \partial V }{ \partial q_{i} } \Bigg{|}_{\underline{q}=0} =0\forall i
$$By redefining $\underline{q}$ we can put this point at $\underline{q}$, to make this first order in $\underline{q}$, we have
$$
    \underline{\ddot{q}}+A\underline{q}=0
$$
With
$$
A_{ij}:=\frac{ \partial^{2}V }{ \partial q_{i}\partial q_{j} }\Bigg{|}_{\underline{q}=0}  
$$
We expect a $2N$ dimensional space of solution
$A$ is a real $N\times N$ [[Symmetric and Anti-Symmetric Matrices|symmetric]] [[Matrices|matrix]], so it has $N$ independent [[Eigenvectors|eigenvectors]] $\underline{v}_{\lambda}:A\underline{v}_{\lambda_{i}}=\lambda_{i}\underline{v}_{\lambda_{i}}$
We assume solutions of the form
$$
\underline{q}(t)=\underline{v}_{\lambda_{i}}f_{\lambda(t)}
$$
$$
\implies \left( \frac{d ^{2}}{dt^{2}} +A \right)\underline{q}(t)=\underline{v}_{\lambda_{i}}\frac{d ^{2} f_{\lambda_{i}}}{dt^{2}} +f_{\lambda_{i}}(t[A\underline{v}_{\lambda_{i}}])
$$
$$
= \underline{v}_{\lambda_{i}}\left( \frac{d ^{2}f_{\lambda_{i}}}{dt^{2}} +\lambda_{i}f_{\lambda_{i}} \right)=0
$$
Note that $\underline{v}_{\lambda_{i}}\neq 0$ and are [[Linear Independence|linearly independent]]
$$
\iff \frac{d ^{2}f_{\lambda_{i}}(t)}{dt^{2}} +\lambda_{i}f_{\lambda_{i}}(t)=0
$$
$$
\implies f_{\lambda_{i}}(t)=\begin{cases}
\alpha_{i}\cos(\sqrt{ \lambda_{i} }t)+\beta_{i}\sin(\sqrt{ \lambda_{i} }t) & \lambda_{i}>0 \\
\alpha_{i}\cosh(\sqrt{ -\lambda_{i} }t)+\beta_{i}\sinh(\sqrt{ -\lambda_{i} }t) & \lambda_{i}<0 \\
C_{i}+D_{i}t & \lambda_{i}=0
\end{cases}

$$
So in general
$$
\underline{q}(t)=\sum_{\lambda_{i}>0}\underline{v}_{\lambda_{i}}(\alpha_{i}\cos(\sqrt{ \lambda_{i} }t)+\beta_{i}\sin(\sqrt{ \lambda_{i} }t))
$$
$$
 +\sum_{\lambda_{i}<0}\underline{v}_{\lambda_{i}}(\alpha_{i}\cosh(\sqrt{ -\lambda_{i} }t)+\beta_{i}\sinh(\sqrt{ -\lambda_{i} }t)+\sum_{\lambda_{i}=0}\underline{v}_{\lambda_{i}}(C_{i}+D_{i}t)
$$
We can understand these by thinking of different graphs of $V$:
![[stuff 2026-01-21 10.26.21.excalidraw]]
![[stuff 2026-01-21 10.26.55.excalidraw]]
We call the case where $\lambda_{i}>0$ normal modes, $\lambda_{i}<0$ instabilities
If $\lambda_{i}=0$, we call a zero mode it is pretty flat, so the "oscillations" are indication of some symmetry of the system
### Example
If $L=\frac{1}{2}m(\dot{x}^{2}_{1}+\dot{x}_{2}^{2})-V(x_{1}-x_{2})$
With a potential invariant under $x_{1}\to x_{1}+c,x_{2}\to x_{2}+c$
If we introduce coordinates
$$
x_{+}:= \frac{1}{\sqrt{ 2 }}(x_{1}+x_{2})
$$
$$
 x_{-}:= \frac{1}{\sqrt{ 2 }}(x_{1}-x_{2})
$$
Then in these coordinates,
$$
L=\frac{1}{2}m(\dot{x}_{+}^{2}+\dot{x}_{-}^{2})-V(x_{-})
$$
$$
\implies A=\begin{pmatrix}
 \frac{ \partial^{2}V }{ \partial x_{+}^{2} } & \frac{ \partial^{2}V }{ \partial x_{+}\partial x_{-} }   \\
 \frac{ \partial^{2}V }{ \partial x_{-}\partial x_{+} }  &  \frac{ \partial^{2}V }{ \partial x_{-}^{2} }
\end{pmatrix}=\begin{pmatrix}
0 & 0 \\
0 & \frac{ \partial^{2}V }{ \partial x_{-}^{2} } 
\end{pmatrix}

$$
So the eigenvalues of $A$ are $\lambda_{1}=0$, the zero mode and $\lambda_{2}=\frac{ \partial^{2}V }{ \partial x_{-}^{2} }$ 
___
Say we have two pendula attached witha a spring with natural length $d$ and spring constant $\kappa$
![[stuff 2026-01-21 10.40.52.excalidraw]]
So we have coordinates $\theta_{1},\theta_{2}$, $L=T-V$,
$$
T=T_{1}+T_{2}=\frac{1}{2}(\dot{x}_{1}^{2}+\dot{y}_{1}^{2})+\frac{1}{2}(\dot{x}_{2}^{2}+\dot{y}_{2}^{2})
$$
Where particle $\hspace{0pt}1$ has position $(x_{1},y_{1})=(\sin\theta_{1},-\cos\theta_{1})$ and particle $\hspace{0pt}2$ has position $(x_{2},y_{2})=(d+\sin\theta_{2},-\cos\theta_{2})$, hence
$$
\dot{x}_{1}=\cos(\theta_{1})\dot{\theta}_{1},~\dot{y}_{1}=\sin(\theta_{1})\dot{\theta}_{1}
$$
$$
 \dot{x}_{2}=\cos(\theta_{2})\dot{\theta}_{2},~\dot{y}_{2}=\sin(\theta_{2})\dot{\theta}_{2}
$$
And 
$$
V=V^{1}_\text{gravitational}+V^{2}_\text{gravitational}+V_\text{spring}
$$
$$
= m_{1}gy_{1}+m_{2}gy_{2}-\frac{1}{2}\kappa(\text{extension}-d)^{2}
$$
$$
= -g\cos(\theta_{1})-g\cos(\theta_{2})-\frac{1}{2}\kappa (\left| \underline{x}_{1}-\underline{x}_{2} \right| -d^{2})
$$
And
$$
\left| \underline{x}_{1}-\underline{x}_{2} \right| =\sqrt{ (x_{1}-x_{2})^{2}+(y_{1}-y_{2})^{2} }=\sqrt{ (\sin(\theta_{1})-d-\sin(\theta_{2}))^{2}+(\cos\theta_{2}-\cos\theta_{1})^{2} }
$$
$$
L=\frac{1}{2}(\dot{\theta}_{1}^{2}+\dot{\theta}_{2}^{2})+g\cos(\theta_{1})+g\cos(\theta_{2})-\frac{1}{2}\kappa (\sqrt{ (\sin(\theta_{1})-d-\sin(\theta_{2}))^{2}+(\cos(\theta_{2})-\cos(\theta_{1}))^{2} }-d^{2})
$$
Using small angle approximations, we get that
$$
L\approx \frac{1}{2}(\dot{\theta}^{2}_{1}+\dot{\theta}^{2}_{2})+g\left( 1-\frac{\theta_{1}^{2}}{2} \right)+g\left( 1-\frac{\theta_{2}^{2}}{2} \right)-\frac{1}{2}\kappa(\theta_{1}^{2}-\theta_{2}^{2})
$$
Dropping constant terms:
$$
\cong \frac{1}{2}(\dot{\theta}^{2}_{1}+\dot{\theta}_{2}^{2})-\frac{g}{2}\theta_{1}^{2}-\frac{g}{2}\theta_{2}^{2}-\frac{1}{2}\kappa(\theta_{1}^{2}-\theta_{2}^{2})
$$
We write the Euler-Lagrange equations:
$$
0=\frac{d }{dt} \left( \frac{ \partial L }{ \partial \dot{\theta}_{1} }  \right)-\frac{ \partial L }{ \partial \theta_{1} } =\ddot{\theta}-(-g\theta_{1}-\kappa\theta_{1}+\kappa\theta_{2})  =\ddot{\theta}+g\theta_{1}+\kappa(\theta_{1}-\theta_{2})
$$
$$
0=\frac{d}{dt} \left( \frac{ \partial L }{ \partial \dot{\theta}_{2} }  \right)-\frac{ \partial L }{ \partial \theta_{2} } = \ddot{\theta}_{2}-(-g\theta_{2}-\kappa\theta_{2}+\kappa\theta_{1})= \ddot{\theta}_{2}+g\theta_{2}+\kappa(\theta_{2}-\theta_{1})
$$
We use 
$$
\underline{q}=\begin{pmatrix}
\theta_{1} \\
\theta_{2}
\end{pmatrix}
$$
To rewrite this in the form
$$
\underline{\ddot{q}}+A\underline{q}=0 \iff \begin{pmatrix}
\ddot{\theta}_{1} \\
\ddot{\theta}_{2}
\end{pmatrix}+\begin{pmatrix}
A_{11} & A_{12} \\
A_{21} & A_{22}
\end{pmatrix}\begin{pmatrix}
\theta_{1} \\
\theta_{2} 
\end{pmatrix}=0
$$
$$
\implies A=\begin{pmatrix}
g+\kappa & -\kappa \\
-\kappa & g+\kappa
\end{pmatrix}

$$
So now we want eigenvalues, so we want to find solutions to
$$
\det(A-\lambda I)=0 
$$
$$
\implies \det \begin{pmatrix}
g+\kappa-\lambda & -\kappa \\
-\kappa & g+\kappa-\lambda 
\end{pmatrix}=(g+\kappa-\lambda)^{2}-\kappa^{2}
$$
$$
= \lambda^{2}-2(g+\kappa)\lambda+(g+\kappa)^{2}-\kappa^{2} = \lambda^{2}-2\lambda(g+\kappa)+g^{2}+2g\kappa 
$$
$$
\implies \lambda_{\pm}= \frac{2(g+\kappa)\pm \sqrt{ 4(g+\kappa)^{2}-4(g^{2}+2g\kappa) }}{2}
$$
$$
= g+\kappa\pm \kappa
$$
So
$$
\lambda_{1}=g+2\kappa,~\lambda_{2}=g
$$
So using
$$
A\underline{v}_{i}=\lambda_{i}\underline{v}_{i}
$$
$$
 \begin{pmatrix}
g+\kappa & -\kappa \\
-\kappa & g+\kappa 
\end{pmatrix}\begin{pmatrix}
v_{1} \\
v_{2} 
\end{pmatrix}=\begin{pmatrix}
0 \\
0
\end{pmatrix}
$$
$$
\implies v_{\lambda_{1}} =\begin{pmatrix}
1 \\
-1
\end{pmatrix},~v_{\lambda_{2}}=\begin{pmatrix}
1 \\
1
\end{pmatrix}
$$
So now we can get 
$$
\underline{q}(t)=\begin{pmatrix}
1 \\
-1 
\end{pmatrix}(\alpha_{1}\cos(\sqrt{ g+2\kappa }t)+\beta_{1}\sin(\sqrt{ g+2\kappa }t))+\begin{pmatrix}
1 \\
1
\end{pmatrix}(\alpha_{2}\cos(\sqrt{ g }t)+\beta_{2}\sin(\sqrt{ g }t))
$$
Which is a combination of two normal modes, the $(1,1)$ mode describes the motion of the two particles in the same direction together, and the $(1,-1)$ mode describes the motion of the two particles towards each other
Assume that at $t=0$, we release the masses from rest from
$$
\begin{pmatrix}
\theta_{1}(t=0) \\
\theta_{2}(t=0) 
\end{pmatrix}=\begin{pmatrix}
\delta \\
-\delta
\end{pmatrix}
$$
Since it is at rest
## Non-Canonical Kinetic Terms
Finally, we consider configurations with non-canonical kinetic terms of the form
$$
L=\frac{1}{2}\sum_{i,j}B_{ij}(q)\dot{q}_{i}\dot{q}_{j}-V(q)
$$
We still obtain a linear differential operator if we restrict $B(q)$ to $B(0)$. Physically, this corresponds to considering oscillations with not too much kinetic energy, which makes sense if we want to stay at the minimum
The resulting equations of motion are
$$
B\underline{\ddot{q}}+A\underline{q}=0
$$

Where we have defined $B:=B(0)$ a constant matrix
$B$ generally does not have zero [[Eigenvalues|eigenvalues]] (since this would correspond to generalised coordinates without a kinetic term), so we assume no zero eigenvalues
This implies $\det(B)\neq 0$, and so $B^{-1}$ exists. We then have an equivalent set of relations:
$$
\underline{\ddot{q}}+B^{-1}A\underline{q}=0
$$
Which reduces to the case we have already studied if we define $C:=B^{-1}A$
There is one small subtlety that needs mentioning however, the fact that $A$ was symmetric was quite important as it ensured that its eigenvalues were real, but in general, $B^{-1} A$ will not be symmetric, even if both $B^{-1}$ and $A$ separately are
Let us assume that $A$ is positive definite: that is, all its eignevalues are positive. Then there exists a symmetric matrix $A^{\frac{1}{2}}$ such that $\left( A^{\frac{1}{2}} \right)^{2}=A$
We can use this matrix to rewrite:
$$
C:=B^{-1} A=A^{-\frac{1}{2}}\left( A^{\frac{1}{2}}B^{-1}A^{\frac{1}{2}} \right)A^{\frac{1}{2}}
$$
So we find that $C$ is [[Similarity Relation|similar]] to $A^{\frac{1}{2}}B^{-1} A^{\frac{1}{2}}$
This matrix is manifestly symmetric, so its eigenvalues are real. Since similar matrices have the same eigenvalues, the eigenvalues of $C$ will be real too
It is straightforward to check that if $\underline{v}$ is an eigenvector of $A^{\frac{1}{2}}B^{-1}A^{\frac{1}{2}}$ with eigenvalue $\lambda$, then $A^{-\frac{1}{2}}\underline{v}$ will be an eigenvector of $C$ with the same eigenvalue
So, in practice, we can simply compute the eigenvalues and eigenvectors of $C$, and proceed as we did above
