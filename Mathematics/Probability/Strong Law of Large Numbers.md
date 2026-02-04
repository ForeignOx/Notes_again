## Theorem: The Strong Law of Large Numbers in [[Lr Space|$L^{4}$]]
Let [[Random Variables|random variables]] $(X_{n})_{n\in\mathbb{N}}$ be [[Independence|independent]] with $\mathbb{E}(X_{k})=\mu$ and $\mathbb{E}((X_{k})^{4})\leq C$ for some constant $C>0$ and all $k$, If 
$$
S_{n}:=X_{1}+X_{2}+\dots +X_{n}=\sum_{k=1}^{n}X_{k}
$$
Then $\frac{S_{n}}{n}\to \mu$ [[Almost Sure Convergence|almost surely]] as $n\to \infty$
### Proof
We may and shall suppose that $\mu=\mathbb{E}(X_{k})=0$, otherwise, consider the centred variables $X_{k}'=X_{k}-\mu$ and deduce the result from the relation $\frac{1}{n}S_{n}'=\frac{1}{n}S_{n}-\mu$ and linearity of almost sure convergence, now
$$
\mathbb{E}((S_{n})^{4})=\mathbb{E}\left( \left( \sum_{k=1}^{n}X_{n} \right)^{4} \right)=\sum_{i,j,k,l=1}^{n}\mathbb{E}(X_{i}X_{j}X_{k}X_{l})=\sum_{k=1}^{n}\mathbb{E}((X_{k})^{4})+6\sum_{1\leq k< m\leq n} \mathbb{E}((X_{k})^{2}(X_{m})^{2})
$$
Where the last equality follows from the fact that if $i\not\in\left\{ j,k,l \right\}$, we have
$$
\mathbb{E}(X_{i}X_{j}X_{k}X_{l})=\mathbb{E}(X_{i})\mathbb{E}(X_{j}X_{k}X_{l})=0
$$
As $\mathbb{E}(X_{i})=0$
By the [[Cauchy-Schwarz Inequality|Cauchy-Schwarz inequality]],$\mathbb{E}((X_{k})^{2}(X_{m})^{2})\leq C$ for all $1\leq k<m\leq n$ so that
$$
\mathbb{E}((S_{n})^{4})\leq 3Cn^{2}
$$
Finally, the [[Markov's Inequality#More General Version|general Markov inequality]] with $g(x)=x^{4}$ implies
$$
\mathbb{P}(\left| S_{n} \right| >n\varepsilon)\leq \frac{\mathbb{E}((S_{n})^{4})}{(n\varepsilon)^{4}}\leq \frac{3C}{n^{2}\varepsilon^{4}}
$$
And the result follows from the sufficient condition of almost sure convergence
## Remark
While the Cauchy-Schwarz inequality works without any assumption on independence of $X$ and $Y$, in the [[Independent and Identically Distributed|i.i.d.]] setting of the theorem, the bound $\mathbb{E}((X_{k})^{2}(X_{m})^{2})\leq C$ can also be obtained by noticing the factorisation 
$$
\mathbb{E}((X_{k})^{2}(X_{m})^{2})=\mathbb{E}((X_{k})^{2})\mathbb{E}((X_{m})^{2})
$$
And the general inequality $\mathbb{E}(Z^{2})\leq \sqrt{ \mathbb{E}(Z)^{4} }$, the latter is immediate from the observation that $\mathbb{V}\mathrm{ar}(Z^{2})=\mathbb{E}(Z^{4})-\mathbb{E}(Z^{2})^{2}\geq 0$ for any random variable $Z$
___
With some additional work, one can obtain the following strong law of large numbers due to Kolmogorov:
## Theorem: Strong Law of Large Numbers in $L^{1}$
Let random variables $(X_{n})_{n\in\mathbb{N}}$ be independent and identically distributed with $\mathbb{E}(\left| X_{k} \right|)<\infty$
If $S_{n}:=X_{1}+X_{2}+\dots+X_{n}$, then $\frac{1}{n}S_{n}\to \mu:= \mathbb{E}(X_{k})$ almost surely, as $n\to \infty$
## Example
Let random variables $(X_{n})_{n\in\mathbb{N}}$ be independent with common [[Exponential Distribution|$\exp 1$]] distribution, i.e. satisfying $\mathbb{P}(X_{k}>x)=e^{ -x }$ for all $x\geq 0$
Denote $M_{n}:= \max_{1\leq k\leq n}X_{k}$, we show that
$$
\frac{M_{n}}{\log n}\to 1
$$
Almost surely as $n\to \infty$
We first verify that
$$
\liminf_{n\to oo} \frac{M_{n}(\omega)}{\log n}\geq 1
$$
On a set [[Sample Spaces|$\Omega_{1}$]] of [[Probabilities|probability]] $\hspace{0pt}1$, $\mathbb{P}(\Omega_{1})=1$
Indeed, by independece of $X_{k}$, for every $y>0$, we have
$$
\mathbb{P}(M_{n}\leq y)=\prod_{k=1}^{n}\mathbb{P}(X_{k}\leq y)=(1-e^{ -y })^{n}
$$
Consequently, for every fixed $\varepsilon>0$,
$$
\mathbb{P}\left(  \frac{M_{n}}{\log n}\leq 1-\varepsilon \right)=(1-e^{ -(1-\varepsilon)\log n })^{n}\leq e^{ -n^{\varepsilon} }
$$
Implying that
$$

$$
$$
 \sum_{n=1}^{\infty}\mathbb{P}\left( \frac{M_{n}}{\log n}\leq 1-\varepsilon \right)\leq \sum_{n=1}^{\infty} e^{ -n^{\varepsilon} }<\infty
$$
Therefore, the event
$$
\Omega_{1}(\varepsilon)=\left\{ \omega \in \Omega :\middle|: \frac{M_{n}(\omega)}{\log n}>1-\varepsilon \text{ for all }n\text{ large enough} \right\}
$$
has probability $\hspace{0pt}1$, equivalently, the random variable
$$
n_{1}=n_{1}(\omega):=\min\left\{ n\geq 1:\middle|:M_{k}(\omega)\geq (1-\varepsilon)\log k\text{ for all }k\geq n \right\}
$$
Is almost surely finite. As $\Omega_{1}(\varepsilon)$ increases with $\varepsilon$, the set $\Omega_{1}:=\bigcap_{\varepsilon>0}\Omega_{1}(\varepsilon)$ has probability $\hspace{0pt}1$, while for each $\omega \in \Omega_{1}$, $\liminf_{ n \to \infty } \frac{M_{n}}{\log n}\geq 1$ holds
We next show that for a set $\Omega_{2}$ of probability $\hspace{0pt}1$, i.e. $\mathbb{P}(\Omega_{2})=1$, we have
$$
\limsup_{ n \to \infty } \frac{M_{n}(\omega)}{\log n}\leq 1
$$
Fixing arbitrary $\omega \in \Omega$ and $\varepsilon>0$, as $\log n\to \infty$, the sets
$$
\left\{ n\in\mathbb{N}:\middle|: M_{n}(\omega)>(1+\varepsilon)\log n \right\},\left\{ n\in\mathbb{N}:\middle|:X_{n}(\omega)>(1+\varepsilon)\log n \right\}
$$
Are either both finite or both infinite. Consequently, the [[Infinitely Often Events|infinitely often events]]
$$
\Omega_{3}(\varepsilon):=\left\{ \omega \in \Omega :\middle|: \frac{M_{n}(\omega)}{\log n}> (1+\varepsilon)\text{ infinitely often} \right\}, \left\{ \omega \in \Omega :\middle|: \frac{X_{n}(\omega)}{\log n}>(1+\varepsilon)\text{ infinitely often} \right\}
$$
Coeincide. We know that $\mathbb{P}(\Omega_{3}(\varepsilon))=0$ and therefore the event $\Omega_{3}:=\bigcup_{\varepsilon>0}\Omega_{3}(\varepsilon)$ also has probability zero. Notice that
$$
\Omega_{3}\equiv \left\{ \omega \in \Omega :\middle|:\limsup_{ n \to \infty } \frac{M_{n}(\omega)}{\log n}>1 \right\}
$$
So that $\limsup_{ n \to \infty } \frac{M_{n}(\omega)}{\log n}\leq 1$ holds with $\Omega_{2}=\Omega_{3}^{c}$
Finally, the set $\Omega_{0}:=\Omega_{1}\cap\Omega_{2}=\Omega_{1}\setminus \Omega_{3}$ has probability $\hspace{0pt}1$ and for each $\omega \in \Omega_{0}$, we have $\frac{M_{n}(\omega)}{\log n}\to 1$ as $n\to \infty$
