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
=\dots= S+\int \int \delta u\left( \frac{ \partial \mathcal{L} }{ \partial u } -\frac{ \partial  }{ \partial x } \left( \frac{ \partial \mathcal{L} }{ \partial u_{x} }  \right)-\frac{ \partial  }{ \partial t } \left( \frac{ \partial \mathcal{L} }{ \partial u_{t} }  \right) \right)+\mathcal{O}() \, dx  \, dt 
$$
