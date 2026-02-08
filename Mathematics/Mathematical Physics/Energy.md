Energy is the ability to do [[Work]], it has a standard unit of $\pu{ J}$, the quantity of energy transferred is equal to the work done. Work is not the only way of transferring energy, [[Internal Energy|internal energy]] can be transferred by heat (conduction, convection or radiation)
## Mathematically
Consider the case of [[Newton's Second Law of Motion|Newton's second law]] where $F=F(x)$ (force depends only on [[Position|position]]). Define $V(x)=-\int F(x) \, dx$ as the potential. Then
$$
\frac{d }{dx} \left( \frac{1}{2}mv^{2} \right)=mv\frac{d v}{dx} =ma=F=-\frac{d V}{dx} 
$$
So
$$
\frac{d }{dx} \left( \frac{1}{2}mv^{2}+V \right)=0
$$
Since the derivative is 0, integrating will give us a connstant:
$$
E=\frac{1}{2}mv^{2}+V(x)
$$
This is a constant in time, so
$$
\frac{d E}{dt} =\frac{d E}{dx} \dot{x}=0
$$
The quantity $E$ is the energy of the particle, and we say that it is conserved. The term $K=\frac{1}{2}mv^{2}$ is the [[Kinetic Energy|kinetic energy]], and $V(x)$ is the potential energy, neither of these is conserved in general, but $E$ is constant in time. This means if one of kinetic and potential increases, the other decreases by the same amount
### Remarks
- A force of the form $F(x)$ is said to be conservative, since it conserves energy
- The potential $V$, and hence the energy $E$, are only defined up to an arbitrary constant; one can always add a constant of integration to either
- Using conservation of energy can give us a good picture of the particle's motion, even when we cannot get $x(t)$ explicitly
### Examples
Gravity close to the surface of a planet, taking $x$ upwards, then force is $F=-mg\implies V(x)=mgx+c$
___
Take $m=2$ and $V(x)=x^{6}$, so $E=\frac{1}{2}mv^{2}+V(x)=\dot{x}^{2}+x^{6}$, can one solve this equation of motion ($x(t)$)
$$
v=\frac{d x}{dt} =\sqrt{ E-x^{6} }
$$
(the plus or minus is whether the particle moves left or right, which is irrelevant)
$$
\implies \int \frac{1}{\sqrt{ E-x^{6} }} \, dx =\int  \, dt 
$$
However we can't do this integral :(
Note however, that $V(x)\leq E$, since $\frac{1}{2}mv^{2}\geq 0$, which restricts 
## In $\mathbb{R}^{3}$
A force $\underline{F}(\underline{r})$ is conservative if there exists a real function $V(\underline{r})=V(x,y,z)$ such that 
$$
\underline{F}=-\frac{ \partial V }{ \partial x } \underline{e}_{1}-\frac{ \partial V }{ \partial y } \underline{e}_{2}-\frac{ \partial V }{ \partial z } \underline{e}_{3}=-\underline{\nabla V} 
$$
### Criterion for Conservative Forces
$\underline{F}$ is conservative iff
$$
\frac{ \partial F_{x} }{ \partial y } =\frac{ \partial F_{y} }{ \partial x } ,\frac{ \partial F_{y} }{ \partial z } =\frac{ \partial F_{z} }{ \partial y } ,\frac{ \partial F_{x} }{ \partial z } =\frac{ \partial F_{z} }{ \partial x } 
$$
#### Proof
Suppose $F$ is conservative, so $F_{x}=-\frac{ \partial V }{ \partial x }$ etc, then
$$
\frac{ \partial F_{x} }{ \partial y } -\frac{ \partial F_{y} }{ \partial x } =-\frac{ \partial^{2}V }{ \partial y\partial x }+ \frac{ \partial^{2}V }{ \partial x\partial y } =0 
$$

You can do the same for the other two by symmetry
#### Remark
In parctice, if given $\underline{F}$, just try to find $V$, if you can, then it is conservative
#### Example
Let $\underline{F}=(z-y)\underline{e}_{1}+(\alpha x-z)\underline{e}_{2}+(\beta x-y)\underline{e}_{3}$, for which values of $\alpha,\beta$ is $\underline{F}$ conservative? For those $\alpha,\beta$, find $V$
Solve
$$
\frac{ \partial V }{ \partial x } -F_{x},\frac{ \partial V }{ \partial y } =-F_{y},\frac{ \partial V }{ \partial z } =-F_{z}
$$
$$
V=(y-z)x+g(y,z)
$$
Substituting this into the $y$-equation:
$$
\frac{ \partial V }{ \partial y } =x+\frac{ \partial g }{ \partial y } =z-\alpha x\iff \alpha=-1, \frac{ \partial g(y,z) }{ \partial y } =z
$$
So
$$
g=zy+h(z)
$$
Finally substitute $V=(y-z)x+zy+h(z)$ into $z$ equation:
$$
\frac{ \partial V }{ \partial z } =y-\beta x=-x+y+\frac{d h}{dz} 
$$
Only if $\beta=1, h=c$ (some constant)
## [[Newton's Second Law of Motion|Equation of Motion]]
If you have a central force
$$
\underline{F}=f(r)\underline{e}_{r}
$$
Recall $\underline{r}=r\underline{e}_{r}$,
$$
\underline{v}=\underline{\dot{r}}= \dot{r}\underline{e}_{r}+r \dot{\theta}\underline{e}_{\theta}
$$
$$
\implies \underline{L}=m\underline{r}\times \underline{v}=mr^{2}  \dot{\theta}\underbrace{ \underline{e}_{r}\underline{e}_{\theta} }_{ =\underline{e}_{3} }
$$
So
$$
L=mr^{2}   \dot{\theta}
$$
Next
$$
\underline{\dot{v}}=\ddot{r}=(\ddot{r}-r \dot{\theta}^{2})\underline{e}_{r}+(2\dot{r} \dot{\theta}+r \ddot{\theta})\underline{e}_{\theta}
$$
So equation of motion
$$
m  \underline{\dot{v}}-\underline{\ddot{v}}=\underline{F}=f(r)\underline{e}_{r}
$$
Becomes
$$
m(\ddot{r}-r \dot{\theta}=f(r))
$$
$$
\implies 2\dot{r}\dot{\theta}+r \ddot{\theta}
$$
Note that
$$
\frac{d L}{dt} =\frac{d }{dt} (mr^{2}  \dot{\theta})=m(2r  \dot{r}  \dot{\theta}+r^{2}  \ddot{\theta})=0
$$
SInce $L$ is constant. So we're left with $mr^{2}  \dot{\theta}=L$ whoch is zero since $L$ is constant, So we're left with
$$
mr^{2}   \dot{\theta}=L
$$
Is constant and
$$
m(  \ddot{r}-r \dot{\theta}^{2})=f
$$
Substituting $\dot{\theta}=\frac{L}{mr^{2}}$ into the $\ddot{r}$ equation gives
$$
m  \ddot{r}-\frac{L^{2}}{mr^{3}}=f(r)
$$
___
We can show that the kinetic energy is equal to
$$
K=\frac{1}{2}m(\dot{r}^{2}+r^{2}\dot{\theta}^{2})=\frac{1}{2}m\left( \dot{r}^{2}+\frac{L^{2}}{m^{2}r^{2}} \right)
$$
And we can guess that the potential energy is given by
$$
V(r)=-\int f(r) \, dr 
$$
We justify this by proving that $\frac{d E}{dt}=0$, where $E=K+V$
$$
 \frac{d E}{dt} =\frac{d K}{dt}+\frac{d V}{dt} =\frac{d }{dt}\left( \frac{1}{2}m\left( \dot{r}^{2}+\frac{L^{2}}{m^{2}r^{2}} \right) \right)-\frac{d }{dt} \int f(r) \, dr   
$$
$$
= m  \dot{r} \ddot{r} -\frac{L^{2}   \dot{r}}{mr^{3}}-f  \dot{r}
$$
By applying the [[Chain Rule|chain rule]] several times
$$
=\dot{r}\left( m  \ddot{r}-\frac{L^{2}}{mr^{3}}-f(r) \right)=0
$$
Since the central part is the equation of motion
### Example
A unit mass particle moves in an attractive central force of magnitude $\frac{8}{r^{3}}$. Initial conditions: $\underline{r}(0)=2\underline{e}_{r}$ and $\underline{\dot{r}}(0)=\frac{1}{2}\underline{e}_{r}+\underline{e}_{\theta}$. Using conservation of $E$, obtain an equation for $\dot{r}$ as a function of $r$, and solve :) good luck!!
Here $m=1$, we want $L$, at time 0:
$$
\underline{L}=\underline{r}\times \underline{\dot{r}}=2\underline{e}_{3}
$$
So $L=2$.
We know
$$
\left| f \right| =\left| \underline{F} \right| =\frac{8}{r^{3}}
$$
$$
\implies f(r)=-\frac{8}{r^{3}}
$$
Since it is attractive
$$
\implies V(r)=-\frac{4}{r^{2}}
$$
Thus
$$
E=\frac{1}{2}  \dot{r}^{2} +\frac{2}{r^{2}}-\frac{4}{r^{2}}=\frac{1}{2}\dot{r}^{2}-\frac{2}{r^{2}}
$$
Which is constant, since energy is conserved. By evaluating at $t=0$, we get $\dot{r}(0)=\frac{1}{2},r(0)=2$
$$
E=\frac{1}{8}-\frac{1}{2}=-\frac{3}{8}
$$
We can rearrange the equation of kinetic energy for orther $t$:
$$
\dot{r}^{2}=\frac{4}{r^{2}}-\frac{3}{4}
$$
Since $\dot{r}^{2}\geq 0$, we have
$$
\frac{4}{r^{2}}\geq \frac{3}{4}
$$
$$
\implies r\leq \frac{4}{\sqrt{ 3 }}
$$
So the trajectory is bounded: $r(t)\leq \frac{4}{\sqrt{ 3 }}$. We solve the equation:
$$
\frac{d r}{dt} =\dot{r}=\frac{\sqrt{ 16-3r^{2} }}{2r}
$$
We take the positive square root, since $\dot{r}(0)=\frac{1}{2}>0$, so $\dot{r}>0\forall r$
$$
\implies \int \frac{2r}{\sqrt{ 16-3r^{2} }} \, dr =\int  \, dt 
$$
$$
\implies r(t)=\sqrt{ 4+2t-\frac{3}{4}t^{2} }
$$
![[Energy 2025-02-21 16.42.16.excalidraw]]
The solution is valid for $0\leq t\leq 4$, to get $\theta(t)$, simply integrate
$$
\frac{d \theta}{dt}=\dot{\theta}=\frac{2}{r^{2}}=\frac{2}{4+2t-\frac{3}{4}t^{2}}
$$
The path will be a kind of spiral... 
# In the Lagrangian Formalism
### Definition
The energy of a system is given by
$$
E:=\left( \sum_{i=1}^{N}\dot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right)-L
$$
One can check that it is [[Principle of Conservation of Energy|conserved]] if $\frac{ \partial L }{ \partial t }=0$
## Remark
It is not obvious that the quantity $E$ that is conserved if $\frac{ \partial L }{ \partial t }=0$ is what is usually known as "energy" in classical mechanics. This is easy to verify. Assume that we have a particle with Lagrangian:
$$
L=T(\dot{x}_{1},\dots,\dot{x}_{N})-V(x_{1},\dots,x_{N})
$$
With $T(\dot{x}_{1},\dots,\dot{x}_{N})=\frac{1}{2}m(\dot{x}_{1}^{2}+\dots+\dot{x}_{d}^{2})$ as we often do in classical mechanics, then applying the definition, one easily finds the expected relation:
$$
E=T+V
$$
The result holds more generally, consider a Lagrangian of the form
$$
L=\underbrace{ \left( \sum_{i,j=1}^{N}K_{ij}(q_{1},\dots ,q_{N})\dot{q}_{i}\dot{q}_{j} \right) }_{ T(\underline{q},\dot{\underline{q}}) }-V(\underline{q})
$$
With the $K_{ij}(\underline{q})$ and $V(\underline{q})$ arbitrary functions on a [[Configuration Spaces|configuration space]] $C$, then it is easy to verify that
$$
E=T+V
$$
# In the Hamiltonian Formalism
In the [[Hamiltonian|Hamiltonian]] formalism, the energy is simply equal to the Hamiltonian itself:
$$
H=\left( \sum_{i=1}^{n}p_{i}\dot{q}_{i}(\underline{q},\underline{p},t) \right)-L(\underline{q},\underline{\dot{q}}(\underline{q},\underline{p},t),t)
$$





#Mathematics #Dynamics #Physics #Energy #Definition