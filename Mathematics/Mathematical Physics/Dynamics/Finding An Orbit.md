We had an equation for $r(t)$, under a central force, such as gravity, namely,
$$
m  \ddot{r}-\frac{L^{2}}{mr^{3}}=f(r)
$$
We want a curve (orbit) as $r=r(\theta)$, so we use the [[Chain Rule|chain rule]]; for any function $h$, we have:
$$
\frac{d h}{dt} =\frac{d h}{d\theta} \frac{d \theta}{dt} =\frac{d h}{d\theta} \frac{L}{mr^{2}}
$$
It is also convenient to change from $r$ to $u=\frac{1}{r}$, then
$$
\frac{d r}{dt} =\frac{d }{dt} \left( \frac{1}{u} \right)=-\frac{1}{u^{2}}\frac{d u}{d\theta} \frac{L}{mr^{2}}=-\frac{L}{m}\frac{d u}{d\theta} 
$$
And
$$
\ddot{r}=\frac{d }{dt} \frac{d r}{dt}=-\frac{L}{m}\frac{d }{dt} \frac{d u}{d\theta} =-\frac{L}{m}\frac{d ^{2}u}{d\theta^{2}} \frac{L}{m}u^{2}=-\frac{L^{2}u^{2}}{m^{2}}\frac{d ^{2}u}{d\theta^{2}} 
$$
So our original equation becomes:
$$
-\frac{L^{2}u^{2}}{m}\frac{d ^{2}u}{d\theta^{2}} -\frac{L^{2}u^{3}}{m}=f\left( \frac{1}{u} \right)
$$
$$
\implies \frac{d u^{2}}{d\theta^{2}} +u=-\frac{m}{L^{2}u^{2}}f\left( \frac{1}{u} \right)
$$
From here we need to specify $f$ to determine a solution to this differential equation
## Example
For gravity, $f(r)=-\frac{1}{r^{2}}$ with $m=1$. Our differential equation becomes:
$$
\frac{d ^{2}u}{d\theta^{2}} +u=-\frac{1}{L^{2}u^{2}}(-u^{2})=\frac{1}{L^{2}}
$$
We have a solution of the form $y_{cf}+y_{pi}$, impose $u'(0)=0$, where $u'=\frac{d u}{d\theta}$. The solution of the complimentary function $u(\theta)$ will be given by:
$$
u(\theta)=A\cos\theta
$$
Since the coefficient of $\sin\theta$ vanishes, then the particular integral will be $\frac{1}{L^{2}}$, so
$$
u(\theta)=A\cos(\theta)+\frac{1}{L^{2}}
$$
This can be written as:
$$
r(\theta)=\frac{L^{2}}{1+\varepsilon \cos\theta}
$$
Where $\varepsilon=AL^{2}$
Note if $\left| \varepsilon \right|<1$, then $r(\theta)$ is finite $\forall\theta$, so the orbit is elliptical as $r_\text{min}\leq r(\theta)\leq r_\text{max}$
Also
$$
L^{2}=r+\varepsilon r\cos\theta=r+\varepsilon x\implies r=L^{2}-\varepsilon x
$$
$$
 \implies r^{2}=x^{2}+y^{2}=(L^{2}-\varepsilon x)^{2}
$$
Which is an equation of an ellipse in the $xy$-plane
Note that $\varepsilon$ is known as the eccentricity of the ellipse
If $\varepsilon=0$, the ellipse has no eccentricity :sob: so the equation is that of a circle; $r=L^{2}$ 
___
Take $m=1,f(r)=-\frac{1}{r^{3}},u'(0)=0$, then our equation is:
$$
u''+u=-\frac{1}{L^{2}u^{2}}(-u^{3})=\frac{u}{L^{2}}
$$
$$
\implies u''+\left( 1-\frac{1}{L^{2}} \right)u=0
$$
The type of this depends on the sign of $1-\frac{1}{L^{2}}$
If $L=1$, then the solution is $u=c$, which means that $r=\frac{1}{c}$, so is a circle (of constant radius)
If initial $\underline{v}$ is perpendicular to $\underline{r}$, then $\underline{\dot{r}}(0)=0\implies u'(0)=0$ (from $\dot{r}=-\frac{L}{m}u'$), this motivates our initial condition :)
If $L>1$, then $1-\frac{1}{L^{2}}>0$, so we write $1-\frac{1}{L^{2}}=-\omega^{2}$, to give solution:
$$
u(\theta)=A\cos(\omega\theta)
$$
$$
\implies r(\theta)=\frac{1}{A\cos(\omega\theta)}
$$
```desmos-graph
A=0.8
\omega=0.3
r(\theta)=1/(A*\cos(\omega*\theta))
```
___
## Circular Orbits
Is there a circular orbit $u=b$? We need $f(r)<0$, we write $g(u)=-f\left( \frac{1}{u} \right)$, so
$$
u''+u=\frac{m}{L^{2}u^{2}}g(u)
$$
So $u=b$ being constant is true iff
$$
L^{2}=\frac{m}{u^{3}}g(u)=\frac{m}{b^{3}}g(b)
$$
For any $b>0$, we can choose the initial speed such that this holds
So we can have a circular orbit of any desired radius
Bt is it stable? If w ut it in a small perturbation, does $u(\theta)$ stay close to $b$?
So take $u(\theta)=b+\varepsilon(\theta)$ with $\varepsilon(\theta)$ small, so keep it simple, let's assume that the perturbation does not change $L$.
Substituting $u(\theta)$ into the orbit equation gives:
$$
\epsilon''+b+\varepsilon=\frac{m}{L^{2}}(b+\varepsilon)^{-2}g(b+\varepsilon)
$$
We can consider the [[Taylor Series|taylor series]] expansions of these as $\varepsilon$ is small, we can use these to approximate;
$$
g(b+\varepsilon)=g(b)+\varepsilon g'(b)+\dots
$$
And we do a similar thing for $(b+\varepsilon)^{-2}$; we use the [[Binomial Theorem|binomial expansion]]:
$$
(b+\varepsilon)^{-2}=\left( b\left( 1+\frac{\varepsilon}{b} \right) \right)^{-2}=b^{-2}\left( 1+\frac{\varepsilon}{b} \right)^{-2}=b^{-2}\left( 1-\frac{2\varepsilon}{b}+\dots \right)
$$
So
$$
\varepsilon''+b+\varepsilon=\frac{m}{L^{2}}b^{-2}\left( 1-\frac{2\varepsilon}{b} \right)(g(b)+\varepsilon g'(b))=\frac{m}{L^{2}b^{2}}\left( g(b)+\varepsilon\left( g'(b)-\frac{2}{b}g(b) \right) \right)+\underbrace{ \varepsilon^{2} }_{ \approx0 }
$$
Using $b=\frac{mg(b)}{L^{2}b^{2}}$ leeaves
$$
\varepsilon''=\left( -1+\frac{m}{L^{2}b^{2}}\left( g'(b)-\frac{2}{b}g(b) \right) \right)\varepsilon
$$
Now we can use $\frac{m}{L^{2}b^{2}}=\frac{b}{g(b)}$:
$$
\varepsilon''=\left( -1+\frac{b}{g(b)}\left( g'(b)-\frac{2}{b}g(b) \right) \right)\varepsilon=\left( -1+\frac{bg'(b)}{g(b)}-2 \right)\varepsilon=\left( \frac{bg'(b)}{g(b)}-3 \right)\varepsilon
$$
If $\frac{bg'(b)}{g(b)}-3>0$ then $\varepsilon(\theta)=A\exp\left( \theta\sqrt{ \frac{bg'(b)}{g(b)}-3 } \right)$ which is unstable
If $\frac{bg'(b)}{g(b)}-3=0$, then $\varepsilon(\theta)=A\theta$, which also is unstable
If $\frac{bg'(b)}{g(b)}-3<0$, then $\varepsilon(\theta)\sim \cos,\sin$ so remains small
So we conclude that the orbit is stable iff
$$
\frac{bg'(b)}{g(b)}-3<0
$$
## Example
If $f(r)=-\frac{k}{r^{2}}$ under gravity, so $g(u)=ku^{2}$, and
$$
\frac{bg'(b)}{g(b)}=\frac{2kb^{2}}{kb^{2}}-3=-1<0
$$
So it is stable
___
If $f(r)=-\frac{k}{r^{3}}$, this has $g(u)=ku^{3}$, then
$$
\frac{bg'(b)}{g(b)}-3=\frac{3kb^{2}b}{kb^{3}}=0
$$
So this is unstable
___
If $f(r)=-\frac{2}{r^{2}}-\frac{1}{r^{3}}$ has $g(u)=2u^{2}+u^{3}$, then
$$
\frac{bg'(b)}{g(b)}-3=\frac{(4b+3b^{2})b}{2b^{2}+b^{3}}-3=\frac{4b^{2}+3b^{3}-6b^{2}-3b^{3}}{2b^{2}+b^{3}}=-\frac{2b^{2}}{2b^{2}+b^{3}}<0
$$
```desmos-graph
y=-2*x^2/(2*x^2+x^3)
```
___
Unit mass in an attractive central force of magnitude $\frac{5}{r^{2}}$, we have initial conditions: $\underline{r}(0)=2\underline{e}_{r}$, $\underline{v}(0)=\gamma \underline{e}_{r}+\underline{e}_{\theta}$ where $\gamma$ is a positive constant. Use $E$ to find $\gamma$ such that the trajectory is bounded. For which $\gamma$ is $r_\text{max}=9r_\text{min}$?
It is bounded iff $E<0$ since $E=\frac{1}{2}mv^{2}+V(r)$, $V=-\int -\frac{5}{r^{2}} \, dr=-\frac{5}{r}$, so $E\geq 0$ to reach $r=\infty$. Here
$$
E=\frac{1}{2}(\gamma^{2}+1)-\frac{5}{2}=\frac{1}{2}(\gamma^{2}-4)
$$
So bounded for
$$
0<\gamma<2
$$
We also know that
$$
E=\frac{1}{2}v^{2}+V=\frac{1}{2}(\dot{r}^{2}+r^{2}\dot{\theta}^{2})-\frac{5}{r}
$$
$$
 L=m\underline{r}\times \underline{v}=2\underline{e}_{r}\times \underline{e}_{\theta}\implies L=2=r^{2}\dot{\theta}
$$
$$
\sum_{k=1}^{k}k\alpha 
$$

$a\in S, \pi n\sin \in$ $M_{n}(\mathbb{R})$