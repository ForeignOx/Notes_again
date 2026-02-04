## Functions of $\hspace{0pt}1$ Variable
For [[Differentiation|differentiating]] the composition of [[Functions|functions]]: $(f\circ g)(x)=f(g(x))$, then the derivative is:
$$
(f\circ g)'(x)=f'(g(x))g'(x)
$$
Or
$$
\frac{d }{dx} f(g(x))=\frac{d f}{dg} \frac{d g}{dx} 
$$
### First Principles
For the function $f(x)$,
$$
\delta f=f(x+\delta x)-f(x)=\frac{d f}{dx} \delta x+R(x)
$$
Where $R(x)$ goes to $\hspace{0pt}0$ faster than $\delta x$. For $\delta x$ getting small,
$$
\delta f\approx \frac{d f}{dx} \delta x
$$
And we can say that if $df$ is an infinitesimal change in $f$, then
$$
df=\frac{d f}{dx} dx
$$
This is not strictly rigorous... We call $df$ a differential. This gives us the chain rule for $\hspace{0pt}1$ variable:
Suppose $y$ is a function of $x$ and $x$ in turn is a function of $t$. We can think of $y$ as a function of $t$; $y(x(t))$, so
$$
dy=\frac{d y}{dt} dt
$$
But also a function of $x$, so
$$
dy=\frac{d y}{dx} dx
$$
But $x$ is a function of $t$, so
$$
dx=\frac{d x}{dt} dt
$$
We can substitute this into the previous equation to get
$$
dy=\frac{d y}{dx} \frac{d x}{dt} dt
$$
And so, comparing with our first equation,
$$
\frac{d y}{dt} =\frac{d y}{dx} \frac{d x}{dt} 
$$
### Proof
$g$ differentiable at $c$ means that $g(x)=g(c)+g_{1}(x)(x-c)$ (we can form a linear approximation), where $g_{1}(x)$ is constant at $c$ and $g_{1}(c)=\lim_{ x \to c }g_{1}(x)=g'(c)$.
Similarly, $f$ differentiable at $f(c)=d$ means that $f(y)=f(g(c))+f_{1}(y)(y-g(c))$, so
$$
f\circ g(x)=f(g(x))=f(g(c))+f_{1}(g(x))(g(x)-g(c))
$$
Substituting our $g(x)$:
$$
= f(g(c))+f_{1}(g(x))(g(c)+g_{1}(x)(x-c)-g(c))
$$
$$
= f(g(c))+f_{1}(g(x))g_{1}(x)(x-c)
$$
From this we claim victory as this is the same as the expression for a derivative, so calling $f\circ g=h$, this is equivalent to:
$$
h(c)+h_{1}(x)(x-c)
$$
Where
$$
h_{1}(x)=f_{1}(g(x))g_{1}(x)
$$
So now we just need to take [[Limit|limits]], so since $f_{1}$ is [[Continuity|continuous]] at $g(c)$, and $g_{1}$ is continuous at $c$, then by continuity
$$
\lim_{ x \to c } h_{1}(x)=f_{1}(g(c))g_{1}(c)=f'(g(c))g'(c)
$$
___
A worse proof would involve doing this:
$$
(f\circ g)'=\lim_{ x \to c } \frac{f(g(x))-f(g(c))}{x-c}=\lim_{ x \to c } \frac{f(g(x))-f(g(c))}{g(x)-g(c)} \frac{g(x)-g(c)}{x-c}=f'(g(c))g'(c)
$$
But $g(x)-g(c)$ could be $\hspace{0pt}0$ quite reasonably, so this bad
### Examples
Calculate $\frac{d }{dx}((x^{2}+3x)^{4})$, Let $f(x)=x^{4}$, $g(x)=x^{2}+3x$, then $(x^{2}+3x)^{4}=f(g(x))$, $f'(x)=4x^{3}$, $g'(x)=2x+3$, so
$$
\frac{d 
}{dx}((x^{2}+3x)^{4})=4(x^{2}+3x)^{3}(2x+3) 
$$
## Many Variables
Relations like $\frac{d y}{dt}=\frac{d y}{dx}\frac{d x}{dt}$ do look like an 'algebraic triviality', and essentially, we can treat ordinary derivatives like fractions, but we cannot do the same with partial derivatives
### Example [[Polar Coordinates|2D polars]]
$$
x=r\cos\theta,y=r\sin\theta 
$$
$$
 r=\sqrt{ x^{2}+y^{2} },\theta=\arctan\left( \frac{y}{x} \right)
$$
$$
\frac{ \partial x }{ \partial r } =\frac{ \partial  }{ \partial r } (r\cos\theta)=\cos\theta
$$
$$
\frac{ \partial r }{ \partial x } =\frac{ \partial  }{ \partial x } (\sqrt{ x^{2}+y^{2} })=2x\times \frac{1}{2\sqrt{ x^{2}+y^{2} }}=\frac{x}{r}=\cos\theta
$$
These are not the reciprocals of each other. We can intuit this by looking at some diagrams
![[Chain Rule 2025-01-23 14.41.22.excalidraw]]
This 'anomaly' occurs because different variables are being held constant. In the first example, $y$ is, in the second, $\theta$ is. We sometimes use the notation for the first part as $\frac{ \partial f }{ \partial x }|_{y}$, and second $\frac{ \partial f }{ \partial r }|_{\theta}$
### Chain Rule for $f(x,y)$
$$
\delta f=f(x+\delta x,y+\delta y)-f(x,y)=\frac{ \partial f }{ \partial x } \delta x+\frac{ \partial f }{ \partial y } \delta y+R(x,y)
$$
Where $R(x,y)$ goes to $\hspace{0pt}0$ faster than $\delta x,\delta y$ as $\left| \vec{\delta x} \right|\to0$, so for small $\delta x,\delta y$
$$
\delta f\approx \frac{ \partial f }{ \partial x } \delta x+\frac{ \partial f }{ \partial y } \delta y
$$
So
$$
df=\frac{ \partial f }{ \partial x } dx+\frac{ \partial f }{ \partial y } dy
$$
#### Situation $\hspace{0pt}1$: $f(x(t),y(t))$
Find $\frac{d f}{dt}$ when $f(x,y)$ and $(x(t),y(t))$ i.e. move along a curve parametrically. $f$ can be thought of as a function of $t$: $f((x(t),y(t)))$, then
$$
df=\frac{d f}{dt} dt
$$
But $f$ can also be thought of as a function of $x,y$, so
$$
df=\frac{ \partial f }{ \partial x } dx+\frac{ \partial f }{ \partial y } dy
$$
$x$ and $y$ are both functions of $t$, so
$$
dx=\frac{d x}{dt} dt,dy=\frac{d y}{dt} dt
$$
So substituting these two into the one for $df$ against $x$ and $y$, we get
$$
df=\frac{ \partial f }{ \partial x } \left( \frac{d x}{dt} dt \right)+\frac{ \partial f }{ \partial y } \left( \frac{d y}{dt} dt \right)=\left( \frac{ \partial f }{ \partial x } \frac{d x}{dt} +\frac{ \partial f }{ \partial y } \frac{d y}{dt}  \right)dt
$$
Comparing with the first equation,
$$
\frac{df}{dt}=\frac{ \partial f }{ \partial x } \frac{d x}{dt} +\frac{ \partial f }{ \partial y } \frac{d y}{dt} 
$$
Note this is essentially the original chain rule statement divided by $dt$, since it is an ordinary derivative
##### Example
$$
H(x,y)=e^{ -x^{2}-y^{2} }
$$
$$
(x(t),y(t))=(t,t^{2})
$$
What is $\frac{d H}{dt}$ at $t=1$?
Method 1: Direct substitution
$$
H=e^{ -t^{2}-(t^{2})^{2} }=e^{ -t^{2}-t^{4} }
$$
$$
\implies \frac{d H}{dt} =(-2t-4t^{3})e^{ -t^{2}-t^{4} }=-6e^{ -2 }
$$
Method 2: Chain Rule
$$
\frac{d H}{dt} =\frac{ \partial H }{ \partial x } \frac{d x}{dt}+ \frac{ \partial H }{ \partial y } \frac{d y}{dt} =(-2xe^{ -x^{2}-y^{2} })\times 1+(-2ye^{ -x^{2}-y^{2} })2t=6e^{ -t }
$$
#### Situation $\hspace{0pt}2$: $f(x,y(x))$
Change in function $f(x,y)$ when we move along a curve $y=y(x)$, what is $\frac{d f}{dx}$. $f$ can be thought of as a function of $x$; $f(x,y(x))$, so
$$
df=\frac{d f}{dx} dx
$$
$f$ can also be thought of as a function of $x$ and $y$, $f(x,y)$, then
$$
df=\frac{ \partial f }{ \partial x } dx+\frac{ \partial f }{ \partial y } dy
$$
We know that $y$ changes as a function of $x$, so
$$
dy=\frac{d y}{dx} dx
$$
We can substitute this $dy$ above:
$$
df=\frac{ \partial f }{ \partial x } dx+\frac{ \partial f }{ \partial y } \left( \frac{d y}{dx} dx \right)=\left( \frac{ \partial f }{ \partial x } +\frac{ \partial f }{ \partial y } \frac{d y}{dx}  \right)dx
$$
We can compare this with the first equation gives:
$$
\frac{d f}{dx} =\frac{ \partial f }{ \partial x } +\frac{ \partial f }{ \partial y } \frac{d y}{dx} 
$$
##### Example
An ellipse is given by the equation $x^{2}+y^{2}+xy=7$, find the gradient $\frac{d y}{dx}$ of $C$ at point $(1,2)$
![[Chain Rule 2025-01-24 15.21.26.excalidraw]]
$\frac{d f}{dx} =0$ along $C$ since $f=7$ is constant, so
$$
\frac{d f}{dx} =0=\frac{ \partial f }{ \partial x } +\frac{ \partial f }{ \partial y } \frac{d y}{dx} 
$$
$$
\frac{ \partial f }{ \partial x } =2x+y
$$
$$
 \frac{ \partial f }{ \partial y } =2y+x
$$
$$
\therefore \frac{d y}{dx} =-\frac{ \partial f }{ \partial x } /\frac{ \partial f }{ \partial y } =-\frac{2x+y}{2y+x}=-\frac{4}{5}
$$
## Chain Rule for [[Curves|Paths]]
Let $U\subset \mathbb{C}$ be an [[Open Sets|open set]] and let $f:U\to \mathbb{C}$ be a [[Holomorphicity|holomorphic]] [[Functions|function]] $U$
Let $\gamma:[0,1]\to U$ be a differentiable path (i.e. its real and imaginary parts are differentiable), then for any $t_{0}\in[0,1]$. Then for any $t_{0}\in[0,1]$
$$
(f\circ \gamma)'(t_{0})=f'(\gamma(t_{0}))\gamma'(t_{0})
$$
### Proof
Just like in real analysis


#Mathematics #Calculus 