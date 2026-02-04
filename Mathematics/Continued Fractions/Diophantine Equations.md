A diophantine equation is a polynomial equation with integer coefficients such that only integer solutions are sought
When we are given a diophantine equation, we typically look to investigate:
1. are there any solutions?
2. if so, are there finitely many or infinitely many?
3. can we find all the solutions?

## Continued Fractions
The [[Convergents]] of a [[Finite Continued Fraction]] can be used to generate all solutions to the diophantine equation $ax+by=1$ for $a,b\in\mathbb{Z}$ such that $gcd(a,b)=1$
### Proof:
1. Find one valid solution using what we know about convergents, $p_{k-1}q_{k}-p_{k}q_{k-1}=(-1)^{k}$, so if we set $p_{k}=a$ and $q_{k}=b$ then for $a,b>0$:
    1. {a} for even $k$, $x=-q_{k-1}$ and $y=p_{k-1}$ gives a valid solution
    2. for odd $k$, $x=q_{k-1}$ and $y=p_{k-1}$ gives a valid solution
2. Show that if there is 1 solution, we can find others; let's call our initial solution $(x_{0},y_{0})$, then consider $x-x_{0}+bn$, $y=y_{0}-an$ for some $n\in\mathbb{Z}$
$$
ax+by=a(x_{0}+bn)+b(y_{0}-an)=ax_{0}+abn+by_{0}-ban=1
$$
3. Show that this family of solutions is all possible solutions. Take two different solution pairs $(x_{1},y_{1})$ and $(x_{2},y_{2})$, then we know $ax_{1}+by_{1}=1$ and $ax_{2}+by_{2}=1$, subtracting theswe we get
$$
a(x_{1}-x_{2})+b(y_{1}-y_{2})=0
$$
$$
\implies a(x_{1}-x_{2})=b(y_{2}-y_{1})
$$
    We know $b|RHS$ and $a,b$ are copime, so we must have $b|(x_{1}-x_{2})$ therefore there is some integer $n$ such that $x_{1}=x_{2}+bn$, similarly $a|LHS$, so we have $a|(y_{2}-y_{1})$, hence $y_{2}=y_{1}+an$
### Example
Solve $767x-201y=1$, we can work out that $\frac{767}{201}=[3;1,4,2,3,5]$ with $c_{4}=\frac{145}{38}$ and $c_{5}=\frac{767}{201}$, we know that:
$$
p_{4}q_{5}-p_{5}q_{4}=-1
$$
$$
\implies 767\times 38-201\times 145=1
$$
so $x_{0}=38$, $y_{0}=145$, so all solutions are of the form $x=38-201n$, $y=145-767n$, $n\in\mathbb{Z}$

#Mathematics #Definition 