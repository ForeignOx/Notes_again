If [[Limit|$\lim_{ x \to a }f=L$]], and $\lim_{ x \to a }g(x)=M\neq 0$, then:
$$
\lim_{ x \to a } \frac{f(x)}{g(x)}=\frac{L}{M}
$$
By the calculus of limits theorem
If $L\neq 0$ and $M=0$, then $\lim_{ x \to a } \frac{f(x)}{g(x)}$ does not exist
If $L=M=0$, we say the limit is of indeterminant form, this means the limit might or might not have a well-defined value, but we can't tell simply by knowing $L$ and $M$
Limits of the following form are all indeterminant:
$$
\frac{L}{M}=\frac{0}{0}, \frac{\infty}{\infty}, 0\times \infty,0^{0}, 1^{\infty},\infty^0
$$
L'Hopital's rule applies to the first two cases
If $f(x)$ and $g(x)$ are [[Differentiation|differentiable]] on $I=(a,b)$:
$$
\lim_{ x \to a^+ } f(x)=\lim_{ x \to a^+ } g(x)=0
$$
And if:
$$
\lim_{ x \to a } \frac{f'(x)}{g'(x)}
$$
Exists, with $g'(x)\neq 0,\forall x\in I$, then:
$$
\lim_{ x \to a^+ }  \frac{f(x)}{g(x)}=\lim_{ x \to a^+ } \frac{f'(x)}{g'(x)}
$$
If applying L'Hopital's rule gives another indeterminant form, then we can apply it again, and so on 
## Mini fake proof
For the case where $f'(a)$ and $g'(a)$ both exist and and are differentiable at $a$ and are [[Continuity|continuous]] and $g'(x)\neq 0$, then
$$
\lim_{ x \to a } \frac{f(x)}{g(x)}=\underbrace{ \lim_{ x \to a } \frac{f(x)-f(a)}{g(x)-g(a)} }_{ \text{since }g(a)=f(a)=0 }=\lim_{ x \to a } \frac{\frac{f(x)-f(a)}{x-a}}{\frac{g(x)-g(a)}{x-a}}=\frac{\lim_{ x \to a } \frac{f(x)-f(a)}{x-a}}{\lim_{ x \to a } \frac{g(x)-g(a)}{x-a}}=\frac{f'(a)}{g'(a)}=\lim_{ x \to a } \frac{f'(x)}{g'(x)}
$$
We can show the last part thus:
$$
f'(a)=\lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h}
$$
Let $x=a+h$:
$$
f'(a)=\lim_{ x \to a } \frac{f(x)-f(a)}{x-a}
$$
## Proof
We can extend $f$ and $g$ to be [[Continuity|continuous]] to $x=a$, since they both have limits that are $\hspace{0pt}0$ by setting $f(a)=g(a)=0$
Take any [[Sequences|sequence]] $x_{n}\in(a,b)$ with $\lim_{ n \to \infty }x_{n}=a$, then we need to show:
$$
\lim_{ n \to \infty }  \frac{f(x_{n})}{g(x_{n})}=L
$$
We now apply [[Mean Value Theorem#Cauchy's Generalised Mean Value Theorem|generalised mean value theorem]] for $f$ and $g$ on the intervals $[a,x_{n}]$, so there exists a $y_{n}\in(a,x_{n})$ such that 
$$
\frac{f'(y_{n})}{g'(y_{n})}=\frac{f(x_{n})-f(a)}{g(x_{n})-g(a)}=\frac{f(x_{n})}{g(x_{n})}
$$
Since $f(a)=g(a)=0$, we can do this since $g'(y_{n})\neq 0$, so by the [[Squeeze Theorem|squeeze theorem]], 
$$
\lim_{ n \to \infty } y_{n}=a
$$
Since $a\leq y_{n}\leq x_{n}$, so since the limits exist at $a$, 
$$
\lim_{ n \to \infty } \frac{f(y_{n})}{g(y_{n})}=\lim_{ n \to \infty }  \frac{f(x_{n})}{g(x_{n})}=L
$$
So we have victory
## <span style="color:rgb(255, 0, 136)">Remarks</span>
It also holds for left-sided limits or both sided limits
It also works if $a=\pm \infty$, since
$$
\lim_{ x \to \pm \infty } \frac{f(x)}{g(x)}=\lim_{ x \to 0^\pm } \frac{f\left( \frac{1}{x} \right)}{g\left( \frac{1}{x} \right)} 
$$
We can also do it for the case of "$\frac{\infty}{\infty}$" is also ok
We can also often do the case of "$0\times \infty$", by writing $f(x)g(x)=\frac{f(x)}{\frac{1}{g(x)}}$ 
## Powers Beat Logs
For $a>0$, 
$$
\lim_{ x \to \infty }  \frac{\ln x}{x^{a}}
$$
Is a limit of the form "$\frac{\infty}{\infty}$", so we can use L'Hopitals:
$$
=\lim_{ x \to \infty } \frac{\frac{1}{x}}{ax^{a-1}}=\lim_{ x \to \infty } \frac{1}{ax^{a}}=0 
$$
Next consider
$$
\lim_{ x \to 0^+ } x^{a}\ln a=\lim_{ x \to 0^+ } \frac{\ln x}{x^{-a}}=\lim_{ x \to 0^+ } \frac{\frac{1}{x}}{-ax^{-a-1}}=\lim_{ x \to 0^+ } -\frac{1}{a}x^{a}=0
$$
## Exponentials Beat Powers
stuf
## Example
$$
\lim_{ x \to 0 } \frac{2\sin x-\sin(2x)}{x-\sin x}=\lim_{ x \to 0 } \frac{2\cos x-2\cos(2x)}{1-\cos x}=\lim_{ x \to 0 }  \frac{-2\sin x+4\sin(2x)}{\sin x}=\lim_{ h \to 0 } \frac{-2\cos x+8\cos(2x)}{\cos x}
$$
$$
= \frac{-2+8}{1}=6 
$$

#Mathematics #Analysis #Calculus #Theorem 