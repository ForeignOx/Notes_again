# For $\mathbb{Z}$
## Lemma
Let $a,b,q\in\mathbb{Z}:a\geq b>0$, we can write 
$$
\text{gcd}(a,b)=\text{gcd}(a,b-a)
$$
$$
=\text{gcd}(a,b-2a)
$$
$$
\vdots
$$
$$
=\text{gcd}(a,b-qa)
$$
### Proof
Want to show:
any divisor of $a$ and $b$ is also a divisor of $b-a$

Let $d|a$ and $d|b$, so $a=xd$ and $b=yd$, for some $x,y\in\mathbb{Z}$
Then $b-a=yd-xd=d(y-x)$, as $y,x \in\mathbb{Z},d|(b-a)$

Conversely want to show:
Each divisor of $a$ and $b-a$ is also a divisor of $b$

Let $k|a$ and $k|(b-a)$ so $a=uk$ and $b-a=vk$, for $u,v \in\mathbb{Z}$, then $a(b-a)=uk+vk\implies b=k(u+v)$ as $u+v \in\mathbb{Z},k|b$ This holds for all divisors, so must also hold for \text{gcd}
## Euclidean Algorithm
Let $a,b\in\mathbb{Z}:a\geq b>0$, we can write $a=qb+r$, where $0 \leq r<b$ by the [[Divisor Algorithm]]
In fact, we have a series of quotients $q$ and remainder $r_{i}$ such that $0\leq r_{i+1}<r$ ($i\in\mathbb{N}$) and $r_{0}=b$ with:
$$
a=q_{1}b+r_{1}
$$
$$
b=q_{2}r_{1}+r_{2}
$$
$$
r_{1}=q_{2}r_{2}+r_{3}
$$
$$
\vdots
$$
$$
r_{n-1}=q_{n+1}r_{n}+r_{n+1}
$$
Until some remainder, $r_{n+1}$ becomes 0, then $r_{n}=\text{gcd}(a,b)$
### Proof
From the Lemma, $g(a,b)=\text{gcd}(a-q_{1}b)$
$$
=\text{gcd}(b,r_{1})
$$
$$
=\text{gcd}(b-q_{2}r_{1},r_{1})
$$
$$
\vdots
$$
$$
=\text{gcd}(r_{n+1}r_{n})
$$
$$
=\text{gcd}(0,r_{n})
$$
$$
=r_{n}
$$
We are guaranteed that this algorithm well terminate: $b=r_{0}>r_{1}>\dots>r_{n}>r_{n+1}=0$
## Example
Use the Euclidean Algorithm to compute $d=\text{gcd}(455,1235)$:
$$
1235=2\cdot 455+325
$$
$$
 455=1\cdot 325+130
$$
$$
 325= 2\cdot 130+65
$$
$$
 130=2 \cdot 65+0
$$
Now the remainder is $0$, so we stop and the $\text{gcd}$ will be the last non-zero remainder; $\hspace{0pt}65$.
Solving for the remainders and substituting back:
$$
65=325-2\cdot 130
$$
$$
= 325-2(455-1\cdot 325)
$$
$$
\vdots
$$
$$
 =455 \cdot (-8)+1235 \cdot 3 
$$
So $x=-8,y=3$.
# For [[Polynomials|Polynomials]]

## Examples
Let $f(x)=x^{2}+1,g(x)=x^{2}+3x+1\in\mathbb{Q}[x]$. 
$$
f(x)=1\cdot g(x)-3x
$$
$$
 g(x)=\left( -\frac{1}{3}x-1 \right)\cdot(-3x)-1
$$
$$
 -3x=(-3x)\cdot1+0
$$
Remainder is $\hspace{0pt}0$, so we stop. So a GCD of $f(x)$ and $g(x)$ is 1.
We ccan use this to write $1$ as a linear combination of $f(x)$ and $g(x)$:
$$
1=g(x)-\left( -\frac{1}{3}x-1 \right)(-3x)=g(x)+\left( -\frac{1}{3}x+1 \right)(f(x)-g(x))
$$
$$
= \left( \frac{1}{3}x+1 \right)f(x)-\frac{1}{3}xg(x)
$$
___
Let $f(x)=x^{2}+7x+6,g(x)=x^{2}-5x-6\in\mathbb{Q}[x]$, use the EA:
$$
f(x)=g(x)+12(x+1)
$$
$$
 g(x)=\frac{1}{12}x\cdot12(x+1)-6(x+1)=(x-6)(x+1)+0
$$
So we stop and a GCD is $12(x+1)$, dividing through by the leading coefficient $\hspace{0pt}12$, we get the monic GCD $x+1$
# General Proof (for integers and polynomials)
Let $R$ be $\mathbb{Z}$ or $\mathbb{F}[x]$, let $a,b\in R$ such that $a\neq 0$ or $b\neq 0$, then
- The GCD of $a$ and $b$ exists and can be computed via the Euclidean Algorithm (given in proof)
- If $R=\mathbb{F}[x]$, the monic GCD is unique, and we denote it by $\gcd(a,b)$
- If $d$ is a GCD of $a$ and $b$, then $\exists\alpha,\beta:\alpha a+\beta b=\gcd(a,b)=d$
## Proof
WLOG we may assume $b\neq 0$, for notational reasons we set $r_{-1}:=a,r_{0}:=b$. By our understanding of divisibility in these rings, we can find $q_{1},r_{1}\in R$ such that
$$
r_{-1}=q_{1}b+r_{1}=q_{1}r_{0}+r_{1}
$$
So either $r_{1}=0$ or $d(r_{1})<d(r_{0})$.
If $r_{1}=0$, we are done, as then $r_{0}|r_{-1}$, hence $r_{0}$ is a GCD, but if $r_{1}\neq 0$, then $d(r_{1})<d(r_{0})$ and we can iterate the process for $r_{0}$ and $r_{1}$ and so on:
$$
r_{-1}=q_{1}r_{0}+r_{1}
$$
$$
 r_{0}=q_{2}r_{1}+r_{2}
$$
$$
 \vdots
$$
$$
 r_{i-2}=q_{i}r_{i-1}+r_{i}
$$
$$
 \vdots
$$
$$
 r_{n-2}=q_{n}r_{n-1}+r_{n}
$$
$$
 r_{n-1}=q_{n+1}r_{n}+0
$$
Where $n$ is the smallest number of iterations needed to get remainder $\hspace{0pt}0$. This $n$ must be finite as $d(r_{i})$ is a natural number that decreases by at least $1$ each time
The last nonzero remainder $r_{n}$ is a common divisor of $a=r_{-1}$ and $b=r_{0}$ because, $r_{n}|r_{n-1}$, hence, by the $n$th equation, $r_{n}|r_{n-2}$, and so on, going up to the top, showing that $r_{n}|r_{i}$ for all $i$, including $i=0,i=-1$
Moreover, any common divisor of $a$ and $b$, call it $e$, must, by the first equation, divide $r_{1}$, so by the second equation, $e|r_{2}$ and so on going all the way down until we get $e|r_{n}$
By this [[Rings#Lemma|lemma]], $d(e)\le d(r_{n})$, so $r_{n}$ is a GCD of $a$ and $b$
This argument also proves the second statement because if $R=\mathbb{F}[x]$ and $e\in R$ is another GCD (apart from $r_{n}$), then $e|r_{n}$ and $d(e)=d(r_{n})$, then $r_{n}=em$ for some $m\in \mathbb{F}[x]$, so, since $d(e)=d(r_{n})=d(em)=d(e)+d(m),d(m)=0$, thus $m$ is a non-zero constant. Among all constant multiples of $r_{n}$, there is a unique one that is monic.
For the third part, we solve for $r_{i}$ and substitute back
$$
r_{n}=r_{n-2}-q_{n}r_{n-1}
$$
$$
 r_{n-1}=r_{n-3}-q_{n-1}r_{n-2}
$$
$$
\vdots
$$
We use the second equation here to eliminate $r_{n-1}$ from the first equation, collecting terms and write in the form $r_{n}=Ar_{n-2}+Br_{n-3}$ for $A,B\in R$, sow solve for $r_{n-1}$ and eliminate from our new equation, so eventually we get:
$$
r_{n}=~\alpha r_{-1}+\beta r_{0}
$$
For some $\alpha,\beta \in R$



#Mathematics #Fractions #Algorithm #Theorem