The real numbers, $\mathbb{R}$ is the [[Sets|set]] of rational and irrational numbers
## Standard Properties (Axioms)
There is a set of real numbers $\mathbb{R}$ which admits [[Functions|functions]]:
### Addition:
$$
+:\mathbb{R}\times \mathbb{R}\to \mathbb{R}
$$
$$
+(x,y)= x+y
$$
Addition satisfies $\hspace{0pt}4$ axioms:
- Commutativity
$$
a+b=b+a\forall a,b\in \mathbb{R}
$$
- Associativity
$$
a+(b+c)=(a+b)+c\forall a,b,c\in \mathbb{R}
$$
- Identity(existence of $\hspace{0pt}0$): there is a real number $\hspace{0pt}0$ such that:
$$
0+a=a+0=a\forall a\in \mathbb{R}
$$
- Inverses (existence of the negative): for every $a\in\mathbb{R}$ there is a unique number $x\in\mathbb{R}$ such that $a+x=0$, we denote this $-a$. By [[Uniqueness of Inverse|uniqueness of the negative]], $-(-a)=a$
### Multiplication
$$
\times:\mathbb{R}\times \mathbb{R}\to \mathbb{R}
$$
$$
\times(a,b)=a\times b=a\cdot b=ab
$$
Multiplication satisfies $\hspace{0pt}4$ axioms:
- Commutativity
$$
a\times b=b\times a\forall a,b\in \mathbb{R}
$$
- Associativity
$$
a\times(b\times c)=(a\times b)\times c\forall a,b,c\in \mathbb{R}
$$
- Identity (existence of $1$): there is a real number $\hspace{0pt}1$ that is different to $0$ such that:
$$
1\times a=a\times 1=a\forall a\in\mathbb{R} 
$$
- Inverses (existance of reciprocal) For every $a\in\mathbb{R}\setminus \{ 0 \}$, there is a unique $x\in\mathbb{R}$ with $a\times x=1$, we denote this $a^{-1}$ or $\frac{1}{a}$
There is also one axiom linking the two operations:
- Distributivity
$$
a\times(b+c)=(a\times b)+(a\times c)
$$
## Consequences
Let $a\in\mathbb{R}$
### $a\times 0=0$
$$
a\times 0=a\times(0+0)=a\times 0+a\times 0
$$
Recall $a\times 0\in\mathbb{R}$, so there is a negative, $-(a\times 0)$, which we can add to this equation to get:
$$
a\times 0-a\times 0=a\times 0+a\times 0-a\times 0
$$
$$
\implies 0=a\times 0
$$
### $-a=-1\times a$
please complete future oren :)
### $(-a)\times(-a)=(-a)^{2}=a^{2}$
also this
## Ordering
The next property of the reals is the existance of an order using [[Inequalities|Inequalities]]
For every $a,b\in\mathbb{R}$ there is a statement $a<b$ "$a$ is smaller than $b$" we need to specify when this is true:
- Exactly one of the following holds: $a<b,a=b,a>b$, this is known as trichotomy 
- If $a<b$ and $b<c$, then $a<c$ (transitivity)
- If $a<b$, then $a+c<b+c$ for all real numbers $c$ (monotony of addition)
- If $a<b$ and $c>0$, then $ac<bc$ (monotony of multipication case 1)
- If $a<b$ and $c<0$, then $ac>bc$ (monotony of multiplication case 2)
Note that if $a$ is different from $\hspace{0pt}0$, then either $a<0$ or $0<a$ then $-a$ is also different from $\hspace{0pt}0$ and by the monotony of addition, either $0<-a$ or $-a<0$ 
### Consequences
Let $a,b,c,d\in\mathbb{R}$ then:
- If $a\neq 0$, then $a^{2}>0$. In particular $1>0$
If $a>0$, then $a^{2}=a\times a>a\times 0=0$, if $a<0$, then $-a>0$ now we use $(-a)^{2}=a^{2}$ to show the same thing, note that $1=1\times 1=1^{2}>0$, so $1>0$
- If $a<b$ and $c<d$, then $a+c<b+d$ which follows from monotony of addition twice
- If $0<a<b$ and $0<c<d$ then $ac<bd$ which follows from monotony of multiplication twice
- If $a<b$ and $c<0$ then $cb<ca$ 
- $a\leq b\iff a^{2}\leq b^{2}$ if $a,b\geq 0$
We use $-c>0$ so $-c\times a<-c\times b$ now apply monotony of addition by adding $c\times a+c\times b$
- If $0<a<b$ then $0<b^{-1}<a^{-1}$
$b^{-1}\neq 0$ because $b\times b^{-1}=1$, $b^{-1}=(b^{-1})^{2}\times b>0$, since $b>0$ and the other term is a square. This also works for $(ab)^{-1}=a^{-1}v^{-1}>0$ lok at $a<b$, multiply with $a^{-1}b^{-1}$, you get $b^{-1}<a^{-1}$
From these, we have $0<1\implies 1<1+1\implies 1+1\neq 0$
We then use the usual symbols for numbers
## Completeness Axiom
Every non-empty subset of $\mathbb{R}$ which is [[Boundedness|bounded]] above has a supremum
### Consequences
Every set that is bounded below will have an infimum

## Decimal Representation
Each real number can be represented by a decimal. If $r=\frac{p}{q}$ is a [[Rational Numbers|rational number]], then its decimal representation is found by dividing the denominator $q$ into the numberator $p$. The resulting decimal expansion will either terminate or repeat. For example, $\frac{3}{5}=0.6$ is a terminating decimal and $\frac{15}{11}=1.3636363636\dots=1.\overline{36}$ is a repeating decimal. The converse is true; every terminating or repeating decimal represents a rational number
The decimal representation of an [[Irrational Numbers|irrational number]] neither terminates nor repeats
If we stop the decimal expansion of a given number at a certain decimal place, then the result is a rational number which appriximates the given number. For instance $3.14$ is a common rational number approximation for $\pi$. More accurate approximations can be obtained by taking more decimal places in the expansions
### Converting Detween Decimal and Fraction
For terminating decimals, this process is very easy, simply set $r$ to be equal to the number and then multiply by a power of $10$ to obtain an integer, for example if it has $\hspace{0pt}3$ digits after the decimal, multiplying by $10^{3}$ will convert it into an integer, from then, simply divide by this power of $\hspace{0pt}10$, and you have a fraction that you can then simplify by cancelling powers of $2$ and $5$ example:
$$
r=0.236
$$
$$
 1000r=236
$$
$$
 r=\frac{236}{1000}=\frac{59}{250}
$$
For repeating decimals, this process is very similar, set $r$ to be equal to the number, multiply by a power of $\hspace{0pt}10$ equal to the number of digits that repeat, so $0.\overline{123}$ would be $10^3$, and then subtracting $r$ from both sides to obtain an integer, then dividing by the multiple of $r$ and simplifying:
$$
r=0.\overline{123}
$$
$$
 1000r=123.\overline{123}
$$
$$
 999r=123
$$
$$
r=\frac{123}{999}=\frac{41}{333}
$$
## Geometric Representation
A fundamental concept in mathematics which connects the abstract notion of a real number with the geometric notion of a point is the representation of the real numbers as points on a straight line. This is done by choosing an arbitary point $O$ on a horizontal line to represent the number $0$, and another point $U$, (usually taken to the right of $O$) to represent the number $\hspace{0pt}1$
![[Real Numbers 2024-10-13 22.02.50.excalidraw]]
The point $O$ is called the origin, and the distance between $O$ and $U$ determines a scale. With $O$ and $U$ specified, each real number can be represented as a point on the line and, conversely, each point on the line represents a real number. A line representing the real numbers is called a real number line; the number associated with a point $P$ on the line is called the coorinate of $P$. The positive numbers are identified with the points on the right side of $O$ and the negative numbers with the points to the left of $O$. The point representing the number $a$ ($a\neq 0$) is $a$ units from $O$ if $a$ is positive, and $-a$ units from $O$ if $a$ is negative
Two important properties of a real number are its sign and size, or magnitude. Geometrically the sign of $a$ tells us whether the point $a$ is on the right or left of $\hspace{0pt}0$ on a number line. The magnitude of $a$ is the distance between the point $a$ and $\hspace{0pt}0$; $\hspace{0pt}0$ itself does not have a sign and its magnitude is $0$. The magnitude of $a$ is more commonly called the [[Absolute Value|absolute value]] of $a$
## Density
Between any two real numbers, there are infinitely many rational numbers and infinitely many irrational numbers. In particular, there is no smallest positive real number

#Mathematics #Set