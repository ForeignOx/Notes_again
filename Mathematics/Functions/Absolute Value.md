Two important properties of a [[Real Numbers|real number]] are its sign and size, or magnitude. Geometrically the sign of $a$ tells us whether the point $a$ is on the right or left of $\hspace{0pt}0$ on a number line. The magnitude of $a$ is the distance between the point $a$ and $\hspace{0pt}0$; $\hspace{0pt}0$ itself does not have a sign and its magnitude is $0$. The magnitude of $a$ is more commonly called the absolute value of $a$, denoted $|a|$, and is a function:
$$
\mathbb{R}\to[0,\infty)]
$$
For $x \in \mathbb{R}$
$$
|x|=\begin{cases}
x && \text{for }x\geq 0\\-x && \text{for }x<0
\end{cases}=\text{max}(a,-a)=\sqrt{ a^{2} }
$$
Geometrically, $|a|$ represents the distance between $a$ and $0$, $|a-c|$ represents the distance between $a$ and $c$
## Properties
Let $a,b\in\mathbb{R}$
- $|a|=0\iff a=0$
- $|-a|=|a|\geq 0$
- $|ab|=|a||b|$
- $|a+b|\leq|a|+|b|$, known as the [[Triangle Inequality|triangle inequality]]. This is analogous to the fact that in a triangle the length of one side cannot exceed the sum of the lengths of the other two sides
- $||a|-|b| |\leq|a-b|$ this is a variant of the triangle inequality
- $|a|^{2}=|a^{2}|=a^{2}$
- $|a|\leq b\iff-b\leq a\leq b$
- $|x|\geq a\iff x\geq a\text{ or }x\leq -a$, these last two also apply for strict inequalities in the way you'd imagine
## $|x-a|<b \iff a-b<x<a+b$ 
If $b<0$ then both statements are never true
We know that either $x-a\geq 0$ or $x-a<0$
If $x-a\geq 0$
$$
x\geq a
$$
$$
\implies |x-a|=x-a
$$
    If $|x-a|<b$
$$
x-a<b
$$
$$
\implies x<a+b
$$
    Since $a\leq x$, $b>0$
$$
a-b< a\leq x
$$
$$
\implies a-b<x
$$
$$
\therefore a-b<x<a+b
$$
    If $a-b<x<a+b$
$$
x-a<b 
$$
$$
\implies |x-a|<b
$$
    So if $x-a\geq 0$ then:
$$
a-b<x<a+b \iff |x-a|<b
$$
If $x-a<0$
$$
|x-a|=-(x-a)=a-x
$$
$$
x<a
$$
    If $|x-a|<b$
$$
a-x<b
$$
$$
\implies a<b+b
$$
$$
\implies a-b<x
$$
    Since $b>0$
$$
x<a<a+b
$$
$$
\implies a-b<x<a+b
$$
    If $a-b<x<a+b$
$$
a<x+b
$$
$$
\implies a-x<b
$$
$$
\implies |x-a|<b
$$
    So if $x-a<0$ then:
$$
|x-a|<b\iff a-b<x<a+b
$$
So $\forall x,a\in\mathbb{R}$, $b\in\mathbb{R}^+$:
$$
|x-a|<b \iff a-b<x<a+b
$$
A graphical depiction is thus
![[Absolute Value 2024-10-20 21.56.25.excalidraw]]
## $0<|x-a|<b\iff a-b<x<c\text{ or }c<x<c+b$ 
This is like the previous inequality, but has the exra requirement that $x\neq a$
The combination of these inequalities are essential to the formal definition of [[Limit|limits]] 

## Examples
1. Solve $|3x-4|\leq 2$:
$$
|3x-4|\leq 2\iff-2\leq 3x-4\leq 2
$$
$$
 \iff 2\leq 3x\leq 6
$$
$$
\iff \frac{2}{3}\leq x\leq 2
$$
$$
\iff x\in \left[ \frac{2}{3},2 \right]
$$
    Solution set is $\left[ \frac{2}{3},2 \right]$
2. Solve $|2x+3|>5$
$$
|2x+3|>5
$$
$$
 \iff 2x+3<-5\text{ or }2x+3>5
$$
$$
\iff x<-4\text{ or }x>1
$$
$$
\iff x\in (-\infty,-4)\cup(1,\infty)
$$
    So the solution set is $(-\infty,-4)\cup(1,\infty)$

3. Solve $|x+2|\leq|2x-1|$
$$
(x+2)^{2}\leq(2x-1)^{2}
$$
$$
 \iff x^{2}+4x+4\leq 4x^{2}-4x+1
$$
$$
 \iff 0\leq 3x^{2}-8x-3=(3x+1)(x-3)
$$
$$
 \iff x\geq 3\text{ or }x\leq-\frac{1}{3}
$$
$$
 \iff x\in \left( \infty,-\frac{1}{3}\right]\cup[3,\infty)
$$
    Solution set is $\left( \infty,-\frac{1}{3}\right]\cup[3,\infty)$
## Extension to [[Complex Numbers|Complex Numbers]]
The absolute value of $z\in\mathbb{C}$ is defined as:
$$
\left| z \right| =\sqrt{ z\cdot\overline{z} }
$$
### Properties
Let $z,w\in\mathbb{C}$, then
- $\left| z \right|=0$ iff $z=0$
- $\left| z\cdot w \right|=\left| z \right|\cdot \left| w \right|$
- $\left| z+w \right|\leq \left| z \right|+\left| w \right|$ ([[Triangle Inequality|triangle inequality]])

#Mathematics #Functions #Definition