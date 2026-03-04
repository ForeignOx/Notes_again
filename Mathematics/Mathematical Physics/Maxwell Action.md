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
The [[Action Principle|action]] is in fact Maxwell's actions:
$$
    S[\varphi,\underline{A}]=\int \frac{\varepsilon_{0}}{2}\underline{E}^{2}-\frac{1}{2\mu_{0}}\underline{B}^{2}-\varphi \rho+\underline{A}\cdot \underline{J} \, dt~d^{3}\underline{x} 
$$
With $\underline{E}$ and $\underline{B}$ written as above
## Gauge Invariance
If we use our action with our gauge invariance terms, we get
$$
S\left[ \varphi-\frac{ \partial \chi }{ \partial t } ,\underline{A}+\underline{\nabla } \chi \right]=\int \frac{\varepsilon_{0}}{2}\underline{E}^{2}-\frac{1}{2\mu_{0}}\underline{B}^{2}-\left( \varphi-\frac{ \partial \chi }{ \partial t }  \right)+(\underline{A}+\underline{\nabla } \chi)\cdot \underline{J} \, dt~d^{3}\underline{x} 
$$
$$
        = S[\varphi,\underline{A}]+\int \frac{ \partial \chi }{ \partial t } \rho+\underline{\nabla } \chi\cdot \underline{J} \, dt~d^{3}\underline{x} 
$$
$$
    = S[\varphi,\underline{A}]+\int \cancelto{ 0 }{ \frac{ \partial \chi \rho }{ \partial t } } +\cancelto{ 0 }{ \underline{\nabla} \cdot (\chi \underline{J})  } \, dt~d^{3}\underline{x} -\int \left( \frac{ \partial  }{ \partial t } \rho+\underline{\nabla} \cdot \underline{J}  \right)\chi \, dt~d^{3}\underline{x}
$$
But  $\frac{ \partial \rho }{ \partial t }+\underline{\nabla} \cdot \underline{J}=0$ because of charge continuity, so we see that Gauge invariance is intimately related to charge conservation
## Example
Consider an electromagnetic pulse in empty space with $\underline{E}(x,t)=f(x-ct)\underline{e}_{y}$ and $f$ a square integrable function such that
$$
    \int_{-\infty}^{\infty} f^{2}(s) \, ds=U<\infty
$$
We first compute the total energy $U_{V}$ of the pule inside the infinite rectangular prism
$$
V=\left\{ (x,y,z):\middle|: x\in \mathbb{R},0<y<L_{y},0<z<L_{z} \right\}
$$
We want to compute the rate $W_{S}$ at which the energy flows through the rectangular 
