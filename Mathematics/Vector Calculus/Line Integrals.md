## Of [[Scalar Fields|Scalar Fields]]
The line integral of a scalar field $f(\underline{x})$ alng a [[Curves|curve]] $C$ with parametrisation $\underline{x}(t)$ for $t\in[t_{0},t_{1}]$ is:
$$
\int _{C}f \, dl=\int _{t_{0}}^{t_{1}}f(\underline{x}(t))\left| \frac{d \underline{x}}{dt}  \right|  \, dt  
$$
One can think of this as integrating the heights of the field along the curve
For the special case $f(\underline{x})=1$, the line integral is called the arclength of the curve:
$$
L=\int _{C} \, dl=\int_{t_{0}}^{t_{1}} \left| \frac{d \underline{x}}{dt}  \right|  \, dt
$$
Which we can think about by considering $\left| \frac{d \underline{x}}{dt} \right|dt$ as the length of an infinitesimal piece of curve
There is always a special arclength parametrisation $\underline{x}(s)$, where $\left| \frac{d \underline{x}}{ds} \right|\equiv1$ all along the curve. In that case, the parameter $s$ corresponds to the distance along the curve and $L=\int_{0}^{L}  \, ds$ 
A curve of finite length is called rectifiable
### Examples
Integrate $f(\underline{x})=y+x^{2}$ around the unit circle, which has parametrisation $\underline{x}(t)=\cos t \underline{e}_{1}+\sin t \underline{e}_{2}$ for $t\in[0,2\pi]$. The [[Differentiation#Curves|tangent vector]] is
$$
\frac{d \underline{x}}{dt} =-\sin t \underline{e}_{1}+\cos t \underline{e}_{2}\implies \left| \frac{d \underline{x}}{dt}  \right| =\sqrt{ \sin ^{2}t+\cos ^{2}t }=1
$$
So
$$
    \int _{C}f \, dl =\int _0^{2\pi}(y+x^{2})(1) \, dt 
$$
$$
 =\int _{0}^{2\pi}\sin t+\cos ^{2}t \, dt=\int _{0}^{2\pi}\cos ^{2}t \, dt =\frac{1}{2}\int _{0}^{2\pi}1+\cos2 t \, dt =\frac{1}{2}[t]_{0}^{2\pi}=\pi
$$
### Proposition
The line integral of a scalar field is independent of the choice of parametrisation.
#### Proof
Suppose we have two parametrisations of the same curve $C$, $\underline{x}(t)$ for $t\in[t_{0},t_{1}]$ and $\underline{x}(\tau)$, for $\tau \in[\tau_{0},\tau_{1}]$. By the [[Chain Rule|chain rule]], 
$$
\frac{d \underline{x}}{dt} =\frac{d \tau }{dt} \frac{d \underline{x}}{d\tau} \implies \left| \frac{d \underline{x}}{dt}  \right| =\left| \frac{d \tau}{dt}  \right| \left| \frac{d \underline{x}}{d\tau}  \right| 
$$
There are now two cases:
- Case 1: $\underline{x}(t_{0})=\underline{x}(\tau_{0})$; they both have the same direction. This would mean that $\frac{d t}{d\tau}>0$, so
$$
\int_{t_{0}}^{t_{1}} f(\underline{x}(t))\left| \frac{d \underline{x}}{dt}  \right|  \, dt=\int _{t_{0}}^{t_{1}}f(\underline{x}(t))\frac{d \tau}{dt} \left| \frac{d \underline{x}}{d\tau}  \right|  \, dt  = \int_{\tau_{0}}^{\tau_{1}} f(\underline{x}(\tau))\left| \frac{d \underline{x}}{d\tau}  \right|  \, d\tau 
$$

    By chain rule which is what we wanted :)
- Case 2: $\underline{x}(t_{0})=\underline{x}(\tau_{1})$ so they are travelling in opposite directions, so $\frac{d t}{d\tau}<0$, so
$$
\int_{t_{0}}^{t_{1}} f(\underline{x}(t)) \left| \frac{d \underline{x}}{dt}  \right|  \, dt=\int_{t_{0}}^{t_{1}} f(\underline{x}(t))\left( -\frac{d \tau}{dt}  \right)\left| \frac{d \underline{x}}{d\tau}  \right|  \, dt =-\int_{\tau_{1}}^{\tau_{0}} f(\underline{x}(\tau)) \left| \frac{d \underline{x}}{d\tau}  \right|  \, d\tau 
$$
$$
    = \int_{\tau_{0}}^{\tau_{1}} f(\underline{x}(\tau))\left| \frac{d \underline{x}}{d\tau}  \right|  \, d\tau 
$$
___
Calculate the arclength of the circle $x^{2}+y^{2}=a^{2}$ is in fact the circumference, so we know that it should be $2\pi a$. To obtain this from the arclength formula, we can recall our parametrisation
$$
\underline{x}(t)=a\cos t \underline{e}_{1}+a\sin t \underline{e}_{2},t\in [0,2\pi]
$$
Differentiating gives the tangent vector
$$
\frac{d \underline{x}}{dt} =-a\sin t \underline{e}_{1}+a\cos t \underline{e}_{2}\implies \left| \frac{d \underline{x}}{dt}  \right| =a
$$
So the arclength is:
$$
L=\int_{0}^{2\pi} a \, dt=a[t]_{0}^{2\pi}=2\pi a 
$$
___
Calculate the arclength of the hypocycloid $\underline{x}(t)=\cos ^{3}t \underline{e}_{1}+\sin ^{3}t \underline{e}_{2}$ for $t\in[0,2\pi]$. Differentiating gives the tangent vector:
$$
\frac{d \underline{x}}{dt} =-3\cos ^{2}t\sin t \underline{e}_{1}+3\sin ^{2}t\cos t \underline{e}_{2}
$$
So
 $$
\left| \frac{d \underline{x}}{dt}  \right| =\sqrt{ 9\cos ^{4}t\sin ^{2}t+9\sin ^{4}t\cos ^{2}t }=3\sqrt{ \cos ^{2}t\sin ^{2}t }\sqrt{ \cos ^{2}t+\sin ^{2}t }=3\left| \cos t\sin t \right| 
$$
By symmetry we only need to integrate overr $t\in\left[ 0,\frac{\pi}{2} \right]$, so
$$
L=\int_{0}^{2\pi} 3\left| \cos t\sin t \right|  \, dt =4\int_{0}^{\frac{\pi}{2}} 3\cos t\sin t \, dt=12\int_{0}^{1} y \, dy =6
$$
## Of [[Vector Fields|Vector Fields]]
The line integral of a vector field $\underline{f}(\underline{x})$ along an oriented curve $C$ with parametrisation $\underline{x}(t)$ for $t \in[t_{0},t_{1}]$ is defined as:
$$
\int _{C} \underline{f}\cdot    \underline{\hat{t}} \, dl=\int_{t_{0}}^{t_{1}} \underline{f}(\underline{x}(t)) \cdot  \underline{\hat{t}}  \left| \frac{d \underline{x}}{dt}  \right| \, dt=\int_{t_{0}}^{t_{1}} \underline{f}(\underline{x}(t)) \cdot \frac{d \underline{x}}{dt}  \, dt 
$$
Where $\underline{\hat{t}}$ is the [[Unit Tangent Vectors|unit tangent vector]], so the line integral of the vector field is the scalar line integral of the tangential component of $\underline{f}$
Warning - changing the orientation $\underline{\hat{t}}\to -\underline{\hat{t}}$ will flip the sign of the integral.
If $C$ is closed, we usually write $\int _{C} \underline{f} \cdot \underline{\hat{t}} \, dl=\oint_{C}\underline{f} \cdot\underline{\hat{t}}\,dl$ which is called the circulation of $\underline{f}$ around $C$
An alternative notation for vector line integrals is $\int _{C}\underline{f} \cdot \underline{\hat{t}}\,dl=\int _{C} \underline{f} \cdot d \underline{x}$, but you must always evaluate by changing variable back to $t$.
### Examples
Evaluate $\int _{C}\underline{f} \cdot \underline{\hat{t}} \, dl$ for $\underline{f}(\underline{x})=-\underline{x}$ and $C$ is the straight line from $(1,0)$ to $(2,0)$.
We first need a parametrisation: $\underline{x}(t)=(1+t)\underline{e}_{1}$ for $t\in [0,1]\implies \frac{d \underline{x}}{dt}=\underline{e}_{1}$, then
$$
\int _{C} \underline{f} \cdot \underline{\hat{t}} \, dl =\int_{0}^{1} (-x\underline{e}_{1}-y\underline{e}_{2})\cdot \underline{e}_{1} \, dt=-\int_{0}^{1} x \, dt =-\int_{0}^{1} 1+t \, dt =\left[ t+\frac{1}{2}t^{2} \right]_{0}^{1}=-\frac{3}{2} 
$$
___
Evaluate $\oint_{C} \underline{f} \cdot\underline{\hat{t}}\,dl$ for $\underline{f}(\underline{x})=-\underline{x}$ and $C$ is the anticlockwise unit circle.
Our parametrisation will be $\underline{x}(t)=\cos t \underline{e}_{1}+\sin t \underline{e}_{2}$ for $t\in[0,2\pi]$, which means $\frac{d \underline{x}}{dt}=-\sin t \underline{e}_{1}+\cos t \underline{e}_{2}$
So
$$
\oint_{C} \underline{f} \cdot\underline{\hat{t}} dl=\int_{0}^{2\pi} (-x\underline{e}_{1} -y\underline{e}_{2})\cdot \frac{d \underline{x}}{dt}  \, dt=\int_{0}^{2\pi} (\cos t\sin t-\sin t\cos t) \, dt=0  
$$
Which makes sense because $\underline{f} \cdot\underline{\hat{t}}=0$ all along the curve
___
Evaluate $\oint_{C}\underline{g} \cdot\underline{\hat{t}}dl$ for $\underline{g}(\underline{x})=(y-x)\underline{e}_{1}-(x+y)\underline{e}_{2}$ and $C$ the anticlockwise unit circle.
This is also the unit circle, so we can use the same parametrisation; so
$$
\oint_{C} \underline{g} \cdot\underline{\hat{t}}\,dl=\int_{0}^{2\pi} ((\sin t-\cos t)\underline{e}_{1}-(\cos t+\sin t)\underline{e}_{2})\cdot (-\sin t \underline{e}_{1}+\cos t \underline{e}_{2})\, dt 
$$
$$
= -\int_{0}^{2\pi}  \, dt  =-2\pi

$$
___
A physical exaple is the [[Work|work]] done by a particle in a force-fielf $\underline{F}(\underline{x})$ under $m\ddot{\underline{x}}=\underline{F}(\underline{x})$.
$$
    W=K(T)-K(0)=\int_{0}^{T} \frac{d K}{dt}  \, dt=\int_{0}^{T}m\underline{\dot{x}}\cdot     \underline{\ddot{x}}  \, dt=\int_{0}^{T} \underline{F} \cdot  \underline{\dot{x}} \, dt=\int _{C}\underline{F} \cdot  \underline{\hat{t}} \, dl 
$$
