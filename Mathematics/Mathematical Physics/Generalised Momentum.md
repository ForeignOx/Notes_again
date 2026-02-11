# In Particle Theory
## Definition
The generalised momentum associated to a generalised coordinate $q_{i}$ is
$$
p_{i}:= \frac{ \partial L }{ \partial \dot{q}_{i} } 
$$
## Proposition
The generalised momentum $p_{i}$ associated to an [[Ignorable Coordinates|ignorable]] coordinate $q_{i}$ is conserved
### Proof
The Euler-Lagrange equation for $q_{i}$ is:
$$
0=\frac{d }{dt} \left( \frac{ \partial L }{ \partial \dot{q}_{i} }  \right)-\cancel{ \frac{ \partial L }{ \partial q_{i} }C }
$$
$$
 \iff \frac{d }{dt} p_{i}=0 
$$
## Example
A particle of mass $m$ is moving freely ($V=0$) in $d$ dimensions:
$$
L=\frac{1}{2}m\sum_{i=1}^{d}\dot{x}^{2}_{i}
$$
And here all the coordinates are ignorable:
$$
p_{i}:= \frac{ \partial L }{ \partial \dot{x}_{i} } =\frac{ \partial  }{ \partial \dot{x}_{i} } \left( \frac{1}{2}m\sum_{k=1}^{d}\dot{x}^{2}_{k} \right)
$$
$$
= \frac{1}{2}m\sum_{k=1}^{d}\frac{ \partial \dot{x}^{2}_{k} }{ \partial \dot{x}_{i} } =\frac{1}{2}m\sum_{k=1}^{d}2\dot{x}_{k}\delta_{k,i}=m\dot{x}_{i}
$$
Which are the momenta $p_{0}$ for the particle
___
IIn the example with $d=2$, in polar coordinates,
$$
L=T=\frac{1}{2}m(^{ot^{2}+r^{2}\dot{\theta}^{2}})
$$
$\theta$ is ignorable as $\frac{ \partial L }{ \partial \theta }=0$, so
$$
p_{\theta}:=\frac{ \partial L }{ \partial \dot{\theta} } =mr^{2}\dot{\theta}
$$
Is conserved
___
## Canonical Kinetic Terms
Assume $T=\frac{1}{2}\sum_{i=1}^{N}\dot{q}_{i}^{2}$ ($m=1$) nand $V=V(\underline{q})$ ($V$ does not depend on velocities), then
$$
L=\frac{1}{2}\sum_{i=1}^{N}\dot{q}_{i}^{2}-V(\underline{q})
$$
Assume that $V$ has an exturemum, so
$$
\frac{ \partial V }{ \partial q_{i} } =0\forall i
$$
At $\underline{q}=0$
This can always be achieved by any particular extremum at $\underline{q}=\underline{a}$ and redefining $\underline{q}\to \underline{q}-\underline{a}$

## Propoition
If $c$ is a constant, $L$ and $L':=L+c$ give the same equations of motion;
### Proof
$$
0=\frac{ \partial L' }{ \partial q_{i} } -\frac{d }{dt} \left( \frac{ \partial L' }{ \partial \dot{q}_{i} }  \right)=\frac{ \partial L }{ \partial q_{i} } -\frac{d }{dt} \left( \frac{ \partial L }{ \partial \dot{q}_{i} }  \right)+\frac{ \partial c }{ \partial q_{i} } 
$$
# In Field Theory
In field theory, we have a generalised momentum $\Pi^{i}$ which is defined as
$$
\Pi^{i}=\frac{ \partial \mathcal{L} }{ \partial u_{i} } 
$$
Where
$$
u_{i}=\frac{ \partial u }{ \partial x_{i} } 
$$
$$
 u_{0}=\frac{ \partial u }{ \partial x } 
$$