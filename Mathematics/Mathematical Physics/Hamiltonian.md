We can show by considering [[Hamiltonian Flow|Hamiltonian flow]] that conserved quentities generate the corresponding [[Symmetries of Configuration Spaces|symmetries]]
It is natural to guess that [[Energy|energy]] will generate time evolution, via Hamiltonian flow. This is indeed the case
## Definition
The Hamiltonian $H$ of a physical system is the energy expressed in terms of generalised [[Coordinates|coordinates]] and [[Generalised Momentum|generalised]] [[Momentum|momenta]]. That is:
$$
H:=\left( \sum_{i=1}^{n}p_{i}\dot{q}_{i}(\underline{q},\underline{p},t) \right)-L(\underline{q},\underline{\dot{q}}(\underline{q},\underline{p},t),t)
$$
## Example
Consider the harmonic oscillator in $\hspace{0pt}1$ dimension, with Lagrangian,
$$
L=\frac{1}{2}m\dot{x}^{2}-\frac{1}{2}\kappa x^{2}
$$
The generalised momentum is $p=m\dot{x}$, so the Hamiltonian for this system is
$$
H=\frac{1}{2m}p^{2}+\frac{1}{2}\kappa x^{2}
$$
___
A more involved example, consider the Lagrangian for a relativistic particle:
$$
L=-mc\sqrt{ c^{2}-\dot{\underline{x}}^{2} }
$$
Where we have introduced the combination $\dot{\underline{x}}^{2}:=\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2}$. We found in that example that the energy was then given by
$$
E=\frac{mc^{3}}{\sqrt{ c^{2}-\dot{\underline{x}}^{2} }}
$$
The Hamiltonian is this energy expressed in terms of Hamiltonian variables, (that is, generalised coordinates and momenta), so we need to express $\underline{\dot{x}}^{2}$ in terms of $x,y,z,p_{x},p_{y},p_{z}$. We have the generalised momenta:
$$
p_{x}=\frac{ \partial L }{ \partial \dot{x} } =\frac{mc\dot{x}}{\sqrt{ c^{2}-\underline{\dot{x}}^{2} }}
$$
$$
p_{y}=\frac{ \partial L }{ \partial \dot{y} } =\frac{mc\dot{y}}{\sqrt{ c^{2}-\underline{\dot{x}}^{2} }}
$$
$$
p_{z}=\frac{ \partial L }{ \partial \dot{z} } =\frac{mc\dot{z}}{\sqrt{ c^{2}-\underline{\dot{x}}^{2} }}
$$
Consider the combination $\underline{P}^{2}:=p_{x}^{2}+p_{y}^{2}+p_{z}^{2}$. We have
$$
\underline{P}^{2}=m^{2}c^{2} \frac{\underline{\dot{x}}^{2}}{c^{2}-\underline{\dot{x}}^{2}}
$$
Which implies, solving for $\underline{\dot{x}}^{2}$:
$$
\underline{\dot{x}}^{2}=\frac{c^{2}\underline{P}^{2}}{m^{2}c^{2}+\underline{P}^{2}}
$$
Pluggin this expression for $\underline{P}$ into our expression for the energy above, we find 
$$
H=\frac{mc^{3}}{\sqrt{ c^{2}-\left( \frac{c^{2}\underline{P}^{2}}{m^{2}c^{2}+\underline{P}^{2}} \right) }}
=c\sqrt{ m^{2}c^{2}+\underline{P}^{2} }
$$
## Theorem
The time evolution of the generalised coordinates and momenta is given by the Hamiltonian flow $\Phi_{H}^{(\varepsilon)}$:
$$
\Phi_{H}^{(\varepsilon)}(q_{i})=q_{i}(t+\varepsilon),~\Phi_{H}^{(\varepsilon)}(p_{i})=p_{i}(t+\varepsilon)
$$
By expanding $\Phi_{H}^{(\varepsilon)}$ from its definition at $q_{i}(t+\varepsilon)=q_{i}(t)+\varepsilon \dot{q}_{i}(t)+\dots$ and similarly for $p_{i}$, we get Hamiltonian's equations of motion:
$$
\dot{q}_{i}=\left\{ q_{i},H \right\}=\frac{ \partial H }{ \partial p_{i} } 
$$
$$
\dot{p}_{i}\left\{ p_{i},H \right\}=-\frac{ \partial H }{ \partial q_{i} } 
$$
### Proof
The first thing to do is to note that when we write the partial derivative in the Hamiltonian picture $\frac{ \partial A }{ \partial q_{j} }$, we are differrentiating $A$ with respect to $q_{j}$, keeping the other $q$'s, any explicit time dependance in $A$, and the $p$'s fixed. This should be contrasted with the Lagrangian picture, where differentiating with respect to $q_{j}$ involved keeping the other $q$'s, time and the $\dot{q}$'s fixed
To highlight this, in this proof, we write $\frac{ \partial A }{ \partial q_{j} }\Big{|}_{\underline{p}}$ or $\frac{ \partial A }{ \partial q_{j} }\Big{|}_{\dot{\underline{q}}}$ to clarify which set of variables are being held fixed when taking partial derivatives
Given this, we halculate the derivatives of $H$ with respect to $q_{j}$ and $p_{j}$. We have
$$
\frac{ \partial H }{ \partial q_{j} } \Bigg{|}_{\underline{p}} =\frac{ \partial  }{ \partial q_{j} } \left( \sum_{i}p_{i}\dot{q}_{i}(q,p,t)-L(q,\dot{q}(q,p,t),t) \right)\Bigg{|}_{\underline{p}} 
$$
$$
= \sum_{i}p_{i} \frac{ \partial \dot{q}_{i} }{ \partial q_{j} } \Bigg{|}_{\underline{p}} -\sum_{i}\frac{ \partial L }{ \partial q_{i} } \Bigg{|}_{\dot{\underline{q}}} \frac{ \partial q_{i} }{ \partial q_{j} } \Bigg{|}_{\underline{p}} -\sum_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }\Bigg{|}_{\underline{q}}\frac{ \partial \dot{q}_{i} }{ \partial q_{j} } \Bigg{|}_{\underline{p}}
$$
$$
= \sum_{i}p_{i} \frac{ \partial \dot{q}_{i} }{ \partial q_{j} } \Bigg{|}_{\underline{p}} -\frac{ \partial L }{ \partial q_{j} } \Bigg{|}_{\underline{\dot{q}}}-\sum_{i}\frac{ \partial L }{ \partial \dot{q}_{i} } \Bigg{|}_{\underline{q}} \frac{ \partial \dot{q}_{i} }{ \partial q_{j} } \Bigg{|}_{\underline{p}} 
$$
$$
= \sum_{i}\left( p_{i}-\frac{ \partial L }{ \partial \dot{q}_{i} }\Bigg{|}_{\underline{q}}   \right)\frac{ \partial \dot{q}_{i} }{ \partial q_{j} } \Bigg{|}_{\underline{p}} -\frac{ \partial L }{ \partial q_{j} } \Bigg{|}_{\dot{\underline{q}}} 
$$
The first pracket in this expression is $\hspace{0pt}0$ by definition of $p_{i}$, so along a physical path,
$$
\frac{ \partial H }{ \partial q_{j} } \Bigg{|}_{\underline{p}} =-\frac{ \partial L }{ \partial q_{j} } \Bigg{|}_{\dot{\underline{q}}} =-\frac{d}{dt} \left( \frac{ \partial L }{ \partial \dot{q}_{j} } \Bigg{|}_{\underline{q}}  \right)=-\dot{p}_{j}
$$
Where for the second equality, we used the [[Euler-Lagrange Equations|Euler-Lagrange equation]] for $q_{j}$
Similarly, calculating $\frac{ \partial H }{ \partial p_{j} }$, we find
$$
\frac{ \partial H }{ \partial p_{j} } \Bigg{|}_{\underline{q}} =\frac{ \partial  }{ \partial q_{j} } \left( \sum_{i}p_{i}\dot{q}_{i}(q,p,t)-L(q,\dot{q}(q,p,t),t) \right)\Bigg{|}_{\underline{q}}
$$
$$
= \sum_{i}\frac{ \partial p_{i} }{ \partial p_{j} } \dot{q}_{i}+\sum_{i}p_{i}\frac{ \partial \dot{q}_{i} }{ \partial p_{j} } \Bigg{|}_{\underline{q}} -\sum_{i}\frac{ \partial L }{ \partial \dot{q}_{i} } \Bigg{|}_{\underline{q}} \frac{ \partial \dot{q}_{i} }{ \partial p_{j} } \Bigg{|}_{\underline{q}} 
$$
$$
= \sum_{i}\delta_{ij}\dot{q}_{i}+\sum_{i}\left( p_{i}-\frac{ \partial L }{ \partial \dot{q}_{i} } \Bigg{|}_{\underline{q}}  \right)\frac{ \partial \dot{q}_{i} }{ \partial p_{j} } \Bigg{|}_{\underline{q}} 
$$
$$
= \dot{q}_{j}
$$
Again using the definition of $p_{i}$ to show the last term vanishes. Note that we did not need to use the Euler Lagrange equations to derive this last question. Accordinly, in practive, this equation just reproduces the result of inverting the definition of the generalised momentum in the Larangian formalism to express $\underline{\dot{q}}$ in terms of $\underline{q},\underline{p}$ and $t$
## Corollary
The time evolution of any function $f(\underline{q},\underline{p})$ on phase space is generated by $\Phi_{H}^{(\varepsilon)}$:
$$
\frac{d f}{dt} =\left\{ f, H\right\}
$$
In the case that $f$ depends explicitly on time, $f=f(\underline{q},\underline{p},t)$, we have
$$
\frac{d f}{dt} =\frac{ \partial f }{ \partial t } +\left\{ f,H \right\}
$$
### Proof
The function $f$ will depend on time through its explicit dependence on $t$, if any, and via its implicit dependence via $\underline{q}$ and $\underline{p}$, who themselves are functions of time. Using the [[Chain Rule|chain rule]], we find
$$
\frac{d f}{dt} =\frac{ \partial f }{ \partial t } =\sum_{i=1}^{n}\left( \frac{ \partial f }{ \partial q_{i} } \dot{q}_{i}+\frac{ \partial f }{ \partial p_{i} } \dot{p}_{i} \right)
$$
$$
= \frac{ \partial f }{ \partial t } +\sum_{i=1}^{n}\left( \frac{ \partial f }{ \partial q_{i} } \frac{ \partial H }{ \partial p_{i} } -\frac{ \partial f }{ \partial p_{i} } \frac{ \partial H }{ \partial q_{i} }  \right)=\frac{ \partial f }{ \partial t } +\left\{ f,H \right\}
$$
Where we have used Hamilton's equations in going to the second line
## Remark
We can apply this corollary to give a very neat proof of [[Principle of Conservation of Energy|conservation of energy]]
Energy in the Hamiltonian formalism is simply equal to the Hamiltonian itself. So the equation for energy conservation can be written as:
$$
\frac{d H}{dt} =\frac{ \partial H }{ \partial t } +\left\{ H,H \right\}=\frac{ \partial H }{ \partial t } 
$$
Using the fact that the Poisson bracket is antisymmetric. We see that if time does not appear explicitly in the expression for the Hamiltonian, then energy is conserved
## Remark
A small variation of this last equation is sometimes included as part of Hamilton's equations. From the definition of the Hamiltonian we have that
$$
\frac{ \partial H(\underline{q},\underline{p},t) }{ \partial t } \Bigg{|}_{\underline{q},\underline{p}}=\frac{ \partial  }{ \partial t } \left( \left( \sum_{i=1}^{n}\dot{q}_{i}(\underline{q},\underline{p},t)p_{i} \right)-L(\underline{q},\dot{\underline{q}}(\underline{q},\underline{p},t),t) \right)\Bigg{|}_{\underline{q},\underline{p}} 
$$
$$
= \left( \sum_{i=1}^{n}p_{i}\frac{ \partial \dot{q}_{i}(\underline{q},\underline{p},t) }{ \partial t } \Bigg{|}_{\underline{q},\underline{p}}  \right)-\frac{ \partial L(\underline{q},\dot{\underline{q}}(\underline{q},\underline{p},t),t) }{ \partial t } \Bigg{|}_{\underline{q},\underline{p}} 
$$
Now note that $L$ can have an explicit dependence on $t$ through $\underline{\dot{q}}$, so we use the chain rule:
$$
\frac{ \partial L(\underline{q},\dot{\underline{q}}(\underline{q},\underline{p},t),t) }{ \partial t } \Bigg{|}_{\underline{q},\underline{p}} =\frac{ \partial L(\underline{q},\dot{\underline{q}}),t }{ \partial t } \Bigg{|}_{\underline{q},\dot{\underline{q}}} 
$$
