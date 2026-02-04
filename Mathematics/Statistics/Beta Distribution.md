zLet a [[Random Variables|random variable]] $X\sim Beta(a,b)$ for $a,b>0$ known, then $X$ has Beta distribution with pdf
$$
f(x)=\frac{1}{\beta(a,b)}x^{a-1}(1-x)^{b-1}=\frac{\Gamma(a+b)}{\Gamma(a)\Gamma(b)}x^{a-1}(1-x)^{b-1},0\leq x\leq 1
$$
And $0$ otherwise, wher $\beta(a,b)$ is the [[Beta Function|beta function]], and $\Gamma(a)$ is the gamma function
Note that $Be ta(1,1)$ is the same as the [[Uniform Distribution|uniform distribution]] between $0$ and $1$; $U[0,1]$, i.e. $f(x)=1$ for $0\leq x\leq 1$
For $a,b$ both large, then approximately, $X\sim N(E(X),Var(X))$ (unless $a\gg b$ or $b\ll a$)
## Core
The [[Core of a Distribution|core]] of $Beta(a,b)$ pdf is
$$
\kappa(x)=x^{a-1}(1-x)^{b-1}
$$
## [[Expectation|Expectation]]
If $X\sim B et a(a,b)$, then
$$
E(X)=\frac{a}{a+b}
$$
## [[Variance|Variance]]
$$
Var(X)=\frac{ab}{(a+b)^{2}(a+b+1)}
$$
## Mode
$$
Mode(X)=\frac{a-1}{a+b-2}
$$
