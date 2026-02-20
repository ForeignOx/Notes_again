## Lemma
Let $f:U\to \mathbb{C}$ be a [[Continuity|continuous]] [[Functions|function]] on [[Open Sets|open set]] $U\subset \mathbb{C}$, then for any $\gamma:[a,b]\to \mathbb{C}$,
$$
\left| \int _{\gamma}f(z) \, dz  \right| \leq \int _{\gamma}\left| f(z) \right|  \, d\left| z \right|  
$$
### Proof
Claim: for any $h:[a,b]\to \mathbb{C}$, $\left| \int ^{b}_{a} h(t) \, dt \right|\leq \int ^{b}_{a} \left| h(t) \right| \, dt$
Note that $\int ^{b}_{a} h(t) \, dt$ is simply a complex number which we write as $re^{ i\theta }$, or even better
$$
\int ^{b}_{a} h(t) \, dt= \left| \int ^{b}_{a} h(t) \, dt  \right| e^{ i\theta } 
$$
$$
\implies \left| \int ^{b}_{a} h(t) \, dt  \right| =e^{ i\theta }\int ^{b}_{a} h(t) \, dt=\mathfrak{R}\left( e^{ -i\theta }\int ^{b}_{a} h(t) \, dt  \right)  
$$
$$
= \mathfrak{R}\left( \int ^{b}_{a} e^{ -i\theta }h(t) \, dt  \right)=\int ^{b}_{a} \mathfrak{R}(e^{ -i\theta }h(t)) \, dt \leq \int ^{b}_{a} \left| e^{ -i\theta }h(t) \right|  \, dt=\int ^{b}_{a} \left| h(t) \right|  \, dt  
$$
Soooo
$$
\left| \int _{\gamma}f(z) \, dz  \right| =\left| \int ^{b}_{a} f(\gamma(t))\gamma'(t) \, dt  \right| \leq \int ^{b}_{a} \left| f(\gamma(t)) \right| \left| \gamma'(t) \right|  \, dt =\int _{\gamma}\left| f(z) \right|  \, d\left| z \right|  
$$
