A periodic [[Continued Fraction]] is an [[Infinite Continued Fraction]] in which $a_{l}=a_{l+k}$ for a fixed position $k$ and all $l>m$ i.e. $[a_{0};a_{1},a_{2},\dots,a_{m},a_{m+1},a_{m+2},\dots, a_{m+k},a_{m+1},a_{m+2}\dots,a_{m+k},\dots]$. We can write this as $[a_{0},a_{1},\dots,a_{m},\overline{a_{m+1},\dots,a_{m+k}}]$ similarly to the notation for repeating decimal expansions
## Examples
Find a closed form expression for $[3;\overline{2,6}]$
$$
x=3+\frac{1}{2+\frac{1}{6+\frac{1}{2+\frac{1}{\ddots}}}}
$$
We can see that part of this is self-similar, let $y=[2;6]$, so
$$
y=2+\frac{1}{6+\frac{1}{y}}
$$
$$
= \frac{13y+2}{6y+1}
$$
$$
\implies 6y^{2}+y=13y+2
$$
$$
\implies 6y^{2}-12y-2=0
$$
$$
\implies y=1\pm \frac{2}{\sqrt{ 3 }}
$$
We know $y=[\overline{2;6}]$, so $y>2$ and hence $y=1+\frac{2}{\sqrt{ 3 }}$
$$
\implies x=3+\frac{1}{y} =3+\frac{1}{1+\frac{2}{\sqrt{ 3 }}}=2\sqrt{ 3 }
$$
## Real Numbers have Periodic Continued Fractions iff they are [[Quadratic Irrationals]]
A real number $x$ has a periodic continued fraction iff $x$ is a quadratic irrational; $x=a+b\sqrt{ d }$, $a,b\in\mathbb{Q}$, $b\neq 0$ and $d$ is a square free integerproof by infinite descent

#Mathematics #Fractions #Definition