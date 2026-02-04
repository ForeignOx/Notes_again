If [[Functions|$f(x)$]] is [[Continuity|continuous]] on [[Intervals|$[a,b]$]] and [[Differentiation|differrentiable]] on $(a,b)$, then $\exists c\in(a,b)$ such that:
$$
f'(c)=\frac{f(b)-f(a)}{b-a}
$$
Geometrically, this means there is at least one point at which the tangent is parallel to the line joining the end points
## Proooooooooooooooooooooooooooooooooof
Let 
$$
g(x)=(b-a)(f(x)-f(a))-(x-a)(f(b)-f(a))
$$
(the shear of $f(x)$), then $g(a)=0=g(b)$ and $g(x)$ satisfies the requirements of [[Rolle's Theorem|Rolle's theorem]], so $\exists c\in(a,b)$ such that $g'(c)=0$, but
$$
g'(x)=(b-a)f'(x)-(f(b)-f(a))
$$
So
$$
g'(c)=(b-a)f'(c)-(f(b)-f(a))=0
$$
implies
$$
f'(c)=\frac{f(b)-f(a)}{b-a}
$$

___
We can use the mean value theorem to prove results relating monoticity to the sign of the derivative
Suppose $f(x)$ is continuous on $[a,b]$, and differentiable on $(a,b)$ with $f'(x)\geq 0\forall x\in(a,b)$, then $f(x)$ is monotonic increasing
## Proof
If $a\leq x_{1}<x_{2}\leq b$, then by the MVT,
$$
\exists c\in(x_{1},x_{2}):f'(c)=\frac{f(x_{2})-f(x_{1})}{x_{2}-x_{1}}
$$
Since $f'(x)\geq 0\forall x\in(x_{1},x_{2})$, then we must have $f(x_{2})\geq f(x_{1})$, so $f(x)$ is monotonic increasing
We can show similar results for monotonic decreasing and strictly monotonic increasing/decreasing
## Cauchy's Generalised Mean Value Theorem
Let $f,g:[a,b]\to \mathbb{R}$ be continuous and differentiable on $(a,b)$. Asume $g'(x)\neq 0\forall x\in(a,b)$. then there exists $c\in(a,b)$ such that
$$
\frac{f'(c)}{g'(c)}=\frac{f(b)-f(a)}{g(b)-g(a)}
$$
If you try the mean value theorem, you get $c\in(a,b)$, with 
$$
f'(c)= \frac{f(b)-f(a)}{b-a}
$$
And
$$
g'(c)= \frac{g(b)-g(a)}{b-a}
$$
This would seem like you could divide here, but the values of $c$ could be different, so we need something else
### Proof
Consider
$$
h(x)=(g(b)-g(a))f(x)-(f(b)-f(a))g(x)
$$
By Rolle there is $c\in(a,b)$ with $h'(c)=0$,
$$
h'(c)=(g(b)-g(a))f'(c)-(f(b)-f(a))g'(c)=0
$$
Which can be rearranged to get the result we want
## Mean Value Theorem for [[Integration|Integration]]
Let $f(x)$ be [[Continuity|continuous]] and integrable on $[a,b]$, then there exists $c\in[a,b]$, such that
$$
\int ^{b}_{a} f(x) \, dx =c(b-a)
$$
### Proof
$f$ is continuous, hence takes minimum $m$, and maximum $M$ (since [[Regulated Functions|regulated functions]] are [[Boundedness|bounded]], so we can find [[Supremum and Infimum|supremum and infimum]], which we take to be the [[Maximum|maximum]] and [[Minimum|minimum]])
We know that
$$
m(b-a)\leq \int ^{b}_{a} f(t) \, dt \leq M(b-a)
$$
Then there exists some number $C$, which we define to be
$$
C=\frac{\int ^{b}_{a} f(t) \, dt}{b-a}
$$
With $m\leq c\leq M$ (by dividing the above equation by $b-a$)
By the [[Intermediate Value Theorem|intermediate value theorem]], there exists $c\in[a,b]:f(c)=C$, so
$$
f(c)(b-a)=C(b-a)=\int ^{b}_{a} f(x) \, dx 
$$
___
We do really need continuity:
For example if we take 
$$
f(x)=\begin{cases}
0 & x\in \left[ 0,\frac{1}{2} \right]\\1 & x\in \left[ \frac{1}{2},1 \right]
\end{cases}
$$
Then $\int_{0}^{1} f(x) \, dx=\frac{1}{2}$, here $b-a=1$, but no value of $f(x)$ takes the value $\frac{1}{2}$, so we have a counterexample
## Mean Value Theorem for [[Double Integrals|Double Integrals]]
If $f:\mathbb{R}^{3}\to \mathbb{R}$ is a continuous [[Scalar Fields|scalar field]] on a closed, bounded and connected domain $A\subset \mathbb{R}^{2}$ then there exists $\underline{x}_{*}$ such that:
$$
\int _{A}f \, dS=\left| A \right| f(\underline{x}_{*}) 
$$
### Proof
Under the given conditions, (closed, bounded, connected), we know that $f$ attains its maximum and minimum on $A$, say $\underline{x}_\text{max},\underline{x}_\text{min}$, also
$$
\left| A\right|f(\underline{x}_\text{min})\leq \int _{A}f \, dS \leq \left| A \right| f(\underline{x}_\text{max}) 
$$
Now let $\underline{x}(t)$ for $t\in[t_{0},t_{1}]$ be a [[Curves|curve]] in $A$, such that $\underline{x}(t_{0})=\underline{x}_\text{min},\underline{x}(t_{1})=\underline{x}_\text{max}$
Let $g(t)=\left| A \right|f(\underline{x}(t))$, so 
$$
g(t_{0})=\left| A \right|f(\underline{x}_\text{min}), g(t_{1})=\left| A \right|f(\underline{x}_\text{max})
$$
And since $g$ is continous (as $f$ is continuous), by the [[Intermediate Value Theorem|intermediate value theorem]], there exits $t_{*}\in[t_{0},t_{1}]$ such that $g(t_{*})=\int _{A} f \, dS$
Then at $\underline{x}_{*}=\underline{x}(t_{*})$, we have $\left| A \right|f(\underline{x}_{*})=\int _{A}f \, dS$



#Mathematics #Calculus #Theorem 