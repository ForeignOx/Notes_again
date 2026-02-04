The total [[Energy|energy]] of an isolated system is constant, though it can be transferred within the system
## In the Newtonian Sense
A particle of mass $m$ moving in a conservative force $\underline{F}$ has conserved energy $E$, where
$$
E=\frac{1}{2}mv^{2}+V
$$
Where $v$ is its speed. Again the first part is the kinetic energy, the second part is the potential energy
So $\frac{d E}{dt}=0$
#### Proof
First:
$$
\frac{d V}{dt} =\frac{ \partial V }{ \partial x } \frac{d x}{dt} +\frac{ \partial V }{ \partial y } \frac{d y}{dt} +\frac{ \partial V }{ \partial z } \frac{d z}{dt} 
$$
Write
$$
\underline{F}=F_{x}\underline{e}_{1}+F_{y}\underline{e}_{2}+F_{z}\underline{e}_{3}
$$
Then
$$
\frac{d V}{dt} =-F_{x}\dot{x}-F_{y}\dot{y}-F_{z}\dot{z}=-\underline{F}\cdot  \underline{\dot{r}}
$$
Then using $v^{2}=\underline{\dot{r}}\cdot  \underline{\dot{r}}$
$$
\frac{d }{dt} \left( \frac{1}{2}mv^{2} \right)=\frac{d }{dt}\left( \frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2}) \right)=m(\dot{x}\ddot{x} +\dot{y}\ddot{y}+\dot{z}\ddot{z})-m \underline{\dot{r}}\cdot  \underline{\ddot{r}}
$$
Thus:
$$
\frac{d E}{dt} = \underline{\dot{r}}\cdot(m  \underline{\ddot{r}}-\underline{F})=0
$$
By equation of motion

## In the Lagrangian Sense
The Heuristic argument for conservation of energy
Consider $t\to t'=t+\varepsilon$, we look at each $q_{i}$:
$$
q_{i}(t)\to q_{i}(t+\varepsilon)=q_{i}(t)+\varepsilon \frac{d q_{i}}{dt} +\mathcal{O}(\varepsilon^{2})
$$
So we say $a_{i}=o\frac{d q_{i}}{dt}$
So 
$$
L(\underline{q}(t),\underline{\dot{q}}(t),t)\to L'=L(\underline{q}(t+\varepsilon),\underline{\dot{q}}(t+\varepsilon),t+\varepsilon)
$$
$$
= L(\underline{q}(t),\underline{\dot{q}}(t),t)+\varepsilon \frac{d L}{dt} +\mathcal{O}(\varepsilon^{2})
$$
This suggests taking $F=L$
We have defined energy in the Lagrangian formalism to be:
$$
E:=\left( \sum_{i=1}^{N}\dot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right)-L
$$
We claim that it is conserved
### Theorem
Along the solution of the equations of motion,
$$
\frac{d E}{dt} =-\frac{ \partial L }{ \partial t } 
$$
where
$$
\frac{ \partial L(\underline{q}(t),\underline{\dot{q}}(t),t)}{ \partial t } :=\lim_{ \varepsilon \to 0 }  \frac{L(\underline{q}(t),\underline{\dot{q}},t+\varepsilon)-L(\underline{q}(t),\underline{\dot{q}}(t),t)}{\varepsilon}
$$
This means that the energy is conserved if the Lagrangian doesn't dpend on time
#### Proof
We prove this by taking the derivative of the energy:
$$
\frac{d E}{dt} =\sum_{i=0}^{N}\frac{d }{dt}\left( \dot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right)-\frac{d L}{dt} 
$$
Where
$$
\frac{d L}{dt} =\sum_{i=1}^{N}\dot{q}_{i}\frac{ \partial L }{ \partial q_{i} } +\ddot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} } +\frac{ \partial L }{ \partial t } 
$$
$$
\frac{d}{dt} \left( \dot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right)=\ddot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} } +\dot{q}_{i}\frac{d}{dt} \left( \frac{ \partial L }{ \partial \dot{q}_{i} }  \right)=\ddot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} } +\dot{q}\frac{ \partial L }{ \partial q_{i} } 
$$
Using that $\frac{ \partial L }{ \partial q_{i} }=\frac{d}{dt}\left( \frac{ \partial L }{ \partial \dot{q}_{i} } \right)$, so
$$
\frac{d}{dt} E=\sum_{i=1}^{N}\left( \dot{q}_{i}\frac{ \partial L }{ \partial q_{i} } +\ddot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right)-\left( \sum_{i=1}^{N}\left( \dot{q}_{i}\frac{ \partial L }{ \partial q_{i}} +\ddot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} } \right) +\frac{ \partial L }{ \partial t }  \right)
$$
___
Alterate proof
Imagine that we take a path $\underline{q}(t)$ satisfying the equations of motion, and we displace it to a new path $\underline{q}'(t)=\underline{q}(t-\varepsilon)$. That is, we move the whole path slightly forward in time, keeping its shape. We have
$$
    S'=\int_{t_{0}}^{t_{1}} L(q_{1}'(t),\dots q_{N}'(t),\dot{q}_{1}'(t),\dots,\dot{q}_{N}'(t),t) \, dt 
$$
$$
= \int_{t_{0}}^{t_{1}} L(q_{1}(t-\varepsilon),\dots,q_{N}(t-\varepsilon),\dot{q}_{1}(t-\varepsilon),\dots,\dot{q}_{N}(t-\varepsilon),t) \, dt
$$
We can compute this expression in two different ways. First, by the [[Chain Rule|chain rule]], we have that
$$
L(q_{1}(t-\varepsilon),\dots,q_{N}(t-\varepsilon),\dot{q}_{1}(t-\varepsilon),\dots,\dot{q}_{N}(t-\varepsilon),t)=
$$
$$
 L(q_{1}(t),\dots,q_{N}(t),\dot{q}_{1}(t),\dots,\dot{q}_{N}(t),t)-\varepsilon \sum_{i=1}^{N}\left( \frac{ \partial L }{ \partial q_{i} } \dot{q}_{i}+\frac{ \partial L }{ \partial \dot{q}_{i} } \ddot{q}_{i} \right)+\mathcal{O}(\varepsilon^{2})
$$
Using the [[Euler-Lagrange Equations|Euler-Lagrange equations]] of motion, we can write this as
$$
\sum_{i=1}^{N}\left( \frac{ \partial L }{ \partial q_{i} } \dot{q}_{i}+\frac{ \partial L }{ \partial \dot{q}_{i} } \ddot{q}_{i} \right)=\sum_{i=1}^{N}\frac{d}{dt} \left( \frac{ \partial L }{ \partial \dot{q}_{i} }  \right)\dot{q}_{i}+\frac{ \partial L }{ \partial \dot{q}_{i} } \ddot{q}_{i}=\frac{d}{dt} \left( \sum_{i=1}^{N}\dot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right)
$$
Substituting these expressions into the [[Action Principle|action]], we have just proven that
$$
S'=S-\varepsilon\left[ \sum_{i=1}^{N}\dot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }  \right]_{t_{0}}^{t_{1}}+\mathcal{O}(\varepsilon^{2})
$$
On the other hand, introducing a new variable $t'=t-\varepsilon$, we can write
$$
S'=\int_{t_{0}}^{t_{1}} L(q_{1}(t-\varepsilon),\dots,q_{N}(t-\varepsilon),\dot{q}_{1}(t-\varepsilon),\dots ,\dot{q}_{N}(t-\varepsilon),t) \, dt 
$$
$$
= \int_{t_{0}-\varepsilon}^{t_{1}-\varepsilon} L(q_{1}(t'),\dots,q_{N}(t'),\dot{q}_{1}(t'),\dots,\dot{q}_{N}(t'),t'+\varepsilon) \, dt' 
$$
We can expand this as a series in $\varepsilon$ using [[Leibniz Rule|Leibniz' rule]], to get
$$
S'=S+\varepsilon \frac{d S'}{d\varepsilon}\Bigg{|}_{\varepsilon=0} +\mathcal{O}(\varepsilon^{2})
$$
$$
= S-\varepsilon L(q_{1}(t_{1}),\dots,q_{N}(t_{1}),\dot{q}_{1}(t_{1}),\dots,\dot{q}_{N}(t_{1}),t_{1})
$$
$$
 +\varepsilon L(q_{1}(t_{0}),\dots,q_{N}(t_{0}),\dot{q}_{1}(t_{0}),\dots,\dot{q}_{N}(t_{0}),t_{0})
$$
$$
 +\varepsilon \left[ \int_{t_{0}-\varepsilon}^{t_{1}-\varepsilon} \frac{ \partial L(q_{1}(t'),\dots,q_{N}(t'),\dot{q}_{1}(t'),\dots,\dot{q}_{N}(t'),t'+\varepsilon) }{ \partial \varepsilon }  \, dt'  \right]_{\varepsilon=0}+\mathcal{O}(\varepsilon^{2}) 
$$
Now, we note that by the chain rule, we have
$$
\frac{ \partial L(q_{1}(t'),\dots,q_{N}(t'),\dot{q}_{1}(t'),\dots,\dot{q}_{N}(t'),t'+\varepsilon) }{ \partial \varepsilon } =\frac{ \partial L(q_{1}(t'),\dots,q_{N}(t'),\dot{q}_{1}(t'),\dots,\dot{q}_{N}(t'),t'+\varepsilon) }{ \partial t' } 
$$
Soo
$$
\left[ \int_{t_{0}-\varepsilon}^{t_{1}-\varepsilon} \frac{ \partial L(q_{1}(t'),\dots,q_{N}(t'),\dot{q}_{1}(t'),\dots,\dot{q}_{N}(t'),t'+\varepsilon) }{ \partial \varepsilon }  \, dt' \right]_{\varepsilon=0} 
$$
$$
= \int_{t_{0}}^{t_{1}} \frac{ \partial L(q_{1}(t),\dots,q_{N}(t),\dot{q}_{1}(t),\dots,\dot{q}_{N}(t),t)}{ \partial t }  \, dt 
$$
The theorem now follows from equating the two expressions for $S'$ that we found
### Example
$$
E=\frac{1}{2}m\dot{x}^{2}+\frac{1}{2}t^{2}x^{2}
$$
$$
\implies \frac{d E}{dt} m\dot{x}\ddot{x}+x \dot{x}t^{2}-tx^{2}
$$
___
For 
$$
L=\frac{1}{2}m(\dot{x}_{1}^{2}+\dot{x}_{2}^{2}+\dot{x}_{3}^{2})-V(x_{1},x_{2},x_{3})
$$
Then
$$
E=\dot{x}_{1}\frac{ \partial L }{ \partial \dot{x}_{1} } +\dot{x}_{2}\frac{ \partial L }{ \partial \dot{x}_{2} } +\dot{x}_{3}\frac{ \partial L }{ \partial \dot{x}_{3} } -(T-V)=T+V
$$
Which we are familiar with, i.e. energy is the sum of kinetic and potential trms
One can show that $E=T+V$ if $L=T-V$ with $V=V(\underline{q})$ and $T=\sum_{i,j}K_{ij}(\underline{q})\dot{q}_{i}\dot{q}_{j}$
___
Consider a one dimensional spring with time dependent spring constant $\kappa(t)$:
$$
L=\frac{1}{2}m\dot{x}^{2}-\frac{1}{2}\kappa(t) x^{2}
$$
Then the Euler-Lagrange equation is 
$$
0=\frac{d}{dt} \left( \frac{ \partial L }{ \partial \dot{x} }  \right)-\frac{ \partial L }{ \partial x } =\frac{d}{dt} (m\dot{x})+\kappa(tx)=m\ddot{x}+\kappa(t)x
$$
So
$$
E=\dot{x}\frac{ \partial L }{ \partial \dot{x} } -L=m\dot{x}^{2}-L
$$
$$
= \frac{1}{2}m\dot{x}^{2}+\frac{1}{2}\kappa(t)x^{2}
$$
So
$$
\frac{d E}{dt} =m\dot{x}\ddot{x}+\kappa(t)x \dot{x}+\frac{1}{2} \frac{d \kappa(t)}{dt}x^{2}
$$
$$
= \dot{x}(m\ddot{x}+\kappa(t)x)+\frac{1}{2} \frac{d \kappa(t)}{dt} x^{2}=\frac{1}{2}x^{2}\frac{d \kappa}{dt} =-\frac{ \partial L }{ \partial t }  
$$
So in this case energy is not conserved, which makes sense as the lagrangian depends on $t$
___
Another example is the Lagrangian for a particle of mass $m$ in special relativity:
$$
L=-mc\sqrt{ c^{2}-\dot{x}^{2}-\dot{y}^{2}-\dot{z}^{2} }
$$
$$
E=\dot{x}\frac{ \partial L }{ \partial \dot{x} } +\dot{y}\frac{ \partial L }{ \partial \dot{y} } +\dot{z}\frac{ \partial L }{ \partial \dot{z} } -L
$$
$$
\dot{x}\frac{ \partial L }{ \partial \dot{x} } = \frac{mc\dot{x}^{2}}{\sqrt{ c^{2}-\dot{x}^{2}-\dot{y}^{2}-\dot{z}^{2} }}
$$
$$
 \dot{y}\frac{ \partial L }{ \partial \dot{y} } = \frac{mc\dot{y}^{2}}{\sqrt{ c^{2}-\dot{x}^{2}-\dot{y}^{2}-\dot{z}^{2} }}
$$
$$
 \dot{z}\frac{ \partial L }{ \partial \dot{z} } = \frac{mc\dot{z}^{2}}{\sqrt{ c^{2}-\dot{x}^{2}-\dot{y}^{2}-\dot{z}^{2} }}
$$
So
$$
E= \frac{mc(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2})}{\sqrt{c^{2}-\dot{x}^{2}-\dot{y}^{2}-\dot{z}^{2} }}+ \frac{mc(c^{2}-\dot{x}^{2}-\dot{y}^{2}-\dot{z}^{2})}{\sqrt{ c^{2}-\dot{x}^{2}-\dot{y}^{2}-\dot{z}^{2} }}
$$
$$
= \frac{mc^{3}}{\sqrt{ c^{2}-\dot{x}^{2}-\dot{y}^{2}-\dot{z}^{2} }}=\frac{mc^{2}}{\sqrt{ 1-\left( \frac{\underline{\dot{x}}}{c} \right)^{2} }}
$$
Now we know that $\left( \frac{\dot{\underline{x}}}{c} \right)^{2}\ll 1$ so
$$
E=mc^{2}+\frac{1}{2}m(\underline{\dot{x}})^{2}+\dots
$$
Which is nice innit
This also involves
$$
\gamma:= \frac{1}{\sqrt{ 1-\left( \frac{\underline{\dot{x}}}{c} \right)^{2} }}
$$
Which is the Lorentz factor






#Physics #Energy #Definition