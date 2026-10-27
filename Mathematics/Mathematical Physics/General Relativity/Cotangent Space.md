The cotangent space $T_{p}^{*}$ is the dual space to $T_{p}$, so the space of linear maps $\omega:T_{p}\to \mathbb{R}$, $V\to\omega(V)$, i.e. elements of $T^{*}_{p}$ map elements of $T_{p}$ to reals
Linearity means that $\omega$ is characterised by its action on the bais vectors $\left\{ \partial_{\mu} \right\}$
Defining $\omega_{\mu}=\omega(\partial_{\mu})$, we have:
$$
\omega(V)=\omega(V^{\mu}\partial_{\mu})=V^{\mu}\omega(\partial_{\mu})=V^{\mu}\omega_{\mu}
$$
The simplest example of a cotangent vector is the differential of a function $f$:
$$
\omega=df
$$
So 
$$
\omega(V)=df(V)=V(f)
$$
To find the component of $(df)_{\mu}$ of $df$, we act on a basis vector $\partial_{\mu}$:
$$
\omega_{\mu}=\omega(\partial_{\mu}) 
$$
$$
\implies  (df)_{\mu}=df(\partial_{\mu})=\partial_{\mu}f=\frac{d f}{dx^{\mu}} 
$$
So the corresponding basis covectors are the coordinate differentials $\left\{ dx^{\mu} \right\}$
To see this, choose $f=x^{\nu}$, then
$$
df(V)=V(f)=dx^{\nu}\partial_{\mu}=\partial_{\mu}x^{\nu}=\frac{ \partial x^{\nu} }{ \partial x^{\mu} } =\delta^{\nu}_{\mu}
$$
Sooooo the $\left\{ dx^{\mu} \right\}$ form a basis for $T_{p}^{*}$. This basis is dual to that for $T_{p}$ formed by the partial derivatives $\left\{ \partial_{\mu} \right\}$
By linearlity, we can decompose $\omega=\omega_{\nu}dx^{\nu}$
