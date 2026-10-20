## Definition
Let $\underline{\alpha}:I\to \mathbb{R}^{2}$ be a [[Smooth Functions|smooth]] regular [[Plane Curves|plane]] [[Curves|curve]] and $\underline{t}:I\to \mathbb{R}^{2}$ be its unit [[Unit Tangent Vectors|tangent vector]], $u_{0}\in I$ and 
$$
\ell(u)=\int_{u_{0}}^{u} \lvert \lvert \underline{\alpha}'(t) \rvert \rvert  \, dt 
$$
Then the curve $\underline{\beta}:I\to \mathbb{R}^{2}$, given by
$$
\underline{\beta}(u):=\underline{\alpha}(u)-\ell(u)\underline{t}(u)
$$
Is called an involute of $\underline{\alpha}$
Note that we have $\underline{\beta}(u_{0})=\underline{\alpha}(u_{0})$ and that the definition of the curve $\underline{\beta}$ depend on the choice of $u_{0}\in I$
## Example
Consider the catenary
$$
\underline{\alpha}(u)=(u,\cosh u)
$$
$$
\underline{\alpha}'(u)=(1,\sinh(u))
$$
$$
 \lvert \lvert \underline{\alpha}'(u) \rvert \rvert =\cosh(u)
$$
$$
\ell(u)=\int_{0}^{u_{0}} \cosh t \, dt=\sinh(u) 
$$
$$
\underline{t}(u)=(\mathrm{sech}(u),\tanh(u))
$$
So
$$
\underline{\beta}(u)=\underline{\alpha}(u)-\ell(u)\underline{t}(u)=(u-\tanh u,\mathrm{sech}(u))
$$
