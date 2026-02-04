Let $X\subset \mathbb{R}$, we say that $X$ is bounded above if:
$$
\exists U\in \mathbb{R}:x\leq U\forall x\in X
$$
$U$ is known as an upper bound
Similarly $X$ is bounded below if:
$$
\exists L\in \mathbb{R}:L\leq x\forall x\in X
$$
$L$ is known as a lower bound
If $X$ is bounded above and bounded below, we say $X$ is bounded
___
Let $X$ be a set which is bounded above, a number $C\in\mathbb{R}$ is called the supremum of $X$ (the least upper bound), if:
- $C$ is an upper bound of $X$
- Whenever $B\in\mathbb{R}$ is an upper bound of $X$, then $C\leq B$
We write $\text{sup}(X)$ for such a $C$
Note that if $X$ has a [[Maximum|maximum]], $U=\text{max}(X)$, then $U$ is the supremum as we have $x\leq M\forall x\in X$, and if $B$ is an upper bound of $X$, then $U\leq B$
___
Similarly, if $X$ is bounded below, a number $c\in\mathbb{R}$ is called the infimum of $X$ (the greatest lower bound) of $X$ if:
- $c$ is a lower bound of $X$
- Whenever $b\in\mathbb{R}$ is a lower bound of $X$, then $b\leq c$
We write $\text{inf}(X)$ for such a $c$
Note that if $X$ has a [[Minimum|minimum]], $L=\text{min}(X)$, then $L$ is the infimum as we have $x\geq L\forall x\in X$, and if $b$ is a lower bound of $X$, then $L\geq b$
### Examples
$$
Y=\left\{  \frac{1}{n}\in \mathbb{R} \mid n\in \mathbb{N} \right\}
$$
This is bounded avove by $\hspace{0pt}1$ as $\frac{1}{n}\leq 1$ for all $n\in\mathbb{N}$; $\hspace{0pt}1$ is an upper bound, and is thus also the supremum
Also $1=\frac{1}{1}\in Y$, so $1=\text{max}(Y)$, note $0<\frac{1}{n}$ for all $n\in\mathbb{N}$, so $Y$ is bounded below by $\hspace{0pt}0$. There is no minimum, since $\frac{1}{n+1}<\frac{1}{n}$ for all $n\in\mathbb{N}$
We now can test whether $\hspace{0pt}0$ is the infimum, the first condition is satisfied, but is there a lower bound that is larger than $\hspace{0pt}0$, but is less that or equal to $\frac{1}{n}$, 
Assume $b\in\mathbb{R}$ satisfies $0<b$, we cannot have $b<\frac{1}{n}$ for all $n\in\mathbb{N}$, as that would be equivalent to $n<\frac{1}{b}$ for all $n\in\mathbb{N}$, which is essentially the [[Theorem of Archimedes|theorem of Archimedes]], so $\hspace{0pt}0$ is the infimum by definition
$$
Z=\{ x\in \mathbb{Q}\mid x^{2}\leq 2 \}
$$
Is a bounded set. If $x\in\mathbb{Z}$, then $-2\leq x\leq 2$, (these are not the minimum bounds, but they work)
If there was a positive rational number $\frac{p}{q}$ with $\frac{p^{2}}{q^{2}}=2$, this would be the maximum, but there is no such $\frac{p}{q}$
$$
\Psi=\{ x\in \mathbb{R}\mid x^{2}\leq 2 \}
$$
bounded above by $\hspace{0pt}2$ of course, but what is the best one, note that $0\in\Psi$, so $\Psi \neq \emptyset$
By the [[Real Numbers#Completeness Axiom|completeness axiom]] $C=\text{sup}\Psi$ exists, we would like to have $C^{2}=2$, so we need to rule out $C^{2}<2$ and $C^{2}>2$ so that only $C^{2}=2$ is the only option left by [[Real Numbers#Ordering|trichotomy]]:
Assume $C^{2}<2$, show that $C$ is not an upper bound, consider 
$$
\left( C+\frac{1}{n} \right)^{2}=C^{2}+\frac{2C}{n}+\frac{1}{n^{2}}=C^{2}+\frac{1}{n}\left( 2C+\frac{1}{n} \right)<C^{2}+\frac{2C+1}{n}=C^{2}+\frac{\alpha}{n}
$$
We assume $C^{2}<2$, so $2-C^{2}>0$, we want:
$$
C^{2}+\frac{\alpha}{n}
$$
So we need $\frac{\alpha}{n}<$
## Functions
Let $f(x)$ be a [[Functions|function]] defined on some [[Intervals|interval]] $I$
$f(x)$ is bounded above in $I$ by an upper bound $U$ if:
$$
f(x)\leq U\forall x\in I
$$
$f(x)$ need not take the value $U$ in $I$, if $\exists x_{1}\in I:f(x_{1})=U$, then we say the upper bound $U$ is attained and $U$ is the global maximum value in $I$
$f(x)$ is bounded below in $I$ by a lower bound $L$ if:
$$
f(x)\geq L\forall x\in I
$$
$f(x)$ need not take the value $L$ in $I$, if $\exists x_{2}\in I:f(x_{2})=L$, then we say the lower bound $L$ is attained and $L$ is the global maximum value in $I$
$f(x)$ is bounded in $I$ if it is bounded both above and below, that is if there exists $M$:
$$
|f(x)|\leq M\forall x\in  I
$$
As for other properties, if we don't specify an interval, we take it to be the domain
## Sequences
Let $a_{n}$ be a [[Sequences|sequence]] of real numbers
___
$a_{n}$ is bounded above if:
$$
\exists U:\forall n\in\mathbb{N},a_{n}\leq U
$$
So $U$ is an upper bound for $a_{n}$
___
$a_{n}$ is bounded below if:
$$
\exists L:\forall n\in\mathbb{N},a_{n}\geq L
$$
So $L$ is a lower bound for $a_{n}$
___
$a_{n}$ is bounded if it is both bounded above and bounded below; iff:
$$
\exists M:\forall n\in\mathbb{N},\left| a_{n} \right|\leq M
$$
___
Let $a_{n}$ be a sequence of real numbers which is bounded from above. $M\in\mathbb{R}$ is called the supremum (or least upper bound) if:
1. $M$ is an upper bound of $a_{n}$, and
2. For any $x<M$, $x$ is not an upper bound of $a_{n}$
Note that, if $x$ is not an upper bound of $a_{n}$ then there exists $i:a_{i}>x$
Note that, if $a_{n}$ is bounded from above, then it must have a supremum

#Mathematics #Definition #Analysis 