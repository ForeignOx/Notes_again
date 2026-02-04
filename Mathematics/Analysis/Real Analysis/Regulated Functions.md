


### Example
How to cook up $f_{n}\to f$, assume $f$ is Lipshitz, so 
$$
\left| f(x)-f(y) \right| \leq M\left| x-y\right| 
$$
We can form an equidistant partition; $x_{k}=a+k \frac{b-a}{n}$, from $k=0,\dots,n$
So we take any $x_{k}^{*}\in[x_{k},x_{k+1}]$, say $x_{k}^{*}=x_{k}$, and set
$$
f_{n}=\begin{cases}
f(x_{k})&\text{if }x\in [x_{k},x_{k+1}]\\f(b)&\text{if }x=b
\end{cases}
$$
This words because
$$
\left| f(x)-f_{n}(x) \right| =\left| f(x)-f(x_{k}^{*}) \right| \leq M\left| x-x_{k}^{*} \right| \leq M  \frac{b-a}{n}\to 0
$$
As $n\to \infty$, so we have uniform convergence
___
Not all functions are regulated, for example
$$
d(x):=\begin{cases}
1&\text{if }x\in \mathbb{Q}\\0&\text{otherwise}
\end{cases}
$$
Note that any open set/interval contains infinitely rational and irrational numbers. If $d(x)$ was regualated
Pick $\varepsilon=\frac{1}{4}$, take the step function $g(x)$ such that
$$
\left| g(x)-d(x) \right| <\frac{1}{4},~\forall x\in [0,1]
$$
As a step function, $g(x)$ is constant on some interval, $g(x)=c,~\forall x\in I$, but $I$ contains $r\in\mathbb{Q}$, and $s \in\mathbb{R}\setminus \mathbb{Q}$, $d(r)=1,d(s)=0$
$$
\left| d(r)-g(r) \right|=\left| 1-c \right| <\frac{1}{4} 
$$
$$
 \left| d(s)-g(s) \right| =c<\frac{1}{4}
$$
Which is possible for no $c$
___
Reculated functions can have infinitely many discontinuities. Take a sequence $a_{k}$ with $\lim_{ k \to \infty }a_{k}=a$, set a function
$$
f(x)=\begin{cases}
a&x=0\\ a_{k}&x\in \left[ \frac{1}{k+1},  \frac{1}{k} \right]
\\a_{0}&x=1
\end{cases}
$$
This is not a step function as it has infinitely many steps, but we set
$$
f_{n}(x)=\begin{cases}
a&\text{if }x\in \left[ 0,  \frac{1}{n+1} \right]\\f(x)&x<\frac{1}{n+1}
\end{cases}

$$
Then
$$
\left| f_{n}(x)-f(x) \right| =\begin{cases}
0 & \text{if }x>\frac{1}{n+1}\\\left| a_{k}-a \right|   & k>n
\end{cases}
$$
Which is not a step function, gut is regulated
___
Monotone functions are regulated
## Further Properties
### Lemma
If $f_{n}\to f$ uniformly converges to $f$ where $f_{n}$ are step functions, then $f_{n}(x),f(x)$ are uniformly bounded; i.e. $\left| f_{n}(x) \right|,\left| f(x) \right|<c\forall x\in[a,b]$
#### Proof
Take $\varepsilon=1$, then there exists $N$ such that 
$$
\left| f_{n}(x)-f(x) \right|<\varepsilon=1\forall x\in[a,b]\forall n\geq N
$$
So $\left| f(x)-f_{N}(x) \right|<\varepsilon=1$ for all $x$, so
$$
\left| f(x) \right| <\left| f_{N}(x) \right| +1
$$
Which means that $f(x)$ is bounded, since $f_{N}(x)$ take only finitely many values. Same for the $f_{n}(x)$, for $n\geq N$, so $f_{1},\dots,f_{N-1}$ are bounded universally, so we just take the maximum
### Proposition "Regulated CoLT"
If $f_{n}\to f,g_{n}\to g$, $f,g$ are regulated, so
- $\alpha f+\beta g$ is regulated by $\alpha f_{n}+\beta g_{n}$
- $fg$ is regulated by $f_{n}g_{n}$
- $\left| f \right|$ is regulated by $\left| f_{n} \right|$
- $\max(f,g),\min(f,g)$ are regulated
