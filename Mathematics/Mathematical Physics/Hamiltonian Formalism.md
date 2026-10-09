The Hamiltonian formalism came about by realising that we didn't need to study positions and velocities necessarily, but position and [[Generalised Momentum|momenta]]  give us the same amount of information, and can be nicer
## Definition
The Hamiltonian formalism studies dynamics on [[Phase Spaces|$\mathscr{P}$]], parametrised by $\underline{q}$ and $\underline{p}$, where $q_{i}:= \frac{ \partial L }{ \partial \dot{q}_{i} }$
We view the equation
$$
q_{i}=\frac{ \partial L(\underline{q},\underline{\dot{q}}) }{ \partial \dot{q}_{i} } 
$$
As an equation to solve for $\underline{\dot{q}}_{i}(\underline{q},\underline{p})$
## Example
Take $L=\frac{1}{2}m(\dot{r}^{2}+r^{2}\dot{\theta}^{2})$, so
$$
p_{r}=\frac{ \partial L }{ \partial   \dot{r} }=m   \dot{r}\implies  \dot{r}=\frac{p_{r}}{m}
$$
$$
 p_{\theta}-\frac{ \partial L }{ \partial \dot{\theta} } =mr^{2}\dot{\theta}\implies\dot{\theta}= \frac{p_{\theta}}{mr^{2}} 
$$
So
$$
L=\frac{1}{2}m\left( \left( \frac{p_{r}}{m} \right)^{2}+r^{2}\left( \frac{p_{\theta}}{mr^{2}} \right) \right)=\frac{1}{2m}\left( q_{r}^{2}+\frac{p_{\theta}^{2}}{r^{2}} \right)
$$
## Why are we Doing this??
We still need to understand how a given [[States|state]] evolves in time in this new formalism. That is, if we know which point in phase space describes a system at a given time, which trajectory in phase space will describe subsequent motion of the system?
In fact, there would be little point in doing this if all we gained was a description of the dynamics in a different set of variables. After all, the Lagrangian formalism will do the job of giving the equations of motion for the system perfectly well (or the Newton formalism, for that matter). We went through the trouble of constructing these formalisms not because we want to find more efficient methods of solving the dynamics of classical systems (although that is sometimes a useful byproduct of switching perspectives), but rather because we wanted to understand better the structure of classical mechanics - important ideas such as the action principle or the relation between symmetries and conserved charges become much more transparent in the Larangian and Hamiltonian formalisms
The advantage of switching to the Hamiltonian formalism is that we will be able to exhibit a rather deep and beautiful geometric structure to classical dynamics, which we will obtain a reciprocal of [[Noether's Theorem|Noether's theorem]]
Recall that Noether's theorem states that every symmetry has an associated conserved charge. We will see that in the Hamiltonian formalism that the conserved charge generates the symmetry: if we know the form of the conserved charge for a symmetry, we will be able to reconstruct systematically the infinitesimal form of the symmetry transformation
