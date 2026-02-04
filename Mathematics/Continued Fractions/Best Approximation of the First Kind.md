An irrational number $\frac{p}{q}$ is a best approximation of the first kind to a real number $x$ if $\left|  x-\frac{p}{q} \right|<\left| x-\frac{a}{b} \right|$ for any other rational number $\frac{a}{b}$, with $b\leq q$
## [[Convergents]]
The convergent $c_{k}=\frac{p_{k}}{q_{k}}$ is the best approximation of the first kind to $x \in\mathbb{R}$ with denominator $\leq q_{k}$
### Proof
By [[Convergents#Convergents oscillate, Odd Numbered Convergents are always Greater than Even Convergents|this theorem]] even convergents form an increasing [[Sequences|sequence]] and odd convergents form a decreasing sequence, with their limit $x$ 'trapped' between them
We know $q_{k}>q_{k-1}$, so $\frac{p_{k-1}}{q_{k-1}}$ and $\frac{p_{k}}{q_{k}}$ both have denominators $\leq q_{k}$
Assume that $\frac{a}{b}$ is the best approximation to $x$ with denominator $\leq q_{k}$, then, due to how convergents oscillate, it has to lie between $\frac{p_{k-1}}{q_{k-1}}$ and $\frac{p_{k}}{q_{k}}$
Consider $\left| \frac{a}{b}-\frac{p_{k-1}}{q_{k-1}} \right|$
$$
\left| \frac{a}{b}-\frac{p_{k-1}}{q_{k-1}} \right|=\left| \frac{aq_{k-1}-bp_{k-1}}{bq_{k-1}} \right|\geq \frac{1}{bq_{k-1}}
$$
By minimising the integer numerator; we know $\left| \frac{a}{b}-\frac{p_{k-1}}{q_{k-1}} \right|\neq 0$ as $c_{k}$ is closer to $x$ than $c_{c-1}$
Also consider that
$$
\left| \frac{a}{b}-\frac{p_{k-1}}{q_{k-1}} \right|\leq \left| \frac{p_{k}}{q_{k}}-\frac{p_{k-1}}{q_{k-1}} \right|
$$
as $\frac{a}{b}$ is between $c_{k}$ and $c_{k-1}$
$$
=\left| \frac{p_{k}q_{k-1}-p_{k-1}q_{k}}{q_{k}q_{k-1}} \right|=\frac{1}{q_{k}q_{k-1}}
$$
Combining these inequalities:
$$
\frac{1}{bq_{k-1}}\leq \left| \frac{a}{b}-\frac{p_{k-1}}{q_{k-1}} \right|\leq \frac{1}{q_{k}q_{k-1}}
$$
$$
\implies \frac{1}{bq_{k-1}}\leq \frac{1}{q_{k}q_{k-1}}
$$
$$
\implies q_{k}\leq b
$$
As all terms are positive
But we have set $b\leq q_{k}$, so we must have equality everywhere. This implies $\frac{a}{b}=\frac{p_{k}}{q_{k}}$. So $c_{k}$ is indeed the best approximation to $x$ with denominator $\leq q_{k}$


#Mathematics #Fractions #Definition #Theorem 