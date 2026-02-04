If [[Functions|$f(x)$]] is [[Continuity|continuous]] on [[Intervals|$[a,b]$]], [[Differentiation|differentiable]] on $(a,b)$ and $f(a)=f(b)$, then $\exists c\in(a,b):f'(c)=0$
## Proof
By the [[Extreme Value Theorem|extreme value theorem]], $\exists x_{1},x_{2}\in[a,b]:f(x_{1})\leq f(x)\leq f(x_{2})\forall x\in[a,b]$
If $x_{2}\in(a,b)$, then $x_{2}$ is a local max and $f'(x_{2})=0$
If $x_{1}\in(a,b)$, then $x_{1}$ is a local minimum, then $f'(x_{1})=0$
If neither are true, $x_{1}$ can't be in the interval and $x_{2}$ cannot be in the interval, so they are endpoints
Otherwise $x_{1}$ and $x_{2}$ are endpoings $a,b$. But since $f(a)=f(b), f(x_{1})$, so $f(a)\leq f(x)\leq f(a)$ for al $x\in(a,b)$
## Corollary
If $f(x)$ is differentiable on an open interval $I$, then each pair of zeros of $f$ is separated by at least one zero of $f'(x)$
This follows from Rolle's Theorem with $a$ and $b$ zeros of $f(x)$ such that $f(a)=f(b)=0$
We can use this to find a bound on the number of distinct zeros of a function
### Example
Show $f(x)=\frac{1}{7}x^7-\frac{1}{5}x^6+x^{3}-3x^{2}-x$ has no more than $\hspace{0pt}3$ distinct real roots
We prove this by contradiction: assume there are at least $\hspace{0pt}4$ real roots of $f(x)$, then by Rolle's theorem, there are at least $\hspace{0pt}3$ distinct real roots of $f'(x)$:
$$
f'(x)=x^6-\frac{6}{5}x^{5}+3x^{2}-6x-1
$$
Then applying Rolle's theorem to $f'(x)$, there are at least $\hspace{0pt}2$ distinct real roots of:
$$
f''(x)=6x^5-6x^4+6x-6=6(x^5-x^4+x-1)=6(x-1)(x^{4}+1)
$$
But $x^{4}\geq 0$, so $x^{4}\neq-1$ in $\mathbb{R}$, so $f''(x)$ has only $\hspace{0pt}1$ real root hence contradiction yayyy


#Mathematics #Analysis #Calculus #Theorem 