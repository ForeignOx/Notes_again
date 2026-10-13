How does the rate of change change depending on the flow rate?
Consider a quantity $\alpha(\underline{x},t)$, it can be scalar or vector... In the Eulerian perspectivve, we fix $\underline{x}$, so
$$
\frac{d a}{dt} =\frac{ \partial a }{ \partial t } \cancelto{ 1 }{ \frac{d t}{dt} } +\frac{ \partial a }{ \partial \underline{x} } \cancelto{ 0 }{ \frac{d \underline{x}}{dt} } =\frac{ \partial a }{ \partial t } 
$$
But in the lagrangian perspective, we are following the fluid particle:
$$
\frac{d a}{dt} =\frac{ \partial a }{ \partial t } +\frac{ \partial a }{ \partial \underline{x} } \cdot \frac{d \underline{x}}{dt} =\frac{ \partial a }{ \partial t } +\underline{u}\cdot \underline{\nabla } a=\left[ \frac{ \partial  }{ \partial t }  +\underline{u}\cdot \underline{\nabla } \right]a
$$
I.e. the change due to time plus the change due to the fluid particle being carried by $\underline{u}$ along $\underline{\nabla }a$
We can thus define the material derivative:
$$
\frac{D}{Dt}=\frac{ \partial  }{ \partial t } +\underline{u}\cdot \underline{\nabla } 
$$
If we're in 3D cartesian, then
$$
\frac{D}{Dt} =\frac{ \partial  }{ \partial t } +u\frac{ \partial  }{ \partial x } +v\frac{ \partial  }{ \partial y }+w\frac{ \partial  }{ \partial z } 
$$
And it represents a bridge between the natural Eulerian way of describing fluids, and the classical mechanics Lagrangian way of describing physics
