## Build Up
We use our equations for the electric and magnetic fields in terms of the vector and scalar potentials, and substitute them into Maxwell's equations, then
$$
-\nabla^{2}\varphi -\frac{ \partial  }{ \partial t } \underline{\nabla} \cdot \underline{A} -\frac{1}{\varepsilon_0}\rho=0 
$$
$$
\implies -\underline{\nabla} \cdot \left( \underline{\nabla } \varphi+\frac{ \partial  }{ \partial t } \underline{A} \right)-\frac{1}{\varepsilon_{0}}\rho=0
$$
$$
\underline{\nabla} \times (\underline{\nabla} \times \underline{A} )=\mu_{0}\underline{J}-\mu_{0}\varepsilon_{0}\frac{ \partial  }{ \partial t } \left( \underline{\nabla } \varphi+\frac{ \partial \underline{A} }{ \partial t }  \right) 
$$
$$
\implies -c^{2}\underline{\nabla} \times (\underline{\nabla} \times \underline{A} )-\frac{ \partial  }{ \partial t }\left( \underline{\nabla } \varphi+\frac{ \partial \underline{A} }{ \partial t }  \right)+\frac{1}{\varepsilon_{0}}\underline{J}=0  
$$
We are looking for a function $S[\varphi,\underline{A}]$, such that $\frac{\delta S}{\delta \varphi}=0$ and $\frac{\delta S}{\delta \underline{A}}=0$ gives us our two equations
The action is in fact:
$$
    S[\varphi,\underline{A}]=\int \frac{\varepsilon_{0}}{2}\underline{E}^{2}-\frac{1}{2\mu_{0}}\underline{B}^{2}-\varphi \rho+\underline{A}\cdot \underline{J} \, dt~d^{3}\underline{x} 
$$
With $\underline{E}$ and $\underline{B}$ written as above
## Gauge Invariance


