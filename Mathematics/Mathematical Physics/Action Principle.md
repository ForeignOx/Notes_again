## Principle
For arbitrary smooth small deformations $\delta x(t)$ around the true path $x(t)$, we have:
$$
\delta S:= S[x+\delta x]-S[x]=\mathcal{O}((\delta x)^{2})
$$
In other words:
It is possible to choose an action [[Functionals|functional]] $S[x(t)]$ such that the paths desribed by physical particles are stationary paths of $S$
___
For nice systems it will be the case that $S$ can be expressed as the time integral of a Lagrangian. That is, we have
$$
S[x]=\int_{t_{0}}^{t_{1}} L(x(t),\dot{x}(t)) \, dt 
$$
For some [[Functions|function]] $L(a,b)$ of two real variables
___
In field theory, if a field is described by the funtion $u(x,t)$, satisfying the equations of motion, then
$$
S[u+\delta u]=S[u]+\mathcal{O}((\delta u)^{2})
$$
This is also the integral of the [[Lagrangian Density|Lagrangian density]]:
$$
S[u+\delta u]=\int \int \mathcal{L}(u+\delta u,u_{x}+\delta u_{x},u_{t}+\delta u_{t}) \, dx  \, dt 
$$
$$
= \int \int \mathcal{L}(u,u_{x},u_{t})+\delta u \frac{ \partial \mathcal{L} }{ \partial u } +\delta u_{x}\frac{ \partial \mathcal{L} }{ \partial u_{t} } +\delta u_{t}\frac{ \partial \mathcal{L} }{ \partial u_{t} }  \, dx  \, dt  
$$
$$
= \int \int \mathcal{L}(u,u_{x},u_{t})+\delta u\frac{ \partial \mathcal{L} }{ \partial u } +\left( \frac{ \partial  }{ \partial x } (\delta u) \right)\frac{ \partial \mathcal{L} }{ \partial u_{x} } +\left( \frac{ \partial  }{ \partial t } (\delta u) \right)\frac{ \partial \mathcal{L} }{ \partial u_{t} }  \, dx  \, dt 
$$
$$
= \int \int \mathcal{L}(u,u_{x},u_{t})+\delta u\frac{ \partial \mathcal{L} }{ \partial u } +\frac{ \partial  }{ \partial x } \left( \delta u\frac{ \partial \mathcal{L} }{ \partial u_{x} }  \right) \, dx  \, dx 
$$
$$
=\dots= S+\int \int\underbrace{  \delta u\left( \frac{ \partial \mathcal{L} }{ \partial u } -\frac{ \partial  }{ \partial x } \left( \frac{ \partial \mathcal{L} }{ \partial u_{x} }  \right)-\frac{ \partial  }{ \partial t } \left( \frac{ \partial \mathcal{L} }{ \partial u_{t} }  \right) \right)+\mathcal{O}((\delta u)^{2})  }_{ =0\text{ for any }\delta u }\, dx  \, dt 
$$
By the Fundamental Lemma of the calculus of variations, hence the Euler Lagrange equation for a field  in one spatial dimension is
$$
\frac{ \partial \mathcal{L} }{ \partial u } -\frac{ \partial  }{ \partial x } \left( \frac{ \partial \mathcal{L} }{ \partial u_{x} }  \right)-\frac{ \partial  }{ \partial t } \left( \frac{ \partial \mathcal{L} }{ \partial u_{t} }  \right)=0
$$
We can generalise this to if we have $N$ unconstrained fields $u^{(1)},\dots,u^{(N)}$, then we obtain $N$ Euler-Lagrange equations:
$$
\frac{ \partial \mathcal{L} }{ \partial u^{(i)} } -\frac{ \partial  }{ \partial x } \frac{ \partial \mathcal{L} }{ \partial u_{x}^{(i)} } -\frac{ \partial  }{ \partial t } \frac{ \partial \mathcal{L} }{ \partial u^{(i)} _{t}} =0 \forall i \in \left\{ 1,\dots,N \right\}
$$
With 
$$
u^{(i)}_{x}=\frac{ \partial u^{(i)} }{ \partial x },~u_{t}^{(i)}=\frac{ \partial u^{(i)} }{ \partial t }  
$$
If we also have $d$ spatial dimensions $x_{1},\dots,x_{d}$, with $x_{0}:= t$, then we have
$$
\frac{ \partial \mathcal{L} }{ \partial u^{(i)} } -\sum_{k=0}^{d}\frac{ \partial  }{ \partial x_{k} } \frac{ \partial \mathcal{L} }{ \partial u^{(i)}_{k} } =0 \forall i
$$
## Example
Massless scalar field, one dimensional string:
$$
\mathcal{L}=\frac{1}{2}\rho u_{t}^{2}-\frac{1}{2}\tau u_{x}^{2}
$$
With $\rho$ being the density and $\tau$ the tension, then we get Euler-Lagrandge equations:
$$
0=\frac{ \partial \mathcal{L} }{ \partial u } -\frac{ \partial  }{ \partial x } \left( \frac{ \partial \mathcal{L} }{ \partial u_{x} }  \right)-\frac{ \partial  }{ \partial t } \left( \frac{ \partial \mathcal{L} }{ \partial u }  \right)
$$
$$
= \tau \frac{ \partial u_{x} }{ \partial x } -\rho \frac{ \partial u_{t} }{ \partial t } =\tau u_{xx}-\rho u_{tt}
$$
$$
 \iff \tau u_{xx}=\rho u_{tt} \iff  u_{tt}=c^{2}u_{x x}
$$
Which is the wave equation!!
$$

$$
