It is rather difficult to get an intuition about [[Convergence|convergence]] of [[Random Variables|random variables]] in a [[Probability Spaces|probability space]] $(\Omega,\mathfrak{F},\mathbb{P})$, but this is an interpretation
A random variable, say $X$ is a measurable [[Functions|map]] $X:\Omega\to \mathbb{R}$. We can thus think of $X(\omega)$ as the opinion expressed by the individual $\omega \in\Omega$. A [[Sequences|sequence]] $(X_{n})_{n\in\mathbb{N}}$ of random variables then is a datavase, where for each fixed $n\in\mathbb{N}$, the values $X_{n}(\omega),\omega \in\Omega$ record the individual answers to a single question at time $n$
Under the assumption that all individuals $\omega \in \Omega$ are immortal, the question of convergence $X_{n}\to X$ as $n\to \infty$ then boils down to finding out to what degree the profile $(X_{n}(\omega))_{\omega \in \Omega}$ at large $n$ is similar to the limiting profile $(X(\omega))_{\omega \in \Omega}$, this method is known as [[Sure Convergence|sure convergence]]
___
One can describe this similarly either at the level of individuals $\omega$, or at the level of the whole population $\Omega$. In the first case, one fixes $\omega \in \Omega$ and studies the large $n$ vahaviour of the sequence $(X_{n}(\omega))_{n\in\mathbb{N}}$ of real numbers
In particular, one determines whether the convergence $X_{n}(\omega)\to X(\omega)$ takes place for the fixed individual $\omega \in \Omega$ 
If the set
$$
\left\{ \omega \in \Omega :\middle|:X_{n}(\omega)\to X(\omega)\text{ as }n\to \infty \right\}
$$
has probability one, we say that $X_{n}$ converges to $X$ with probability one (or [[Almost Sure Convergence|converges almost surely]]). The individual approach is very important in computer science
___
Alternatively, one can prefer the population level view, and for each fixed $n\in\mathbb{N}$ quantify to what extent the profile $(X_{n}(\omega))_{\omega \in \Omega}$ at time $n$ differs from the limiting profile $(X(\omega))_{\omega \in \Omega}$
Two popular choices are as follows;
One can fix $\varepsilon>0$ and $n\in\mathbb{N}$ an evaluate the [[Probabilities|probability]]
$$
\mathbb{P}(\left| X_{n}-X \right| >\varepsilon)\equiv \mathbb{P}(\left\{ \omega \in \Omega :\middle|:~ \left| X_{n}(\omega)-X(\omega) \right| >\varepsilon \right\})
$$
If for each fixed $\varepsilon>0$, this probability vanishes asymtotically, as $n\to \infty$, one speaks of [[Convergence in Probability|convergence in probability]]
___
Another popular choice is, for fixed $r>0$, to describe the discrepancy between $X_{n}$ and $X$ through the value of the expectation
$$
\mathbb{E}(\left| X_{n}-X \right| ^{r})\equiv \mathbb{E}(\left| X_{n}(\omega)-X(\omega) \right| ^{r})
$$
If, for some $r>0$, this expectation goes to zero as $n\to \infty$, one says that $X_{n}$ [[Convergence in Lr|converges to $X$ in $L^{r}$]]. The case of $r\geq 1$ is of special interest, as the corresponding space of random variables satisfying, in particular, $\mathbb{E}(\left| X \right|^{r}<\infty)$ has additional useful properties
## Comparisons Between methods
![[Convergence of Random Variables 2026-02-03 13.16.30.excalidraw]]
### Theorem $X_{n}\overset{p}\to X \centernot\implies X_{n}\overset{a.s.}\to X,X_{n}\overset{L^{r }}\to X\centernot\implies X_{n}\overset{a.s.}\to X$
We have that neither [[Convergence in Probability|convergence in probability]] nor [[Convergence in Lr|convergence in $L^{r}$]] imply almost sure convergence
#### Proof
For $n\geq 1$, put $m=\lfloor \log_{2} n \rfloor$ i.e. let $m\geq 0$ be such that $2^{m}\leq n<2^{m+1}$. Consider the events
$$
A_{n}=\left[  \frac{n-2^{m}}{2^{m}}, \frac{n+1-2^{m}}{2^{m}} \right]\subseteq [0,1]
$$
In the [[Canonical Probability Space|canonical probability space]], and let $X_{n}(\omega)=\mathbb{1}_{A_{n}}(\omega)$, since
$$
\mathbb{P}(\left| \mathbb{1}_{A_{n}} \right| >0)=\mathbb{P}(A_{n})\equiv \mathbb{E}(\mathbb{1}_{A_{n}})=2^{-\lfloor \log_{2}n \rfloor }< \frac{2}{n}\to 0
$$
As $n\to \infty$, the sequence $X_{n}$ converges to $X\equiv 0$ in probability and in $L^{r}$ for each fixed $r>0$
However
$$
\left\{ \omega \in \Omega\mid X_{n}(\omega)\to X\equiv0\text{ as }n\to \infty \right\}=\emptyset
$$
I.e. there is no point $\omega \in \Omega$ for which the sequence $X_{n}(\omega)\in\left\{ 0,1 \right\}$ converges to $X(\omega)=0$; in fact, for each $\omega \in\Omega$, there real sequence $X_{n}(\omega)$ never stops jumping between $0$ and $1$
### Theorem $X_{n}\overset{a.s.}\to X\implies X_{n}\overset{p}\to X$
If $X_{n}\to X$ almost surely, then $X_{n}\overset{p}\to X$
#### Proof
We know there is an event $E$ with $\mathbb{P}(E)=1$ such that if $\omega \in E$, then $X_{n}(\omega)\to X(\omega)$
Picking $\varepsilon>0$, suppose $\omega \in E$, there is a random integer $N=N(\omega)$ such that
$$
\left| X_{n}-X \right| <\varepsilon \text{ if }n>N
$$
So
$$
\mathbb{P}(N<\infty)=1
$$
Because $N<\infty$ if $\omega \in E$, as $\left\{ N<\infty \right\}\supseteq E$
Consider $\mathbb{P}(\left| X_{n}-X \right|>\varepsilon)$, we want this to go to 0
$$
\mathbb{P}(\left| X_{n}-X \right|>\varepsilon)=\mathbb{P}(\left| X_{n}-X \right| >\varepsilon,n>N)+\mathbb{P}(\left| X_{n}-X \right| >\varepsilon,n\leq N)
$$
By the [[Partition Theorem|partition theorem]]
$$
\left\{ \left| X_{n}-X \right| >\varepsilon,n>N \right\}=\emptyset\implies \mathbb{P}(\left| X_{n}-X \right| >\varepsilon)=\mathbb{P}(\left| X_{n}-X \right| >\varepsilon,N\geq n) \leq \mathbb{P}(N\geq n)
$$
$$
0\leq\lim_{ n \to \infty } \mathbb{P}(\left| X_{n}-X \right| >\varepsilon)\leq \lim_{ n \to \infty } \mathbb{P}(N\geq n)=\mathbb{P}(N=\infty)=0
$$
___
Alternate proof:
For simplicity let $(X_{n})_{n\in\mathbb{N}}$ be such that $X_{n}\overset{a.s.}\to 0$ as $n\to\infty$. THen the variables $Z_{n}:= \frac{\left| X_{n} \right|}{1+\left| X_{n} \right|}$ which are uniformly bounded and, by the bounded convergence theorem, $Z_{n}\overset{L^{1 }}\to 0$
As a result, $Z_{n}\overset{p}\to 0$, and it is straightforward to show that then $X_{n}\overset{p}\to 0$ also
### Theorem $X_{n}\overset{a.s.}\to X \centernot\implies X_{n}\overset{L^{r }}\to X$
Almost sure convergence doesn't imply convergence in $L^{r}$
#### Proof
For every $n\geq 1$, consider the variable
$$
X_{n}(\omega):= e^{ n }\mathbb{1}_{\left[ 0,\frac{1}{n} \right]}(\omega)\equiv \begin{cases}
e^{ n } & 0\leq\omega \leq \frac{1}{n} \\
0 & \omega>\frac{1}{n}
\end{cases}
$$
in the canonical probability space. Clearly, $X_{n}\overset{a.s.}\to 0$ as $n\to \infty$, however, given $r>0$, we have
$$
\mathbb{E}(\left| X_{n} \right| ^{r})= \frac{e^{ nr }}{n}\to \infty
$$
As $n\to \infty$, i.e. $X_{n} \not\overset{L^{r }}\to 0$, giving what we want
### Theorem $X_{n}\overset{a.s.}\to X\implies X_{n}\overset{L^{1 }}\to X$ for $X_{n}$ Bounded
Let $X,Y,(X_{n})_{n\in\mathbb{N}}$ be random variables such that $X_{n}\overset{a.s.}\to X$ and $\mathbb{P}(\left| X_{n} \right|\leq Y~\forall n\geq 1)=1$, where $\mathbb{E}(Y)<\infty$, then $X_{n}\overset{L^{1 }}\to X$
#### Proof
Fix arbitrary $\omega$ such that $\left| X_{n}(\omega) \right|\leq Y(\omega)$ for all $n\geq 1$, and $X_{n}(\omega)\to X(\omega)$ as $n\to\infty$. Then $\left| X(\omega) \right|\leq Y(\omega)$
Denote $Z_{n}:=\left| X_{n}-X \right|$, we have
$$
\mathbb{P}(\left\{ \omega \in \Omega :\middle|: \left| Z_{n}(\omega) \right| \leq 2Y(\omega)~\forall n\geq 1 \right\})=1
$$
$$
 \mathbb{P}(\left\{ \omega \in \Omega :\middle|:Z_{n}(\omega)\to o \right\})=1
$$
As $\mathbb{E}(Y)<\infty$, the almost sure version of [[Dominated Convergence Theorem|dominated convergence theorem]] implies that $\mathbb{E}(Z_{n})\to 0$ as $n\to\infty$, equivalently, $X_{n}\overset{L^{1 }}\to Z$
### Theorem $X_{n}\overset{p}\to X\centernot\implies X_{n}\overset{L^{r }}\to X$
Convergence in probability doesn't imply convergence in $L^{r}$
#### Proof
Consier random variables $X_{n}$ where
$$
X_{n}=\begin{cases}
a_{n}\neq 0 &\text{with probability }p_{n} \\
0 &  \text{with probability }1-p_{n} 
\end{cases}
$$
$$
\mathbb{P}(\left| x_{n} \right| >\varepsilon)=\mathbb{P}(X_{n}=a_{n})=p_{n}
$$
Then $X_{n}\to 0$ iff $p_{n}\to 0$
$$
\mathbb{E}(\left| X_{n} \right| ^{r})=\left| a_{n} \right| ^{r}p_{n}=\left( n^{\frac{2}{r}} \right)^{r} \frac{1}{n}=n
$$
Take $p_{n}=\frac{1}{n}\to 0$, and $a_{n}=n^{\frac{2}{r}}$, then
$$
\mathbb{E}(\left| X_{n} \right| ^{r})\not \to 0
$$
So $X_{n}\not\to 0$ in $L^{r}$, but it does in probability
So convergence in probability does not imply convergence in $L^{r}$
### Theorem $X_{n}\overset{L^{r }}\to X\implies X_{n}\overset{p}\to X$
If $X_{n}\to X$ in $L^{r}$, then $X_{n}\to X$ in probability
#### Proof
We know 
$$
\mathbb{E}(\left| X_{n}-X \right| ^{r})\to 0\text{ as }n\to \infty
$$
We want
$$
\mathbb{P}(\left| X_{n}-X \right| >\varepsilon)\to 0\text{ as }n\to \infty
$$
So we relate $\mathbb{P}(A)$ to $\mathbb{E}(\cdot)$
If event $A$ imples event $B$, then
$$
\mathbb{P}(A)\leq \mathbb{P}(B)
$$
$$
0\leq \mathbb{P}(\left| X_{n}-X \right| >\varepsilon)\leq \mathbb{P}(\left| X_{n}-X \right| ^{r}>\varepsilon^{r})\geq  \frac{\mathbb{E}(\left| X_{n}-X \right| ^{r})}{\varepsilon^{r}}
$$
Since $\mathbb{E}(\left| X_{n}-X \right|^{r})\to 0$ by the squeeze theorem,
$$
0\leq \lim_{ n \to \infty } \mathbb{P}(\left| X_{n}-X \right| >\varepsilon)\leq \lim_{ n \to \infty }  \frac{\mathbb{E}(\left| X_{n}-X \right| ^{r})}{\varepsilon^{r}}
$$
So $\lim_{ n \to \infty }\mathbb{P}(\left| X_{n}-X \right|>\varepsilon)=0$
This means that $\mathbb{P}(X_{n}\text{ converges in probability})\geq \mathbb{P}(X_{n}\text{ converges in }L^{r})$ 
### Therem $X_{n}\overset{p}\to X\implies X_{n}\overset{L^{1 }}\to X$ for $X_{n}$ Bounded
Let random variables $(X_{n})_{n\in\mathbb{N}}$ be bounded, $\left| X_{n}(\omega) \right|\leq M$ for a constant $M<\infty$, while $X_{n}\overset{p}\to X$ as $n\to\infty$, then $X_{n}\overset{L^{1 }}\to X$
### Proof
The limit is also bounded, $\left| X(\omega) \right|\leq M$, and
$$
\mathbb{E}(\left| X_{n}-X \right| )\leq\delta \mathbb{P}(\left| X_{n}-X \right| \leq \delta)+2M\mathbb{P}(\left| X_{n}-X \right| >\delta)
$$
For each $\delta>0$
As $X_{n}\overset{p}\to X$, the RHS above is smaller than $2\delta$ for all $n$ large enough, equivalently $X_{n}\overset{L^{1 }}\to X$ as $n\to\infty$