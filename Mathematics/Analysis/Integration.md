# Real Integration
## Definite Integrals
There are many examples of ways to construct definite integrals analytically, for example [[Regulated Integrals|regulated integrals]], Riemann integrals and Lebesgue integrals to name some
The regulated integral is based on the approximation of the function by step functions. This can be thought of as focusing on a partition of the values of $f$ on the $y$-axis
The regulated integral arises as the limit of integrals of the approximating functions
The Riemann integral on the other hand directly approximates the signed area under the graph of $f$
The Riemann integral focuses on the partition of the $x$-axis
Since Riemann integration is fairly difficult to deal with, we usually consider the equivalent definition which is of Darboux Integrability
The Lebesgue integral is a generalisation of the Riemann integral. The Lebesgue integral uses a much more refined construction, which allows one to integrate over different spaces, and, under suitable conditions, allows to interchange limits and integrals 
The construction of the Lebesgue integral is via [[Measures|measure]] theory, which was created to provide a more detailed analysis of lengths of subsets of the real line, and more generally, area and volume for subsets of Euclidean spaces
The Lebesgue integral is extremely important in many fields, including [[Probabilities|probability]], where we can integrate with respect to the probability measure; the [[Expectation|expectation]]
In fact, part of this theory allows for the construction of probability measures on uncountable spaces, such as the uniform probability measure on $[0,1]$
### Regulated Integrals
Let $f:[a,b]\to \mathbb{R}$ be a [[Regulated Functions|regulated function]], say [[Sequences of Functions|$f_{n}\to f$]] where $f_{n}$ are [[Step Functions|step functions]], then we say the integral of $f$ is:
$$
I(f)=\lim_{ n \to \infty } I(f_{n})
$$
Where $I(f_{n})$ is the integral of the step functions, or the [[Riemann Sums|riemann sums]]
We need to check whether this limit exists however
### Riemann Integrals
A function $f$ is called Riemann integrable if the limit of all Riemann sums exists as the mesh of the partition (the length of the largest sub-interval) goes to $\hspace{0pt}0$, if there exists a number $s$ (the integral of $f$) such that for all $\varepsilon>0$ there exists $\delta>0$ such that for all Riemann sums associated to a partition with mesh less that $\delta$, we have
$$
\left| s-\sum_{k=0}^{N-1}f(x_{k}^{*})(x_{k+1}-x_{k}) \right| <\varepsilon
$$
### Darboux Integration
A function $f$ is Darboux integrable, if for any partition $P$, one sets 
$$
m_{k}=\inf_{x\in [x_{k},x_{k+1}]}\left\{ f(x) \right\}
$$
$$
M_{k}=\sup_{x\in [x_{k},x_{k+1}]}\left\{ f(x) \right\}
$$
Here, one needs to assume $f$ is [[Boundedness|bounded]]
And defines the lower and upper Riemann sums as
$$
L(f,P)=\sum_{k=0}^{N-1}m_{k}(x_{k+1}-x_{k}),~U(f,P)=\sum_{k=0}^{N-1}M_{k}(x_{k+1}-x_{k})
$$
One then defines the lower and upper Riemann integrals by
$$
L_{f}=\sup_{P}L(f,P)=\underline{\int}_{P}f,~    U_{f}=\inf_{P}(f,P)=\overline{\int}_{P}f
$$
And calls $f$ Darboux-integrable if $U_{f}=L_{f}$
## Indefinite Integrals (or Anti-[[Differentiation|Derivative]]s)
A [[Functions|function]] $F(x)$ is called an indefinite integral or antiderivative of a function $f(x)$ in the [[Intervals|interval]] $(a,b)$ if $F(x)$ is differentiable:
$$
F'(x)=f(x)\forall x\in (a,b)
$$
We write:
$$
F(x)=\int f(x) \, dx
$$
Note that if $F(x)$ is an indefinite integral, then so is $F(x)+c$ for any constant $c$, since $\frac{d }{dx}(F(x)+c)=\frac{d }{dx}(F(x))$
It is important to include this arbitrary constant when writing indefinite integrals
If $F_{1}(x)$ and $F_{2}(x)$ are both indefinite integrals of $f(x)$, then $F_{2}(x)-F_{1}(x)=c$, since:
$$
\frac{d }{dx} (F_{2}(x)-F_{1}(x))=\frac{d }{dx} (F_{2}(x))-\frac{d }{dx} (F_{1})(x)=f(x)-f(x)=0
$$
Therefore $F_{2}(x)-F_{1}(x)$ is constant. or is it...? yeh it is
___
### Examples
Let $f(x)=\frac{1}{x}$ on $(0,\infty)$, set 
$$
L(x)=\int_{1}^{x} \frac{1}{t} \, dt
$$
Then $L(1)=0$, $L'(x)=\frac{1}{x}$ from [[Fundamental Theorem of Calculus|FToC]]. Now $L(x)$ is increasing, $L'(x)>0$, we also have 
$$
L(xy)=L(x)+L(y)
$$
We can show it is true for one point $y=1$, we want to take derivatives and show that it is constant:
$$
LHS:  y\times \frac{1}{xy}=\frac{1}{x}
$$
$$
RHS: \frac{1}{x}
$$
These are the same, so this is always true, so we also have by letting $y=\frac{1}{x}$:
$$
L\left( \frac{1}{x} \right)=-L(x)
$$
We also know that $L(2)>\frac{1}{2}$, since
$$
\int_{1}^{2} \frac{1}{t} \, dt >\int_{1}^{2} \frac{1}{2} \, dt
$$
We can then say that $L(2^{n})>\frac{n}{2}$ by using the addition law many times, i.e. $nL(2)$, so $L(x)\to \infty$ as $x\to \infty$
So we have a function that satisfies all the logarithm properties, so it is the logarithm, hence we have the exponential function as the inverse, so from this we can get $\sinh$ and $\cosh$ properties ect. We can do the same technique with $\arcsin$ to find $\sin$
## Integrability
We say $f(x)$ is integrable in $(a,b)$ if it has an indefinite integral on $(a,b)$ which is [[Continuity|continuous]] on $[a,b]$
## Definite Integrals
A definite integral of a function $f(x)$ gives the (signed) area between $f(x)$ and the $x$-axis
![[Integration 2024-11-05 14.26.00.excalidraw]]
In the above diagram, the green would have positive area, and the blue, negative
We define this as the [[Limit|Limit]] of a [[Riemann Sums|Riemann Sum]], by splitting the area into rectangles:
![[Integration 2024-11-05 14.28.16.excalidraw]]
There are lots of ways we could do this, by choosing where we place the $x_{i}$s and where we define the heights of the rectangles. If $f(x)$ is continuous, and the rectangles have small width, we expect this to be a good approximation and the error can be reduced to zero by taking the limit of the width of the rectangles to zero. We say this limit exists if it is independent of how we construct hte rectangles
The definite integral is given in terms of a Riemann sum by taking a limit as the [[Subdivisions|norm]] $|S|$ goes to 0
We say this limit exists if it is independent of subdivision and set of sample points:
Let $f(x)$ be defined $\forall x\in[a,b]$, the definite integral of $f(x)$ from $a$ to $b$ is then:
$$
\int ^{b}_{a} f(x) \, dx =\lim_{ |S| \to 0 } R
$$
It can be shown that this limit does exists if $f$ is continuous on $[a,b]$
We can define:
$$
\int ^{b}_{a} f(x) \, dx= -\int ^{a}_{b}  f(x)\, dx 
$$
Which implies:
$$
\int ^{a}_{a} f(x) \, dx=0
$$
### Properties
The definite integral satisfies the following properties:
Let $f(x),g(x)$ be integrable functions in $(a,b)$
- Linearity, if $\lambda,\mu \in\mathbb{R}$, then $(\lambda f+\mu g)(x)$ is also integrable in $(a,b)$ with
$$
\int ^{b}_{a} (\lambda f+\mu g)(x) \, dx =\lambda \int ^{b}_{a} f(x) \, dx +\mu \int ^{b}_{a} g(x) \, dx 
$$
- If $c\in[a,b]$, then we have additivity:
$$
\int ^{b}_{a} f(x) \, dx =\int ^{c}_{a} f(x) \, dx +\int ^{b}_{c} f(x) \, dx 
$$
- If $f(x)\geq g(x)\forall x\in(a,b)$, then we have monotonicity:
$$
\left| \int ^{b}_{a} f(x) \, dx  \right| \leq \int ^{b}_{a} \left| f(x) \right|  \, dx 
$$
$$
\int ^{b}_{a} f(x) \, dx \geq \int ^{b}_{a} g(x) \, dx 
$$
- If $m\leq f(x)\leq M\forall x\in(a,b)$ then
$$
m(b-a)\leq\int ^{b}_{a} f(x) \, dx \leq M(b-a)
$$
- If $f(x)\geq 0\forall x\in(a,b)$, then and $f$ continuous and there exists a point $c\in[a,b]:f(c)>0$
$$
\int ^{b}_{a} f(x) \, dx >0
$$
#### Proof of Monotonicity
By linearity, it is enough to consider if $f(x)\geq 0$ and show $\int ^{b}_{a} f(x) \, dx \geq 0$. So take $f_{n}\to f$ uniformly, so given $\varepsilon>0$, find $f_{n}(x)$ such that $\left| f(x)-f_{n}(x) \right|<\varepsilon \forall x\in[a,b]$
Since $f(x)>0$, we get
$$
f_{n}(x)>-\varepsilon \forall x\in [a,b]
$$
(We can't rule out that $f_{n}$ is not negative, but the most negative it can be is if $f(x)=0\forall x\in[a,b]$, giving us the above inequality)
![[Integration 2025-03-13 11.26.40.excalidraw]]
This means that
$$
I(f_{n})>-\varepsilon(b-a)
$$
So $\lim_{ n \to \infty }I(f_{n})$ is bigger than any negative number $\implies I(f)\geq 0$
Next consider that $\left| f(x) \right|=\pm f(x)$, so $f(x)\leq \left| f(x) \right|$, but $\left| f(x) \right|>0$, so we get our property with absolute values we want
For the last part we can consider the following diagram:
![[Integration 2025-03-13 11.33.41.excalidraw]]
#### Proof of $f(x)\geq 0\implies \int ^{b}_{a} f(x) \, dx\geq 0$ 
Set $C=f(c)$, by continuity, there exists a $\delta>0$ such that $f(x)>\frac{C}{2}$ for $\left| x-c \right|<\delta$ with this:
$$
\int ^{b}_{a} f(x) \, dx =\int_{a}^{c-\delta} \underbrace{ f(x) }_{ \geq 0 } \, dx +\int_{c-\delta}^{c+\delta} \underbrace{ f(x) }_{ \geq \frac{C}{2} } \, dx +\int_{c+\delta}^{b} \underbrace{ f(x)  }_{ \geq 0 }\, dx \geq 0+\frac{C}{2}2\delta+0=C\delta>0
$$
This does in fact require continuity, consider the function
$$
f(x)=\begin{cases}
0 & x\neq 0\\1 & x=0
\end{cases}
$$
Which is not continuous at $x=0$, and $f(x)\geq 0$, but $\int_{-1}^{1} f(x) \, dx=0$ since the step functions tend to 0
# Complex Integration
## Definition
Consider a continuous function $f:[a,b]\to \mathbb{C}$ where $[a,b]\subseteq \mathbb{R}$, we define
$$
\int ^{b}_{a} f(t) \, dt=\int ^{b}_{a} \mathfrak{R}(f(t))+i\mathfrak{I}(f(t)) \, dt=\int ^{b}_{a} \mathfrak{R}(f(t)) \, dt+i\int ^{b}_{a} \mathfrak{I}(f(t)) \, dt    
$$

## Example
Find $\int_{0}^{1} f(t) \, dt$ where $f(t)=t+it$
$$
    \int_{0}^{1} t+it \, dt =\int_{0}^{1} t \, dt+i\int_{0}^{1} t \, dt  =\frac{1+i}{2}
$$
## Lemma
Let $f_{1}$ and $f_{2}$ be continuous functions from $[a,b]$ to $\mathbb{C}$, then
$$
\int ^{b}_{a} f_{1}(t)+f_{2}(t) \, dt=\int ^{b}_{a} f_{1}(t) \, dt+\int ^{b}_{a} f_{2}(t) \, dt   
$$
For any complex number $c\in\mathbb{C}$,
$$
\int ^{b}_{a} cf_{1}(t) \, dt=c\int ^{b}_{a} f_{1}(t) \, dt  
$$
### Proof
By definition
## Contour Integration
Let $U\subseteq \mathbb{C}$ be an open set and let $f:U\to \mathbb{C}$ be a continuous function. Let $\gamma:=[a,b]\to U$ be $C^{1}$. Then we define the integral of $f$ along the curve $\gamma$ by its [[Line Integrals|contour integral]]:
$$
\int _{\gamma}f(z) \, dz:=\int ^{b}_{a} f(\gamma(t))\gamma'(t) \, dt  
$$
If $\gamma:[a,b]\to U$ is a contour with partition $a=a_{0}<a_{1}<\dots<a_{n}=b$ such that $\gamma |_{[a_{i-1},a_{i}]}\to \mathbb{C}$ are $C^{1}$ curves for $i=1,\dots,n$, then we define
$$
\int _{\gamma}f(z) \, dz=\sum_{i=1}^{n} \int _{\gamma_{i}}f(z) \, dz 
$$
Note that integration in this form is not as simple as line integration as the dot product and complex multiplication are not comparable



#Mathematics #Calculus #Definition