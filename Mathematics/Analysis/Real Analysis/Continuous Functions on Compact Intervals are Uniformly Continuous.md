Lef $f$ be a [[Continuity|continuous]] [[Functions|function]] on a compact [[Intervals|interval]] $[a,b]$, then $f$ is [[Uniform Continuity|uniformly continuous]] on $[a,b]$
## Proof
Assume $f$ is not uniformly continuous, this means
$$
\exists\varepsilon>0:\forall\delta>0\exists x,y\in [a,b]\text{ with }\left| x-y \right| <\delta \text{ but }\left| f(x)-f(y) \right| \geq\varepsilon
$$
Fix such an $\varepsilon>0$ and take $\delta=\delta_{n}=\frac{1}{n}$ for all $n\in\mathbb{N}$. We find $x_{n},y_{n}\in[a,b]$ such that
$$
\left| x_{n}-y_{n} \right| <\frac{1}{n}
$$
But 
$$
\left| f(x_{n})-f(y_{n}) \right| \geq\epsilon
$$
Using the [[Bolzano-Weierstrass Theorem|Bolzano-Weierstrass Theorem]]

#Mathematics #Analysis #Theorem 