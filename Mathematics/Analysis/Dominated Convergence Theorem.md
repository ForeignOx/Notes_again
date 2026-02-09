# For Borel Functions
## Theorem
Let $f_{n}(x)$ be a [[Sequences of Functions|sequence]] of [[Borel Functions|borel]] [[Functions|functions]] that converges to $f(x)$ as $n\to \infty$ where $\left| f_{n}(x) \right|\leq g(x)$ for all $n\geq 1$, if the [[Lebesgue Integration|Lebesgue integral]] of $g(x)$ is finite, then the sequence of Lebesgue integrals of $f_{n}(x)$ converges to the Lebesgue integral of $f(x)$
# For Random Variables
## Theorem
Let [[Random Variables|random variables]] $X,Y$ and $(X_{n})_{n\in\mathbb{N}}$ be such that for all $\omega \in \Omega$ [[Sure Convergence|$X_{n}(\omega)\to X(\omega)$]]: 

$$
 \left| X_{n}(\omega) \right| \leq Y(\omega)~\forall n\geq 1
$$
Then if [[Expectation|$\mathbb{E}(Y)<\infty$]], then $\mathbb{E}(X_{n})\to \mathbb{E}(X)$ as $n\to\infty$
## Remark
As with the [[Monotone Convergence Theorem|monotone convergence theorem]], the result holds if the assumptions are relaxed to their [[Almost Sure Convergence|almost sure]] versions:
$$
\mathbb{P}(\left\{ \omega \in \Omega :\middle| :\left| X_{n}(\omega) \right| \leq Y(\omega)~\forall n\geq 1 \right\})=1
$$
$$
 \mathbb{P}(\left\{ \omega \in \Omega :\middle|: X_{n}(\omega)\to X(\omega) \right\})=1
$$
## Example
Given a random variable $X\geq 0$ with $\mathbb{E}(X^{2})<\infty$, define $(Y_{k})_{k\in\mathbb{N}}$ via
$$
Y_{k}:=X^{2}\mathbb{1}_{X>k}\equiv \begin{cases}
X^{2} & X>k \\
0 & \text{otherwise}
\end{cases}
$$
Notice that $\left| Y_{k}(\omega) \right|\leq X^{2}(\omega)$ for all $k\geq 1$ and $\omega \in \Omega$, while $Y_{k}\overset{a.s.}\to 0$ and $X^{2}$ is integrable, this implies:
$$
k^{2}\mathbb{P}(X>k)\leq \mathbb{E}(X^{2}\mathbb{1}_{X>k})=\mathbb{E}(Y_{k})\to{0}\text{ as }k\to \infty
$$
In particular, $\mathbb{P}(X>k)$ decays faster than $\frac{1}{k^{2}}$. Notice that this is a better estivate than
$$
\mathbb{P}(X>k)\leq \frac{\mathbb{E}(X^{2})}{k^{2}}
$$
Implied by [[Markov's Inequality|Markov's inequality]]
___
Let $X$ be a random variable, and 
$$
X_{n}=\frac{n\sin\left( \frac{X}{n} \right)}{X(1+X^{2})}
$$
For $n\geq 1$, we want to find $\lim_{ n \to \infty }\mathbb{E}(X_{n})$
The function $\sin y$ satisfies:
$$
\lim_{ y \to 0 }  \frac{\sin(y)}{y}=1
$$
so
$$
X_{n}= \frac{\sin\left( \frac{X}{n} \right)}{\frac{X}{n}(1+X^{2})}
$$
$$
\implies \left| X_{n} \right| =\left| \frac{\sin\left( \frac{X}{n} \right)}{\frac{X}{n}} \right| \left| \frac{1}{1+X^{2}} \right| \leq 1\cdot \frac{1}{1+X^{2}}\leq 1
$$
So $X_{n}\to \frac{1}{1+X^{2}}$ almost surely as $n\to \infty$, and $\left| X_{n} \right|\leq 1$
So by dominated convergence theorem $\mathbb{E}(X_{n})\to \mathbb{E}\left(  \frac{1}{1+X^{2}} \right)$ 
# For Sequences
## Theorem
Let [[Convergence#Sequences of Multiple Indices|$(a_{m,n})_{m,n\in\mathbb{N}}$]], $(a_{m})_{m\in\mathbb{N}}$ and $(b_{m})_{m\in\mathbb{N}}$ be collections of numbers such that for every fixed $m\in\mathbb{N}$, we have
$$
\lim_{ n \to \infty } a_{m,n}=a_{m},~\left| a_{m,n} \right| \leq b_{m},~\sum_{m=1}^{\infty}b_{m}<\infty
$$
Then
$$
\lim_{ n \to \infty } \sum_{m=1}^{\infty}a_{m,n}=\sum_{m=1}^{\infty}a_{m}=\sum_{m=1}^{\infty}\lim_{ n \to \infty } a_{m,n}
$$
### Proof
Fix an arbitrary $\varepsilon>0$. By assumption, choosing $M$ large enough, we can get
$$
\sum_{m=M}^{\infty}\left| a_{m,,n}-a_{m} \right| \leq 2\sum_{m=M}^{\infty}b_{m}< \frac{\varepsilon}{2}
$$
For a finite $M$ with this property, we can find $n$ large enough so that 
$$
\sum_{m=1}^{M}\left| a_{m,n}-a_{m} \right| <\frac{\varepsilon}{2}
$$
Since $\varepsilon>0$ is arbitrary, the result follows

