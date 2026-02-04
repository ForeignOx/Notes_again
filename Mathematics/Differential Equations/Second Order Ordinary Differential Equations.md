## Linear Constant-Coefficient ODEs
### Homogeneous
#### Linear Algebra Derivation
If we have:
$$
a\ddot{x}+b\dot{x}+cx=0
$$
With $x(0)=\alpha$, $\dot{x}(0)=\beta$, we introduce $y\equiv \dot{x}$, then our equation becomes
$$
a\dot{y}+by+cx=0
$$
So is equivalent to the [[Systems of 1st Order ODEs|1st order system of ODEs]]:
$$
\dot{x}=y
$$
$$
 \dot{y}=-\frac{c}{a}x-\frac{b}{a}y
$$
Which we can solve with [[Matrices|matrices]], by rewriting:
$$
\begin{pmatrix}
\dot{x}\\\dot{y}
\end{pmatrix}=\begin{pmatrix}
0&1\\-\frac{c}{a}& -\frac{b}{a}
\end{pmatrix}\begin{pmatrix}
x\\y
\end{pmatrix}
$$
$$
\dot{\underline{x}}=B\underline{x}
$$
So we will want to [[Diagonalisation|diagonalise]] $B$:
$$
p_{B}(t)=\det \begin{pmatrix}
-t&1\\-\frac{c}{a} & -\frac{b}{a}-t
\end{pmatrix}=t^{2}+\frac{b}{a}t+\frac{c}{a}
$$
$$
\implies at^{2}+bt+c=0
$$
Os the characteristic polynomial for our original equation
This is always fine unless we have a repeated root :(
___
#### Method
For a 2nd order, linear homogeneous ODE with constant coefficients:
$$
a \frac{d^{2}y}{dx^{2}}+b \frac{dy}{dx}+cy=0
$$
Consider a solution of the form:
$$
y=e^{\lambda x}
$$
$$
\implies \frac{dy}{dx}=\lambda e^{\lambda x}
$$
$$
\implies \frac{d^{2}y}{dx^{2}}=\lambda^{2}e^{\lambda x}
$$
Substitute these back into the original equation
$$
a(\lambda^{2}e^{\lambda x} )+b(\lambda e^{\lambda x})+c(e^{\lambda x})=0
$$
$$
\implies e^{\lambda x}(a\lambda^{2}+b\lambda+c)=0
$$
So we get the auxiliary equation:
$$
a\lambda^{2}+b\lambda+c=0
$$
With solutions: $\lambda=\alpha$ and $\lambda=\beta$
$\therefore$ the general solution is the sum of these:
$$
y=Ae^{\alpha x}+Be^{\beta x}
$$
The particular solution can be found using initial conditions
### Repeated Roots
If $\alpha=\beta$, the general solution will instead be:
$$
y=(A+Bx)e^{\alpha x}
$$
Note that in this case the product rule will be needed to find the particular solution
We know this as $y_{2}=xe^{ \lambda x }$ is also a solution to $y_{1}=e^{ \lambda x }$, since:
$$
0=ay''+by+c
$$
Which one can rewrite as:
$$
0=a(y''-2\lambda y'+\lambda^{2}y)
$$
Since there is a repeated root
We have:
$$
y_{2}'=e^{ \lambda x }+\lambda e^{ \lambda x }
$$
$$
y_{2}''=\lambda e^{ \lambda x }+\lambda e^{ \lambda x }+\lambda^{2}xe^{ \lambda x }=2\lambda e^{ \lambda x }+\lambda^{2}xe^{ \lambda x }
$$
So:
$$
y_{2}''-2\lambda y_{2}'+\lambda^{2}y_{2}=(2\lambda e^{ \lambda x }+\lambda xe^{ \lambda x })-2\lambda(e^{ \lambda x }+\lambda e^{ \lambda x })+\lambda^{2}(xe^{ \lambda x })=0
$$
So $y_{2}$ is a second independent solution, as required
### Complex Roots
If $\alpha,\beta \in \mathbb{C}$, $\alpha=\beta ^{*}$, ie. $\alpha=a+bi$, $\beta=a-bi$ and the general solution will be:
$$
y=Ae^{(a+bi)x}+Be^{(a-bi)x}=e^{a}(Ae^{bix}+Be^{-bix})
$$
$$
=e^{a}(A(\cos bx+i\sin bx)+B(\cos bx-i\sin bx))
$$
$$
=e^{a}((A+B)\cos bx+(A-B)i\sin bx)
$$
Which can be rewritten as:
$$
y=e^{a}(P\cos bx+Q\sin bx)
$$
Which is the new general solution which can then be rewritten in harmonic form:
$$
y=e^{a}R\cos(bx-\theta)
$$
Where $R=\sqrt{ P^{2}+Q^{2} }$ and $\theta=\arctan\left( \frac{Q}{P} \right)$
### Non-Homogeneous
For a 2nd order, linear non-homogeneous ODE with constant coefficients:
$$
a \frac{d^{2}y}{dx^{2}}+b \frac{dy}{dx}+cy=\phi(x)
$$
#### General Form
If $y=y_{1}$ is a solution to:
$$
ay''+by'+cy=f(x)
$$
and $y=y_{2}$ is a solution to:
$$
ay''+by'+cy=0
$$
Then let 
$$
y=y_{1}+y_{2}
$$
$$
\implies y'=y_{1}'+y_{2}'
$$
$$
\implies y''=y_{1}''+y_{2}''
$$
$$
\implies a(y_{1}''+y_{2}'')+b(y_{1}'+y_{2}')+c(y_{1}+y_{2})
$$
$$
=(ay_{1}''+by_{1}'+cy_{1})+(ay_{2}''+by_{2}'+cy_{2})
$$
$$
=f(x)+0=f(x)
$$
So our general solution can be in the form $y=y_{1}+y_{2}$
#### Complimentary Function
This is $y_{2}$ from above, always do this first, this is the same as with homogeneous:
$$
y=Ae^{\alpha x}+Be^{\beta x}
$$
#### Undetermined Coefficients
We need to find a particular integral to satisfy the ODE
When $\phi(x)$ ha s the form of a polynomial, exponential or $\sin$ or $\cos$ function, or a sum or product of these, we can apply the method of undetermined coefficients
To apply this method, we try a $y_{PI}$ of a particular form based on the form of $\phi$ containing some unknown constant coefficients. We then determine these coeffifiences such that $y_{PI}$ solves the original equation
The following table lists terms that can appear in $\phi$ in order to use this method, and the corresponding form to try for $y_{PI}$

| Term in $\phi(x)$ | Form to try for $y_{PI}$                   |
| ----------------- | ------------------------------------------ |
| $e^{ \gamma x }$  | $a_{1}e^{ \gamma x }$                      |
| $x^{n}$           | $a_{0}+a_{1}x+a_{2}x^{2}+\dots+a_{n}x^{n}$ |
| $\cos(\gamma x)$  | $a_{1}\cos(\gamma x)+a_{2}\sin(\gamma x)$  |
| $\sin(\gamma x)$  | $a_{1}\cos(\gamma x)+a_{2}\sin(\gamma x)$  |
If $\phi(x)$ contains sums or products of the above terms, we try the corresponding sum/product of the corresponding forms
If the listed form to try is already in the complimentary function, then putting this into the original ODE will give $0$ rather than $\phi(x)$, we then try a $y_{PI}$ of the suggested form multiplied by $x$. We can apply this rule twice (or more times) if the first applicatio also gives a terms in $y_{CF}$
### Method of Variation of Parameters
Our method of undetermined coefficients allows us to solve an inhomogeneous ODE, but only when the inhomogeneous terms $\phi(x)$ takes particular forms. The following method allows us to solve more general inhomogeneous ODEs
We wish to find a particular integral for the inhomogeneous ODE, we swtart by considering the two linearly independent solutions $y_{1},y_{2}$ of the associated homogeneous ODE:
$$
y_{CF}=Ay_{1}+By_{2}
$$
We now replace the constants $A$ and $B$ in $y_{CF}$ by functions $u_{1}(x)$ and $u_{2}(x)$ respectively. That is, we look for solutions of the form:
$$
y_{PI}=u_{1}(x)y_{1}(x)+u_{2}(x)y_{2}(x)
$$
We wish to find $u_{1}(x)$ and $u_{2}(x)$ such that $y_{PI}$ is a solution to the original ODE. This give one constraint on $u_{1}$ and $u_{2}$ so to find unique function we should impose a second constraint on $u_{1}$ and $u_{2}$, we choose:
$$
u_{1}'y_{1}+u_{2}'y_{2}=0
$$
Then
$$
y'_{PI}=u_{1}'y_{1}+u_{1}y_{1}'+u_{2}'y_{2}+u_{2}y_{2}'=u_{1}y_{1}'+u_{2}y_{2}'
$$
From above and:
$$
y_{PI}''=u_{1}'y_{1}'+u_{1}y_{1}''+u_{2}'y_{2}'+u_{2}y_{2}''
$$
Next, we need to substitute this into the original ODE in order to identify $u_{1}(x)$ and $u_{2}(x)$, which gives:
$$
a_{2}(u_{1}'y_{1}'+u_{1}y_{1}''+u_{2}'y_{2}'+u_{2}y_{2}'')+a_{1}(u_{1}y_{1}'+u_{2}y_{2}')+a_{0}(u_{1}y_{1}+u_{2}y_{2})=\phi
$$
Collecting the $u_{1}$ and $u_{2}$ terms gives:
$$
u_{1}\underbrace{ (a_{2}y_{1}''+a_{1}y_{1}'+a_{0}y_{1}) }_{ =0 }+u_{2}\underbrace{ (a_{2}y_{2}''+a_{1}y_{2}'+a_{0}y_{2}) }_{ =0 }+a_{2}(u_{1}'y_{1}'+u_{2}'y_{2}')=\phi
$$
Since $y_{1}$ and $y_{2}$ are solutions to the homogeneous equation, so our equation simplifies to:
$$
a_{2}(u_{1}'y_{1}'+u_{2}'y_{2}')=\phi
$$
Which is first order in the derivatives of $u_{i}$
We now have two simultaneous equations for $u_{1}$ and $u_{2}$, namely: $a_{2}(u_{1}'y_{1}'+u_{2}'y_{2}')=\phi$ and $u_{1}'y_{1}+u_{2}'y_{2}=0$, which can be solved by multiplying the first by $y_{1}$ and rearranging:
$$
u_{1}'y_{1}'y_{1}+u_{2}'y_{2}'y_{1}=\frac{\phi y_{1}}{a_{2}}
$$
Then using $u_{1}'y_{1}=-u_{2}'y_{2}$,
$$
u_{2}'(y_{2}'y_{1}-y_{1}'y_{2})=\frac{\phi y_{1}}{a_{2}}
$$
$$
\implies u_{2}'=\frac{\phi y_{1}}{a_{2}W(y_{1},y_{2})}
$$
Where $W(y_{1},y_{2})$ is the [[Wronskian|wronskian]]
And then also:
$$
u_{1}'=\frac{-\phi y_{2}}{a_{2}W(y_{1},y_{2})}
$$
Hence we find $u_{1}$ and $u_{2}$ by integrating:
$$
u_{1}(x)=-\int \frac{\phi(x)y_{2}(x)}{a_{2}W(y_{1},y_{2})} \, dx 
$$
$$
u_{2}(x)=\int \frac{\phi(x)y_{1}(x)}{a_{2}W(y_{1},y_{2})} \, dx 
$$
#### Examples
Solve $y''-y=e^{ 2x }$, which is doable by the method of undetermined coefficients, but we want to cause maximal suffering (to check our new method)
The auxiliary equation is:
$$
\lambda^{2}-1=0\iff\lambda=\pm 1
$$
So:
$$
y_{CF}=Ae^{ x }+Be^{ -x }
$$
Therefore $y_{1}=e^{ x }$ and $y_{2}=e^{ -x }$, so we can find the Wronskian:
$$
W(y_{1},y_{2})=\det \begin{pmatrix}
y_{1}&y_{2}\\y_{1}'&y_{2}'
\end{pmatrix}=\det \begin{pmatrix}
e^{ x }&e^{ -x }\\e^{ x }&-e^{ -x }
\end{pmatrix}=-2
$$
So
$$
    u_{1}=-\int \frac{e^{ 2x }e^{ -x }}{-2} \, dx =\frac{1}{2}\int e^{ x } \, dx =\frac{1}{2}e^{ x }
$$
$$
u_{2}=\int \frac{e^{ 2x }e^{ x }}{-2} \, dx =-\frac{1}{2}\int e^{ 3x } \, dx =-\frac{1}{6}e^{ 3x }
$$
Therefore
$$
y_{PI}=u_{1}y_{1}+u_{2}y_{2}=\frac{1}{2}e^{ x }e^{ x }+\left( -\frac{1}{6}e^{ 3x } \right)e^{ -x }=\frac{1}{3}e^{ 2x }
$$
So the general solution to the ODE is then:
$$
y(x)=y_{CF}+y_{PI}=Ae^{ x }+Be^{ -x }+\frac{1}{3}e^{ 2x }
$$
The reason we can ignore the constants is that they become reincorporated into the $A$ and $B$
___
Solve
$$
y''-2y'+y=\frac{e^{ x }}{x^{2}+1}
$$
Now $\phi=\frac{e^{ x }}{x^{2}+1}$ is not a sum or product of things we had in our table of particular integrals, so we must use variation of parameters
Firstly the characteristic equations is:
$$
\lambda^{2}-2\lambda+1=0
$$
So we have a repeated root at $\lambda=1$, so
$$
y_{CF}=Ae^{ x }+Bxe^{ x }
$$
So $y_{1}=e^{ x }$, $y_{2}=xe^{ x }$, so we can calculate their Wronskian
$$
W(y_{1},y_{2})=\det \begin{pmatrix}
e^{ x }&xe^{ x }\\e^{ x }&e^{ x }+xe^{ x }
\end{pmatrix}=e^{ 2x }+xe^{ 2x }-xe^{ 2x }=e^{ 2x }
$$
Which is not identically $\hspace{0pt}0$, telling us that $y_{1}$ and $y_{2}$ are not linearly independent
And so
$$
u_{1}=-\int \frac{e^{ x }xe^{ x }}{(x^{2}+1)e^{ 2x }} \, dx =-\int \frac{x}{x^{2}+1} \, dx =-\frac{1}{2}\ln(x^{2}+1)
$$
$$
u_{2}=\int \frac{e^{ x }e^{ x }}{(x^{2}+1)e^{ 2x }} \, dx =\int \frac{1}{x^{2}+1} \, dx =\arctan(x)
$$
So
$$
y_{PI}=u_{1}y_{1}+u_{2}y_{2}=-\frac{1}{2}e^{ x }\ln(x^{2}+1)+xe^{ x }\arctan(x)
$$
And so the general solution to the ODE is
$$
y(x)=y_{CF}+y_{PI}=e^{ x }\left( A+Bx-\frac{1}{2}\ln(x^{2}+1)+x\arctan(x) \right)
$$
## Linear ODEs
The canonical form of a second order linear ODE is:
$$
\frac{d ^{2}y}{dx^{2}} +p(x)\frac{d y}{dx} +q(x)y=0
$$
We can solve these by finding [[Power Series|power]] [[Series|series]] of the form
$$
y=\sum_{n=0}^{\infty} a_{n}(x-x_{0})^{2} 
$$
A solution can be found in this form provided $x_{0}$ is a regular point of the ODE
### Example
Find series solution for $\frac{d ^{2}y}{dx^{2}}-y=0$, in canonical form, $p=0$, $q=-1$, these functions are equal to their [[Taylor Series|Taylor series]], so are analytic everywhere, so all points are regular. Choose $x_{0}=0$, and
$$
y=\sum_{n=0}^{\infty} a_{n}x^{n} 
$$
We substitute this in:
$$
\frac{d ^{2}}{dx^{2}} \left( \sum_{n=0}^{\infty} a_{n}x^{n}  \right)-\sum_{n=0}^{\infty} a_{n}x^{n}=0
$$
$$
\implies \sum_{n=0}^{\infty} a_{n}n(n-1)x^{n-2}-\sum_{n=0}^{\infty} a_{n}x^{n}=0
$$
Relabel $n\to n+2$:
$$
\implies \sum_{n=-2}^{\infty} a_{n+2}(n+2)(n+1)x^{n}-\sum_{n=0}^{\infty} a_{n}x^{n}=0    
$$
But the first two terms of the first series are both $\hspace{0pt}0$, so:
$$
\sum_{n=0}^{\infty} a_{n+2}(n+2)(n+1)x^{n}-\sum_{n=0}^{\infty} a_{n}x^{n}  =0
$$
$$
\implies \sum_{n=0}^{\infty} x^{n}(a_{n+2}(n+2)(n+1)-a_{n})=0
$$
$$
\implies a_{n+2}=\frac{a_{n}}{(n+1)(n+2)} 
$$
By looking at some terms, we get
$$
a_{2}=\frac{a_{0}}{2\times 1},a_{4}=\frac{a_{2}}{4\times 3}=\frac{a_{0}}{4\times 3\times 2\times 1}
$$
We essentially get:
$$
a_{2n}=\frac{a_{0}}{(2n)!},a_{2n+1}=\frac{a_{1}}{(2n+1)!}
$$
So
$$
y=\sum_{n=0}^{\infty} a_{k} 
$$

#Mathematics #Calculus