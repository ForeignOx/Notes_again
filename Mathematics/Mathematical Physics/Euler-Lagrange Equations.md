## 1D
Consider a particle moving in one dimension and we want to determine its motion. Its trajectory is given by a function $x(t)$ with $t$ the time coordinate. For many physical problems, [[Newton's Second Law of Motion|equations of motion]] are second order in $x(t)$, so we need data to fix two integration constants. In the Lagrangian formalism these are given by fixing the initial and final positions. That is, we will assume that we know the initial position of the particle $x(t_{0})$ at time $t_{0}$ and its final position $x(t_{1})$ at time $t_{1}$
### Equation
$$
\frac{ \partial L }{ \partial x } -\frac{d }{dt} \frac{ \partial L }{ \partial \dot{x} } =0
$$
### Derivation
Whenever a Lagrangian exists, the [[Action Principle|variational principle]] together with the fundamental lemma of the calculus of variations leads to a set of [[Differential Equations|differential equations]] that determine $x(t)$
The argument is as follows. If we [[Taylor Series|Taylor]] expand the perturbed Lagrangian to first order in $\delta x(t)$, we get
$$
L(x(t)+\delta x(t),\dot{x}(t)+\delta \dot{x}(t))=L(x(t),\dot{x}(t))+\frac{ \partial L }{ \partial x } \delta x(t)+\frac{ \partial L }{ \partial \dot{x} } \delta \dot{x}(t)+\dots
$$
Putting this expansion of the Lagranginan into the variation of the action we have:
$$
\delta S = \int_{t_{0}}^{t_{1}} L(x(t)+\delta x(t),\dot{x}(t)+\delta \dot{x}(t))-L(x(t),\dot{x}(t)) \, dt 
$$
$$
    = \int_{t_{0}}^{t_{1}} \frac{ \partial L }{ \partial x } \delta x(t)+\frac{ \partial L }{ \partial \dot{x} } \delta \dot{x}(t) \, dt
$$
Where we have ommitted second order or higher in $\delta x$
We can make this assumtion since any time we are expanding on $\delta x$, we are expanding on a small parameter $\epsilon$ inside $\delta x(t)=\epsilon z(t)$, where $z(t)$ is defined as in [[Stationary Functions|stationary functions]]
The variation $\delta \dot{x}(t)=\epsilon \dot{z}(t)$ clearly has the same dependence on $\epsilon$, since $\epsilon$ is just a constant that does not depend on time. We therefore have that $\delta \dot{x}(t)$ is first order in $\delta x(t)$, at least for the purposes of counting degrees when expanding
[[Integration by Parts|Integrating by parts]] for the second term allos us to rewrite this:
$$
\delta S=\int_{t_{0}}^{t_{1}} \left( \frac{ \partial L }{ \partial x } -\frac{d }{dt} \frac{ \partial L }{ \partial \dot{x} }  \right) \delta x(t)+\frac{d }{dt} \left( \delta x(t)\frac{ \partial L }{ \partial \dot{x} }  \right)\, dt 
$$
The last term is a total derivative, so we can integrate it to give:
$$
\delta S=\left[ \delta x(t)\frac{ \partial L }{ \partial \dot{x} }  \right]_{t_{0}}^{t_{1}}+\int_{t_{0}}^{t_{1}} \left( \frac{ \partial L }{ \partial x } -\frac{d }{dt} \frac{ \partial L }{ \partial \dot{x} } \right)\delta x(t)  \, dx 
$$
Now we have that $\delta x(t_{0})=\delta x(t_{1})=0$ by definition, as the paths that we consider all start and end on the same positions. This implies that the first teerm vanishes, so
$$
\delta S=\int_{t_{0}}^{t_{1}} \left( \frac{ \partial L }{ \partial x } -\frac{d }{dt} \frac{ \partial L }{ \partial \dot{x} }  \right)\delta x(t) \, dt 
$$
We recall that the action principle demands that this variation cancels (to first order in $\delta x(t)$) for arbitrary $\delta x(t)$. By the [[Fundamental Lemma of the Calculus of Variations|fundamental lemma of the calculus of variations]], the only way that this could possibly be true is if the function multiplying $\delta x(t)$ in the integral vanihes;
$$
\frac{ \partial L }{ \partial x } -\frac{d }{dt} \frac{ \partial L }{ \partial \dot{x} } =0
$$
Which is known as the Euler-Lagrange equation, in the case of 1-D problems
___
A somewhat subtle point in the Lagrangian formulation is to note that the lagrangian $L$ is nothing more than an ordinary function of two parameters and knows nothing about paths. (with $N$ generalised coordinates, it is a function of $2N$ parameters)
When using the Lagrangian function to construct the action, we evaluated the function at $(x(t),\dot{x}(t))$ at each instant in time, but it is important to keep in mind that the Lagrangian itself treates $x(t)$ and $\dot{x}(t)$ are independent variables
In general, if we wanted to study how this function changes under small displacements of $x$ and $\dot{x}$, we would use the chain rule:
$$
L(x+\delta x,\dot{x}+\delta \dot{x})=L(x,\dot{x})+\frac{ \partial L }{ \partial x } \delta x+\frac{ \partial L }{ \partial \dot{x} } \delta \dot{x}+\dots
$$
Where the dots determine higher order in $\delta x$ and $\delta \dot{x}$
What this all means is that the partial derivatives treat the first and second arguments of the function independently, leading to some interesting rules;
$$
\frac{ \partial x }{ \partial \dot{x} } =\frac{ \partial \dot{x} }{ \partial x } =0
$$
This also makes it clear that the rules are not something that one should expect to hold outside of the Lagrangian formalism. And indeed, when we study the Hamiltonian framework  this rule will be replaced by a different one