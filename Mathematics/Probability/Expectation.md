$\mathbb{E}(X)$ is the expected value, or mean of a [[Discrete Random Variables|discrete random variable]] X, and is defined as:
$$
\int X(\omega) \, d\mathbb{P}(\omega) 
$$
A Lebesgue integral.
For a discrete
$$
\mathbb{E}(X)=\sum_{x\in X} x\mathbb{P}(X=x)=\sum_{x\in X}xf(x)
$$
Or for a [[Continuous Random Variables|continuous random variable]],
$$
\mathbb{E}(X)=\int_{-\infty}^{\infty} xf(x) \, dx 
$$
Note expectation does not always exist, since expectation exists finitely, which means that, for discrete $\sum|x|p(x)<\infty$, and for continuous, $\int_{-\infty}^{\infty} |x|f(x) \, dx<\infty$
___
This process is equivalent to having the function:
$$
X:\Omega\to \mathbb{R}\to \mathbb{R}
$$
$$
g_{0}(x)\to \text{random variable}\to \mathbb{R}
$$
$$
g_{0}(x)=g(X(\omega))
$$
To find $\mathbb{E}(f(X))$, where $f(X)$ is a function of $X$, you can use the formula:
$$
\mathbb{E}(f(X))=\sum f(x)\mathbb{P}(X=x)
$$
This is useful for calculating [[Variance|variance]]
This is also useful to show:
$$
\mathbb{E}(aX+b)=\sum (ax+b)\mathbb{P}(X=x)
$$
$$
=a\sum x\mathbb{P}(X=x)+b\sum \mathbb{P}(X=x)
$$
Probabilities sum to one
$$
=a\sum x\mathbb{P}(X=x)+b=a\mathbb{E}(X)+b
$$
$$
\therefore \mathbb{E}(aX+b)=a\mathbb{E}(X)+b
$$
Since integrals are also linear, we can do the same with continuous
## Proof
Let $Y=g(x)$, then by definition,
$$
\mathbb{E}(g(x))=\mathbb{E}(Y)=\sum_{y}y\mathbb{P}(g(X)=y\mid x\in X)
$$
Note that $\mathbb{P}(Y=y)=\mathbb{P}(g(X)=y)$, note that $\mathbb{P}(g(X)-y\mid X=x)=1$, otherwise
$$
\mathbb{P}(Y=y)=\sum_{x:g(x)=y}\mathbb{P}(g(x)=y\mid X=x)\mathbb{P}(X-x)=\sum_{x:g(x)=y}1\times \mathbb{P}(X=x)=\sum_{x:g(x)=y}p(x)
$$
Putting this in $1$:
$$
\mathbb{E}(g(x)\sum_{y}y\left( \sum_{x:g(y)=x} p(x) \right)
$$
Interchanging the order of summation:
$$
=\sum_{x}\sum_{y\in g(\mathbb{R})}yp(x)=\sum_{x\in \mathbb{R}}q(x)|p(x)
$$
___
Consider two [[Discrete Random Variables|discrete random variables]] $X$ and $Y$, where 
$$
p(x,y)=\mathbb{P}(X=x, Y=y)
$$
We can write
$$
\mathbb{E}(X+Y)=\sum^{x}\sum^{y}(x+y)p(x,y)
$$
$$
=\sum^{x}\sum^{y}(xp(x,y)+yp(x,y))
$$
$$
=\sum^{x}x\sum^{y}p(x,y)+\sum^{y}y\sum^{x}p(x,y)
$$
$$
=\mathbb{E}(X)+\mathbb{E}(Y)
$$
Similarly, $\mathbb{E}(X-Y)=\mathbb{E}(X)-\mathbb{E}(Y)$, hence:
$$
\mathbb{E}(X\pm Y)=\mathbb{E}(X)\pm \mathbb{E}(Y)
$$
___
## [[Law of the Unconscious Statistician|LotUS]]
$$
\mathbb{E}(g(X))=\sum_{x} g(x)p(x)
$$
For discrete
$$
\mathbb{E}(g(X))=\int_{-\infty}^{\infty} g(x)f(x) \, dx 
$$
For continuous
### Multivariate
$$
\mathbb{E}(g(X,Y))=\sum_{x}\sum_{y}g(x,y)p(x,y)
$$
For discrete
$$
\mathbb{E}(g(X,Y))=\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x,y)f(x,y) \, dx  \, dy 
$$
### Linearity
$$
\mathbb{E}(\alpha X+\beta Y)=\alpha \mathbb{E}(X)+\beta \mathbb{E}(Y)
$$
For $\alpha,\beta \in\mathbb{R}$
## Monotonicity of Expectation
Let $X:\Omega\to \mathbb{R}$, $a\in\mathbb{R}$ such that $\mathbb{P}(X\geq a)=1$, then $\mathbb{E}(X)\geq a$
### Proof
Define $Y:\Omega\to \mathbb{R}$ as $Y=X-a$, since $\mathbb{P}(X\geq a)=1$, $\mathbb{P}(Y\geq 0)=1$ therefore $\mathbb{E}(Y)\geq0$
Let us assume $X$ is continuous, then 
$$
\mathbb{E}(Y)=\int_{-\infty}^{\infty} xf(x) \, d-\int_{-\infty}^{\infty} af(x)\, dx  =\mathbb{E}(X)-a\underbrace{ \int_{-\infty}^{\infty} f(x) \, dx }_{ =1 } =\mathbb{E}(X)-a
$$
We know $\mathbb{E}(Y)\geq 0$, so $\mathbb{E}(X)-a\geq 0$ so $\mathbb{E}(X)\geq a$

### Example
If $\mathbb{P}(X\geq Y)=1$, then $\mathbb{E}(X)\geq \mathbb{E}(Y)$
#### Proof
Define $Z:=X-Y$

Then $\mathbb{P}(Z\geq 0)=1$, since $\mathbb{P}(X\geq Y)=1$ using the monotonicity of expectation
We also know linearity of independence
$$
\mathbb{E}(Z)=\mathbb{E}(X)-\mathbb{E}(Y)\geq 0
$$
$$
\implies \mathbb{E}(X)\geq \mathbb{E}(Y)
$$
___
$\mathbb{E}(X^{2})\geq (\mathbb{E}(X))^{2}$
#### Proof
Ovserve that
$$
Y=(X-\mathbb{E}(X))^{2}\geq 0
$$
From the monotonicity, we have $\mathbb{E}(Y)\geq 0$, substituting these:
$$
\mathbb{E}(X^{2})-(\mathbb{E}(X))^{2}\geq 0
$$
$$
\implies \mathbb{E}(X^{2})\geq(\mathbb{E}(X))^{2}
$$
# As a [[Linear Differential Operators|Linear Operator]]
We think of $X$ as a random variable which is an analogue to a function we are familiar with in calculus, then integrating the function gives you information about the average, which has the analogue in probability to expectation, which is calculated with a Lebesgue integral
In a linear algebra perspective, we can consider the [[Vectorspaces|vectorspace]] of all random variables, and expectation can be viewed as a linear operator
### Key Properties of Expectation
- Indicators: $\mathbb{E}(\mathbb{1}_{A})=\mathbb{P}(A)$
- Linearity: $\mathbb{E}(aX+bY)=a\mathbb{E}(X)+b\mathbb{E}(Y)$
- Monotonicity: if $X\leq Y$, then $\mathbb{E}(X)\leq \mathbb{E}(Y)$
- Monotone Convergence: Suppose $X_{n}$ are random variables such that $0\leq X_{n}\leq X_{n+1}$ for every $n$, suppose $\lim_{ n \to \infty }X_{n}=X$, then
$$
\mathbb{E}(X)=\lim_{ n \to \infty } \mathbb{E}(X_{n})
$$
It is possible to prove that these uniqely determine $\mathbb{E}$
### Determining Expectation by Approximation
Let $x\geq 0$ be a real number. Define
$$
x_{n}=\lfloor 2^{n}x \rfloor 2^{-n}
$$
Consider the set
$$
D_{n}=\left\{ a_{0}+\frac{a_{1}}{2}+\frac{a_{2}}{2^{2}}+\dots+ \frac{a_{n}}{2^{n}}:\middle|:a_{0}\in \mathbb{Z},a_{1},\dots,a_{n}\in \left\{ 0,1 \right\} \right\}
$$
Then $x_{n}\in D_{n}$ for every $n$. To see this, simply write $x$ in binary:
$$
x=b_{0}+\frac{b_{1}}{2}+\frac{b_{2}}{2^{2}}+\dots
$$
Where $b_{0}\in\mathbb{Z}$ is non-negative and $b_{k}\in\left\{ 0,1 \right\}\forall k\geq 1$, then
$$
x_{n}=b_{0}+\frac{b_{1}}{2}+\frac{b_{2}}{2^{2}}+\dots+\frac{b_{n}}{2^{n}}\in D_{n}
$$
It holds that $0\leq x_{n}\leq x_{n+1}$ and $x_{n}\to x$ as $n\to \infty$
#### Proof
Since $x\geq 0$, we have $x_{n}\geq 0$, we can see that
$$
x_{n}=b_{0}+\frac{b_{1}}{2}+\dots+\frac{b_{n}}{2^{n}}\leq b_{0}+\frac{b_{1}}{2}+\dots+\frac{b_{n}}{2^{n}}+\frac{b_{n+1}}{2^{n+1}}=x_{n+1}
$$
Next, note that $y-1\leq \lfloor  y \rfloor\leq y$ for every $y\in\mathbb{R}$
Therefore, $2^{n}x-1\leq \lfloor 2^{n}x \rfloor\leq 2^{n}x$, multiplying this by $2^{-n}$ shows that
$$
x-2^{-n}\leq x_{n}\leq x
$$
Which implies that
$$
\left| x_{n}-x \right| \leq 2^{-n}
$$
Therefore $x_{n}\to x$ as $n\to \infty$ by the [[Squeeze Theorem|squeeze theorem]]
___
Suppose $X$ is a random variable such that $X\geq 0$. Define
$$
X_{n}=\lfloor 2^{n}X \rfloor 2^{-n}
$$
From above, $0\leq X_{n}\leq X_{n+1}$ and $X_{n}\to X$ as $n\to \infty$
Now notice that $X_{n}$ is a discrete random variable as it takes values in the set $D_{n}$. Therefore, $\mathbb{E}(X_{n})$ is well defined by our axioms. By the monotone convergece property of expectation, we simply define
$$
\mathbb{E}(X)=\lim_{ n \to \infty } \mathbb{E}(X_{n})
$$
We say the non-negative random variable $X$ is integravle if $\mathbb{E}(X)<\infty$
For general $X$ we decompose $X^{+}$ to be $\max\left\{ X,0 \right\}$ and $X^{-}=\max\left\{ -X,0 \right\}$ then define 
$$
X=X^{+}-X^{-}
$$
We say $X$ is integrable if both $\mathbb{E}(X^{+}),\mathbb{E}(X^{-})<\infty$, in this case, we define
$$
\mathbb{E}(X)=\mathbb{E}(X^{+})-\mathbb{E}(X^{-})
$$
Note that $\mathbb{E}(X)$ depends only on the law of $X$
#### Examples
Let $X\equiv 1$, then we want to show that $\mathbb{E}(X)=1$
We know
$$
\mathbb{1}_{\Omega}\equiv1
$$
$$
\implies \mathbb{E}(1) = \mathbb{E}(\mathbb{1}_{\Omega})=\mathbb{P}(\Omega)=1
$$
___
Show $\mathbb{E}(\mathbb{E}(X))=\mathbb{E}(X)$, if $\mathbb{E}(X)=a$, is a scalar, then setting $X=a\cdot 1$, then
$$
\mathbb{E}(X)=a\mathbb{E}(1)=a
$$
So $\mathbb{E}(\mathbb{E}(X))=\mathbb{E}(X)$
___
Show $\left| \mathbb{E}(X) \right| \leq \mathbb{E}(\left| X \right| )$
$$
-\left| X \right| \leq X\leq \left|  X \right| 
$$
$$
\implies -\mathbb{E}(X)\leq \mathbb{E}(X)\leq \mathbb{E}(\left| X \right| ) 
$$
$$
 \iff \left| \mathbb{E}(X) \right| \leq \mathbb{E}(\left| X \right| )
$$
___
Let $X$ be a random variable such that $\mathbb{E}(\left| X \right|)<\infty$. Then $\mathbb{P}(\left| X \right|=\infty)=0$
We have that 
$$
\left\{ \left| X \right| \right\}=\bigcap_{n=1}^{\infty}\left\{ \left| X \right|>n \right\}
$$
And the events $\left\{ \left| X \right|>n \right\}$ are [[Monotone Events|monotone decreasing]]. Therefore
$$
\mathbb{P}(\left| X \right| =\infty)=\lim_{ n \to \infty } \mathbb{P}(\left| X \right| >n)
$$
By [[Markov's Inequality|Markov's inequality]]
___
We also have
$$
\mathbb{E}(\left| X \right| )^{2}\leq \mathbb{E}(X^{2})
$$
This follows from the fact that for any random variable $Y$, $\mathbb{V}\mathrm{ar}(Y)\geq 0$, since $\mathbb{V}\mathrm{ar}(Y)=\mathbb{E}(Y^{2})-\mathbb{E}(Y)^{2}$, we infer $\mathbb{E}(Y)^{2}\leq \mathbb{E}(Y^{2})$, applying this to $Y=\left| X \right|$, we get our result
___
Let $\underline{v}_{1},\underline{v}_{2},\dots,\underline{v}_{n}\in \mathbb{R}^{d}$ be [[Vectors|vectors]], there is a choice of signs $\sigma_{1},\sigma_{2},\dots,\sigma_{n}\in\left\{ \pm 1 \right\}$ such that the [[Norms|norm]]
$$
\left\lvert  \left\lvert  \sum_{i=1}^{\infty}\sigma_{i}\underline{v}_{i}  \right\rvert  \right\rvert ^{2}\geq \sum_{i=1}^{n}\lvert \lvert \underline{v}_{i} \rvert \rvert  ^{2}
$$
The idea is to choose the signs at random! Let $X_{1},\dots,X_{n}$ be independent random signs, that is,
$$
\mathbb{P}(X_{k}=-1)=\mathbb{P}(X_{k}=1)=\frac{1}{2}~\forall k
$$
Let $S=\sum_{i=1}^{n}X_{i}\underline{v}_{i}$. We will compue $\mathbb{E}(\lvert \lvert  S \rvert \rvert^{2})$, firstly
$$
\lvert \lvert S \rvert \rvert ^{2}=\left< S,S \right> =\sum_{i,j=1}^{n}X_{i}X_{j}\left< \underline{v}_{i},\underline{v}_{j} \right> 
$$
Taking expectations gives
$$
\mathbb{E}(\lvert \lvert S \rvert \rvert ^{2})=\sum_{i,j=1}^{n}\mathbb{E}(X_{i},X_{j})\left< \underline{v}_{i},\underline{v}_{j} \right> 
$$
If $i=j$, then $X_{i}X_{j}=X_{i}^{2}=1$, so $\mathbb{E}(X_{i}^{2})=1$, when $i\neq j$, by [[Independence|independence]], $\mathbb{E}(X_{i}X_{j})=\mathbb{E}(X_{i})\mathbb{E}(X_{j})=0$, therefore
$$
\mathbb{E}(\lvert \lvert S \rvert \rvert ^{2})=\sum_{i=1}^{n}\left< \underline{v}_{i},\underline{v}_{i} \right> =\sum_{i=1}^{n}\lvert \lvert \underline{v}_{i} \rvert \rvert ^{2}
$$
Hence there must exist some choice of signs such that $\lvert \lvert  S \rvert \rvert\geq \mathbb{E}(\lvert \lvert  S \rvert \rvert^{2})$ as if $\sigma_{1},\dots,\sigma_{n}$ denotes such a choice, then the claim follows



#Mathematics #Statistics #Probability
