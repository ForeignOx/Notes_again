A [[Functions|function]] $f(x)$ is monotonic increasing on an [[Intervals|interval]] $[a,b]$ if 
$$
f(x_{1})\leq f(x_{2})\forall x_{1},x_{2}:a\leq x_{1}< x_{2}\leq b
$$
A function $f(x)$ is strictly monotonic increasing in $[a,b]$ if 
$$
f(x_{1})< f(x_{2})\forall x_{1},x_{2}:a\leq x_{1}<x_{2}\leq b
$$
A function $f(x)$ is monotonic decreasing on an interval $[a,b]$ if 
$$
f(x_{1})\leq f(x_{2})\forall x_{1},x_{2}:a\leq x_{1}< x_{2}\leq b
$$
A function $f(x)$ is strictly monotonic decreasing in $[a,b]$ if 
$$
f(x_{1})< f(x_{2})\forall x_{1},x_{2}:a\leq x_{1}<x_{2}\leq b
$$
## Growth Theorem
Let $f:I\to \mathbb{R}$ be a [[Continuity|continuous]] function on an interval $I$, [[Differentiation|differentiable]] in its interior, then
- If $f'(x)=0$ for all $x$, then $f$ is constant
- If $f'(x)\geq 0$, for all $x$, then $f$ is monotonically increasing
- If $f'(x)\leq 0$ for all $x$, then $f$ is monotonically decreasing
- If $f'(x)>0$ for all $x$, then $f$ is strictly monotonically increasing
- If $f'(x)<0$ for all $x$, then $f$ is strictly monotonically decreasing
## Proof
Let $c<d$ be two points in $I$, by [[Mean Value Theorem|MVT]] there is a $\alpha \in(c,d)$ such that
$$
f(d)-f(c)=(d-c)f'(\alpha)=\begin{cases}
0&\text{in case }1
\\
\geq0&\text{in case }2
\\
>0&\text{in case }3
\end{cases}
$$
So we have our result


#Mathematics #Analysis #Definition 