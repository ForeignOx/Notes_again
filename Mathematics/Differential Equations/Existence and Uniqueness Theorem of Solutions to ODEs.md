## Theorem
Consider the system of [[First Order Ordinary Differential Equations|ODEs]] 
$$
\begin{cases}
\frac{d \underline{X}}{d\tau} (\tau)=\underline{f}(\tau,\underline{X}(\tau)) \\
\underline{X}(t_{0})=\underline{X}_{0}
\end{cases}
$$
Where $\underline{f}:\mathbb{R}\times \mathbb{R}^{n}\to \mathbb{R}^{n}$, $t_{0}\in\mathbb{R}$, $\underline{X}_{0}\in\mathbb{R}^{n}$ are given. Assume there exists $\delta>0$ and $M>0$ such that $\underline{f}$ is continuous in its first variable on $[t_{0}-\delta,t_{0}+\delta]\times \overline{B_{M}(\underline{X}_{0})}$ and that there exists $L(\underline{X}_{0})$ such that 
$$
\left| \underline{f}(\tau,\underline{X})-\underline{f}(\tau,\underline{Y}) \right| \leq L(\underline{X}_{0})\left| \underline{X}-\underline{Y} \right| 
$$
For all $(\tau,\underline{X})\in[t_{0}-\delta,t_{0}+\delta]\times \overline{B_{M}(\underline{X}_{0})}$, then there exists $\varepsilon>0$ and a unique continuously differentiable function $\underline{X}:(t_{0}-\varepsilon,t_{0}+\varepsilon)\to \mathbb{R}^{n}$ that solves the ODE system
### Proof
The idea is to rewrite the ODE as an integral equation:
$$
\underline{X}(t)=\underline{X}_{0}+\int_{t_{0}}^{t} f(\tau,\underline{X}(\tau)) \, d\tau 
$$
For all $t\in(t_{0}-\varepsilon,t_{0}+\varepsilon)$
We define the operator $T$ from continuous functions on $(t_{0}-\delta,t_{0}+\delta)$ to $\mathbb{R}^{m}$ to continuous functions on $(t_{0}-\delta,t_{0}+\delta)$ to $\mathbb{R}^{m}$ by
$$
T(\underline{g})(t)=\underline{X}_{0}+\int_{t_{0}}^{t} \underline{f}() \, dx 
$$