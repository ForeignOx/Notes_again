# Real Functions
## Definition
A [[Sequences of Functions|sequence of functions]] $f_{n}$ [[Convergence|converges]] to a [[Functions|function]], $f$ on an [[Intervals|interval]] $I$, if
$$
\forall\varepsilon>0\exists N>0:\forall x\in I\forall n\geq N,\left| f_{n}(x)-f(x) \right|<\varepsilon 
$$
The difference between this and [[Pointwise Convergence|pointwise limit]] is that the for all $x$ has been brought inside, so $N$ cannot depend on $x$
If you have uniform convergence, you have pointwise convergence, uniform convergence is stricter
![[Uniform Convergence 2025-02-24 16.27.18.excalidraw]]
So $f_{n}(x)$ is uniformly convergent if for all $n\geq N$ all $f_{n}(x)$ lie in a strip of $f(x)\pm\varepsilon$ 
The contradiction to this definition, $f_{n}(x)$ doesn't converge uniformly if:
$$
\exists\varepsilon>0:\forall N>0\exists n\geq N:\exists x=x_{n}\in I:\left| f_{n}(x_{n})-f(x) \right|\geq\varepsilon 
$$
## Examples
Consider $f_{n}(x)=x^{n}$ on $I=[0,1]$, we have already shown that it does have pointwise convergence to
$$
f(x)=\begin{cases}
0&x\in [0,1)\\1&x=1
\end{cases}
$$
But we will show that it doesn't converge uniformly
Pick $x_{n}=\sqrt[n]{ \frac{1}{2} }$ (note $x_{n}\to 1$ as $n\to \infty$)
Then 
$$
f_{n}(x_{n})=\left( \sqrt[n]{ \frac{1}{2} } \right)^{n}=\frac{1}{2}
$$
So
$$
\left| f(x_{n})-f_{n}(x_{n}) \right| =\left| 0-\frac{1}{2} \right| =\frac{1}{2}
$$
So we can pick $\varepsilon=\frac{1}{2}$, so there exists an epsilon such that for all $N$ there exist $n\geq N$ and some $x$ with $\left| f_{n}(x_{n})-f(x_{n}) \right|\geq\varepsilon$ which is what we want
Instead restrict in a region from $[0,r]$ with $r<1$
We claim that $x^{n}$ converes uniformly to $\hspace{0pt}0$ on $[0,1]$ for any $r<1$, indeed
$$
\left| f_{n}(x)-f(x) \right| =\left| x^{n}-0 \right| =\left| x^{n} \right| \leq r^{n}\forall x\in [0,1]
$$
And $r^{n}\to 0$ as $n\to \infty$ independently of $x$, so given $\varepsilon>0$, find $N$ such that $r^{n}<\varepsilon \forall n\geq N$, meaning yeah
___
Consider
$$
f_{n}(x)=3x^{3}+ \frac{\cos(nx)}{n}
$$
This will have pointwise limit $f(x)=3x^{3}$ since 
$$
0\leq\left|  \frac{\cos(nx)}{n} \right|\leq \frac{1}{n} 
$$
So by [[Squeeze Theorem|squeezing]], $\lim_{ n \to \infty } \frac{\cos(nx)}{n}=0$
Does it converge uniformly on $\mathbb{R}$?
$$
\left| f_{n}(x)-f(x) \right|=\left| \frac{\cos(nx)}{n} \right| \leq \frac{1}{n}
$$
And $\frac{1}{n}$ is independent of $x$, and tends to $\hspace{0pt}0$, so...
Pick $\varepsilon>0$, let $N=\frac{1}{\varepsilon}$, then $\left| f_{n}(x)-f(x) \right|<\frac{1}{n}\leq \frac{1}{N}=\varepsilon$ for $n\geq N$
## Uniform Convergence on Compact [[Subsets|Subsets]] (Subintervals)
This is more strict than pointwise convergence, but less strict than uniform convergence, it is the goldilocks
If $f_{n}:I\to \mathbb{R}$ tends to $f$ uniformly in compact subintervals if $f_{n}\to f$ on all $[a,b]\subset I$
## Lemma (Criterion)
- If $\left| f(x)-f_{n}(x) \right|\leq a_{n}$ for all $x\in I$ with $\lim_{ n \to \infty }a_{n}=0$, then uniform convergence on $I$ (where $a_{n}$ must not depend on $x$)
- If $\exists\varepsilon>0$ and a sequence $x_{n}\in I$ such that for all $n$ sufficiently large, $\left| f(x)-f_{n}(x_{n}) \right|\geq\varepsilon$, then convergence is not uniform on $I$
## Theorem
Assume $f_{n}\to f$ uniformly on compact subsets on $I$, with $f_{n}$ [[Continuity|continuous]], then $f$ will be continuous on $I$
### Proof
We have $f_{n}\to f$ uniformly, so pick $\varepsilon>0$, so
$$
\exists N:\forall x\in I,\forall n\geq N,\left| f(x)-f_{n}(x) \right| <\varepsilon
$$
So we can take $N$, then, since $f_{n}(x)$ is continuous, given $c\in I$ we can find $\delta>0$ such that 
$$
|f_{n}(x)-f(c)|<\varepsilon \forall x:\left| x-c \right|<\delta
$$
We need to look at $\left| f(x)-f(c) \right|$ and need this to be smol. Due to convergence, $f$ is close to $f_{N}$, so
$$
\left| f(x)-f(c) \right| =\left| f(x)-f_{N}(x)+f_{N}(x)-f(c) \right| 
$$
But $f_{N}(x)$ is close to $f_{N}(c)$, and $f_{N}(c)$ is close to $f(c)$ by uniform convergence, so we have:
$$
\left| f(x)-f(c) \right| =\left| f(x)-f_{N}(x)+f_{N}(x)-f_{N}(c)+f_{N}(c)-f(c) \right|
$$
$$
 \leq \underbrace{ \left| f(x)-f_{N}(x) \right| }_{ <\varepsilon } +\underbrace{ \left| f_{N}(x)-f_{N}(c) \right| }_{ <\varepsilon } +\underbrace{  \left| f_{N}(c)-f(c) \right|  }_{ <\varepsilon }<3\varepsilon
$$
The first from our definition of uniform convergence, second from continuity, third from definition of uniform convergence, so letting each $\varepsilon=\frac{\varepsilon}{3}$, we get our result
We can in fact do this on only compact subsets of $I$ by taking $c\in I$, finding an interval $[a,b]$ containing $c$, on $[a,b]$ we have uniform convergence, so we have continuity of $f$ for $x\in[a,b]$ 
## Theorem
Say we have a sequence of functions $f_{n}:I\to \mathbb{R}$ that are all [[Differentiation|differentiable]] with $f'(x)$ continuous, assume $f_{n}\to f$ pointwise and $f_{n}'$ converges uniformly (in compact subsets) to some function $g(x)$, then $f(x)$ is differentiable on $I$ with $f'(x)=g(x)=\lim_{ n \to \infty }f_{n}'(x)$ 
### Proof
laterz
## Example
Consider $f_{n}(x)=\frac{\sin(nx)}{n}$, since $\sin(nx)$ is bounded in $[-1,1]$, this tends $\hspace{0pt}0$, uniformly on $\mathbb{R}$;
$$
\left| f_{n}(x)-f(x) \right| =\left| \frac{\sin(nx)}{n} \right| \leq \frac{1}{n}
$$
And $\frac{1}{n}$ is independent of $x$, so we can find an $\varepsilon$ and we have convergence :)
So the limit function is continuous which is good since it is 0
But 
$$
f_{n}'(x)=\frac{n\cos(nx)}{n}=\cos(nx)
$$
Which doesn't even converge pointwise (for most $x$)
# Complex Functions
## Definition
Let $D\subseteq C$ be a given set and let $\left\{ f_{n} \right\}:D\to \mathbb{C}$ be a sequence of functions. We say that $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ converges uniformly to the limit function $f:D\to \mathbb{C}$ on $D$ if we have that
$$
\sup_{z\in  D}\left| f_{n}(z)-f(z) \right| \to 0
$$
In other words, for any $\varepsilon>0$ there exists $N(\varepsilon)\in\mathbb{N}$ such that if $n>N(\varepsilon)$
$$
\left| f_{n}(z)-f(z) \right| <\varepsilon~\forall z\in  D
$$
Note that here $N(\varepsilon)$ does not depend on the specific choice of $z\in D$ - the same $N$ works for all of them
___
We say that the series $\sum_{n=1}^{\infty}f_{n}(z)$ converges uniformly to $S:D\to \mathbb{C}$ on $D$ if the sequence of functions $\left\{ S_{N} \right\}_{N\in\mathbb{N}}:D\to \mathbb{C}$ defined by
$$
S_{N}(z)=\sum_{n=1}^{N}f_{n}(z)
$$
Converges uniformly to the function $S$ on $D$
## Theorem: Uniform limits of continuous functions are continuous
Let $\left\{ f_{n} \right\}_{n\in\mathbb{N}}:D\to \mathbb{C}$ be a sequence of continuous functions that converges uniformly to $f$ on $D$. Then $f$ is continuous on $D$
## Lemma: Criteria for Uniform Convergence and Lack of Uniform Convergence for Sequences
Let $\left\{ f_{n} \right\}_{n\in\mathbb{N}}:D\to \mathbb{C}$ be a sequence of functions that converges pointwise to a limit function $f$ on $D$
- If there exists a non-negative sequence of real numbers $\left\{ s_{n} \right\}_{n\in\mathbb{N}}$ that converges to zero and $n_{0}\in\mathbb{N}$ (independent of $z$) such that for all $n\geq n_{0}$
$$
\left| f_{n}(z)-f(z) \right| \leq s_{n}~\forall z\in  D
$$
    Then the sequence of functions $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ converges uniformly to $f$ on $D$
- If there exists a non-negative sequence of real numbers $\left\{ s_{n} \right\}_{n\in\mathbb{N}}$ that converges to $c>0$, $n_{0}\in \mathbb{N}$ (independent of $z$), and a sequence $\left\{ z_{n} \right\}_{n\in\mathbb{N}}\subset  D$ such that for all $n\geq n_{0}$
$$
\left| f_{n}(z_{n})-f(z_{n}) \right|\geq _{n} 
$$
    Then the sequence of functions $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ does not converge uniformly to $f$ on $D$
### Proof
For the first part, since $\left\{ s_{n} \right\}_{n\in\mathbb{N}}$ is non-negative and independent of $z$, we have that for all $n\geq n_{0}$,
$$
0\leq \sup_{z\in  D}\left| f_{n}(z)-f(z) \right|\leq s_{n}
$$
Using the [[Squeeze Theorem|squeeze theorem]] we conclude that
$$
\lim_{ n \to \infty } \sup_{z\in  D} \left| f_{n}(z)-f(z) \right| =0
$$
Which is the desired result.


## Remark
In many cases we have that $n_{0}=1$ in the conditions for the above lemma. A simpleer version of the second  part of the lemma is:
If there exists $c>0$ and a sequence $\left\{ z_{n} \right\}_{n\in\mathbb{N}}\subset D$ such that $\forall n\in\mathbb{N}$
$$
\left| f_{n}(z_{n})-f(z_{n})\geq c \right| 
$$
Then the sequennce of functions $\left\{ f_{n} \right\}_{n\in\mathbb{N}}$ does not converge uniformly to $f$ on $D$
## Example
Show that the sequence of functions
$$
f_{n}(z)=e^{ z }+\frac{1}{n}
$$
Converges to $e^{ z }$ uniformly on $\mathbb{C}$
$$
\left| f_{n}(z)-f(z) \right| =\frac{1}{n}=s_{n}
$$
$s_{n}>0$ for all $n$, and $s_{n}$ is independent of $z$ and $s_{n}\to 0$, so by our theorem, this converges uniformly
___
Show that for any $R>0$, the sequence of functions $f_{n}(z)=e^{ z }+\frac{z}{n}$ converges to $e^{ z }$ uniformly on $B_{R}(0)$, does this converge uniformly on $\mathbb{C}$?
$$
\left| f_{n}(z)-f(z) \right| =\left| \frac{z}{n} \right| =\frac{\left| z \right| }{n}
$$
If $z\in B_{R}(0)$, then
$$
\left| f_{n}(z)-f(z) \right| \leq \frac{R}{n}=s_{n}(R)
$$
$s_{n}(R)>0$, it is independent of $z$ and $s_{n}(R)\to 0$, so nby our theorem, $f_{n}$ converges uniformly on $B_{R}(0)$
It does not necessary bound $z$ uniformly on $\mathbb{C}$, indeed, choosing $z_{n}=n$, we see that
$$
\left| f_{n}(z_{n})-e^{ z_{n} } \right| = \frac{\left| z_{n} \right| }{n}=1
$$
Which shows that the convergence is not uniform according to the sequence part of the above lemma
By choosing $s_{n}=1$
