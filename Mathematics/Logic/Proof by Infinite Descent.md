A proof by infinite descent is a particuar type of proof by contradiction. It shows that if a statement holds for some positive integer solution, then there must be some smaller positive intefer solution and this shows infinitely many smaller positive integers, but no such infinite set of integers exists
It shows that a statement cannot hold for any positive by showing that if it did hold for some positive integer, then it would also hold for a smaller positive integer leading to an infinite descent, but no such infinite [[Sequences|decreasing sequence]] of integers $n_{0}>n_{1}>n_{2}>\dots>0$ exists
Note that this is similar to proof by induction
Alternatively, we can say that if there are solutions, we can choose one that is in some way minimal, e.g. has the smallest $\left| x \right|>0$, then if you can show that this implies the existance of a smaller solution, this is a contradiction
Used in Euclid's elements such as in book 7 proposition 31
Fermat also used this frequently, so is also sometimes called Fermat's Method of Infinite Descent
## Example
Show that the only integer solution of the [[Diophantine Equations|diophantine equation]] $x^{3}+4x^{2}y=2y^{3}$ is $x=y=0$, if we have a solution with $x=0$, then $y=0$
Assume, for a contradiction, there is an integer solution with $x\neq 0$. Choose a solution $(x,y)$ such that $\left| x \right|$ is minimal across all solutions with $x\neq 0$
$2y^{3}$ and $4x^{2}y$ are divisible by $2$, so $x^{3}$ is divisible by $2$ and $x$ is an integer, so $x=2x_{0},x_{0}\in\mathbb{Z}$, substituting this we get:
$$
(2x_{0})^{3}+4(2x_{0})^{2}y=2y^{3}
$$
$$
\implies 8x_{0}^{3}+16x_{0}^{2}y=2y^{3}
$$
$$
\implies 4x_{0}^{3}+8x_{0}^{2}y=y^{3}
$$
The left-hand side is divisile by $4$, so $y^{3}$ must be divisible by $4$, so $y=2y_{0},y_{0}\in\mathbb{Z}$, substituting this, we get:
$$
4x_{0}^{3}+8x_{0}(2y_{0})=(2y_{0})^{2}
$$
$$
\implies 4x_{0}^{3}+16x_{0}^{2}y_{0}=8y_{0}^{3}
$$
$$
\implies x_{0}^{3}+4x_{0}^{2}y_{0}=8y_{0}^{3}
$$
So $(x_{0},y_{0})$ is an integer solution to our original euation: $\left| x_{0} \right|=\frac{1}{2}\left| x \right|>0$ so we have a contradiction. Hence, there is only the trivial solution $x=y=0$

#Mathematics #Logic