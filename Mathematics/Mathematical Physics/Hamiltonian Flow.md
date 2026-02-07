Denote by $\mathscr{F}$ the space of all [[Functions|functions]] from [[Phase Spaces|phase space]] $\mathscr{P}$ to $\mathbb{R}$
Given any function $f\in\mathscr{F}$, we can define an operator $\Phi_{f}$ that generates infinitesimal transformations on $\mathscr{F}$ using the [[Poisson Bracket|poisson bracket]]
## Definition
The hamiltonian flow defined by $f:\mathscr{P}\to \mathbb{R}$ is the infinitesimal transformation on $\mathscr{F}$ defined by
$$
\Phi_{f}^{(\varepsilon)}:\mathscr{F}\to \mathscr{F}
$$
$$
 \Phi_{f}^{(\varepsilon)}(g)=g+\varepsilon \left\{ g,f \right\}+\mathcal{O}(\varepsilon^{2})
$$
## Remark
This is the infinitesimal version of what is commonly known as the Hamiltonian flow in literature, which is typically defined for finite transformations. The finite version of the transformation is obtained by the exponentiation:
$$
\Phi_{f}^{(a)}(g):=e^{ a\left\{ \cdot,f \right\} }g=g+a\left\{ g,f \right\}+\frac{a^{2}}{2!}\left\{ \left\{ g,f \right\},f \right\}+\frac{a^{3}}{3!}\left\{ \left\{ \left\{ g,f \right\},f \right\},f \right\}+\dots
$$
___
By studying the action of $\Phi_{f}^{(\varepsilon)}$ on the coordinates $\underline{q},\underline{p}$ of the phase space, we can also understand $\Phi_{f}^{(\varepsilon)}$ as the generator of a map from phase space to itself. We have
$$
\Phi_{f}^{(\varepsilon)}(q_{i})=q_{i}+\varepsilon \left\{ q_{i},f \right\}+\mathcal{O}(\varepsilon^{2})=q_{i}+\varepsilon \frac{ \partial f }{ \partial p_{i} } +\mathcal{O}(\varepsilon^{2})
$$
$$
 \Phi_{f}^{(\varepsilon)(p_{i})}=p_{i}+\varepsilon \left\{ p_{i},f \right\}+\mathcal{O}(\varepsilon^{2})=p_{i}-\varepsilon \frac{ \partial f }{ \partial q_{i} } +\mathcal{O}(\varepsilon^{2})
$$
The two definitions are compatible:
$$
\Phi_{f}^{(\varepsilon)}(g)=g(q_{1}+\varepsilon \left\{ q_{1},f \right\},\dots,q_{n}+\varepsilon \left\{ q_{n},f \right\},p_{1}+\varepsilon \left\{ p_{1},f \right\},\dots,p_{n}+\varepsilon \left\{ p_{n},f \right\})
$$
$$
= g(q_{1},\dots,q_{n},p_{1},\dots,p_{n})+\varepsilon \sum_{i=1}^{n}\left( \frac{ \partial g }{ \partial q_{i} } \left\{ q_{i},f \right\}+\frac{ \partial g }{ \partial p_{i} } \left\{ p_{i},f \right\} \right)
$$
$$
= g(q_{1},\dots,q_{n},p_{1},\dots,p_{n})+\varepsilon \sum_{i=1}^{n}\left( \frac{ \partial g }{ \partial q_{i} } \frac{ \partial f }{ \partial p_{i} } -\frac{ \partial g }{ \partial p_{i} } \frac{ \partial f }{ \partial q_{i} }  \right)=g+\varepsilon \left\{ g,f \right\}
$$
Where in the second line, we have done a [[Taylor Series|Taylor]] expansion, and we have omitted higher order terms in $\varepsilon$ throughout for notational simplicity
## Example
As a simple example, consider a particle moving in one dimension. The Hamiltonian flow $\Phi_{p}$ associated to the canonical momentum $p$ acts on phase space functions as:
$$
\Phi_{p}^{(\varepsilon)}(g(q,p))=g(q,p)+\varepsilon \frac{ \partial g }{ \partial q } +\mathcal{O}(\varepsilon^{2})
$$
Alternatively, $\Phi_{p}^{(\varepsilon)}$ acts on the coordinate $q$ as $q\to q+\varepsilon$, o the effect of $\Phi_{p}^{(\varepsilon)}$ on the phase space is a uniform shift in the $q$ direction
![[Pasted image 20260204225718.png]]
We can reproduce the effect on arbitrary functions of $q$ from this viewpoint by doing a Taylor expansion:
$$
g(q+\varepsilon,p)=g(q,p)+\varepsilon \frac{ \partial g }{ \partial p } +\mathcal{O}(\varepsilon^{2})
$$
One might also find it interesting to reproduce the full form of the Taylor expansion of $f(x+a)$ around $x$ using the exponentiated version of the definition
___
As a second example, consider a particle of unit mass moving in two dimension, expressed in Cartesian coordinates, which we call $q_{1},q_{2}$. We choose the Lagrangian to be of the form
$$
L=\frac{1}{2}(\dot{q}_{1}^{2}+\dot{q}_{2}^{2})-V(q_{1},q_{2})
$$
For the function generating the flow, we will choose $j=q_{1}\dot{q}_{2}-q_{2}\dot{q}_{1}$ (this is in fact [[Angular Momentum|angular momentum]] which [[Noether's Theorem|Noether's theorem]] associated with rotations around the origin)
From the Lagrangian, we have $p_{1}=\dot{q}_{1},p_{2}=\dot{q}_{2}$, so in terms of standard $\underline{q},\underline{p}$ coordinates of phase space, we have
$$
J(\underline{q},\underline{p})=q_{1}p_{1}-q_{2}p_{1}
$$
The Hamiltonian flow $\Phi_{J}^{(\varepsilon)}$ then acts on phase space as:
$$
\Phi_{J}^{(\varepsilon)}(q_{1})=q_{1}+\varepsilon \left\{ q_{1},J \right\}=q_{1}+\varepsilon \frac{ \partial J }{ \partial p_{1} } =q_{1}-\varepsilon q_{2}
$$
$$
 \Phi_{J}^{(\varepsilon)}(q_{2})=q_{2}+\varepsilon \left\{ q_{2},J \right\}=q_{2}+\varepsilon \frac{ \partial J }{ \partial p_{2} } =q_{2}+\varepsilon q_{1}
$$
$$
\Phi_{J}^{(\varepsilon)}(p_{1})=p_{1}+\varepsilon \left\{ p_{1},J \right\}=p_{1}-\varepsilon \frac{ \partial J }{ \partial q_{1} } =p_{1}-\varepsilon p_{2}
$$
$$
 \Phi_{J}^{(\varepsilon)}(p_{2})=p_{2}+\varepsilon \left\{ p_{2},J \right\}=p_{2}-\varepsilon \frac{ \partial J }{ \partial q_{2} } =p_{2}+\varepsilon p_{1}
$$
Omitting higher orders in $\varepsilon$
So the effect of $J$ on the coordinates can be written as an infinitesimal rotation on the $\underline{q}$ and the $\underline{p}$ (independently):
$$
\Phi_{J}^{(\varepsilon)}\begin{pmatrix}
q_{1} \\
q_{2}
\end{pmatrix}=\begin{pmatrix}
1 & -\varepsilon \\
\varepsilon & 1 
\end{pmatrix}\begin{pmatrix}
q_{1} \\
q_{2}
\end{pmatrix}
$$
$$
\Phi_{J}^{(\varepsilon)}\begin{pmatrix}
p_{1} \\
p_{2}
\end{pmatrix}=\begin{pmatrix}
1 & -\varepsilon \\
\varepsilon & 1 
\end{pmatrix}\begin{pmatrix}
p_{1}  \\
p_{2}
\end{pmatrix}
$$
For instance, the action of $\Phi_{J}^{(\varepsilon)}$ on the $(q_{1},q_{2})$ slice of phase space (which in this case has four dimensions) is as in the following picture:
![[Pasted image 20260204231453.png]]
## Flows for Conserved Charges
We have just seen that linear momentum $p$ generates spatial translations, and angular momentum generates rotations. This is in fact general: assume that we have a transformation acting as $q_{i}\to q_{i}+\varepsilon a_{i}(\underline{q})+\mathcal{O}(\varepsilon^{2})$ on the generalised coodinates
Noether's theorem assigns a charge to this transformation given, in the Lagrangian framework, by
$$
Q(\underline{q},\dot{\underline{q}},t)=\left( \sum_{i=1}^{n}a_{i}(\underline{q})\frac{ \partial L(\underline{q},\underline{\dot{q}},t) }{ \partial \dot{q}_{i} }  \right)-F(\underline{q},t)
$$
This charge can be written in the Hamiltonian framework in terms of generalised coordinates and generalised momenta as:
$$
Q(\underline{q},\underline{p},t)=\left( \sum_{i=1}^{n}a_{i}(\underline{q})p_{i} \right)-F(\underline{q},t)
$$
If we now compute the Hamiltonian flow associated to this charged on the generalised coordinates, we find
$$
\Phi_{Q}^{(\varepsilon)}(q_{i})=q_{i}+\varepsilon \left\{ q_{i},Q \right\}+\mathcal{O}(\varepsilon^{2})=q_{i}+\varepsilon a_{i}+\mathcal{O}(\varepsilon^{2})
$$
### Remark
This is a very important result: Noether's theorem told us that [[Symmetries of Configuration Spaces|symmetries]]  imply the existance of conserved quentities
We have just seen that we can go in the other direction too: conserved quantities generate the correspondig symmetry transformations via the associated Hamiltonian flow

