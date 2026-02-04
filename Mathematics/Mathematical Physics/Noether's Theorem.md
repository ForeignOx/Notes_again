## Theorem
Consider a [[Transformations of Configuration Spaces|transformation]] [[Generators of Transformations|generated]] by $a_{i}$ ($q_{i}\to q_{i}+\varepsilon a_{i}$) such that $L\to L+\varepsilon \frac{d F}{dt}+\mathcal{O}(\varepsilon^{2})$, i.e. the transformation is a [[Symmetries of Configuration Spaces|symmetry]], then the Noether charge, defined as
$$
Q:= \left( \sum_{i=1}^{N}a_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right)-F
$$
Is conserved, so $\frac{d Q}{dt}=0$ along the equation of motion
## Proof
Considering the [[Action Principle|action principles]],
$$
\delta S=\varepsilon X+\mathcal{O}(\varepsilon^{2})
$$
Where $X$ is the contribution from the endpoints, this is because
$$
\delta S=\int_{t_{0}}^{t_{1}} L(\underline{q}+\varepsilon \underline{a},\underline{\dot{q}}+\varepsilon  \underline{\dot{a}}) \, dt-\int_{t_{0}}^{t_{1}} L(\underline{q},\dot{\underline{q}}) \, dt 
$$
$$
    = \int_{t_{0}}^{t_{1}} L(\underline{q},\underline{\dot{q}})+\sum_{i=1}^{N}\varepsilon a_{i}\frac{ \partial L }{ \partial q_{i} } +\sum_{i=1}^{N}\varepsilon \dot{a}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} } +\mathcal{O}(\varepsilon^{2}) \, dt   -\int_{t_{0}}^{t_{1}} L(\underline{q},\underline{\dot{q}}) \, dt 
$$
$$
= \varepsilon \sum_{i=1}^{N}\int_{t_{0}}^{t_{1}} a_{i}\frac{d }{dt} \left( \frac{ \partial L }{ \partial \dot{q}_{i} }  \right)+\dot{a}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \, dt   +\mathcal{O}(\varepsilon^{2})
$$
$$
= \varepsilon \sum_{i=1}^{N}\int_{t_{0}}^{t_{1}} \frac{d }{dt} \left( a_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right) \, dt +\mathcal{O}(\varepsilon^{2})
$$
$$
=\varepsilon\underbrace{ \left[ \sum_{i=1}^{N}a_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right]_{t_{0}}^{t_{1}} }_{ =X }+\mathcal{O}(\varepsilon^{2})
$$
As required
We also show that if the transformation is a symmetry, then
$$
\delta S=\varepsilon F\big{|}_{t_{0}}^{t_{1}}+\mathcal{O}(\varepsilon^{2})=\int_{t_{0}}^{t_{1}} S' \, dt-\int_{t_{0}}^{t_{1}} S \, dt
$$
Since it is a symmetry, we equate both expressions for $\delta S$:
$$
\varepsilon\left[ \sum_{i=1}^{N}a_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right]_{t_{0}}^{t_{1}}=\varepsilon[F]_{t_{0}}^{t_{1}}
$$
$$
\iff \varepsilon[Q(t_{1})-Q(t_{0})]=0 ~\forall\varepsilon>0
$$
Taking $t_{1}=t_{0}+\beta$, where $\beta\ll 1$, then
$$
Q(t_{1})=Q(t_{0}+\beta)=Q(t_{0})+\beta \frac{d Q}{dt} +\mathcal{O}(\beta^{2})=Q(t_{0})~\forall \beta 
$$
$$
\implies \frac{d Q}{dt} =0
$$
Hence proved :)
## Example
For some ignorable coordinate $q_{i}$, by symmetry,
$$
q_{k}\implies q_{k}'=\begin{cases}
q_{k} & k\neq i  \\
q_{k}+\varepsilon & k=i
\end{cases}
$$
$$
 a_{k}=\delta_{k,i}
$$
So
$$
q_{k}\to q_{k}+\varepsilon a_{k},Q=\sum_{k=1}^{N}\frac{ \partial L }{ \partial q_{k} } -\cancel{ F }
$$
$$
= \sum_{k=1}^{N} \delta_{k,i} \frac{ \partial L }{ \partial \dot{q}_{k} } =\frac{ \partial L }{ \partial \dot{q}_{i} } =0
$$
As we'd expect
___
Let
$$
L=\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2})-V(x^{2}+y^{2})
$$
Since $V$ is in terms of $\hspace{0pt}1$ variable, which in polar coorinates is $r$, we have that $\theta$ is ignorable,
Let's consider rotations:
$$
\begin{pmatrix}
x  \\
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
To put this into first order in $\varepsilon$, we use small angle approximations:
$$
\begin{pmatrix}
x \\
y 
\end{pmatrix}\to \begin{pmatrix}
x' \\
y'
\end{pmatrix}=\begin{pmatrix}
x-\varepsilon y \\
\varepsilon x+y
\end{pmatrix}
$$
$$
\begin{pmatrix}
\dot{x} \\
\dot{y}
\end{pmatrix}\to \begin{pmatrix}
\dot{x}' \\
\dot{y}'
\end{pmatrix}=\begin{pmatrix}
\dot{x}-\varepsilon \dot{y} \\
\varepsilon \dot{x}+\dot{y}
\end{pmatrix}
$$
So
$$
\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2})\to \frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2})+\mathcal{O}(\varepsilon^{2})
$$
$$
x^{2}+y^{2}\to x^{2}+y^{2}+\mathcal{O}(\varepsilon^{2})=x^{2}+y^{2}+\varepsilon^{2}f(\varepsilon)
$$
$$
V(x^{2}+y^{2})\to V(x^{2}+y^{2})+\mathcal{O}(\varepsilon^{2})=V(x^{2}+y^{2})+\varepsilon^{2}f(\varepsilon)V'(x^{2}+y^{2})+\dots
$$
$$
L\to L'=L+\mathcal{O}(\varepsilon^{2})
$$
So this is a symmetry for $F=0$
So the Noether charge is:
$$
Q=a_{x} \frac{ \partial L }{ \partial \dot{x} } +a_{y}\frac{ \partial L }{ \partial \dot{y} } -F=-ym\dot{x}+xm\dot{y}~(=\underline{r}\times \underline{p}=\underline{L})
$$
Which shows that angular momentum is conserved
___
For the example where
$$
L=\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2})-y\dot{x}-\frac{1}{2}x^{2}
$$
We have $x\to x'=x,y\to y'=y+\varepsilon$ is a symmetry with $F=-x,a_{x}=0,a_{y}=1$, so 
$$
Q=a_{x}\frac{ \partial L }{ \partial \dot{x} } +a_{y}\frac{ \partial L }{ \partial \dot{y} } -F=m\dot{y}+x
$$
We can see that this is conseved by examining the Euler-Lagrange equations:
$$
0=\frac{ \partial L }{ \partial x } -\frac{d }{dt} \left( \frac{ \partial L }{ \partial \dot{x} }  \right)=-x-m\ddot{x}+\dot{y}
$$
$$
 0=\frac{ \partial L }{ \partial y } -\frac{d }{dt} \left( \frac{ \partial L }{ \partial \dot{y} }  \right)=-\dot{x}-m\ddot{y}=-\frac{d }{dt} (x+m\dot{y})=-\frac{d Q}{dt} 
$$
So we see that the second gives us our Noether charge being conserved
