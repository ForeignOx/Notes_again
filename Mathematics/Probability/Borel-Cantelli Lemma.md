Let $A_{n},n\geq 1$ be a [[Sequences|sequence]] of [[Events|events]] from some [[Probability Spaces|probability space]] $(\Omega,\mathfrak{F},\mathbb{P})$. One is often interested in finding out how many of the events $A_{n}$ occur. We can do this by considering [[Infinitely Often Events|infinitely often events]]
## Lemma
If $\sum_{n=1}^{\infty}\mathbb{P}(A_{n})<\infty$, then
$$
\mathbb{P}(A_{n}\text{ infinitely often})=0
$$
Suppose $A_{n}$ are mutually [[Independence|independent]], if $\sum_{n=1}^{\infty}\mathbb{P}(A_{n})=\infty$, then
$$
\mathbb{P}(A_{n}\text{ infinitely often})=1
$$
## Proof
For every $n\geq 1$, let $B_{n}:=\bigcup _{k=n}^{\infty}A_{k}$ be the event that at least one of $A_{k}$ with $k\geq n$ occurs. As $A\subset B_{n}$ for all $n\geq 1$, we have
$$
0\leq \mathbb{P}(A)\leq \mathbb{P}(B_{n})\leq \sum_{k=n}^{\infty}\mathbb{P}(A_{k})\to 0
$$
As $n\to \infty$  whenever $\sum_{k=n}^{\infty}\mathbb{P}(A_{k})<\infty$. Consequently $\mathbb{P}(A)=0$
For the second part, the event $A^{c}=\left\{ A_{n}\text{ finitely often} \right\}$ is related to the sequence
$$
B_{n}^{c}=\bigcap_{k=n}^{\infty}A_{k}^{c}\equiv \left\{ \text{none of }A_{k},k\geq n,\text{occurs} \right\}
$$
So for $\mathbb{P}(A^{c})=0$, it is sufficient to show that $\mathbb{P}(B_{n}^{c})=0$ for all $n\geq 1$. By independence and the elementary inequality $1-x\leq e^{ -x }$ with $x\geq 0$, we get
$$
\mathbb{P}\left( \bigcap_{k=n}^{m}A_{k}^{c} \right)=\prod_{k=n}^{m}\mathbb{P}(A^{c}_{k})=\prod_{k=n}^{m}(1-\mathbb{P}(A_{k}))\leq \exp\left( -\sum_{k=n}^{m}\mathbb{P}(A_{k}) \right)
$$
So that
$$
\mathbb{P}(B_{n}^{c})=\lim_{ m \to \infty } \mathbb{P}\left( \bigcap_{k=n}^{m}A^{c}_{k} \right)\leq \exp\left( -\sum_{k=n}^{\infty}\mathbb{P}(A_{k}) \right)=0
$$
as the sum diverges. Hence $0\leq \mathbb{P}(A^{c})\leq \sum_{n=1}^{\infty}\mathbb{P}(B_{n}^{c})=0$, so by sub-additivity, $\mathbb{P}(A)=1$
___
Proof using expectation,
Let $X=\sum_{n=1}^{\infty}\mathbb{1}_{A_{n}}$ with $X(\omega)$ equal to the number of $n$ such that $\omega \in A(n)$
## Remark
The independence condition in the second part cannot be relaxed, otherwise, let $A_{n}=E$ for all $n\geq 1$, where $E\in\mathfrak{F}$ satisfies $0<\mathbb{P}(E)<1$ (and thus the events $A_{k}$ are not independent). Then $A=E$ and $\mathbb{P}(A)=\mathbb{P}(E)\neq 1$
___
An even more interesting couterexample without the independence property can be constructed as follows:
Let $X\sim U(0,1)$ be a [[Uniform Distribution|uniform]] [[Random Variables|random variable]] on $(0,1)$. For $n\geq 1$ consider the event $A_{n}=\left\{ X< \frac{1}{n} \right\}$. It is easy to see that 
$$
A=\left\{ A_{n}\text{ infinitely often} \right\}=\emptyset
$$
So that one can have $\sum_{n=1}^{\infty}\mathbb{P}(A_{n})=\infty$ together with $\mathbb{P}(A)=\mathbb{P}(A_{n}\text{ infinitely often})=0$
## Examples
A standard 6-sided die is tossed repeatedly. Let $N_{k}$ denote the total number of tosses when face $k$ was observed. Assming that the individual outcomes are independent, show that
$$
\mathbb{P}(N_{1}=\infty)=\mathbb{P}(N_{2}=\infty)=\mathbb{P}(N_{1}=\infty,N_{2}=\infty)=1
$$
Solution: Equalities $\mathbb{P}(N_{1}=\infty)=\mathbb{P}(N_{2}=\infty)=1$ can be derived so that the intersection event also has probability $\hspace{0pt}1$,
Alternatively, we derive the firsst equality from the Borel-Cantelli lemma. To this end, fix $k\in\left\{ 1,2,\dots,6 \right\}$ and denote $A_{n}^{k}=\left\{ n\text{th toss shows }k \right\}$. For different $n$, the events $A_{n}^{k}$ are independent and have the same probability $\frac{1}{6}$. As $\sum_{n=1}^{\infty}\mathbb{P}(A_{n}^{k})=\infty$, the Borel-Cantelli lemma implies that the event $\left\{ N_{k}=\infty \right\}\equiv \left\{ A_{n}^{k}\text{ infinitely often} \right\}$ has probability $\hspace{0pt}1$. The remaining claims now follow as indicated above
___
A coin showing 'heads' with probability $p$ is tossed repeatedly. With $X_{n}$ denoting the result of the $n$th toss, let $C_{n}=\left\{ X_{n}=T,X_{n-1}=H \right\}$. Show that $\mathbb{P}(C_{n}\text{ infinitely often})=1$
Solution:  we have $\left\{ C_{2n}\text{ infinitely often} \right\}\subset \left\{ C_{n}\text{ infinitely often} \right\}$, where $\mathbb{P}(C_{2n})=pq$ and $C_{2n}$ are independent. The result follows by our lemma
___
The Borel-Cantelli lemma is often used to describe the long-term behaviour of sequences of random variables
For example, let $(X_{k})_{k\geq 1}$ be [[Independent and Identically Distributed|iid]] random variable with common [[Exponential Distribution|exponential distribution]] of mean $\frac{1}{\lambda}$, i.e. $\mathbb{P}(X_{1}>x)=e^{ -\lambda x }$ for all $x\geq 0$. One can show that $X_{n}$ grows like $\frac{1}{\lambda}\log n$, more precisely that
$$
\mathbb{P}\left( \limsup_{n\to \infty} \frac{X_{n}}{\log n}=\frac{1}{\lambda} \right)=1
$$
Solution: For $\varepsilon>0$ denote
$$
A_{n}^{\varepsilon}:=\left\{ \omega :\middle|: X_{n}(\omega)> \frac{1+\varepsilon}{\lambda}\log n \right\},~~B_{n}^{\varepsilon}:= \left\{ \omega :\middle|: X_{n}(\omega)> \frac{1-\varepsilon}{\lambda}\log n \right\}
$$
We clearly have $\mathbb{P}(A_{n}^{\varepsilon})=n^{-(1+\varepsilon)}$ and $\mathbb{P}(B_{n}^{\varepsilon})=n^{-(1-\varepsilon)}$
As $\sum_{n=1}^{\infty}\mathbb{P}(A_{n}^{\varepsilon})<\infty$, by the Borel-Cantelli lemma, the event $\left\{ A_{n}^{\varepsilon}\text{ infinitely often} \right\}$ has probability zero
Similarly, the $B_{n}^{\varepsilon}$ are independent and $\sum_{n=1}^{\infty}\mathbb{P}(B_{n}^{\varepsilon})=\infty$, thus the event $\left\{ B_{n}^{\varepsilon}\text{ infinitely often} \right\}$ has probability 1
As for all $n\geq 1$, the events $B_{n}^{\varepsilon}$ increase with $\varepsilon$, the event $B^{*}(\varepsilon):=\bigcap_{\varepsilon>0}\left\{ B_{n}^{\varepsilon}\text{ infinitely often} \right\}$ has probability $\hspace{0pt}1$
Similarly, for all $n\geq 1$, the events $A_{n}^{\varepsilon}$ decrease with $\varepsilon$, and therefore the event $A^{*}(\varepsilon):= \bigcap_{\varepsilon>0}\left\{ A_{n}^{\varepsilon}\text{ finitely often} \right\}$ also has probability 1
By the characterisation of $\limsup$, we finally deduce that
$$
\left\{ \limsup_{ n \to \infty } \frac{X_{n}}{\log n}=\frac{1}{\lambda}  \right\}\equiv \bigcap_{\varepsilon>0}(\left\{ A_{n}^{\varepsilon}\text{ finitely often} \right\}\cap \left\{ B_{n}^{\varepsilon}\text{ infinitely often} \right\})=\bigcap_{\varepsilon>0}(A^{*}\cap B^{*}(\varepsilon))
$$
Which is an event of probability 1
___
A slightly more general version of the argument allows to control the limiting behaviour of the records:
Let $(X_{k})_{k\geq 1}$ be iid exponential random variables with distribution $\mathbb{P}(X_{k}>x)=e^{ -x }$, and let 
$$
M_{n}:=\max_{k=1}^{n}\left\{ X_{k} \right\}
$$
Then
$$
\mathbb{P}\left( \frac{M_{n}}{\log n}\to 1 \right)=1
$$
i.e. the normalised maximum $\frac{M_{n}}{\log n}$ converges to $\hspace{0pt}1$ almost surely as $n\to \infty$
___
Let variables $(X_{n})_{n\in\mathbb{N}}$ be iid with $X_{n}\sim U[0,1]$. For $\alpha>0$, we have $\mathbb{P}(X_{n}>1-n^{-\alpha})=n^{-\alpha}$ so that 
$$
\mathbb{P}(X_{n}>1-n^{-\alpha}\text{ infinitely often})=1\iff \alpha \leq 1
$$
A similar analysis shows that
$$
\mathbb{P}\left( X_{n}>1- \frac{1}{n(\log n)^{\beta}}\text{ infinitely often} \right)=\begin{cases}
1 & \beta \leq 1 \\
0&\beta>1
\end{cases}
$$
### Showing Convergence
If $(X_{k})_{k\geq 1}$ is a sequence of random variables such that for every $\varepsilon>0$, the event
$$
A(\varepsilon)\equiv \left\{ \left| X_{k} \right|>\varepsilon \text{ infinitely often}  \right\}
$$
Has probability $\hspace{0pt}1$, then $X_{k}$ is said to converge to zero with probability 1
As a simpple illustration, let $X_{k}= \frac{1}{k}X$ where a variable $X\geq 0$ has finite mean $\mathbb{E}(X)<\infty$, one can then show that, for each $\varepsilon>0$,
$$
\sum_{k=1}^{\infty}\mathbb{P}(\left| X_{k} \right| >\varepsilon)=\sum_{k=1}^{\infty}\mathbb{P}(X>k\varepsilon)<\infty
$$
And thus by the Borel-Cantelli lemma, the event $A(\varepsilon)\equiv \left\{ \left| X_{k} \right|>\varepsilon \text{ finitely often} \right\}$ has probability $\hspace{0pt}1$ for all such $\varepsilon$
By the discussion in the remark above and the monotonicity of $A(\varepsilon)$, the convergence event $C=\bigcap_{\varepsilon>0}A(\varepsilon)$ has probability $\hspace{0pt}1$. A more general result in the setting of the almost sure convergence is also considered