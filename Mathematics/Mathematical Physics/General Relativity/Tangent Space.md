The tangent space is the [[Vectorspaces|vectorspace]] formed by the tangent vectors, $V^{\mu}=\frac{d x^{\mu}}{d\lambda}$ of all possible [[curves|curves]] through some point
We similarly define the cotangent space: the space of covectors formed from the gradients $\frac{ \partial f }{ \partial x^{\mu} }$ of all possible $f(x^{\mu})$ at some point
These are dual; so given some curve $x^{\mu}(\lambda)$ and function $f(x^{\mu})$,
$$
w_{\mu}V^{\mu}=\frac{ \partial f }{ \partial x^{\mu} } \frac{d x^{\mu}}{d\lambda} =\frac{d f}{d\lambda} 
$$
Which is the change in $f$ along a curve
____
Note this is baroque, elaborate, byzantine and spaghetti involving, but could be useful
Say we have a coordinate chart $\varphi:M\to \mathbb{R}^{n},p\mapsto x^{\mu}(p)$, 
A parametrised curve $\gamma:\mathbb{R}\to M,\lambda \mapsto p(\lambda)$ 
A smooth function $f:M\to \mathbb{R},p\mapsto f(p)$
The directional derivative of $f$ along the curve is:
$$
\frac{d }{d\lambda} f=\frac{d }{d\lambda} (f\circ \gamma)=\frac{d }{d\lambda} ((f\circ \varphi ^{-1})\circ (\varphi \circ \gamma))=\frac{d x^{\mu}}{d\lambda} \frac{ \partial f }{ \partial x^{\mu} } 
$$
Some of the function $f$ was arbitrary, the directional derivative (by itself) is
$$
\frac{d }{d\lambda} =\frac{d x^{\mu}}{d\lambda}\frac{ \partial  }{ \partial x^{\mu} }  
$$
So we can view the directional derivative $V=\frac{d }{d\lambda}$ as a coordinate free definition of the tangent vector to the curve $\gamma$
The $V^{\mu}=\frac{d x^{\mu}}{d\lambda}$ are now the components of the vector $V$;
The set of partial derivatives $\left\{ \partial_{\mu} \right\}=\left\{ \frac{ \partial  }{ \partial x^{0} },\frac{ \partial  }{ \partial x^{1} },\frac{ \partial  }{ \partial x^{2} },\dots \right\}$ are the corresponding basis vectors
Thus $V=V^{\mu}\partial_{\mu}$ is a coordinate independent vector, but our basis vectors are still coordinate dependent
The space of directional derivative operators along curves through $p \in M$ forms a vectorspace which is the tangent space $T_{p}$
These satisfy vectorspace axioms, if $V=\frac{d }{d\lambda},W=\frac{d }{d\rho}$, then
$$
aV+bW=a\frac{d }{d\lambda} +b\frac{d }{d \rho} =(aV^{\mu}+bW^{\mu})\frac{ \partial  }{ \partial x^{\mu} } 
$$
$$
(aV+bW)(f)=aV(f)+bW(f)
$$
Mathematically, a vector is a linear map from the space of smooth functions on $M$ to $\mathbb{R}$
Leibniz also holds:
$$
(aV+bW)(fg)=(aV+bW)(f)+(aV+bW)(g)
$$
Note the vectors on $M$ do not live in $M$
Rather, all the vectors at some point $p \in M$ live in the tangent space $T_{p}$ 
This is a specific vectorspace associated with the point $p$
The tangent spaces $t_{p}$ and $T_{q}$
