A logarithm is the [[Inverses|inverse]] of an [[Exponential Functions|exponential]] [[Real Functions|function]]: if $y=b^{x}$, then $x=\log_{b}(y)$. As with exponential functions, we have to specify the base of the logarithm
The domain of a logarithm function is the image of an exponential function and hence is $(0,\infty)$. The image of a logarithm function is the domain of an exponential function and thus is $\mathbb{R}$
When the base of a logarithm is $e$, we call our function the natural logarithm denoted by $\ln (x)$ 
A logarithm grows very slowly as $x$ grows large and positive (more slowly than a linear function) and has a vertical asymptote at $x=0$
Some important properties of logarithms are:
- $\log_{b}1=0$ (this follows from $b^{0}=1$)
- $\log_{b}b^{x}=x$
- $\log_{b}\alpha\beta=\log_{b}\alpha+\log_{b}\beta$
- $\log_{b} \frac{\alpha}{\beta}=\log_{b}\alpha-\log_{b}\beta$
- $\log_{b}(x^{r})=r\log_{b}x$
___
## The $\ln$ function
Let $a>0$, then there exists a unique $x\in\mathbb{R}$ with $\exp(x)=a$
### Proof
Consider $X=\{ y\in\mathbb{R}\mid \exp(y)<a \}$, for $n\in\mathbb{N}$,
$$
\exp(n)=e^{ n }>1^{n}=1
$$
So it is unbounded, so $e^{ n }$ is an [[Boundedness|unbounded]] [[Sequences|sequence]]
So there is [[Natural Numbers|$n\in\mathbb{N}$]] with $e^{ n }>a$ also if $x>n$, $e^{ n }<e^{ x }$ as $e^{ x }$ is monotonically increasing, so $n$ is an upper bound for $X$
Look at $e^{ -n }=\frac{1}{e^{n}}\to 0$, then there is $n\in\mathbb{N}$ with $e^{ -n }<a$, so $-n\in X$, so $X$ is not empty
Now we can use [[Supremum and Infimum|$x=\sup(X)$]] from the [[Real Numbers#Completeness Axiom|completeness axiom]]
Now we want to show that $\exp(x)<a$ or $\exp(a)>a$ is not true:
Assume $\exp(x)>a$, look at $\exp\left( x-\frac{1}{n} \right)$ with $n\in\mathbb{N}$
$$
\exp\left( x-\frac{1}{n} \right)=\frac{\exp(x)}{\exp\left( \frac{1}{n} \right)}
$$
Recall $1+x\leq e^{ x }\leq \frac{1}{1-x}$, using this in the denominator, we get
$$
\exp\left( x-\frac{1}{x} \right)\geq \frac{\exp(x)}{\frac{1}{1-\frac{1}{n}}}=\exp(x)\left( 1-\frac{1}{n} \right)
$$
So
$$
\exp\left( x-\frac{1}{n} \right)\geq \exp(x)-\frac{\exp(x)}{n}
$$
We want this to be $>a$, so chose $n$ so large that
$$
\frac{\exp(x)}{n}<\exp(x)-a
$$
By the [[Theorem of Archimedes|theorem of Archimedes]], with such $n$ we have
$$
\exp\left( x-\frac{1}{n} \right)>\exp(x)-\exp(x-a)=a
$$
So $x-\frac{1}{n}$ is an upper bound for $X$, contradicting that $x$ was the supremum, so $\exp(x)\leq a$
Next you'd have to show that $\exp(a)\not<a$
___
Now we can define the logarithm:
$$
\ln:(0,\infty)\to \mathbb{R}
$$
Defined by $\ln x=a$, where $a\in\mathbb{R}$ is such that $\exp(a)=x$
___
## Other Bases
For $a>0$, $a\neq 1$, define
$$
\log_{a}(x)=\frac{\ln(x)}{\ln (a)}
$$
### Properties
Let $a,b>0$ with $b\neq 1$ and $x,y\in\mathbb{R}$, then
- $\log_{b}(xy)=\log_{b}(x)+\log_{b}(y)$ for $x,y>0$
- $\log_{b}(x^{y})=y\log_{b}(x)$ for $x>0$
## Useful [[Inequalities|Inequality]]
$$
\frac{x-1}{x}\leq \ln x\leq x-1
$$
proof laters jeez
### Example
For $k\in\mathbb{N}$, we have
$$
\lim_{ n \to \infty } \frac{n^{k}}{e^{ n }}=0
$$
# Complex Logarithms
On $\mathbb{R}$ we know that the exponentia; has an inverse; the logarithm. On $\mathbb{C}$, however, we know that $e^{ z }$ is not injective in general, but we can make it injective by restricting its domain. This motivates the following:
## Lemma 
Inverting the exponential function:
For every $w\in\mathbb{C}^{*}=\mathbb{C}\setminus \left\{ 0 \right\}$, the equation
$$
e^{ z }=w
$$
has a solution $z$. Furthermore, if we write $w=\left| w \right|e^{ i\phi }$ with $\phi=\mathrm{Arg}(w)$, then all solutions to the equation are given by
$$
z=\log \left| w \right| +i(\phi+2\pi k),~k\in \mathbb{Z}
$$
Here, $\log \left| w \right|$ is the usual natural logarithm of the real number $\left| w \right|$. Note that there are infinitely many solutions
### Proof
Choosing $z=\log \left| w \right|+i(\phi+2\pi k)$ for some $k\in\mathbb{Z}$, we find that
$$
e^{ z }=e^{ \log \left| w \right|  }e^{ i(\phi+2\pi k) }=\left| w \right| e^{ i\phi }=w
$$
This shows that a solution exists. Conversely, assume that $z=x+iy$ satisfies $e^{ z }=w$. Then
$$
\left| w \right| =\left| e^{ z } \right| =e^{ x },~\mathrm{Arg}(w)=\mathrm{Arg}(e^{ z })=y\mod 2\pi
$$
The first equality implies that $x=\log \left| w \right|$ andd the second equality imples that $y=\mathrm{Arg}(w)+2\pi k$ for $k\in\mathbb{Z}$
___
A natural question at this point is whether or not we can choose an inverse for the exponential on its range $\mathbb{C}^{*}$?
It seems that there is nothing to stop us from defining the logarithm function as:
$$
\log(z)=\log \left| z \right| +i\mathrm{arg}(z)
$$
Where $\mathrm{arg}$ represents some choice of an argument function. There is some small issue with the above that stops the function being "nice"
To illustrate this issue, let us chose the principle argument $\mathrm{Arg}$, in the above, i.e. the angle we choose is in the interval $(-\pi,\pi]$. By definition
$$
\log(-1)=\log(e^{ i\pi })=\log \left| 1 \right| +i\pi=i\pi
$$
What would happen, however if we get closer to $-1$ from below? For instance by getting closer to $-1$ from points in the upper unit circle
![[Pasted image 20260118133929.png]]
If we choose $\theta=-\pi+\delta$, where $\delta>0$ is really small, then
$$
\mathrm{Arg}(e^{ i(-\pi+\delta) })=-\pi+\delta
$$
Which is almost $2\pi$ away from $\pi$! In other words, as we approach the negative real axis, our argument sees a jump in the value we expect to get $(\approx-\pi)$ and the value we actually get $(\pi)$. We will see the same issue with the logarithm as it is defined by the argument
This issue, is one of lack of continuity. One can visualise this as if our problemtatic approach on the circle is one that corresponds to looking at the shadow of an upwards or downwards path on a helix (completing a full rotation on the shadow of the helix means we went up or down a level):
![[Pasted image 20260118134258.png]]
Consequently, in order to be able to define a logarithm in a way that we don't get this jump in value by approaching a point from two different directions, we need to remove the ability to have a full concentric circle in our domain. We ccan achieve that by removing the closed ray (i.e. the [[Rays|ray]] that includes the origin)
$$
R_{\theta}=\left\{ re^{ i\theta }\mid r\in \mathbb{R},r\geq 0 \right\}

$$
For some fixed $\theta$
## Definition
For any two real numbers $\theta_{1}<\theta_{2}$ with $\theta_{2}-\theta_{1}=2\pi$, let $\mathrm{arg}$ be the choice of argument function with values in $(\theta_{1},\theta_{2}]$. Then the function
$$
\log(z):= \log \left| z \right| +i\mathrm{arg}(z)
$$
Is called a branch of logarithm. It has a jump discontinuity along the ray $R_{\theta_{1}}=R_{\theta_{2}}$. This ray is called a branch cut
If we choose $\mathrm{arg}(z)=\mathrm{Arg}(z)\in(-\pi,\pi]$, then we obtain a branch of logarithm called the principle branch of $\log$
We write $\mathrm{Log}$ for this principle branch; it is given by the formula
$$
\mathrm{Log}(z):=\log \left| z \right| +i\mathrm{Arg}(z)
$$
The principle branch of logarithm has a jump discontinuity along the ray goven by the non-positive real axis $\mathbb{R}_{\leq 0}$
## Remark
- Any time one talks about a function called $\log$, one has to declare which branch they use. This is normally done by simply stating the [[Intervals|interval]] $(\theta_{1},\theta_{2}]$ where $\mathrm{arg}(z)$ lives
- The branch of $\log$ corresponding to $\mathrm{arg}(z)\in(\theta_{1},\theta_{2}]$ is continuous on $\mathbb{C}\setminus \mathbb{R}_{\theta_{1}}$
- The principle branch, $\mathrm{Log}$ agrees with the natural logarithm $\log$ on the real line; that is, for $x>0$, we have $\mathrm{Log}\,x=\log x$, for this reason it is common to use the principle branch unless otherwise stated
## Properties
 We have the following properties when using any given branch of logarithm:
$$
e^{ \log  z }=z \forall z\in \mathbb{C}\setminus \left\{ 0 \right\}
$$
In general,
$$
\log(zw)\neq \log(z)+\log(w)
$$
In general
$$
\log(e^{ z })\neq z
$$
## Mapping
- A branch of the map $\log(z)$ injectively takes a ray of angle $\theta$ without the origin, to the line $y=\theta$, there $\theta$ is measured with respect to the branch cut
- A branch of the map $\log(z)$ takes a concentric circle of radius $r$, minus the intersection of this circle with the branch cut, to an open segment of length $2\pi$ on the line $x=\log r$ with its lowest point given by the angle that defines the branch cut
![[Pasted image 20260118140622.png]]
## Complex Powers
Motivated by what we know on the real line, we can use the logarithm to define general complex powers
For $w\in\mathbb{C}$ fixed, by choosing any branch of $\log$, we can define a branch of the function $z\mapsto z^{w}$ by the expression
$$
z^{w}:= e^{ w\log z }
$$
For example, if $w=\frac{1}{n}$ and we use the principle branch, we get:
$$
z^{\frac{1}{n}}=e^{ \frac{\log \left| z \right|}{n}  +i \frac{\mathrm{Arg}(z)}{n}}=\left| z \right| ^{\frac{1}{n}}e^{ i \frac{\mathrm{Arg}(z)}{n} }
$$
Note that different branches of $\log$ can give different power functions, so one must always specify which branch is being used
Note that this definition is consitent with 
$$
z^{n}=\underbrace{ z\cdot z\cdot z\dots\cdot z }_{ n\text{ times} }
$$
For $n\in\mathbb{N}$ no matter the branch cut
## Remark
One can check that for $w=\frac{1}{n}$ and the choice of branch cut $R_{\leq 0}$ all the branches we get are of the form
$$
z^{\frac{1}{n}}=\left| z \right| ^{\frac{1}{n}}e^{ i\left(  \frac{\mathrm{Arg}(z)}{n}+ \frac{2\pi k}{n} \right) }, k\in \overline{n-1}
$$
## Examples
Find $(1-i)^{\frac{1}{2}}$ using the principle branch of the logarithm:
$$
(1-i)^{\frac{1}{2}}=e^{ \frac{1}{2}\mathrm{Log}(1-i) }=e^{ \frac{\log(\sqrt{ 2 })-i \frac{\pi}{4}}{2} }=\sqrt[4]{2  }e^{ -i\frac{\pi}{8} }
$$
___
Find $2^{\frac{1}{2}}$ for all possible branches:
There are two branches; 
$$
k=0,~~ 2^{\frac{1}{2}}=e^{ \frac{1}{2}(\log 2+i0) }=\sqrt{ 2 }
$$
$$
 k=1,~ ~ 2^{\frac{1}{2}(\log 2+2\pi i)}=\sqrt{ 2 }e^{ i\pi }=-\sqrt{ 2 }
$$


#Mathematics #Functions 