A quantity $z$ is a functional of the [[Functions|function]] $x(t)$ in the [[Intervals|interval]] $(a,b)$ when it depends on all the values taken by $x(t)$ when $t$ varies in the interval $(a,b)$; or, alternatively, when a law is given by which everry function $x(t)$ defined within $(a,b)$ (the independent variable within a certain functional field), there can be made to correspond one and only one quantity $z$ perfectly determined, denoted:
$$
z=F\left| \left[x(\underset{a}{\overset{b}t})\right]\right| 
$$
But for the sake of simplicity, when there is no ambiguity, we can use one of the following:
$$
F|[x(t)]|, F \left[x(\underset{a}{\overset{b}t})\right], F[x(t)]
$$
This definition of a functional recalls expecially the ordinary general [[Functions#Formal Dirichlet-Bourbaki Definition|definition of a function given by Dirichlet]]
If other variables $\alpha,\beta,\dots$ also occur in the function $x(t)$, ($t$being the independent variable), we shall write:
$$
z= F \left[x(\underset{a}{\overset{b}t},\alpha,\beta,\dots)\right]=z(\alpha,\beta ,\dots)
$$
To indicate that the functional operator $F$, which when applied to the variable function $x$ as a function of $t$ alone, i.e. supposing that in $x$, the quantities $\alpha,\beta ,\dots$ are constant; $z$ will then be an ordinary function of $\alpha,\beta,\dots$, and it is to be noted that it will not be a function of $t$ as $x$ was
The functional may also contain certain parameters $\lambda,\mu,\dots$
$$
z= F \left[x(\underset{a}{\overset{b}t});\lambda,\mu, \dots\right]
$$
in this case, the quantity $z$, for every system of values of the parameters, will be a functional of $x(t)$, in the sense stated above, while it will be an ordinary function $z(\lambda,\mu, \dots)$ of the parameters when $x(t)$ is fixed. We can also say that in this case, corresponding to every function $x(t)$, defined within a certain field of variation, the functional operator $F$ determines another function, so we can say:
$$
z(\lambda, \mu, \dots)=F \left[x(\underset{a}{\overset{b}t});\lambda,\mu, \dots\right]
$$
With both of these cases, when there is no abiguity about the role of the variable $t$ and of other variables $\alpha,\beta, \dots;\lambda,\mu,\dots$ and simply write:
$$
F[x(t,\alpha,\beta ,\dots)],F[x(t);\lambda,\mu ,\dots]
$$
## Multiple Functions
The notion of a functional can be extended to the quantities of $z$ which depend on all the values taken not by one, but by several functions in several intervals, e.g. by two: $x=x(t),y=y(t)$ in the intervals $(a,b)$ and $(c,d)$ respectively:
$$
z=F \left[x(\underset{a}{\overset{b}t}),y(\underset{c}{\overset{d}{u}})\right]
$$
The conideration of these functions presents little interest, as they can be immediately reduced to those depending on a single variable function, for example, let $a'b'=a'c'+c'b'$ be an interval of variation of a parameter $v$, of amplitude equal to the sum of the two intervals $(a,b)$ and $(c,d)$; and let $c'$ be a point within $(a'b')$ such that $c'-a'=b-a,b'-c'=d-c$. For every pair of functions $x(t),y(u)$ defined in $(a,b),(c,d)$ respectively, let us construct a new function $X(v)$ deined as follows in the interval $(a',b'):$ for $v=a'$, or within the interval $(a',c'), X(v)=x(a+v-a')$; for $v=b'$, or within the interval $(c',b'),X(v)=y(c+v-c')$ for $v=c'$, we shall give $X(c')$ one of the two values $x(b)$ or $y(c)$
Since the pair of functions $x(t),y(u)$ completely determine the function $X(v)$ (with the sole exception of $v=c'$), and vice versa, $X(v)$ determines the two functions (with the exception of $t=b$ for $x$ and $u=c$ for $y$), we can say, so long as the indeterminateness of the variable function at an isolated point does not affect the value of the functional, that the quantity can be expressed as a single function like so:
$$
z=F \left[x(\underset{a}{\overset{b}t}),y(\underset{c}{\overset{d}{u}})\right]=G\left[\overline{X}(\underset{a'}{\overset{b'}v})\right]
$$
___
Another generalisation of the concept of a functional is obtained by considering those quantities $z$ which depend on all the values taken by one or more functions $\phi_{1}(x_{1},x_{2},\dots,x_{n}),\phi_{2}(y_{1},y_{2},\dots,y_{m}),\dots$ of severa variables defined within certain fields $C_{1},C_{2},\dots$ respectively;
$$
z=F[\phi_{1}(x_{1},x_{2},\dots,x_{n}),\phi_{2}(y_{1},y_{2},\dots,y_{m}),\dots]
$$
___
This concept of a functional also includes functions of lines, and more generally, of hyperspaces. We say, in face, that a quantity $z$ is a function of a variable hyperspace $S_{r}$ contained in another $S_{n}$, $(n\geq r)$ and parametrically defined by the equations:
$$
x_{i}=\phi_{i}(t_{1},t_{2},\dots,t_{r}),i=1,2,\dots,n
$$
when to every such $S_{r}$ there corresponds one definite value of the quantity $z=F[S_{r}]$, which thus comes to depend on all the values taken by the $n$ functions $\phi_{i}$ at the points of the field of $C$ (of $r$ dimensions) for which they are defined. It is to be noted, however, that this function $z$, a function of the hyperspace $S_{r}$ is not a general functional of the $n$ functions $\phi_{i}$; in fact, if the parameters $t_{k}$ are changed into others $u_{l}$ by means of the transformation:
$$
t_{k}=t_{k}(u_{1},u_{2},\dots,u_{r}),k=1,2,\dots,r
$$
$$
\frac{d (t_{1},t_{2},\dots,t_{r})}{d(u_{1},u_{2},\dots,u_{r})}\neq 0 
$$
the coordinates $x_{i}$ will no longer be given by the functions $\phi$ of the $t_{k}$'s but by other functions $\psi$ of the $u_{l}$'s:
$$
x_{i}=\psi_{i}(u_{1},u_{2},\dots,u_{r})=\phi_{i}(t_{1},t_{2},\dots,t_{r})
$$
but the quantity $z$ which depends only on the form of the hyperspace $S_{r}$ (or manifold, as it is often called), and not on the mode of representation, will not have changed; i.e. $z$ is a functional of the functions $\phi_{i}$ which does not vary when the $\phi_{i}$'s are replaced by other functions $\psi_{i}$ obtained from them by a change of parameters

## Example
Consider the function
$$
S[y(t)]=\int ^{b}_{a} (y(t))^{2} \, dt 
$$
___
The length of a path is also an example