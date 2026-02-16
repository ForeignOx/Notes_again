## Derivation
Given a close region $V\subset \mathbb{R}^{3}$ with boundary $S=\partial V$, the change $\frac{d Q_{V}}{dt}$ can only be accounted for by the flow of charge $I_{S=\partial V}(t)$:
$$
\frac{d Q_{V}}{dt} =-I_{\partial V}(t)
$$
$$
\frac{d Q_{V}}{dt} (t)=\frac{d}{dt} \left( \int _{V} \rho(t,\underline{x}) \, d V \right)=\int _{V} \frac{ \partial \rho(t,\underline{x}) }{ \partial t }  \, dV 
$$
$$
    I_{\partial V}(t)=\int _{\partial V} \underline{J}(t,\underline{x})\cdot \, d \underline{S}=\int _{V}\underline{\nabla} \cdot \underline{J}(t,\underline{x})  \, dV
$$
Which tells us that
$$
\int _{V} \frac{ \partial \rho(t,\underline{x}) }{ \partial t }  \, dV = -\int _{V} \underline{\nabla} \cdot \underline{J} (t,\underline{x}) \, dV 
$$
$$
\implies \int _{V}\frac{ \partial \rho(t,\underline{x}) }{ \partial t } +\underline{\nabla} \cdot \underline{J} (t,\underline{x}) \, dV =0  
$$
For any $V$. This means that
$$
\frac{ \partial \rho(t,\underline{x}) }{ \partial t } +\underline{\nabla} \cdot \underline{J} (t,\underline{x})=0
$$
Which is called the charge continuity equation