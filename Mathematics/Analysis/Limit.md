The rough idea behind a limit is that a [[Functions|function]] $f(x)$ las a limit $L$ at a point $x=a$ if $f(x)$ is close to $L$ whenever $x$ is close to $a$. More precisely, how can we check if $f$ is close to $L$ if $x$ is close to $a$? If we have an acceptable error $\varepsilon$ ($\varepsilon>0$) betewen $f$ and $L$, then I would need the distance $|f(x)-L|<\varepsilon$ for all $x$ in some interval around $a$. So if I can always (for any $\varepsilon>0$) I can find some distance $\delta,\delta>0$ such that $|f(x)-L|<\varepsilon \forall 0<|x-a|<\delta$ then we say that $f(x)$ has a limit $L$ as $x$ tends to $a$, or: $\lim_{ x \to a }f(x)=L$
![[Limit 2024-10-15 14.31.22.excalidraw]]
We essentially need to find a certain $\delta$ for a given $\varepsilon$ such that this is true
## Definition
The formal definition is thus:
$$
\lim_{ x \to c } f(x)=L\iff \forall\varepsilon>0\exists\delta>0:|f(x)-L|<\varepsilon \forall x :0<|x-c|<\delta
$$
If there is no such $L$ then the limit does not exist
Note we do not require $f(a)=L$ or for $f(c)$ to even exist, as we only consider the interval $0<|x-c|<\delta$
## Limit not Existing Definition
The limit $\lim_{ x \to c }f(x)$ does not exist if 
$$
\exists\varepsilon>0:\forall\delta>0\exists x:\left| x-c \right| <\delta \text{ with }\left| f(x)-L \right| \geq\varepsilon
$$

## Link to Sequences
$\lim_{ x \to c } f(x)=L\iff$ for all [[Sequences|sequences]] $(x_{n})$ with [[Convergence|$\lim_{ n \to \infty }x_{n}=c$]], we have $\lim_{ n \to \infty }f(x_{n})=L$
### Proof
$\implies$ direction:
Assume $\lim_{ x \to c }f(x)=L$, take $(x_{n})\in(a,b)$, $x_{n}\neq c$ with $\lim_{ n \to \infty }x_{n}=c$. Take $\varepsilon>0$, we need an $N$ such that
$$
\left| f(x_{n})-L \right| <\varepsilon \forall n\geq N
$$
We also know, since the function converges that we have a 
$$
\delta>0:\left| f(x)-L \right|<\varepsilon \forall \left| x-c \right|<\delta
$$
Since $\lim_{ n \to \infty }x_{n}=c$, there exists $N$ such that $\left| x_{n}-c \right|<\delta \forall n\geq N$ (we are essentially using the definition above to use $\delta$ as our $\varepsilon$ for the sequence), so the sequence converges
$\impliedby$ direction:
This will be done by contradiction. Assume $\lim_{ x \to c}f(x)\neq L$ (or doesn't exist) we want to find a sequence with $\lim_{ n \to \infty }x_{n}=c$ but $\lim_{ n \to \infty }f(x_{n})\neq L$ (or doesn't exist)
For the limit to not exist we first take $\delta=\frac{1}{n}$ and a "bad" $\varepsilon>0$ to get at $x=x_{n}$ with 
$$
\left| x_{n}-c \right| <\delta=\frac{1}{n}\implies \lim_{ n \to \infty } x_{n}=c
$$
But 
$$
\left| f(x)-L \right| \geq\epsilon\implies \lim_{ n \to \infty } f(x_{n})\neq L
$$
So that is a proof or somethin
## Facts About Limits
You can use the following facts without proof:
- The limit is unique at any point
- If $f(x)=g(x)$ (except possiby at $x=a$) in some [[Intervals|interval]] containing $a$, then they have the same limit at $x=a$; $\lim_{ x \to a }f(x)=\lim_{ x \to a }g(x)$
- If $f(x)$ is [[Boundedness|bounded]] from below, $f(x)\geq k$ on either some interval $(a,b)$ or $(c,a)$ and if $\lim_{ x \to a }f(x)=L$ then $L\leq k$
- If $f(x)$ is bounded from above, $f(x)\leq k$ on either some interval $(a,b)$ or $(c,a)$ and if $\lim_{ x \to a }f(x)=L$ then $L\geq k$
- [[Calculus of Limits Theorem|Calculus of Limits theorem]] (CoLT): If $\lim_{ x \to a }f(x)=L$ and $\lim_{ x \to a }g(x)=M$, then:
    - $\lim_{ x \to a }(f(x)+g(x))=L+M$, 
    - $\lim_{ x \to a }(f(x)g(x))=LM$, 
    - if $M\neq 0$, $\lim_{ x \to a }\left( \frac{f(x)}{g(x)} \right)=\frac{L}{M}$
## Examples
$$
\lim_{ x \to 0 } \frac{1}{x^{2}}
$$
Does not exist as limits must be real numbers and $\infty$ is not a real number
We can use the calculus of limits theorem here:
$$
\lim_{ x \to \frac{\pi}{2} } x^{2}\sin x=\left( \lim_{ x \to \frac{\pi}{2} }x^{2}  \right)\times\left( \lim_{ x \to \frac{\pi}{2} } \sin x \right)=\frac{\pi^{2}}{4}\times 1=\frac{\pi^{2}}{4}
$$
And we know that the limit if the function is defined at a point $a$ is $f(a)$
Here is a trickier case:
$$
\lim_{ x \to 3 } \frac{2x^{2}-18}{x-3}=\lim_{ x \to 3 } \frac{2(x-3)(x+3)}{x-3}=\lim_{ x \to 3 } 2(x+3)=12
$$
We can perfom the simplification with factorising when doing limits, as they are defined arount $x=3$, but the functions are in fact different as $x=3$ is not in the domain of the first function
### Two Trigonometric Limits
Two important limits are:
$$
\lim_{ x \to 0 } \frac{\sin x}{x}=1,\lim_{ x \to 0 } \frac{1-\cos x}{x}=0
$$
These can be proven usen the squeeze theorem
We can use this to rewrite other trigonometric limits, for example:
$$
\lim_{ x \to 0 } \frac{\tan x}{x}=\lim_{ x \to 0 } \left( \frac{\sin x}{x} \right)\left( \frac{1}{\cos x} \right)=1\cdot 1=1
$$
### Limits with Logarithms, Powers, and Exponentials
#### Lemma 1
$$
\forall x\geq 0,e^{ x }\geq 1+x
$$
##### Proof
Consider $f(x)=e^{ x }-(1+x)$, we have $f(0)=0$, and $f'(x)=e^{ x }-2$, so $f(x)$ is [[Monotonic Functions|monotonic increasing]] on $[0,\infty)$, so $f(x)\geq 0$ on $[0,\infty)$
#### Lemma 2
$$
\forall x\geq 0,n\in \mathbb{N},e^{ x }\geq \sum_{ j=0} ^{ n}  \frac{x^{j}}{j!}
$$
##### Proof
Note that when $n=1$, this is Lemma 1
Now let 
$$
f_{n}(x)=e^{ x }-\sum_{ j=0} ^{ n} \frac{x^{j}}{j!}=e^{ x }-\left( 1+x+\frac{x^{2}}{2}+\dots+\frac{x^{n}}{n!} \right)  
$$
Note $f_{n}(0)=0\forall n\in\mathbb{N}$
$$
f_{n}'(x)=e^{ x }-\left( 1+x+\frac{x^{2}}{2}+\dots+\frac{x^{n-1}}{(n-1)!} \right)=e^{ x }-\sum_{ j=0} ^{ n-1} \frac{x^{j}}{j!}  
$$
So since $f_{1}(x)\geq 0$, by Lemma $\hspace{0pt}1$, $f_{2}'(x)\geq 0$, so $f_{2}(x)\geq 0$, then we can repeat to get that $f_{n}(x)\geq 0$ by [[Proof by Mathematical Induction!!!!!|induction]]
#### Powers beat logs
For any $a>0$,
$$
\lim_{ x \to \infty } \frac{\ln x}{x^{a}}=0
$$
##### Proof
Let $x=e^{ y }$, then
$$
\lim_{ x \to \infty } \frac{\ln x}{x^{a}}=\lim_{ y \to \infty } \frac{y}{e^{ ay }}
$$
For $y>0$, using Lemma $\hspace{0pt}2$ with $n=2$, so
$$
\frac{y}{e^{ ay }}\leq \frac{y}{1+ay+\frac{a^{2}y^{2}}{2}}\leq \frac{y}{\frac{1}{2}a^{2}y^{2}}=\frac{2}{a^{2}y}
$$
Since 
$$
\lim_{ y \to \infty } \frac{2}{a^{2}y}=0
$$
By the pinching theorem,
$$
\lim_{ y \to \infty } \frac{y}{e^{ ay }}=0=\lim_{ x \to \infty } \frac{\ln x}{x^{a}}
$$
#### Exponentials beat powers
For any $a>0$,
$$
\lim_{ x \to \infty } \frac{x^{a}}{e^{ x }}=0
$$
##### Proof
Let $n$ be the smallest integer such that $n>a$, then by Lemma $\hspace{0pt}2$ (for $x>0$):
$$
0\leq\frac{x^{a}}{e^{ x }}\leq \frac{x^{a}}{1+x+\frac{x^{2}}{2}+\dots+\frac{x^{n}}{n!}}=\frac{x^{a-n}}{x^{-n}+x^{1-n}+\frac{x^{2-n}}{2}+\dots+\frac{1}{n!}}
$$
As $a-n<0$, the numerator goes to $\hspace{0pt}0$, as and the terms in the denominator also goes to $\hspace{0pt}0$, except the $\frac{1}{n!}$ term, and since the numerator goes to zero, and the denominator goes to a constant, the limit is $\hspace{0pt}0$, so using the squeeze theorem again,
$$
\lim_{ x \to \infty } \frac{x^{a}}{e^{ x }}=0
$$
#### Exponential as a limit
For any $a\in\mathbb{R}$,
$$
\lim_{ x \to \infty } \left( 1+\frac{a}{x} \right)^{x}=e^{ a }
$$
##### Proof
Let $f(x)=\ln x$, then $f'(x)=\frac{1}{x}$ and:
$$
f'(1)=\lim_{ h \to 0 } \frac{\ln(1+h)-\ln(1)}{h}=\lim_{ h \to 0 } \frac{\ln(1+h)}{h}
$$
Now letting $h=\frac{a}{x}$,
$$
1=\lim_{ x \to \infty } \frac{\ln\left( 1+\frac{a}{x} \right)}{\frac{a}{x}}
$$
So
$$
a=\lim_{ x \to \infty } x\ln\left( 1+\frac{a}{x} \right)=\lim_{ x \to \infty } \ln\left( 1+\frac{a}{x} \right)^{x}
$$
Now exponentiating both sides gives:
$$
e^{ a }=e^{  \lim_{ x \to \infty } \ln\left( 1+\frac{a}{x} \right)^{x}}=\lim_{ x \to \infty } e^{ \ln(1+a/x)^{x} }=\left( 1+\frac{a}{x} \right)^{x}
$$
Using the fact that $e^{ x }$ is continuous
## Limits as $x\to \infty$
Rough idea: a function has a limit $L$ as $x\to \infty$ if $f(x)$ can be kept arbitrarily close to $L$ by making $x$ sufficiently large
Formal definition:
$$
\lim_{ x \to \infty } f(x)=L\iff \forall\varepsilon>0\exists S>0:|f(x)-L|<\varepsilon \forall x>S
$$
Similarly limits can be done as $x\to-\infty$:
$$
\lim_{ x \to -\infty } f(x)=L\iff \forall\varepsilon>0\exists S>0:|f(x)-L|<\varepsilon \forall x<-S
$$
An easy way to calculate limits as $x\to \infty$ is to make the substitution $x=\frac{1}{u}$ then:
$$
\lim_{ x \to \infty } f(x)=\lim_{ u \to 0^+ } f\left( \frac{1}{u} \right)
$$
Note, the graph of $f(x)$ has a horizontal asymptote to the right (or left) at $y=L$ if $\lim_{ x \to \infty }f(x)=L$ (or $\lim_{ x \to -\infty }f(x)=L$ respectively)
### Examples
$$
\lim_{ x \to \infty } \frac{x\cos\left( \frac{1}{x} \right)+2}{x}=\lim_{ u \to 0^+ } (\cos u+2u)=1+0=1
$$
$$
\lim_{ x \to \infty } \frac{2x+3}{x+5}=\lim_{ x \to \infty } \frac{2+\frac{3}{x}}{1+\frac{5}{x}}=\lim_{ u \to 0^+ } \frac{2+3u}{1+5u}=\frac{2}{1}=2 
$$
# Complex Limits
Just like with real limits, we can define these via sequences:



#Mathematics #Analysis #Definition