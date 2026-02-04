## Definition
The [[Sets|set]] of all possible instantaneous (fixed $t$) configurations (positions, angles but not velocities as if you took a photo) of the system is known as the configuration space, denoted by $C$
## Examples
A particle moving in 1D of a space, the configuration space is $C=\mathbb{R}$
___
A particle moving in $d$ dimensions of space $C=\mathbb{R}^{d}$
___
If we have $N$ particles moving in $\hspace{0pt}1$ spatial diension $C=\mathbb{R}^{N}$
___
If we have $N$ particles moving in $d$ spatial dimensions, $C=\mathbb{R}^{Nd}$
___
$N$ charged particles moving in $\hspace{0pt}3$ dimensions is still $C=(\mathbb{R}^{N})^{3}=\mathbb{R}^{3N}$
___
If we have two particles moving in $d$ spatial dimnesions connected by a rigid rod of length $l$, then $\dim(C)=2d-1$, so if they were $\underline{x}_{1}$ and $\underline{x}_{2}$, each would have $d$ components, but there would be $\hspace{0pt}1$ constraint: $\lvert \lvert \underline{x}_{1}-\underline{x}_{2} \rvert \rvert =l$
___
A chair moving in $\hspace{0pt}3$ dimensions has $\dim(C)=6$ as we can specify the location of its centre of mass and $\hspace{0pt}3$ angles, or we could specify two points on the chair subject to the constraint of the length between them but also allowing rotations about the axis formed by them
## Definition
Given a system $S$ with configuration space $C$, we say that $S$ has $\dim(C)$ degrees of freedom
## Definition
A set of coordinates on $C$ isz known as a set of generalised coordinates
We denote $q_{i}$ for generalised coodinate names and $\underline{q}$ for the vector of generalised coordinates whenever equations hold in any coordinate system for $C$
### Example
A particle moving in $\hspace{0pt}2$ dimensions, we may describe with cartesian coordinates $(x,y)$, or polar coordinates $(r,\theta)$
___
Say we are considering a bead on a circular wire, $\dim(C)=1$, and since it is a circle, $C=S^{1}$, we can think of the dimension as the angle $\theta$, or we can think of $x$ and $y$ with the constraint $x^{2}+y^{2}=1$, but these are constrained variable which can get messy, we are going to work with unconstrained variables
___
Assume $S[\underline{q}(t)]=\int _{t_{0}}^{t_{1}} L(\underline{q}(t),\underline{\dot{q}}(t)) \, dt$, where $\underline{q}$ has $N:=\dim(C)$ components and hence degrees of freedom, so $L$ is a function of $2N$ arguments
Then 
$$
\delta S:= S[\underline{q}(t)+\delta \underline{q}(t)]-S[\underline{q}(t)]=\mathcal{O}((\delta \underline{q})^{2})
$$
$$
S[\underline{q}+\delta \underline{q}]=\int_{t_{0}}^{t_{1}} L(\underline{q}+\delta \underline{q},\underline{\dot{q}})+\delta \underline{\dot{q}} \, dt 
$$
$$
= \int_{t_{0}}^{t_{1}} L(\underline{q},\underline{\dot{q}}) \, dt +\int_{t_{0}}^{t_{1}} \sum_{i=1}^{N} \delta q_{i} \frac{ \partial L }{ \partial q_{i} }  \, dt+\int_{t_{0}}^{t_{1}} \sum_{i=1}^{N}\delta \dot{q}_{i} \frac{ \partial L }{ \partial \dot{q}_{i} }  \, dt +\mathcal{O}((\delta \underline{q})^{2})
$$
$$
\implies \delta S=\int_{t_{0}}^{t_{1}} \sum_{i=1}^{N} \left( \delta q_{i}\frac{ \partial L }{ \partial q_{i} } +\delta \dot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right) \, dt  +\mathcal{O}((\delta \underline{q})^{2})
$$
We know that $\delta \dot{q}_{i}=\frac{d }{dt}(\delta q_{i})$, we use this to integrate by parts
$$
=\int_{t_{0}}^{t_{1}} \sum_{i=1}^{N} \left( \delta q_{i}\frac{ \partial L }{ \partial q_{i} } +\left( \frac{d }{dt} (\delta q_{i}) \right)\frac{ \partial L }{ \partial \dot{q}_{i} }  \right) \, dt +\mathcal{O}((\delta \underline{q})^{2})
$$
And we know that 
$$
\frac{d }{dt}\left( \delta q_{i}\frac{ \partial L }{ \partial \dot{q}_{i} } \right)=\left( \frac{d }{dt}(\delta q_{i}) \right)\frac{ \partial L }{ \partial \dot{q}_{i} } +\delta q_{i}\frac{d }{dt} \frac{ \partial L }{ \partial q_{i} } 
$$
Thus doing the integration by parts:
$$
=\int_{t_{0}}^{t_{1}} \sum_{i=1}^{N}\left( \delta q_{i}\frac{ \partial L }{ \partial q_{i} } +\frac{d }{dt} \left( \delta q_{i}  \right) \frac{ \partial L }{ \partial \dot{q}_{i} } -\delta q_{i}\frac{d }{dt} \frac{ \partial L }{ \partial \dot{q}_{i} }  \right) \, dt +\mathcal{O}((\delta \underline{q})^{2})
$$

$$
\implies \delta S = \cancel{ \left[ \sum_{i=1}^{N}\delta q_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right]_{t_{0}}^{t_{1}} }+\int_{t_{0}}^{t_{1}} \sum_{i=1}^{N}\left( \frac{ \partial L }{ \partial q_{i} } -\frac{d }{dt} \frac{ \partial L }{ \partial \dot{q}_{i} }  \right)\delta q_{i} \, dt +\mathcal{O}((\delta \underline{q})^{2}) 
$$
If $\underline{q}(t)$ is a physical path, this must vanish for any choice of $\delta \underline{q}$, by the [[Fundamental Lemma of the Calculus of Variations|fundamental lemma of the calculus of variations]] 
For instance pick $\delta q_{i}=0\forall i\neq 1$, thus
$$
\delta S = \int_{t_{0}}^{t_{1}} \left( \frac{ \partial L }{ \partial q_{1} } -\frac{d }{dt} \frac{ \partial L }{ \partial \dot{q}_{1} }  \right)\delta q_{1} \, dt +\mathcal{O}((\delta q_{1})^{2}) 
$$
$$
\implies \frac{ \partial L }{ \partial q_{1} } -\frac{d }{dt} \frac{ \partial L }{ \partial \dot{q}_{1} } =0
$$
Rhi works similarly for the other $\delta q_{i}$, we obtain $N$ equations:
$$
\delta S =  \mathcal{O}((\delta q)^{2}) \iff \frac{ \partial L }{ \partial q_{i} } -\frac{d }{dt} \frac{ \partial L }{ \partial \dot{q}_{i} } =0\forall i\in  \overline{N}
$$
Which gives us $N$ Euler-Lagrange equations
Note that in the Euler-Lagrange equations, 
$$
\frac{ \partial q_{i} }{ \partial \dot{q}_{j} } =\frac{ \partial \dot{q}_{i} }{ \partial q_{j} } =0
$$
$$
 \frac{ \partial q_{i} }{ \partial q_{j} } =\frac{ \partial \dot{q}_{i} }{ \partial \dot{q}_{j} } =\delta_{ij}
$$

## Deriving Classical Mechanics
We claim that classical mechanics i obtained by chooseing $L=T-V$, where $T$ is the kinetic energy and $V$ is the potential energy
### Example
A particle of mass $m$ moving in $\mathbb{R}^{3}$, we have $C=\mathbb{R}^{3}$ and choose cartesian coordinates.
$$
L=T-V
$$
$$
 T=\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2}) 
$$
$$
 V=V(x,y,z)
$$
So our Euler-Lagrange equations are:
$$
\frac{ \partial L }{ \partial x } -\frac{d }{dt} \frac{ \partial L }{ \partial \dot{x} } =0
$$
$$
 \frac{ \partial L }{ \partial y } -\frac{d }{dt} \frac{ \partial L }{ \partial \dot{y} } =0
$$
$$
 \frac{ \partial L }{ \partial z } -\frac{d }{dt} \frac{ \partial L }{ \partial \dot{z} } =0
$$
We have:
$$
\frac{ \partial L }{ \partial \dot{x} } =\frac{ \partial T-V }{ \partial \dot{x} } =\frac{ \partial T }{ \partial \dot{x} } -\underbrace{ \frac{ \partial V }{ \partial \dot{x} } }_{ =0 } =m\dot{x}
$$
$$
\implies \frac{d }{dt} \left( \frac{ \partial L }{ \partial \dot{x} }  \right)=m\ddot{x}
$$
Similarly,
$$
\frac{d }{dt} \frac{ \partial L }{ \partial \dot{y} } =m\ddot{y},\frac{d }{dt} \frac{ \partial L }{ \partial \dot{z} } =m\ddot{z}
$$
Then
$$
\frac{ \partial L }{ \partial x } =\frac{ \partial T-V }{ \partial x } =\underbrace{ \frac{ \partial T }{ \partial x } }_{ =0 } -\frac{ \partial V }{ \partial x } 
$$
Thus we have
$$
\frac{ \partial V }{ \partial x } =-m\ddot{x}
$$
$$
 \frac{ \partial V }{ \partial y } =-m\ddot{y}
$$
$$
 \frac{ \partial V }{ \partial z } =-m\ddot{z}
$$
Which are the equations of motion in classical mechanics, since $\underline{F}=-\underline{\nabla }V$
### Example
A particle of mass $m$ moving freely in $d$ dimensions, $C=\mathbb{R}^{d}$, we choose Cartesian coordinates $(x_{1},x_{2},\dots,x_{d})$ with $L=T-V$, with $V=0$ by assumption,
$$
T=\frac{1}{2}m \sum_{i=1}^{d} \dot{x}_{i}^{2}
$$
Our Euler-Lagrange equations give:
$$
0=\frac{ \partial L }{ \partial x_{i} } -\frac{d }{dt} \left( \frac{ \partial L }{ \partial \dot{x}_{i} }  \right)=-\frac{d }{dt} \left( \frac{ \partial  }{ \partial \dot{x}_{i} } \left( \frac{1}{2}m\sum_{j=1}^{d}\dot{x}_{j}^{2} \right) \right)
$$
$$
= -\frac{d }{dt} \left( \frac{1}{2}m\sum_{j=1}^{d} \frac{ \partial \dot{x}_{j}^{2} }{ \partial \dot{x}_{i} }  \right)
$$
And by the chain rule
$$
\frac{ \partial \dot{x}^{2}_{j} }{ \partial \dot{x}_{i} } =2\dot{x}_{j}\frac{ \partial \dot{x}_{j} }{ \partial \dot{x}_{i} } =2\dot{x}_{j}\delta_{ij}
$$

