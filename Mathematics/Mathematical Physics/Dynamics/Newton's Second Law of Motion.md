zThe rate of change of [[Momentum|momentum]] of a body is directly proportional to the resultant force acting upon it
This implies that the [[Acceleration|acceleration]] of an object depends on the [[Mass|mass]] of the object and the amount of force applied
For constant mass, this implies $F=ma=m\dot{v}=m\ddot{x}$
In SI, we define the rate of change of momentum as equal to the force expressed in $\pu{ N }$, so
$$
\sum F=\frac{dp}{d t}=\dot{p}
$$
This gives us an equation of motion
So in general, force can depend on time, [[Position|position]], or even [[Velocity|Velocity]], so
$$
F=F(t,x,\dot{x})=m\ddot{x}
$$
This is a [[Second Order Ordinary Differential Equations|second order differential equation]] which cannot be solved explicitly in general, but we tend to focus on special cases which can be solved
___
## Constant Force
The simplest example is if the force is constant, which arises in many cases, for example, vertical motion under [[Gravitational Force|gravity]] close to the surface of a planet. In this case, the magnitude of $F$ is $\left| F \right|=mg$
known as the weight, and $g$ is some constant and is different depending on what planet you are on
### Example
An object is shot up vertically from the ground with some initial [[Speed|speed]] $u$. What maximum height $h$ does it reach?
We could use $x$ pointing upwards or $x$ pointing downwards for the axis describing the position of the particle. We can choose a convenient one. Here having $x$ pointing upwards seems more natural as all the motion is upwards. It makes sense for us to say that the origin is the ground level, so $x=0$ at the ground. Then our equation of motion is given by:
$$
m\ddot{x}=-mg
$$
$$
\implies \ddot{x}=-g\overset{\int  \, dt }{\implies}\dot{x}=-gt+u
$$
Where $u$ is the constant of integration
$$
\overset{\int  \, dt }{\implies}x=-\frac{1}{2}gt^{2}+ut+0
$$
Where $0$ is the constant of integration, since we started at the ground
So we have a formula for the height of the particle above the ground at a given time
By calculus, we have a maximum when $\dot{x}=0\implies t=\frac{u}{g}$, so 
$$
h=x\left( \frac{u}{g} \right)=-\frac{1}{2}g\left( \frac{u}{g} \right)^{2}+u\left( \frac{u}{g} \right)=\frac{u^{2}}{2g}
$$
___
## Force as Function of Time
The next simplest case is if $F=F(t)$; where force is only a function of time. In this case the same method works; you do [[Integration|$\int  \, dt$]] twice
### Example
You have a particle of mass $m=1$ is at rest ($u=0$) at $x=0$. A force $F=e^{ -t }$ is switched on at time $t=0$. Find $x(t)$ for $t>0$ (note for $t\leq 0$, $x=0$ as the particle is stationary)
Note: expect $\dot{x}>0$ and $x>0$ for $t>0$, since the force is always positives
Our equation of motion is
$$
\ddot{x}=e^{ -t }
$$
$$
\overset{\int  \, dt }{\implies}\dot{x}=-e^{ -t }+c=e^{ -t }+1 
$$
Here we find $c=1$, since at $t=0$, $v=0$, and that happends for $c=1$
$$
\overset{\int  \, dt }{\implies}x(t)=e^{ -t} t-1
$$
With the latest consant of integration being $k=-1$ to make the function to be non-negative
![[Newton's Second Law of Motion 2025-01-13 14.45.37.excalidraw]]
___
## Force as Function of Velocity
The next simplest case is when $F=F(\dot{x})$. Here  $m\ddot{x}=F(\dot{x})$, this is a non-linear differential equation. We can rewrite this as $m\dot{v}=F(v)$, which is a non-linear [[First Order Ordinary Differential Equations|first order differential equation]] that is separable. This can be solved to get $v(t)$, then integrating with respect to time gives $x(t)$
Another method for this is to say that the equation of motion is equivalent to $mv\frac{d v}{dx}=F(v)$ which is separable, can e $v(x)$ then $\frac{d x}{dt}=v(t)$
### Example
Particle of mass $m$ is slowed by frictional force of magnitude $be^{ av }$. Assume it has initial speed $u$. What time $T$ does it take before coming to rest
We are not told the directions of the force or the speed, so our solution has to have a choice; either the particle is moving to the right or the left, but either way, since it is a frictional force, it is implied that it acts against the movement. Both options will give the same answer
So what we know is that 
$$
m\frac{d v}{dt} =-be^{ av }
$$
And now it is just calculus:
$$
\int e^{ -av }dv=-\frac{b}{m}\int  \, dt 
$$
This will give a constant of integration, which we will need to be fixed by setting $v$ at $t=0$ as $u$. However, there is a way to avoid this, by turning the indefinite integrals to definite ones:
$$
\int _{u}^{0}e^{ -av } \, dv =-\frac{b}{m}\int _{0}^{T} \, dt 
$$
Since the speed is going from $u$ to $\hspace{0pt}0$, and the time is going from $0$ to $T$
$$
\implies \left[ -\frac{1}{a}e^{ -av } \right]_{u}^{0}=-\frac{bT}{m}
$$
$$
\implies T=\frac{m}{ab}(1-e^{ -au })
$$
___
Mass $m$ falls downwards under gravity with a resistive force $bw$, where $w$ is its speed. Initial $w(0)=0$, find $w(t)$. What is the “least upper bound” of $w$, the terminal speed?
Again we could have the axis pointing up or down, since all the motion is downwards, we'll choose that
The equation of motion is:
$$
m\dot{v}=mg-bv
$$
Where $v$ is the velocity, since all the velocity is in the same direction, this is also the speed, so $v=w$, so
$$
m\dot{w}=mg-bw
$$
$$
\implies \frac{d w}{dt} =g-\frac{b}{m}w
$$
$$
\implies \int \frac{1}{g-\frac{b}{m}w} \, dw =\int  \, dt 
$$
$$
\implies w(t)=\frac{mg}{b}(1-e^{ -bt/m })
$$
To find the terminal speed, we take the limit as $t\to \infty$, whereby the $e^{ -bt/m }\to0$, so
$$
w(\infty)=\frac{mg}{b}
$$
And $\frac{mg}{b}$ is the terminal speed
___
A unit mass ($m=1$) experiences a frictional force of magnitude $v+v^{2}$ ($v>0$ is its velocity). Find the general solution for $x(t)$
Using the second method
$$
v\frac{d v}{dx} =-(v+v^{2})
$$
$$
\implies \frac{d v}{dx} =-(1+v)
$$
$$
\implies \int \frac{1}{1+v} \, dv =-\int  \, dx 
$$
$$
\implies \ln(1+v)=-x+c
$$
$$
\implies v(x)=e^{ c-x }-1
$$
Then since $\frac{d x}{dt}=v=e^{ c-x }-1$, so
$$
\int \frac{1}{e^{ c-x }-1} \, dx =\int  \, dt =t+b
$$
Now using the fact that 
$$
\int \frac{e^{ x }}{e^{ c }-e^{ x }} \, dx =e^{ c } -e^{ x }
$$
$$
e^{ c }-e^{ x }=e^{ -b-t }
$$
$$
\implies x=\ln(e^{ c }-e^{ -b-t })
$$

___
## Force as a Function of Position
Here $m\ddot{x}=F(x)$, which is a second order differential equation. If $F(x)=bx+c$, i.e. it is [[Linear|linear]], then
$$
m\ddot{x}-bx=c
$$
Which can be solved using a complimentary function plus a particular integral. If $F$ is non-linear, this doesn't work
In that case, you think of the velocity $v$ as a function of $x$, $v=v(x)$, then
$$
m\frac{d v}{dt}= m\frac{d }{dx} v(x(t))=m\frac{d v}{dx} \frac{d x}{dt} =mv\frac{d v}{dx} =F(x)
$$
So we arrive at a first order separable differential equation, which you solve to get $v(x)$, to get $x(t)$, simply use $\frac{d x}{dt}=v(x)$, so you have another first order separable differential equation
### Example
A mass $m=2$ moves in a force $F=3x^{2}$, and the initial conditions are $x=1$ and $v=1$ at $t=0$. At what time $T$ does it take to reach $x=9$?
Note that the force is non-linear in $x$, so our equation of motion is:
$$
2v\frac{d v}{dx} =3x^{2}
$$
$$
\implies \int 2v \, dv =\int 3x^{2} \, dx 
$$
$$
\implies v^{2}=x^{3}+c
$$
But using our initial conditions, we get $c=0$, so
$$
v^{2}=x^{3}
$$
$$
\implies v=x^{3/2}
$$
We take the positive square root since $x=v>0$ at $t=0$, now
$$
\frac{d x}{dt} =x^{3/2}
$$
$$
\implies \int_{1}^{9} x^{-3/2} \, dx =\int_{0}^{T}  \, dt 
$$
$$
\implies T=-2\left[ x^{-\frac{1}{2}} \right]_{1}^{9}=-2\left( \frac{1}{3}-1 \right)=\frac{4}{3}
$$
___
A unit mass is acted on by force $F=\frac{1}{1+x^{2}}$, it "starts" at $x=-\infty$ with $\dot{x}=u_{0}>0$. What is $\dot{x}$ as $x\to \infty$? Note $F>0$, so expect an answer greater than $u_{0}$
We really want $v(x)$ and expect the graph to look like:
![[Newton's Second Law of Motion 2025-01-17 16.43.13.excalidraw]]
And the equation is 
$$
v\frac{d v}{dx} =\frac{1}{1+x^{2}}
$$
$$
\implies \int _{u_{0}}^{u_{1}}v \, dv =\int_{-\infty}^{\infty} \frac{1}{1+x^{2}} \, dx 
$$
(This is assuming $u_{1}$ exists, but if it doesn't, then it will be because the RHS doesn't converge)
$$
\implies \frac{1}{2}u_{1}^{2}-\frac{1}{2}u_{0}^{2}=[\arctan x]_{-\infty}^{\infty}=\frac{\pi}{2}--\frac{\pi}{2}=\pi 
$$
$$
\implies u_{1}=\sqrt{ u_{0}^{2}+2\pi }
$$
(Which is greater than $u_{0}$ as expected) 
___
## Force as a Function of Velocity and Time
For $F=F(t,\dot{x})$, we have
$$
m\ddot{x}=F(t,\dot{x})
$$
Which we re-write as
$$
m\dot{v}=F(t,v)
$$
Which is a first order differential equation which we can solve if we have the methods to do so
Then if needed as a function of position, simply integrate
### Example
$F(t,v)=-v+e^{ -t }$ is a linear equation so can be solved with an integrating factor, which yields (with $v(0)=0$), $v(t)=t e^{ -t }$
___
## Variable Mass
The case where $m=m(t)$, this has no general method, but with some logic can be achieved
### Example
A rocket of mass $m(t)$ burns fuel at a constant rate $\dot{m}=-c$ (with $c>0$) which produces a constant force $F=kc$. Start with $x(0)=0$ and $\dot{x}(0)=0$, and initial mass $m_{0}$
Here the equation of motion is 
$$
\frac{d }{dt} (mv)=F
$$
Where $v=\dot{x}$, so integrating with respect to time gives:
$$
mv=kct+0
$$
(the $0$ is the constant of integration)
Now $\dot{m}=-c$, so
$$
m(t)=-ct+m_{0}
$$
Thus
$$
v(t)=\frac{kct}{m_{0}-ct}
$$
For $0\leq t<\frac{m_{0}}{c}$ as otherwise the problem doesn't make sense, finally
$$
x(t)=\int v(t) \, dt =\dots
$$




 
#Mathematics #Dynamics #Law #Equation