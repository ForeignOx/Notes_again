A natural method for parametrising [[spacecurves|spacecurves]] is by arclength, denoted $s$. The arclength of some spacecurve can be related to an arbitrary parametrisation $t$ as:
$$
s(t)=\int_{0}^{t} \sqrt{ (x'(t))^{2}+(y'(t))^{2}+(z'(t))^{2} } \, dt
$$
Where $s$ represents the total distance travelled along the curve. This is derived from the [[Line Integrals|line integral]] form of arclength.
The derivative of a curve $\underline{x}$ parametrised by $s$ is always of unitary value; $\left| \underline{x}'(s) \right|=1$, thus the [[Tantrix Curves|tantrix]] is given by $\underline{\hat{T}}_{\underline{x}}(s)=\underline{x}'(s)$
## Definition
The arclength of a segment of a curve $\underline{\alpha}:I\to \mathbb{R}^{n}$ given by $\underline{\alpha}|_{[a,b]}$ with $[a,b]\in I$.
We choose a partition of $[a,b]$, that is,
$$
a=u_{0}<u_{1}<\dots<u_{m}=b
$$
And approximaate the length of $\underline{\alpha}:[a,b]\to \mathbb{R}^{n}$By the expression
$$
\sum_{i=0}^{m-1}\lvert \lvert \underline{\alpha}(u_{i+1})-\underline{\alpha}(u_{i}) \rvert \rvert 
$$
Which is nothing but the length of the piecewise linear approxiamtion of $\underline{\alpha}|_{[a,b]}$ by consecutive points $\underline{\alpha}(u_{0}),\underline{\alpha}(u_{1}),\dots ,\underline{\alpha}(u_{m})$ on the curve
If we take a refinement of this partition