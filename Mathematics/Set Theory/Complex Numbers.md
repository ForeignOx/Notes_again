Whenever $x\in\mathbb{R}$, $x^{2}\geq 0$. This means the equation $x^{2}+1=0$ does not have a solution in [[Real Numbers|$\mathbb{R}$]]. Historically, complex numbers arose by adding an 'imaginary' number $i$ to the reals which satisfies $i^{2}=-1$, and then calculate as if we just dealt with real numbers. A formal approach that justifies this method can be descrived as follows. We define the set $\mathbb{C}$ of complex numbers to be the [[Cartesian Product|cartesian product]] of $\mathbb{R}$ with itself. That is, a complex number $z\in\mathbb{C}$ is an ordered pair of real numbers
$$
z=(x,y)\in \mathbb{R}^{2}
$$
We can think of $\mathbb{R}$ as sitting inside $\mathbb{C}$ by identifying $x\in\mathbb{R}$ with $(x,0)\in\mathbb{C}$
In order to calculate with complex numbers, we need to define how to add and multiply them. This should of course extend the addtition and multiplication of real numbers via our identification. For this, let $(x_{1},y_{1}),(x_{2},y_{2})\in\mathbb{C}$ and set
$$
(x_{1},y_{1})+(x_{2},y_{2})=(x_{1}+x_{2},y_{1}+y_{2})\in \mathbb{C}
$$
And
$$
(x_{1},y_{1})\cdot(x_{2},y_{2})=(x_{1}x_{2}-y_{1}y_{2},x_{1}y_{2}+y_{1}x_{2})\in \mathbb{C}
$$
In particular, addition is defined coordinate wise, whereas multiplication is not
One can show that $\mathbb{C}$ with this addition and multiplication satisfies the axioms of addition, multiplication and distributivity of the real numbers
One can now also check that
$$
(0,1)\cdot(0,1)=(-1,0)=(0,-1)\cdot(0,-1)
$$
And now also introducd the more usual notation
$$
(x,y)=x+iy
$$
And hence
$$
i^{2}=-1=(-i)^{2}
$$
## Complex Conjugate
Let $z=x+iy\in\mathbb{C}$. THe complex conjugate of $z$, denoted $\overline{z}$, is defined as:
$$
\overline{z}=x-iy
$$
Let $z,w\in\mathbb{C}$ with $z=x+iy$. Then
- $\overline{z+w}=\overline{z}+\overline{w}$
- $\overline{z\cdot w}=\overline{z}\cdot\overline{w}$
- $\overline{\overline{z}}=z$
- $\overline{z}=z$ iff $z=x$
- $\overline{z}=-z$ iff $z=iy$
- $z\cdot\overline{z}=x^{2}+y^{2}\geq 0$, since $x$ and $y$ are real numbers

## Important Properties of Complex Numbers
- $z_{1}z_{2}=0 \iff z_{1}=0\text{ or }z_{2}=0$
- $\left| z \right|=\sqrt{ z \overline{z} }$
- $\overline{zw}=\overline{z}\cdot\overline{w}$
- $\mathrm{Re}(z)= \frac{z+\overline{z}}{2},\mathrm{Im}(z)= \frac{z-\overline{z}}{2i}$
- $z^{-1}= \frac{\overline{z}}{\left| z \right|^{2}}$

## Polar Form
We define for any $z\in\mathbb{C}$
$$
r:=\sqrt{ x^{2}+y^{2} }=\sqrt{ \mathrm{Re}(z)^{2}+\mathrm{Im}(z)^{2} }=\left| z\right| 
$$
And for any $z\neq 0$
$$
\theta:=\begin{cases}
\arctan\left( \frac{y}{x} \right) & x>0 \\
\frac{\pi}{2} & x=0,y>0 \\
-\frac{\pi}{2} &  x=0,y<0 \\
\arctan\left( \frac{y}{x} \right)+\pi & x<0,y>0 \\
\arctan\left( \frac{y}{x} \right)-\pi & x<0,y<0
\end{cases}
$$
Here $\theta$ is the anticlockwise angle measured from the real axis and is called the argument of $z$, denoted $\text{arg}(z)$
The argument is only defined up to multiples of $2\pi$:
$$
\text{arg}(z)=\theta+2\pi k,k\in \mathbb{Z}
$$
And is hence not a [[Functions|function]]
To define an argument, we need to define a range of values; The principle value of $\text{arg}(z)$ is the value in the interval $(-\pi,\pi]$ and is denoted $\text{Arg}(z)$
### Properties of Argument
- $\mathrm{arg}(z_{1}z_{2})=\mathrm{arg}(z_{1})+\mathrm{arg}(z_{2})\mod 2\pi$
- $\mathrm{arg}\left( \frac{1}{z} \right)=-\mathrm{arg}(z)\mod 2\pi$
- $\mathrm{arg}(\overline{z})=-\mathrm{arg}(z) \mod 2\pi$
### Geometrical Intuition for Complex Multiplication
Geometrically, multiplication in $\mathbb{C}$ is given by a dilated rotation; if $z_{1}=r_{1}(\cos(\theta_{1})+i\sin(\theta_{1})),z_{2}=r_{2}(\cos(\theta_{2})+i\sin(\theta_{2}))$, then
$$
z_{1}z_{2}=r_{1}r_{2}(\cos(\theta_{1}+\theta_{2})+i\sin(\theta_{1}+\theta_{2}))
$$
Which we can show manually using trig identities. Which also proves the first property of argument
### Exponential Notation
This motivates the notation
$$
e^{ i\theta }:=\cos\theta+i\sin\theta
$$
And we find that
$$
e^{ i\theta_{1} }e^{ i\theta_{2} }=e^{ i(\theta_{1}+\theta_{2}) }
$$
(But this is just notation for now)
We also find that
- $\left| z_{1}z_{2} \right|=\left| z_{1} \right|\left| z_{2} \right|$
- De Moivre's Theorem $(\cos\theta+i\sin\theta)^{n}=\cos(n\theta)+i\sin(n\theta)$
The modulus also has the following important properties (derived from it being a [[Norms|norm]]):
- [[Triangle Inequality|Triangle Inequality]] $\left| z_{1}+z_{2} \right|\leq \left| z_{1} \right|+\left| z_{2} \right|$
- $\left| z \right|\geq 0$ and $\left| z  \right|=0 \iff z=0$, known as positivity
- $\max(\left| \mathrm{Re}(z) \right|,\left| \mathrm{Im}(z) \right|)\leq \left| z \right|\leq \left| \mathrm{Re}(z)+\mathrm{Im}(z) \right|$
## Geometric Domains
We can use $\mathrm{arg}(z)$ and $\left| z \right|$ to describe geometric sets:
- $\mathbb{D}:=\left\{ z\in\mathbb{C}\mid \left| z \right|<1 \right\}$ is the unit disc (without the circle)
- $\mathbb{H}:=\left\{ z\in \mathbb{C}\mid \mathrm{Im}(z)>0 \right\}$ is the upper half plane (without the $x$-axis)
- $\mathbb{H}_{R}:=\left\{ z\in\mathbb{C}\mid \mathrm{Re}(z)>0 \right\}$ is the right half of the plane (without the $y$-axis)
- $\mathbb{H}_{L}:=\left\{ z\in\mathbb{C} \right\}\mid \mathrm{Re}(z)<0$ is the left halve of the plane (without the $y$-axis)
- $\left\{ z\in \mathbb{C}\mid\mathrm{arg}(z)=\alpha \right\}$ A ray of angle $\alpha$ 
- $\left\{ z\in\mathbb{C}\mid \left| z-z_{0} \right|=r_{0} \right\}$ is a circle centred at $z_{0}$ with radius $r_{0}$
### Example
What is the set $\left| z-i \right|=\left| z+i \right|$
We are looking for the points whose distance from $i$ is the same as from $-i$, so the real line
$$
\left| x+i(y-1) \right| =\left| x+i(y+1) \right| 
$$
$$
 \iff \left| x+i(y-1) \right| ^{2}=\left| x+i(y+1) \right|^{2}
$$
$$
 \vdots
$$
$$
 \iff 4y=0 
$$





#Mathematics #Set 