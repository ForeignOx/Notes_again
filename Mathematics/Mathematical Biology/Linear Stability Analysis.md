## General Single Autonomous ODEs
The general method for performing a linear stability analysis of an autonomous ODE of the form:
$$
F\left( x(t),\frac{d x}{dt} ,\dots,\frac{d x^{n}}{dt^{n}}  \right)=0
$$
At equilibrium $x=x_{0}$, all $t$ derivatives must vanish, so we are left with some function of $x_{0}$ along:
$$
F(x_{0},0,\dots,0)=0
$$
Then we linearise the system, assuming a solution of the form $x=x_{0}+\varepsilon x_{1}$
$$
F\left( x_{0}+\varepsilon x_{1}(t),0+\varepsilon \frac{d x_{1}}{dt} ,\dots,0+\varepsilon \frac{d ^{n}x_{1}}{dt^{n}}  \right)=0
$$
Now Now perform an $n$-dimensional [[Taylor Series|taylor]] expansion in $\varepsilon$ about $\varepsilon=0$, denoting $\frac{d ^{n}x}{dt^{n}}=x^{(n)}$, we get
$$
F(x_{0},0,\dots,0)+\varepsilon\left( \frac{ \partial F }{ \partial x } x_{1}+\frac{ \partial F }{ \partial x^{(1)} } x_{1}^{(1)}+\dots+\frac{ \partial F }{ \partial x^{(n)} } x_{1}^{(n)} \right)=0
$$
To $\mathcal{O}(\varepsilon^{2})$
Since we are evaluating the partial derivatives at $\varepsilon=0$, $x=x_{0}$, the partial derivatives $\frac{ \partial F }{ \partial x^{(n)} }$ are constants, sooo if we ignore the term of $\mathcal{O}(\varepsilon^{2})$, we have:
$$
a_{0}x_{1}+a_{1}\frac{d x_{1}}{dt} +\dots+a_{n}\frac{d^{n}x_{1}}{dt^{n}}=0,~a_{n} =\frac{ \partial F }{ \partial x^{(n)} } \Bigg{|}_{x=x_{0}} 
$$
Which is a constant coefficient ODE
Next we solve the linearised system gives a polynomial in the form:
$$
a_{0}+a_{1}\lambda+\dots+a_{n}\lambda^{n}
$$
And hence the full solution of the correction $x_{1}$ takes the general form:
$$
x_{1}=c_{1}e^{ \lambda_{1}t }+\dots+c_{n}e^{ \lambda_{n}t }
$$
Of course, some of these could be complex giving solutions of the form $e^{ \mu_{i}t }(A\cos(\nu_{i}t)+B\sin(\nu_{i}t))$, for the sake of stability analysis, we know that the imaginary part of $\lambda$ does not control growth, only the real part does
Finally we assess stability...
### Asymptotic Stability
An equation is aymptotically stable if
- It is Lyapunov stable
- $\exists\varepsilon$ such that $\left| x(0)-x_{0} \right|<\varepsilon$ then $\lim_{ t \to \infty }\left| x(t)-x_{0} \right|=0$
I.e. when you start arbitrarily close to $x_{0}$, you end up at $x_{0}$
It is possible for both criteria to be satisfied independently
If all $\mathfrak{R}(\lambda_{n})<0$ in the system, then it will be asymptotically stable
## Instability
If any of the $\mathfrak{R}(\lambda_{i})$ are positive, then $x_{1}$ will grow exponentially, we class such equilibria $x_{0}$ for which this $x_{1}$ is our small correction $x_{0}+\varepsilon x_{1}$ as unstable. 
As this growth continues, the linear approxiamtion become invalid and the nonlinear dynamics take over. All that matters for stability is that the solution cannot approach $x_{0}$ if the initial condition $x(0)$ is not the equilibrium (it is essentially repelled from $x_{0}$)
## The Degenerate Case
Sometimes we encounter the case where one of the $\mathfrak{R}(\lambda_{i})=0$, if all other $\mathfrak{R}(\lambda_{i})$ are less than or equal to 0, this fits neither of the previous definitions, it is not unstable as there is no exponential growth, but the solution will not decay, so it is not asymptotically stable
There is no simple answer as to what this implies, but usually it will be one of three possibilities:
- The solutions close to equilibrium are periodic limit cycles
- The equilibrium itself is degenerate i.e. $\frac{d x}{dt}=0$, this solution is any permissible $x_{0}\in \mathbb{R}(>0)$ thus any equilibrium is local to another equilibrium and cannot be stable
- Equations such as
$$
\frac{d x}{dt} +x^{3}=0
$$
    Whose equilibrium is $x_{0}=0$, and the expansion of $(x_{0}+\varepsilon x_{1})^{3}$ is just $\varepsilon^{3}x_{1}^{3}$ (all other terms involve $x_{0}=0$), this means the linear equation is simply
$$
\frac{d x_{1}}{dt} =0
$$
    Such cases are more complex and suggest wwe have ignored some terms in the linearisation that we shouldn't have
## General Systems of First Order Autonomous ODEs
More generally we could consider a systems of $m$ ODEs in $m$ functions $x^{1}(t),\dots,x^{m}(t)$:
$$
F^{1}\left( x^{1}(t),\frac{d x^{1}}{dt} ,\dots,\dots,x^{m}(t),\frac{d x^{m}}{dt} ,\dots,\frac{d ^{n}x^{m}}{dt^{n}}  \right)=0 
$$
$$
 \vdots
$$
$$
 F^{m}\left( x^{1}(t),\frac{d x^{1}}{dt} ,\dots,\dots,x^{m}(t),\frac{d x^{m}}{dt} ,\dots,\frac{d ^{n}x^{m}}{dt^{n}}  \right)=0 
$$
