## Example
For an arbitrary fixed $x\in[0,1)$, let $(d_{k})_{k\geq 1}$ be the coefficients of its dyadic decomposition
$$
\sum_{k=1}^{\infty} \frac{d_{k}}{2^{_{k}}}
$$
With $d_{k}=d_{k}(x)\in\left\{ 0,1 \right\}$ satisfying
$$
d_{k}=1 \iff x\in D_{k}:=\bigcup_{\ell=1}^{2^{k-1}}\left[ \frac{2\ell-1}{2^{k}}, \frac{2\ell}{2^{k}} \right]
$$
Clearly, each set $D_{k}$ is a finite union of intervals of total length $\left| D_{k} \right|=\frac{1}{2}$. Furthermore, for each $n\geq 1$:
$$
0\leq x-\sum_{k=1}^{n} \frac{d_{k}(x)}{2^{k}}\leq \frac{1}{2^{n}}
$$
So that the dyadic decomposition [[Monotone Events|converges]] to $x$ a $n\to \infty$. We prove that $x\in[0,1)$ is the value of a [[Uniform Distribution|uniform]] [[Random Variables|random variable]] $U[0,1)$ iff the sequence $(d_{k}(x))_{k\geq 1}$ of its dyadic coefficients forms an infinite [[Sequences|sequence]] of [[Independence|independent]] [[Bernoulli Distribution|bernoulli]] $\mathrm{Ber}\left( \frac{1}{2} \right)$ random variables
$$
\delta_{k}(\omega):=\begin{cases}
1 & X(\omega )\in D_{k} \\
0 & X(\omega)\not\in D_{k}
\end{cases}
\iff\delta_{k}(\omega)\equiv \mathbb{1}_{D_{k}}(\omega)
$$
## Lemma
The collection of variables $\left\{ \delta_{k} \right\}_{k\geq 1}$ from above is mutually independent in $([0,1),\mathcal{B}[0,1),\mathbb{P})$
### Proof
We know that $\mathbb{P}(D_{k})=\frac{1}{2}$ for each integer $k\geq 1$. We fix arbitrary integer $n>1$ and show that $\left\{ D_{k} \right\}_{k= 1}^{n}$ are mutually independent by verifying the condition in [[Independent Bernoulli Sequences#Lemma|this lemma]]. We can then show that this means that the corresponding indicator functions $\left\{ \delta_{k} \right\}_{k=1}^{n}$ are mutually independent Bernoulli variables
To this end, fix arbitrary index subset $\mathcal{J}\subset \left\{ 1,\dots ,n \right\}$ and let $j^{*}:=\max\left\{ j\mid j\in\mathcal{J} \right\}$ and $\mathcal{J}_{*}:=\mathcal{J}\setminus \left\{ j^{*} \right\}$, hence
$$
\mathbb{E}\left( \prod_{\ell \in \mathcal{J}}\rho_{D_{\ell}} \right)=\mathbb{E}\left( (\mathbb{1}_{D_{j^{*}}}-\mathbb{1}_{(D_{j^{*}})^{c}})\prod_{\ell \in \mathcal{J_{*}}}\rho_{D_{\ell}} \right)
$$
And we separately integrate the last expression on each interval 
$$
\triangle_{j^{*}}^{\ell}:=\left[ \frac{\ell-1}{2^{j^{*}-1}},\frac{\ell}{2^{j^{*}-1}} \right)
$$
With integer $\ell \in\left\{ 1,\dots,2^{j^{*}-1} \right\}$
However, since the product $\prod_{\ell \in\mathcal{J}_{*}}\rho_{D_{\ell}}$ is constant on $\triangle_{j^{*}}^{\ell}$, while the variable $\rho_{D_{j^{*}}}$ averages to zero there. Consequently, the integral in the lastdisplay vanishes, implying the condition that
$$
\mathbb{E}\left( \prod_{\ell \in \mathcal{J}}  \rho_{D_{\ell}}\right)=0
$$
Thus the claim is shown
## Lemma
We also have the converse result; let $\left\{ d_{k} \right\}_{k\geq 1}$ be independent random variables with $d_{k}\sim Ber\left( \frac{1}{2} \right)$ for all $k\geq 1$. Then $Y(\omega):=\sum_{k=1}^{\infty} \frac{d_{k}(\omega)}{2^{k}}$ has $U[0,1)$ distribution
### Proof
It is sufficient to show that
$$
\mathbb{P}\left( Y\in \left[ \frac{m-1}{2^{k}}, \frac{m}{2^{k}} \right) \right)=\frac{1}{2^{k}}
$$
For all integer $k\geq 0$ and $1\leq m\leq 2^{k}$
To this end, fix integer $n\geq 1$ and let $Y_{n}$ be the finite sum approximation to $Y$, namely, $Y_{n}(\omega):=\sum_{k=1}^{n} \frac{d_{k}(\omega)}{2^{k}}$
It is straightforward to verify that $Y_{n}$ has uniform distribution in the finite set $\left\{ \frac{\ell}{2^{n}} \right\}_{\ell=0}^{2^{n}-1}$. By the apriori estimate
$$
0\leq x-\sum_{k=1}^{n} \frac{d_{k}(x)}{2^{k}}\leq \frac{1}{2^{n}}
$$
For all $0\leq a\leq b\leq 1$, we have 
$$
\mathbb{P}\left( Y_{n}\in \left[ 1,b-\frac{1}{2^{n}} \right) \right)\leq \mathbb{P}(Y\in [a,b))\leq \mathbb{P}\left( Y_{n}\in \left[ a- \frac{1}{2^{n}} ,b\right) \right)
$$
And so the probaility we wanted to show satisfies, for all integer $n\geq k$
$$
\frac{1}{2^{k}}-\frac{1}{2^{n}}=\frac{2^{n-k}-1}{2^{n}}\leq \mathbb{P}\left( Y\in \left[ \frac{m-1}{2^{k}},\frac{m}{2^{k}} \right) \right)\leq \frac{2^{n-k}+1}{2^{n}}=\frac{1}{2^{k}}+\frac{1}{2^{n}}
$$
## Theorem
Given $X\sim U[0,1)$ in the [[Canonical Probability Space|canonical probability space]] $([0,1),\mathcal{B}[0,1),\mathbb{P})$, define $\mathrm{Ber}\left( \frac{1}{2} \right)$ variables $\delta_{k}$ as above, then $\left\{ \delta_{k} \right\}_{k\geq 1}$ forms a mutually indepenent collection of random variables
Given a sequence $\left\{ \varepsilon_{k} \right\}_{k\geq 1}$ of mutually independent $\mathrm{Ber}\left( \frac{1}{2} \right)$ random variables on the canonical probability space $(([0,1),\mathcal{B}[0,1),\mathbb{P}))$, define
$$
Y(\omega):=\sum_{k=1}^{\infty}\varepsilon_{k}(\omega)2^{-k}
$$
Then $Y\sim U[0,1)$
### Proof
Taking the limit in the above lemma as $n\to \infty$, we get our reesult and thus finish the proof

## Theorem
In the canonical probability space $([0,1),\mathcal{B}[0,1),\mathbb{P})$, there is a sequence $(X_{n})_{n\geq 1}$ of mutually independent variables with common $U[0,1)$ distribution
### Proof
Let $\left\{ \delta_{k} \right\}_{k\geq 1}$ be a sequence of independent $\mathrm{Ber}\left( \frac{1}{2} \right)$ random variables as constructed above, then using a [[Bijective Functions|bijection]] $\mathbb{N}\to \mathbb{N}^{2}$ with $k\mapsto(n,m)\in\mathbb{N}^{2}$, we renumber these variables as $\left\{ \delta^{n}_{m} \right\}_{m,n\geq 1}$ and define
$$
X_{n}(\omega):= \sum_{m=1}^{\infty} \frac{\delta_{m}^{n}}{2^{m}}
$$
By construction, the variables $X_{n}$ are mutually independent, and, by the theorem above, have $U[0,1)$ ditribution
___
It remains to show how arbitrary distributions can be generated
## Example
Let $F(\cdot)$ be an arbitrary distribution function such that $F:\mathbb{R}\to[0,1]$ is a non-decreasing right-continuous function that tends to $0$ at $-\infty$ and to $1$ at $+\infty$, we define its left-continuous inverse on $[0,1]$ via
$$
F^{-1}(x):=\inf\left\{ z\in \mathbb{R}\mid F(z)\geq x \right\},x\in [0,1]
$$
Where, as usual, the [[Supremum and Infimum|infimum]] of the empty set is $\infty$. Define
$$
Y(\omega):=F^{-1}(X(\omega))
$$
Where $X\sim U[0,1)$
Then
$$
\mathbb{P}(Y\leq y)=\mathbb{P}(F^{-1}(X)\leq y)=\mathbb{P}(X\leq F(y))=F(y),~\forall y\in \mathbb{R}
$$
that is, $Y$ has cumulative distribution function $F(\cdot)$
## Theorem
Let $(F_{n}(\cdot))_{n\geq 1}$ be an arbitrary sequence of distribution functions. Then there exists a sequence $(Y_{n})_{n\geq 1}$ of independent random variables such that $Y_{n}$ has distribution $F_{n}$
### Proof
If $(X_{n})_{n\geq 1}$ is the sequence of independent $U[0,1)$ variables as in the theorem above, then $Y_{n}(\omega):=F^{-1}(X_{n}(\omega))$ are independent random variables where $Y_{n}$ has cumulative distribution function $F_{n}$
___
## Example
If [[Events|events]] $(A_{n})_{n\geq 1}$ form an [[Monotone Events|increasing]] [[Sequences|sequence]], then for each fixed $\omega \in\Omega$ the real sequence $(x_{n})_{n\geq 1}$ with $x_{n}:=\mathbb{1}_{A_{n}}(\omega)\in\left\{ 0,1 \right\}$ is non-decreasing, and therefore [[Convergence|converges]]
In particular, there are only three possibilities:
- $x_{n}=0$ for all $n\geq 1$, that is, $\omega$ is outside each set $A_{n}$ and their limit $A:=\lim_{ n \to \infty }A_{n}=\bigcup_{n=1}^{\infty}A_{n}$
- $x_{n}=1$ for all $n\geq 1$, that is, $\omega$ belongs to each $A_{n}$ and to the limit set $A$
- there is a $k\geq 1$ such that $x_{1}=\dots=x_{k-1}=x_{k}=0$ while $x_{k+1}=x_{k+2}=\dots=1$, that is, $\omega$ belongs to all but finitely many $A_{n}$, and to the limit set $A$
In the setting of increasing sequences $(A_{n})_{n\geq 1}$, for each $\omega \in \Omega$ we know whether $\omega \in A=\lim_{ n \to \infty }A_{n}$ or not. In particular, in the former case, $\omega$ must belong to all $A_{n}$ with sufficiently large $n$, such a statement is often abbreviated as [[Eventual Events|$\omega \in \left\{ A_{n}\text{ eventually} \right\}$]]
And of course, a similar description holds for a decreasing sequence $(A_{n})_{n\geq 1}$
## Eventual and Infinite Events
It is very tempting to use the same approach for general sequences $(A_{n})_{n\geq 1}$ of events, by declaring that a sequence of events $(A_{n})_{n\geq 1}$ in $\Omega$ conveerges iff the indicator sequence $\mathbb{1}_{A_{n}}\in\left\{ 0,1 \right\}$ converges for each $\omega \in \Omega$
However, without any condition (such as monotonicity) there is no guarantee that the indicator values $\mathbb{1}_{A_{n}}(\omega)$ would converge for all (or at least most) $\omega \in\Omega$
Neveertheless, for each sequence $(A_{n})_{n\geq 1}$ there are two particular events [[Infinitely Often Events|$\left\{ A_{n}\text{ infinitely often} \right\}$]]$,\left\{ A_{n}\text{ eventually} \right\}$ which provide useful informatiuon about the large $n$ behaviour of the sequence $(A_{n})_{n\geq 1}$
These events are well suited for studying limits of sequences of random variables, say $(X_{n})_{n\in\mathbb{N}}$. Their usefulness is due to the following simple observation:
Let $(x_{n})_{n\in\mathbb{N}}$ be a sequence of real numbers, then
$$
\lim_{ n \to \infty } x_{n}=x \iff \forall\varepsilon>0 \text{ the condition }\left| x_{n}-x \right| <\varepsilon \text{ holds eventually}
$$
$$
 \iff \forall\varepsilon>0\text{ the condition }\left| x_{n}-x \right| \geq \varepsilon \text{ holds finitely often}
$$
## Definition
By separately applying this description of convergence $X_{n}(\omega)\to X(\omega)$ for individual $\omega \in\Omega$, we can describe the covergence event as:
$$
C:=\left\{ \omega \in \Omega\mid X_{n}(\omega)\to X(\omega) \right\}\equiv \bigcap_{\varepsilon>0}\left\{ \left| X_{n}(\omega)-X(\omega) \right| \geq \varepsilon \text{ finitely often} \right\}
$$
$$
 =\bigcap_{\varepsilon>0}\left\{ \left| X_{n}(\omega)-X(\omega) \right| <\varepsilon \text{ eventually} \right\}
$$
## Remark
Recall that the events $A(\varepsilon)\equiv \left\{ A_{n}(\varepsilon)\text{ finitely often} \right\}\equiv \left\{ X<\infty \right\}$ if $\mathbb{P}(X<\infty)=1$ do not depend on $\varepsilon$, as a result, the convergence event:
$$
C:= \left\{ \omega\mid X_{n}(\omega)\to 0 \right\}\equiv \bigcap _{\varepsilon>0}\left\{ A_{n}(\varepsilon)\text{ finitely often} \right\}\equiv \left\{ X<\infty \right\}
$$
has probability 1
For this reason, we ay that the random variables $X_{k}$ converge to zero with probability $\hspace{0pt}1$ (or almost surely)
Other modes of convergence are available.
