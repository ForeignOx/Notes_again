For positive integers $n,t$, the coefficient of $x_{1}^{n_{1}}x_{2}^{n_{2}}x_{3}^{n_{3}}\dots x_{t}^{n_{t}}$ in the expansion of $(x_{1}+x_{2}+x_{3}+\dots+x_{t})^{n}$ is:
$$
\frac{n!}{n_{1}!n_{2}!n_{3}!\dots n_{4}!}
$$
Where each $n_{i}$ is an integer with $0\leq n_{i}\leq n$ for all $1\leq i\leq t$ and $n_{1}+n_{2}+\dots+n_{t}=n$
## Proof
The coefficient of $x_{1}^{n_{1}}x_{2}^{n_{2}}x_{3}^{n_{3}}\dots x_{t}^{n_{t}}$ is the number of ways we can select $x_{1}$ from the $n_{1}$ of the $n$ factors, $x_{2}$ from the $n_{2}$ of the $n-n_{1}$ remaining factors, $x_{3}$ from the $n_{3}$ of the $n-n_{1}-n_{2}$ now remaining factors,..., and $x_{t}$ from $n_{t}$ of the last $n-n_{1}-n_{2}-n_{3}-\dots-n_{t-1}=n_{t}$ remaining factors. This can be carried out as:
$$
{n \choose n_{1} }{n-n_{1} \choose n_{2} }{n-n_{1}-n_{2} \choose n_{3} }\dots {n-n_{1}-n_{2}-n_{3}-\dots-n_{t-1} \choose n_{t} }
$$
Ways, which gives:
$$
\frac{n!}{n_{1}!n_{2}!n_{3}!\dots n_{4}!}
$$
Which is also written as:
$$
{n \choose n_{1},n_{2},n_{3},\dots,n_{t} }
$$
And is called the multinomial coefficient

#Mathematics #Discrete #Theorem 