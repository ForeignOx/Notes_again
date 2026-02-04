Let $f(x),g(x)$ be two [[Functions|functions]], then the convolution of $f$ and $g$ is defined to be:
$$
    (f*g)(x)=\int_{-\infty}^{\infty} f(t)g(x-t) \, dt 
$$
This is a [[Bilinear Form|bilinear]] [[Inner Product|inner product]], if $f=\alpha f_{1}+\beta f_{2}$, then
$$
f*g=(\alpha f_{1}+\beta f_{2})*g=\alpha f_{1}*g+\beta f_{2}*g
$$
The product is symmetric; $f*g=g*f$:
$$
f*g=\int_{-\infty}^{\infty} f(t)g(x-t) \, dt
$$
Let $t'=x-t$, then $dt'=-dt$, so
$$
=\int_{-\infty}^{\infty} f(x-t')g(t') \,( -dt' )=\int_{-\infty}^{\infty} g(t')f(x-t') \, dt'=g*f 
$$
