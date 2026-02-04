If we have a [[Functions|funciton]] $f(x)$ which is [[Continuity|continuous]] on $[a,b]$ and [[Differentiation|differentiable]] on $(a,b)$, with $f'(x)>0\forall x\in(a,b)$, then its [[Inverses|inverse]] exists $g(y)$ such that $g(f(x))=x$, and is differentiable $\forall f(a)<y<f(b)$ with:
$$
g'(y)=\frac{1}{f'(g(y))}
$$
Similarly if $f'(x)<0$, then $g(y)$ is still differentiable, but $\forall f(b)<y<f(a)$
## Proof
Assuming $g(y)$ exists and is differentiable, this follows from the [[Chain Rule|chain rule]]:
$$
\frac{d }{dx} x=\frac{d }{dx}g(f(x))=g'(f(x))f'(x)=1
$$

And so with $y=f(x)$,
$$
g'(y)=\frac{1}{f'(g(y))}
$$
## Example
$f(x)=\sin x$ has $f'(x)=\cos x$, so $f'(x)>0\forall x\in\left( -\frac{\pi}{2}, \frac{\pi}{2} \right)$, the inverse $g(y)=\sin ^{-1}(y)$ is therefore differentiable on $(-1,1)$ with:
$$
g'(y)=\frac{1}{\cos(g(y))}=\frac{1}{\sqrt{ 1-\sin ^{2}(g(y)) }}
$$
Since $\sin(g(y))=f(g(y))=y$, so
$$
g'(y)=\frac{1}{\sqrt{ 1-y^{2} }}
$$
So
$$
\frac{d }{dx} \sin ^{-1}(x)=\frac{1}{\sqrt{ 1-x^{2} }}
$$
___
For $\ln x=(e^{ x })^{-1}$ (the inverse), we have
$$
(\ln x)'=\frac{1}{e^{ \ln x }}=\frac{1}{x}
$$


#Mathematics #Calculus #Theorem 