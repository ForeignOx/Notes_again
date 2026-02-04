2The generic first order [[Differential Equations|ODE]] can be written in the form:
$$
\frac{d y}{dx} =f(x,y)
$$
Generically this has a one parameter family of solutions; the general solution, which will always contain a single arbitrary constant. Assigning a particular value to this constant gives the particular solution requireing that the solution satisfies an initial condition $y(x_{0})=y_{0}$ for fixed $y_{0}$ will fix a specific solution to the ODE. In this case, the ODE is called an initial value problem (IVP). To solve an IVP, one should first find the general solution to the ODE and then use the initial condition (initial value) to find the specific solution which satisfies the IVP
The method used to solve the ODE depends on the form of $f(x,y)$ (most cannot be solved)
## First Order Separable ODEs
The ODE $\frac{d y}{dx}=f(x,y)$ is separable is $f(x,y)=X(x)Y(y)$, and can be solved by direct integration:
$$
\frac{1}{Y(y)}\frac{d y}{dx} =X(x)\iff \int \frac{1}{Y(y)} \, dy =\int X(x) \, dx 
$$
Which we can check by differentiating both sides with respect to $x$:
$$
    \frac{d }{dx} \int \frac{1}{Y(y)} \, dy =\frac{d }{dx} \int X(x) \, dx 
$$
Then using the chain rule for the LHS
### Example
Solve the IVP $\frac{d y}{dx}=xe^{ y-x }$ with $y(0)=0$
$$
y'=xe^{ y }e^{ -x }
$$
$$
\implies \int e^{ -y } \, dy =\int xe^{ -x } \, dx 
$$
$$
\implies -e^{ -y }=-xe^{ -x }+\int e^{ -x } \, dx
$$
By [[Leibniz Rule|Leibniz rule]] 
$$
e^{ -y }=-xe^{ -x }-e^{ -x }+c
$$
$$
\implies e^{ -y }=e^{ -x }(1+x)-c
$$
$$
\implies y=-\ln(e^{ -x }(1+x)-c)
$$
Which is the general solution, now using the initial condition $y(0)=0$, 
$$
y(0)=-\ln(1-c)=0
$$
$$
\implies c=0
$$
So the particular solution is:
$$
y=-\ln(e^{ -x }(1+x))=x-\ln(1+x)
$$
___
Solve:
$$
y'=\frac{x^{2}y-y}{1+y}=(x^{2}-1) \frac{y}{1+y}
$$
$$
\implies \int \frac{1+y}{y} \, dy= \int x^{2}-1 \, dx 
$$
$$
\implies y+\ln|y|=x^{3}-x+c
$$
Which is the general solution to the ODE in implicit form
## First Order Homogeneous ODEs
The ODE is homogeneous if in $\frac{d y}{dx}=f(x,y)$, the $f(x,y)=f(tx,ty)\forall t\in\mathbb{R}$
In this case, the substitution $y=xv(x)$ which gives a seqarable ODE for $v(x)$
### Example
Solve:
$$
y'=\frac{y^{2}-x^{2}}{xy}
$$
With:
$$
f(x,y)=\frac{y^{2}-x^{2}}{yx},f(tx,ty)=\frac{t^{2}y^{2}-t^{2}x^{2}}{t^{2}xy}=f(x,y)
$$
Let $y(x)=xv(x)$, 
$$
y'=v(x)+xv'(x)=\frac{x^{2}v^{2}-x^{2}}{x^{2}v}=\frac{v^{2}-1}{v}=v-\frac{1}{v}
$$
$$
\implies v'=-\frac{1}{vx}
$$
Which is separable:
$$
\int v \, dv =\int -\frac{1}{x} \, dx 
$$
$$
\implies \frac{v^{2}}{2}=-\ln |x|+\ln |a|=\ln\left| \frac{a}{x}\right|
$$
$$
\implies v=\pm \sqrt{ 2\ln\left| \frac{a}{x} \right| }
$$
So $y(x)=xv(x)=\pm x \sqrt{ 2\ln\left| \frac{a}{x} \right| }$
## First Order Linear ODEs
The ODE is linear if $f(x,y)=-P(x)y+Q(x)$, we can then write the ODE:
$$
y'+P(x)y=Q(x)
$$
Or:
$$
\frac{dy}{dx}+P(x)y=Q(x)
$$
Let $P=P(x), Q=Q(x)$, we want to find a function $I=I(x)$ (known as the integrating factor):
$$
I\frac{dy}{dx} +PIy=QI
$$
Such that $I\frac{dy}{dx}+PIy$ is a perfect derivative by [[Leibniz Rule]]:
$$
I\frac{dy}{dx} +PIy=\frac{d }{dx} (Iy)
$$
$$
\implies I\frac{d y}{dx} +PIy=I\frac{d y}{dx} +y \frac{d I}{dx} 
$$
$$
\implies PI=\frac{d I}{dx} 
$$
$$
\implies \int P \, dx =\int \frac{1}{I}\frac{d I}{dx}  \, dx =\int \frac{1}{I} \, dI 
$$
$$
\implies \int P \, dx =\ln I
$$
$$
\implies I = e^{ \int P \, dx  }
$$
So the differential equation becomes
$$
\frac{d }{dx} (Iy)=QI
$$
$$
\implies Iy = \int QI \, dx 
$$
$$
\implies y=\frac{1}{I}\int QI \, dx 
$$
### Example
Solve the IVP $y'-\frac{2}{x}y=3x^{2}$ with $y(-1)=2$
Here we have $P(x)=-\frac{2}{x}$ and $Q(x)=3x^{3}$, so
$$
I=\exp\left( \int P(x) \, dx  \right)=\exp(-2\ln x)=x^{-2}
$$
$$
 \therefore y=\frac{1}{x^{-2}}\int 3x^{2}\times x^{-2} \, dx 
$$
$$
= x^{2}\int 3x \, dx =x^{2}\left( \frac{3}{2}x^{2}+c \right)=\frac{3}{2}x^{4}+cx^{2}
$$
Is the general solution
Let $x=-1$, $y=2$:
$$
2=\frac{3}{2}(-1)^{4}+c(-1)^{2}
$$
$$
\implies c=\frac{1}{2}
$$
And the particular solution is thus:
$$
y(x)=\frac{3}{2}x^{4}+\frac{1}{2}x^{2}
$$
## First Order Exact ODEs
A first order ODE can also be written in the form $M(x,y)dx+N(x,y)dy=0$, this can be rearranged to:
$$
N(x,y)\frac{d y}{dx} +M(x,y)=0
$$
Or:
$$
\frac{d y}{dx} =\frac{-M(x,y)}{N(x,y)}
$$
Note that $f(x,y)$ does not correspond to a unique $M$ or $N$, as multiplying $M$ and $N$ by the same arbitrary function, obtains the same $f$
For a function $g(x,y)$, the total differential $dg$ is defined as:
$$
dg=\frac{ \partial g }{ \partial y } dx+\frac{ \partial g }{ \partial y } dy
$$
We can think of $dg$ as the small change in $g$ that occurs when moving from the point $(x,y)$ to the point $(x+dx,y+dy)$ for small $dx$ and $dy$, then $dg$ being $\hspace{0pt}0$ means that $g$ is constant
The ODE $M(x,y)dx+N(x,y)dy=0$ is exact if there is a function $g(x,y)$ such that the left-hand side of the equation is the total differential $dg$, i.e. such that:
$$
\frac{ \partial g }{ \partial x } =M(x,y),\frac{ \partial g }{ \partial y } =N(x,y)
$$
If so, the ODE is equivalnt to $dg=0$, in which case $g$ must be constant, and $g=c$ gives a solution to the ODE
The equality of the mixed partial derivatives:
$$
\frac{ \partial^{2}g }{ \partial x\partial y }=\frac{ \partial^{2}g }{ \partial y \partial x }  
$$
Requires that for an exact ODE:
$$
\frac{ \partial N }{ \partial x } =\frac{ \partial M }{ \partial y } 
$$
We therefore have the following test for exactness: The ODE $M(x,y)dx+N(x,y)dy=0$ is exact iff $\frac{ \partial N }{ \partial x }=\frac{ \partial M }{ \partial y }$
### Example
Show that $(3e^{ 3x }y+e^{ x })dx+(e^{ 3x }+1)dy=0$ is exact and hence find the general solution
We have
$$
M(x,y)=3e^{ 3x }y+e^{ x },N(x,y)=e^{ 3x }+1
$$
So
$$
\frac{ \partial N }{ \partial x } =3e^{ 3x }=\frac{ \partial M }{ \partial y } 
$$
From $M=\frac{ \partial g }{ \partial x }$, $\frac{ \partial g }{ \partial x }=3e^{ 3x }y+e^{ x }$, so we must have:
$$
g(x,y)=e^{ 3x }y+e^{ x }+\phi(y)
$$
Where we have some arbitrary function $\phi(y)$ in place of our usual constant of integration
We also have $\frac{ \partial g }{ \partial y }=e^{ 3x }+\phi'(y)=N(x,y)=e^{ 3x }+1$, so $\phi'(y)=1$ and hence $\phi(y)=y+c$
The general solution is then:
$$
g(x,y)=e^{ 3x }y+e^{ x }+y+c=a
$$
$$
= e^{ 3x }y+e^{ x }+y=c
$$
This gives a solution in implicit form, in this case we can rearrange this into explicit form:
$$
e^{ 3x }y+y=e-e^{ x }
$$
$$
\implies y(e^{ 3x+1 })=c-e^{ x }
$$
$$
\implies y= \frac{c-e^{x}}{e^{ 3x }+1}
$$
By rewriting the ODE in the original form to check that this is indeed a solution
___
Consider an ODE $Mdx+Ndy=0$ which is not exact, i.e. with $\frac{ \partial M }{ \partial y }\neq \frac{ \partial N }{ \partial x }$, multiplying the ODE by $I(x,y)$ gives an equivalent ODE $mdx+ndy=0$, where $m=MI$ and $n=NI$, if this new ODE is exact, i.e. $\frac{ \partial m }{ \partial y }=\frac{ \partial n }{ \partial x }$, then $I(x,y)$ is an integrating factor for the original ODE
### Example
Show that $x$ is an integrating factor for $(3xy-y^{2})dx+x(x-y)dy=0$ and hence find the general solution
$$
M=3xy-y^{2},N=x^{2}-xy
$$
So
$$
\frac{ \partial M }{ \partial y } =3x-2y,\frac{ \partial N }{ \partial x } =2x-y
$$
So not exact, but with $I(x,y)=x$, we have
$$
m=MI=3x^{2}y-xy^{2}
$$
$$
 n=NI=x^{3}-x^{2}y
$$
And
$$
\frac{ \partial m }{ \partial y } =3x^{2}-2xy=\frac{ \partial n }{ \partial x} 
$$
So $mdx+ndy=0$ is exact, we can now solve with previous method:
$$
m=\frac{ \partial g }{ \partial x } =3x^{2}y-xy^{2}
$$
So
$$
g(x,y)=x^{3}y-\frac{1}{2}x^{2}y^{2}+\phi (y)
$$
Then
$$
\frac{ \partial g }{ \partial y } =x^{3}-x^{2}y+\phi'(y)
$$
And
$$
n=x^{3}-x^{2}y
$$
So $\phi'(y)=0$, so we can take $\phi(y)=0$, so final solution is then $g=c$, so
$$
x^{3}y-\frac{1}{2}x^{2}y^{2}=c
$$
Research how to find these integrating factors plssss
Sam my baby thinks that there is always an integrating factor, but there is not a perfect method to find them :(
## Bernoulli Equations
A Bernoulli Equation is a non-linear [[Differential Equations|ODE]] of the form
$$
y'+p(x)y=q(x)y^{n}
$$
With $n\neq 0,1$
Dividing through by $y^{n}$ gives
$$
y^{-n}y'+p(x)y^{1-n}=q(x)
$$
Using the substitution $v(x)=y^{1-n}(x)$, we have $v'=(1-n)y^{-n}y'$, and so we can re-write the ODE in terms of $v$ as
$$
\frac{1}{1-n}v'+p(x)v=q(x)
$$
Or
$$
v'+(1-n)p(x)v=(1-n)q(x)
$$
Which is now linear for $v$, so we we can solve it using the above method for linear ODEs
### Example
Solve
$$
y'-\frac{2y}{x}=-x^{2}y^{2}
$$
This is Bernoulli with $n-2$, so we make the substitution $v(x)=y^{1-n}=y^{-1}$, hence $v'=-y^{-2}y'$ and so if we divide our original ODE by $y^{2}$, we get that:
$$
y^{-2}y'-\frac{2}{xy}=-x^{2}
$$
Then we can write this in terms of $v$ as:
$$
-v'-\frac{2v}{x}=-x^{2}
$$
So we have the linear ODE
$$
v'+\frac{2v}{x}=x^{2}
$$
The integrating factor is $I(x)=\exp\left( \int \frac{2}{x} \, dx \right)=x^{2}$ and hence the solution is
$$
v(x)=\frac{1}{I}\int QI \, dx=x^{-2}\int x^{4} \, dx =\frac{1}{5}(x^{3}+cx^{-2}) 
$$
Hence the solution to the original Bernoulli ODE is:
$$
y(x)=\frac{1}{v(x)}=\frac{5x^{2}}{x^5+c}
$$



#Mathematics #Calculus 