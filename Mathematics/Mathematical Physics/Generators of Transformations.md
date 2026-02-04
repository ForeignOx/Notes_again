## Definition
We define the generator $a_{i}$ of a [[Transformations of Configuration Spaces|transformation]] to be 
$$
a_{i}=\lim_{ \varepsilon \to 0 }  \frac{\phi(\varepsilon)-\phi(0)}{\varepsilon}=\frac{d \phi(\varepsilon)}{d\varepsilon} \Bigg{|}_{\varepsilon=0} 
$$
So in coordinates,
$$
q_{i}\to \phi_{i}(\varepsilon)=\phi_{i}(0)+\varepsilon \frac{d \phi_{i}}{d\varepsilon} \Bigg{|}_{\varepsilon=0}+\mathcal{O}(\varepsilon^{2}) 
$$
By [[Taylor Series|Taylor expansion]], soo
$$
q_{i}\to q;_{i}=q_{i}+\varepsilon a_{i}+\mathcal{O}(\varepsilon^{2})
$$
## Lemma
The [[Euler-Lagrange Equations|Euler-Lagrange]] equations of motion do not change under
$$
L\to L+\frac{d F(\underline{q},t)}{dt} 
$$
Where $F$ depends only on $\underline{q}$, not $\underline{\dot{q}}$
### Proof
Plug $L'$ into the Euler-Lagrange equations and show
$$
\frac{d }{dt} \left( \frac{ \partial L' }{ \partial \dot{q}_{i} }  \right)-\frac{ \partial L' }{ \partial q_{i} } =\frac{d }{dt} \left( \frac{ \partial L }{ \partial \dot{q}_{i} }  \right)-\frac{ \partial L }{ \partial q_{i} } 
$$
The second part is that our action changes, so
$$
S'=\int_{t_{0}}^{t_{1}} L' \, dt =\int_{t_{0}}^{t_{1}} L \, dt+\int_{t_{0}}^{t_{1}} \frac{d F}{dt}  \, dt=S+F(\underline{q}(t_{1}),t_{1})-F(\underline{q}(t_{0}),t_{0})
$$
Since we are considering all paths such that $\underline{q}(t_{0})=\underline{q}_{0}(t_{0}),\underline{q}(t_{1})=\underline{q}_{0}(t_{1})$, this doesn't affect what we are looking for:
$$
\delta S'=\delta S+\cancel{ \delta F(\underline{q}(t_{1}),t_{1}) }-\cancel{ \delta F(\underline{q}(t_{0}),t_{0}) }
$$
