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
If all $\mathfrak{R}(\lambda_{n})>$
