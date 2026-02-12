# Real Case
## Theorem
*The* following theorem connects definite and indefinite [[Integration|integrals]]
If [[Functions|$f(x)$]] is [[Regulated Functions|regulated]] on [[Intervals|$[a,b]$]], then the function
$$
F(x)=\int ^{x}_{a} f(t) \, dt 
$$
Is Lipschitz continuous on $[a,b]$ with $M=\sup(\left| f(x) \right|),x\in[a,b]$, hence $F$ is [[Continuity|continuous]] on 
### Proof
$$
\left| F(x)-F(y) \right| =\left| \int_{a}^{x} f(t) \, dt -\int_{a}^{y} f(t) \, dt  \right|=\left| \int_{y}^{x} f(t) \, dt   \right| 
$$
By additivity. By monotonicity:
$$
\leq \int_{x}^{y} \left| f(t) \right|  \, dt \leq \int_{x}^{y} M \, dt =M(x-y)
$$
___
## Theorem
$F(x)$ must be defined for all points $x\in[a,b]$ is continuous on $[a,b]$, [[Differentiation|differentiable]] on $(a,b)$ and has derivative $f(x)$ on $(a,b)$, i.e.
$$
F'(x)=\frac{d }{dx} \int ^{x}_{a} f(t) \, dt =f(x)\forall x\in (a,b)
$$
Furthermore if $\tilde{F}(x)$ is any indefinite integral of $f(x)$ on $(a,b)$, then
$$
\int ^{b}_{a} f(t) \, dt =\tilde{F}(b)-\tilde{F}(a)=[\tilde{F}(x)]^b_{a}
$$
In fact it only needs to be continuous at some $c\in(a,b)$ which can be used to show differentiability
## Proof
Important parts only (for now)
For $a\leq x<x+h<b$, we have:
$$
    F(x+h)-F(x)=\int ^{x+h}_{a} f(t) \, dt -\int ^{x}_{a} f(t) \, dt
$$
$$
= \int ^{x+h}_{a} f(t) \, dt +\int ^{a}_{x} f(t) \, dt =\int _{x}^{x+h}f(t) \, dt 
$$
Using the property $\hspace{0pt}2$ of definite integrals
Let $m(h)$ and $M(h)$ denote the min and max values of $f(x)$ on $[x,x+h]$ which must exist due to the [[Extreme Value Theorem|extreme value theorem]]. Then by the 4th property:
$$
hm(h)\leq \int _{x}^{x+h}f(t) \, dt \leq hM(h)
$$
Substituting this and dividing by $h$,
$$
m(h)\leq \frac{F(x+h)-F(x)}{h}\leq M(h)
$$
Since $f(x)$ is continuous on $[x,x+h]$, we have:
$$
\lim_{ h \to 0^+ } m(h)=f(x)=\lim_{ h \to 0^+ } M(h)
$$
And so by the [[Squeeze Theorem|squeeze theorem]],
$$
\lim_{ h \to 0^+ } \frac{F(x+h)-F(x)}{h}=f(x)
$$
To get the limit for $h\to0^-$ we can give a similar argument, so putting them together:
$$
F'(x)=\lim_{ h \to 0 } \frac{F(x+h)-F(x)}{h}=f(x)
$$
Showing $F(x)$ is an indefinite integral of $f(x)$
![[Fundamental Theorem of Calculus 2024-11-07 14.35.42.excalidraw]]
For the final part, if $\tilde{F}(x)$ is an indefinite integral of $f(x)$ in $(a,b)$, then $\tilde{F}(x)=F(x)+c$ for some $c\in\mathbb{R}$, and so
$$
[\tilde{F}(x)]_{a}^{b}=\tilde{F}(b)-\tilde{F}(a)=(F(b)+c)-(F(a)+c)=F(b)-F(a)=\int ^{b}_{a} f(t) \, dt 
$$
The FTOC gives a simple rule for differentiating a definite integral with respect to its limits
___
Analysis proof
Let $c\in(a,b)$. Need to show that
$$
\lim_{ x \to c }  \frac{F(x)-F(c)}{x-c}
$$
Exists and is equal to $f(c)$. So for $x\neq c$,
$$
\frac{1}{x-c}\left( \int_{a}^{x} f(t) \, dt  -\int_{a}^{c} f(t) \, dt\right)=\frac{1}{x-c}\int_{c}^{x} f(t) \, dt 
$$
Assume $x>c$, (it is the same if $x<c$), using the [[Mean Value Theorem|MVT]] for integrals,
$$
=\frac{1}{x-c}(x-c)f(\xi)=f(\xi)
$$
With $\xi \in(c,x)$, as $x\to c,\xi\to c$, so $f(\xi)=f(c)$

## Example
$$
\frac{d }{dx}\int ^{x}_{0} \frac{1}{1+\sin ^{2}t}  \, dt=\frac{1}{1+\sin ^{2}x}
$$
This can be combined with the [[Chain Rule|chain rule]] for more complicated expressions. For example:
$$
\frac{d }{dx} \int _{0}^{x^{2}} \frac{1}{1+e^{t}} \, dt
$$
Letting $u=x^{2}$,
$$
\frac{d }{dx} \int _{0}^{u} \frac{1}{1+e^{t}} \, dt=\left( \frac{d }{du} \int _{0}^{u} \frac{1}{1+e^{ t} } \, dt  \right)\left( \frac{d u}{dx}  \right)
$$
$$
= \frac{1}{1+e^{u}}2x=\frac{2x}{1+e^{x^{2}}}
$$
# Complex Case

#Mathematics #Calculus #Theorem 