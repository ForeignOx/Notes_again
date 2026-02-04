## Almost Sure Convergence
Let $X_{n}$ be a [[Sequences|sequence]] of [[Random Variables|random variables]]. $X_{n}\to X$ almost surely if
- There is an event $E$ with $\mathbb{P}(E)=1$
- If $\omega \in E$, then $X_{n}(\omega)\to X(\omega)$ as $n\to \infty$
Another way of wrtiting this is to say that $(X_{n})_{n\in\mathbb{N}}$ converges to $X$ with probability $\hspace{0pt}1$ if 
$$
\mathbb{P}(\left\{ \omega \in \Omega :\middle|: X_{n}(\omega)\to X(\omega)\text{ as }n\to \infty \right\})=1
$$
### Example
This is similar to [[Sure Convergence|sure convergence]], but can be different:
Let $\Upsilon \sim U[0,1]$
Let 
$$
X_{n}=n\cdot \mathbb{1}_{\left\{ \Upsilon \leq \frac{1}{n} \right\}}=\begin{cases}
n & \Upsilon \leq \frac{1}{n} \\
0 & \text{otherwise}
\end{cases}

$$
Suppose $\Upsilon(\omega)>0$, suppose $n> \frac{2}{\Upsilon(\omega)}$, then
$$
\Upsilon(\omega) \not \leq \frac{1}{n} \implies X_{n}(\omega)=0\text{ for }n> \frac{2}{\Upsilon(\omega)}
$$
$$
E=\left\{ \Upsilon>0 \right\}=\left\{ \omega\mid\Upsilon(\omega)>0 \right\}
$$
If $\omega \in E$, then
$$
\lim_{ n \to \infty } X_{n}(\omega)=0
$$
So
$$
\mathbb{P}(\Upsilon \in [a,b])=b-a\implies \mathbb{P}(\Upsilon=0)=0-0=0
$$
So
$$
\mathbb{P}(E)=1
$$
so yeah idk
## Remark
For $\varepsilon>0$, let $A_{n}(\varepsilon)=\left\{ \omega \in \Omega :\middle|: \left| X_{n}(\omega)-X(\omega) \right|>\varepsilon \right\}$ saying that $A_{n}$ converges almost surely is equivalent to saying for every $\varepsilon>0$,
$$
\mathbb{P}(\left\{ A_{n}(\varepsilon)\text{ finitely often} \right\})=1
$$
Linking convergence of random variables to [[Infinitely Often Events|finitely often events]], which is why the [[Borel-Cantelli Lemma|Borel-Cantelli]] lemma is very useful for studying almost sure limits
## Proposition
Suppose $X_{n}\to X$ almost surely, let $f:\mathbb{R}\to \mathbb{R}$ be a continuous function, then $f(X_{n})\to f(x)$ almost surely
### Proof
We know $X_{n}\to X$ almost surely, we want $f(X_{n})\to f(X)$ almost surely
From the almost sure convergence of the $X_{n}$'s there is an event $E$, with $\mathbb{P}(E)=1$ and if $\omega \in E$, then $X_{n}(\omega)\to X(\omega)$ as $n\to \infty$
Recall that if $f$ is continuous and $y_{n}\to y$ (a sequence of numbers), then $f(y_{n})\to f(y)$
We claim that if $\omega \in E$, then $f(X_{n}(\omega))\to f(X(\omega))$ as $n\to \infty$
Since $f$ is continuous, the sequence $f(X_{n}(\omega))$ will converge to $f(X(\omega))$

## Proposition
Let $X_{n}$ and $X$ be random variables, suppose that for every $\varepsilon>0$, it holds that
$$
\sum_{n=1}^{\infty}\mathbb{P}(\left| X_{n}-X \right| >\varepsilon)<\infty
$$
Then $X_{n}\to X$ almost surely
### Example
Let $U_{1},U_{2},U_{3},\dots$ be i.i.d. unifrom $[0,1]$ random variables, then
$$
X_{n}=\min (U_{1},U_{2},\dots,U_{n}),n\geq 1
$$
Then we claim $X_{n}\to 0$ as $n\to \infty$
Suppose $\varepsilon>0$, consider $\mathbb{P}(X_{n}>\varepsilon)$
$$
\left\{ X_{n}>\varepsilon \right\}=\bigcap_{i=1}^{n}\left\{ U_{i}>\varepsilon \right\}
$$
As they are are independent events,
$$
\mathbb{P}(X_{n}>\varepsilon)=\prod_{i=1}^{n}\mathbb{P}(U_{i}>\varepsilon)
$$
$$
\mathbb{P}(U_{i})>\varepsilon=\begin{cases}
1-\varepsilon  & 0<\varepsilon<1 \\
0 & \varepsilon \geq 1
\end{cases}
$$
$$
\implies \mathbb{P}(X_{n}>\varepsilon)=\begin{cases}
(1-\varepsilon)^{n} & 0<\varepsilon<1 \\
0 & \varepsilon \geq 1
\end{cases}
$$
So 
$$
\mathbb{P}(X_{n}>\varepsilon)\leq \sum_{n=1}^{\infty} (1-\varepsilon)^{n}= \frac{1-\varepsilon}{1-(1-\varepsilon)}= \frac{1-\varepsilon}{\varepsilon}
$$
So by the proposition,  $X_{n}\to 0$
### Proof
Let 
$$
E_{m}=\left\{ \left| X_{n}-X \right|\leq \frac{1}{m}\text{ eventually} \right\}
$$
for $m\geq 1$, then
$$
E=\bigcap_{m\geq 1}E_{m}
$$
We claim that if $\omega \in E$, then $X_{n}(\omega)\to X(\omega)$. Let $\varepsilon>0$, choose $m$ such that $\frac{1}{m}<\varepsilon$
We know $\omega \in E_{m}$ so
$$
\left| X_{n}(\omega)-X(\omega) \right| \leq \frac{1}{m}\text{ eventually}
$$
o there is an $N=N(m,\omega)$, such that if $n>N$, then
$$
\left| X_{n}-X \right|\leq \frac{1}{m}
$$
$$
 \left| X_{n}(\omega)-X(\omega) \right| \leq \frac{1}{m}<\varepsilon
$$
So $X_{n}(\omega)\to X(\omega)$ as $n\to \infty$
We claim $\mathbb{P}(E) =1$. Since the $E_{m}$ are decreasing, then
$$
E^{c}_{m}=\left\{ \left| X_{n}-X \right| \leq \frac{1}{m}\text{ eventually} \right\}^{c}
$$
$$
=  \left\{ \left| X_{n} -X\right| > \frac{1}{m}\text{ infinitely often} \right\}
$$
Consider
$$
\sum_{n=1}^{\infty} \mathbb{P}\left( \left| X_{n}-X \right| >\frac{1}{m} \right)<\infty
$$
By Borel-Contelli
$$
\mathbb{P}\left( \left| X_{n}-X \right| > \frac{1}{m}\text{ infinitely often} \right)=0
$$
QED or sommet

