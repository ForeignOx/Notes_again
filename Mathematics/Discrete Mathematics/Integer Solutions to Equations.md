If we have a problem of the form: How many integer solutions $(x_{1},x_{2},\dots,x_{n})$ are there to the equation:
$$
x_{1}+x_{2}+\dots+x_{n}=k
$$
Such that each $x_{i}$ follows a specific rule, such as each $x_{i}\geq i+1$, we can solve this by thinking of it as a problem of [[Ordered Grouping of Indistinguishable Objects|ordered grouping of indistinguishable objects]] by considering the space each $x_{i}$ takes up on a number line and moving bars between them. This gives for the simplest case, if $x_{i}\geq 0$, the number to be:
$$
{n+k-1 \choose n-1 }={n+k-1 \choose k }
$$
Or if $x_{i}\geq 1$, the number to be:
$$
{k-1 \choose n-1 }
$$
We can use either of these to convert inequalities in $x_{i}$ to some $z_{i}\geq 0$ using the following method:
If the restraint is $x_{i}\geq f(i)$, let $z_{i}=x_{i}-f(i)$ which gives the condition $z_{i}\geq 0$, so we can consider
$$
x_{1}+x_{2}+\dots+x_{n}=k
$$
$$
\implies x_{1}-f(1)+x_{2}-f(2)+\dots+x_{n}-f(n)=k-f(1)-f(2)-\dots-f(n)
$$
$$
 \implies z_{1}+z_{2}+\dots+z_{n}=k-\sum_{i=1}^{n}f(i)=j
$$
Giving the answer to be:
$$
{n+j-1 \choose n-1 }
$$


#Mathematics #Discrete 