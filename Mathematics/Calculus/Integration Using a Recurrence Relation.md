Once common way we find [[Integration|integrals]] via [[Recurrence Relations|recurrence relations]] is when [[Integration by Parts|integrating by parts]]
## Examples
Calculate $\int _{0}^{1}x^{3}e^{ x } \, dx$, let
$$
I_{n}=\int _{0}^{1}x^{n}e^{ x } \, dx \forall n\in \mathbb{Z}^+_{0}
$$
And consider integrating by parts:
$$
I_{n+1}=\int _{0}^{1}x^{n+1}e^{ x } \, dx =[x^{n+1}e^{ x }]^1_{0}-\int _{0}^{1}(n+1)x^{n}e^{ x } \, dx =e-(n+1)I_{n}
$$
Since we can easily calculate $I_{0}$:
$$
I_{0}=\int _{0}^{1}e^{ x } \, dx =[e^{ x }]^1_{0}=e-1
$$
The recurrence relation $I_{n+1}=e-(n+1)I_{n}$ can be used to calculate $I_{n}$ for any $n>0$:
$$
I_{1}=e-I_{0}=e-(e-1)=1
$$
$$
 I_{2}=e-2I_{1}=e-2
$$
$$
 I_{3}=e-3I_{2}=6-2e
$$
___
Note that one can also obtain recurrence relations without integrating by parts (e.g. using trig identities), for example calculating $\int \tan ^{4}x \, dx$
$$
I_{n}=\int \tan^nx \, dx \text{ for }n\geq 0,\,(n\neq 1)
$$

$$
I_{n}=\int \tan ^{n-2}x(\sec ^{2}x-1) \, dx =\int \tan ^{n-2}x\sec ^{2}x \, dx -\int \tan ^{n-2}x \, dx 
$$
Then letting $u=\tan x$, $du=\sec ^{2}xdx$,
$$
I_{n}=\int u^{n-1} \, du -I_{n-2}
$$
$$
= \frac{u^{n-1}}{n-1}-I_{n-2}=\frac{\tan ^{n-1}x}{n-1}-I_{n-2}
$$
Which gives a recurrence relation relating odd $n$ with odd $n$, and even $n$ with even $n$
We have $I_{0}=\int  \, dx=x+c$, so
$$
I_{2}=\tan x-(x+c)
$$
$$
I_{4}=\frac{1}{3}\tan ^{3}x-\tan x+x+a 
$$

#Mathematics #Calculus 