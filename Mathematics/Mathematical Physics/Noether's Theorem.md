# In Particle Theory
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
## Charge iff Symmetry?
We can now close the circle of ideass that has been developed. We have seen that every symmetry implies the existence of a conserved Noether charge $Q$, and we have alsol shown that the Noether charge associated to a symmetry generates the right transformations on the generalised coodinates. It is natural to ask whether any conserved charge generate a symmetry transformation?
This is indeed the case, as we now show for the class of conserved charges
## Theroem
Assume that we have a function $Q(\underline{q},\underline{p},t)$ of the form
$$
Q(\underline{q},\underline{p},t)=\left( \sum_{i=1}^{n}a_{i}(\underline{q})p_{i} \right)-F(\underline{q},t)
$$
Such that 
$$
\frac{d Q}{dt} -\left\{ Q,H \right\}+\frac{ \partial Q }{ \partial t } =0
$$
Then [[Hamiltonian Flow|$\Phi_{Q}^{(\varepsilon)}(L)=L+\varepsilon \frac{d F}{dt}+\mathcal{O}(\varepsilon^{2})$]], so $Q$ generates a symmetry, whose Noether charge is $Q$
### Proof
Let's start by proving auxiliary results. Note first that
$$
\left\{ q_{i},Q \right\}=\frac{ \partial Q }{ \partial p_{i} } =a_{i}(\underline{q})
$$
Which implies, in particular, that
$$
\frac{ \partial \left\{ q_{i},Q \right\} }{ \partial t } =\frac{ \partial a_{i}(\underline{q}) }{ \partial t } =0
$$
Note also that since $Q$ is conserved, and the only explicit time dependence of $Q$ is via $F$, we have
$$
\left\{ Q,H \right\}=\frac{d Q}{dt} -\frac{ \partial Q }{ \partial t } =-\frac{ \partial Q }{ \partial t } =\frac{ \partial F }{ \partial t } 
$$
So
$$
-\left\{ \left\{ Q,H \right\},q_{i} \right\}=\left\{ q_{i},\left\{ Q, H\right\} \right\}=\frac{ \partial \left\{ Q,H \right\} }{ \partial p_{i} } =\frac{ \partial  }{ \partial p_{i} } \left( \frac{ \partial F(\underline{q},t) }{ \partial t }  \right)=0
$$
Using these two results we find that
$$
\frac{d \left\{ q_{i},Q \right\}}{dt} =\frac{ \partial \left\{ q_{i},Q \right\} }{ \partial t } +\left\{ \left\{ q_{i},Q \right\},H \right\} 
$$
$$
= \left\{ \left\{ q_{i},Q \right\},H \right\} = -\left\{ \left\{ H,q_{i} \right\},Q \right\}-\left\{ \left\{ Q,H \right\},q_{i} \right\} = \left\{ \left\{ q_{i},H \right\},Q \right\}
$$
Where we have used Jacobi's identity for [[Poisson Bracket|Poisson brackets]] in the third equality
[[Hamiltonian|Hamilton's equations]] then imply that
$$
\frac{d \left\{ q_{i},Q \right\}}{dt} =\left\{ \dot{q}_{i},Q \right\}
$$
Using these results it is straightforward to compute the change in the Lagrangian due to $Q$
The Lagrangian in Hamiltonian coordinates is
$$
L(\underline{q},\underline{p},t)=\sum_{i=1}^{n}\dot{q}_{i}(\underline{q},\underline{p}),p_{i}-H(\underline{q},\underline{p},t)
$$
Since $Q$ is conseved, we have
$$
\left\{ L,Q \right\}= \sum_{i=1}^{n}(\left\{ \dot{q}_{i},Q \right\}p_{i}+\dot{q}_{i}\left\{ p_{i},Q \right\}) +\left\{ Q,H \right\} 
$$
$$
= \sum_{i=1}^{n}(\left\{ \dot{q}_{i},Q \right\}p_{i}+\dot{q}_{i}\left\{ p_{i},Q \right\})-\frac{ \partial Q }{ \partial t } 
$$
Which becomes, using the results above:
$$
\left\{ L,Q \right\}=\sum_{ i=1} ^{ n}  \left( p_{i}\frac{d}{dt} \left\{ q_{i},Q \right\}+\dot{q}_{i}\left\{ p_{i},Q \right\} \right)-\frac{ \partial Q }{ \partial t } 
$$
$$
= \sum_{ i=1} ^{ n}  \left( \frac{d}{dt} (\left\{ q_{i},Q \right\}p_{i})-\dot{p}_{i}\left\{ q_{i},Q \right\}+\dot{q}_{i}\left\{ p_{i},Q \right\} \right)-\frac{ \partial Q }{ \partial t } 
$$
$$
= \sum_{ i=1} ^{ n}  \left( \frac{d}{dt} (\left\{ q_{i},Q \right\}p_{i})-\dot{p}_{i}\frac{ \partial Q }{ \partial p_{i} } -\dot{q}_{i}\frac{ \partial Q }{ \partial q_{i} }  \right)-\frac{ \partial Q }{ \partial t } 
$$
$$
= \frac{d}{dt} \left( \sum_{ i=1} ^{ n}  \left\{ q_{i},Q \right\}p_{i} \right)-\frac{d Q}{dt} 
$$
Finally, we find that
$$
\sum_{ i=1} ^{ n}\left\{ q_{i},Q \right\}p_{i}\sum_{ i=1} ^{ n}  q_{i}p_{i}=Q+F
$$
Which implies
$$
\left\{ L,Q \right\}=\frac{d (Q+F-Q)}{dt} =\frac{d F}{dt} 
$$

Recalling the definition of the Hamiltonian flow operator, this gives
$$
\Phi_{Q}^{(\varepsilon)}(L)=L+\varepsilon \left\{ L ,Q\right\}+\mathcal{O}(\varepsilon^{2})=L+\varepsilon \frac{d F}{dt} +\mathcal{O}(\varepsilon^{2})
$$
And we are done
# In Field Theory
## Definition
The Noether current (a [[Vectors|vector]] with $d+1$ components) we define associated to a transformation is defined as
$$
\underline{J}=a\underline{\Pi}
$$
Or in components
$$
J_{i}:=a\frac{ \partial \mathcal{L} }{ \partial u_{i} } 
$$
## Theorem
If $\underline{J}$ is the Noether current associated to a symmetry, then
$$
\underline{\nabla} \cdot \underline{J} :=\sum_{i=0}^{d}\frac{ \partial J_{i} }{ \partial x_{i} } =0
$$
### Proof
We can proced analogously as to what we did when proving Noether's theorem for discrete ystems. Under a generic transformation, we have
$$
\delta \mathcal{L}=\varepsilon \frac{ \partial \mathcal{L} }{ \partial u } +\varepsilon \sum_{i=0}^{d}\frac{ \partial a }{ \partial x_{i} } \frac{ \partial \mathcal{L} }{ \partial u_{i} } +\mathcal{O}(\varepsilon^{2})
$$
Using thee Euler-Lagrange equations, this becomes
$$
\delta \mathcal{L}=\varepsilon \sum_{i=0}^{d}\frac{ \partial  }{ \partial x_{i} } \left( a\frac{ \partial \mathcal{L} }{ \partial u_{i} }  \right)+\mathcal{O}(\varepsilon^{2})
$$
Which equating with the explicit action of the symmetry on $\mathcal{L}$ leads to
$$
\sum_{i=0}^{d}\frac{ \partial  }{ \partial x_{i} } \left( a\frac{ \partial \mathcal{L} }{ \partial u_{i} }  \right)=0
$$
## Definition
Given a Noether current $\underline{J}$ asociated to a transformation, we define the Noether charge density
$$
\mathcal{Q}:=J_{0}
$$
Furthermore, in the $d=1$ case (one spatial dimnsion), we define the charge contained inan interval $(a,b)$ to be
$$
    \mathcal{Q}_{(a,b)}:=\int ^{b}_{a} \mathcal{Q} \, dx =\int ^{b}_{a} J_{0} \, dx 
$$
## Proposition
Assume $d=1$, then
$$
\frac{d \mathcal{Q}_{(a,b)}}{dt} =J_{1}(a)-J_{1}(b)
$$

