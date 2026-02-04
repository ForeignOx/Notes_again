
## Case for $x^{4}+y^{4}=z^{2}$
The diophantine equation $x^{4}+y^{4}=z^{2}$ has no positive integer solutions
### Proof
Assume a solution $(x_{0},y_{0},z_{0})$ exists such that $z_{0}$ is minimal
1. Show [[Greatest Common Divisor|$gcd(x_{0},y_{0},z_{0})=1$]]; they are coprime
Consider $p|x_{0}$ and $p|y_{0}$ for some prime $p$, then we can write $x_{0}=px_{1}$ and $y_{0}=py_{1}$ for some $x_{1},y_{1}\in\mathbb{Z}$, Thus:
$$
(px_{1})^{4}+(py_{1})^{4}=z_{0}^{2}
$$
$$
\implies p^{4}x_{1}^{4}+p^{4}y_{1}^{4}=z_{0}^{2}
$$
As $p^{4}|LHS$, $p^{4}|RHS$, so $p^{2}|z_{0}$ (as we are only using integers) and we can write $z_{0}=p^{2}z_{1}$ for some $z_{1}\in\mathbb{Z}$
Hence $p^{4}(x_{1}^{4}+y_{1}^{4})=p^{4}z_{1}^{2}$, so $x_{1}^{4}+y_{1}^{4}=z_{1}^{2}$, so there is another solution with $z_{1}<z_{0}$ which gives a contradiction by [[Proof by Infinite Descent]] 
A similar argument can be used to show $gcd(x_{0},z_{0})=1$ and $gcd(y_{0},z_{0})=1$ (only one needs to be shown)
2. Use what we know about [[Primitive Pythagorean Triples]] 
As $gcd(x_{0},y_{0},z_{0})=1$, we know $gcd(x_{0}^{2},y_{0}^{2},z_{0}^{2})=1$, then $x_{0}^{2}$, $y_{0}^{2}$, $z_{0}^{2}$ is a solution to $x^{2}+y^{2}=z^{2}$, it is a pythagorean triple. Choose $x_{0}^{2}$ to be even, then we can say:
$$
x_{0}^{2}=2st
$$
$$
y_{0}^{2}=t^{2}-s^{2}
$$
$$
z_{0}^{2}=s^{2}+t^{2}
$$
For $s,t\in\mathbb{Z}^{+}$ with $gcd(s,t)=1$ and $s,t$ have different parities
3. Want to show in fact $s$ is even and $t$ is odd
$$
y_{0}^{2}=t^{2}-s^{2}
$$
$$
\implies t^{2}=y_{0}^{2}+s^{2}
$$
We know $y_{0}^{2}$ is odd as $x_{0}$ is even, hence it has a remainder of 1 on division by 4, so $RHS=t^{2}=4k+1$ for some $k\in\mathbb{Z}$, which is impossible for an integer square. Hence, $s^{2}$ can't be odd, so $s$ must be even and $t$ must be odd. We can use this to write $s=2r,r\in\mathbb{Z}^+$
4. Use what we know about primitive pythagorean triples
$$
t^{2}=y_{0}^{2}+s^{2}
$$
with $gcd(s,t)=1$, so $gcd(s,t,y_{0})=1$ so $(s,t,y_{0})$ is another pythagorean triple with $s$ being even, so we can write:
$$
s=2uv
$$
$$
y_{0}=v^{2}-u^{2}
$$
$$
t=u^{2}+v^{2}
$$
FOr $u,v\in\mathbb{Z}^+$, $gcd(u,v)=1$ and $u,v$ have different parities
5. Consider $x_{0}^{2}=2st$
$$
x_{0}^{2}=2(2r)t=4rt
$$
$$
\implies \left( \frac{x_{0}}{2} \right)^{2}=rt
$$
LHS is a perfect square, so RHS must be also, we know $gcd(s,t)=1$, so $gcd(r,t)=1$ 
Hence $r$ and $t$ must each be perfect squares, and we can write $r=w_{1}^{2}$ and $t=z_{1}^{2}$ for $w_{1},z_{1}\in\mathbb{Z}^+$
6. Consider also $s=2uv$
$$
2r=2uv
$$
$$
\implies r=uv
$$
$$
\implies w_{1}^{2}=uv
$$
We know $gcd(u,v)=1$, so $u$ and $v$ must be perfect squares, so we can write $u=x_{1}^{2}$ and $v=y_{1}^{2},x_{1},y_{1}\in\mathbb{Z}^+$
7. Substitute for $t,u,v$ in $t=u^{2}+v^{2}$
$z_{1}^{2}=x_{1}^{4}+y_{1}^{4}$, so we have constructed a solution $(x_{1},y_{1},z_{1})$ such that
$$
z_{1}<z_{1}^{2}=t<t^{2}<s^{2}+t^{2}=z_{0}
$$
Hence we have a contradiction by infinite descent
Hence the diophantine equation $x^{4}+y^{4}=z^{2}$ has no positive integer
## Case for $x^{4}+y^{4}=z^{4}$
The diophantine equation $x^{4}+y^{4}=z^{4}$ has no integer solutions and can be proven by substituting $z=z^{2}$ in the diophantine equation above
### Proof
If a solution $(\alpha,\beta,\gamma^{2})$ existed, then $\alpha,\beta,\gamma^{2}$ would be a solution to $x^{4}+y^{4}=z^{2}$, but from above, no such solution exists, hence $x^{4}+y^{4}=z^{4}$ has no positive integer solutions
### Usefulness
Consider $x^{n}+y^{n}=z^{n}$, for $n>2$, $n\in\mathbb{Z}^+$, $n$ must either be divisible by some odd prime $p$ or a power of 2
If $n$ is a power of 2, then $n=4k$ for some $k\geq 1,k\in\mathbb{Z}^+$, we can rewrite $x^{n}+y^{n}=z^{n}$ as:
$$
(x^{k})^{4}+(y^{k})^{4}=(z^{k})^{4}
$$
Which has no positive integer solutions
If $n$ has an odd prime factor $p$, we can write $n$ as $pk$ for some $k\in\mathbb{Z},k\geq 1$ and our equation can be rewritten as:
$$
(x^{k})^{p}+(y^{k})^{p}=(z^{k})^{p}
$$
Hence proving Fermat's conjecture reduces to showing $x^{p}+y^{p}=z^{p}$ for odd, prime $p$ has no positive integer solutions

#Mathematics #Theorem