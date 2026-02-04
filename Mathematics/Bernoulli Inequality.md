Let $x\geq-1$, $n\in\mathbb{N}$, then:
$$
(1+x)^{n}\geq 1+nx
$$
It is very useful when $x\approx0$
## Proof
Proof by [[Proof by Mathematical Induction!!!!!|induction]]
For $x=-1$:
$$
(1+(-1))^{n}=0^{n}=0\geq 1-n
$$
Which is true as $n\in\mathbb{N}$ so the base case is true
So assume $x>-1$, now we use induction on $n$:
For $n=1$:
$$
(1+x)^{n}\geq 1+x
$$
This is true fairly obviously
Assume the statement holds for some $n$, then:
$$
(1+x)^{n+1}=(1+x)(1+x)^{n}\geq\underbrace{ (1+x) }_{ >0 }(1+nx)=1+nx+x+nx^{2}=1+(n+1)x+\underbrace{ nx^{2} }_{ \geq0 }\geq 1+(n+1)x
$$

#Mathematics 