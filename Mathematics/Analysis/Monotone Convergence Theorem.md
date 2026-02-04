# For Borel Functions
## Theorem
Let $f_{n}(x)\geq 0$ be a [[Monotonic Functions|non-decreasing]] [[Sequences of Functions|sequence]] of [[Borel Functions|borel]] [[Functions|functions]] that converges to $f(x)$ as $n\to \infty$. 
Then the [[Lebesgue Integration|Lebesgue integral]] of $f_{n}(x)$ converges to the Lebesgue integral of $f(x)$
# For Random Variables
## Theorem
Let [[Random Variables|random variables]] $X_{n}$ be such that for each $\omega \in \Omega$ the real [[Sequences|sequence]] $X_{n}(\omega)$ is non-decreasing and [[Sure Convergence|converges surely]] to $X(\omega)$ as $n\to \infty$
Then [[Expectation|$\mathbb{E}(X_{n})\nearrow \mathbb{E}(X)\leq \infty$]] as $n\to \infty$
## Remark
Notice there is no integrability condition here, the result holds even if $\mathbb{E}(X)=\infty$
___
The value of the Lebesgue integral does not change, if the function is modified on a set of probability zero, the assumptions of the monotone convergence theorem can be relaxed to their [[Almost Sure Convergence|almost sure]] version:
$$
\mathbb{P}(\left\{ \omega \in \Omega :\middle| :X_{n}(\omega)\leq X_{n+1}(\omega) ~\forall n\geq 1 \right\})=1
$$
$$
 \mathbb{P}(\left\{ \omega \in \Omega :\middle| :X_{n}(\omega)\to X(\omega) \right\})=1
$$
## Example
Given nonnegative random variables $(Z_{k})_{k\in\mathbb{N}}$, define $R_{m}:=\sum_{k=1}^{m}Z_{k}$. The variables $R_{m}\geq 0$ form a monotone sequence, $R_{m}\leq R_{m+1}$ for all $m\geq 1$, with $R_{m}\nearrow \sum_{k=1}^{\infty}Z_{k}$. Then, by the monotone convergence theorem,
$$
\mathbb{E}\left( \sum_{k=1}^{\infty}Z_{k} \right)=\mathbb{E}(\lim_{ m \to \infty } R_{m})=\lim_{ m \to \infty } \mathbb{E}(R_{m})=\sum_{k=1}^{\infty}\mathbb{E}(Z_{k})
$$
___
Boole's inequality can be shown:
For a sequence $(A_{n})_{n\in\mathbb{N}}$ of [[Events|events]], $A_{n}\in \mathfrak{F}$, let $B_{n}:=\bigcup_{k=1}^{n}A_{k}$ 
Let $Z_{n}:= \mathbb{1}_{A_{n}}$, and as above, denote $R_{m}:= \sum_{k=1}^{m}Z_{k}$, then for each $n\geq 1$,
$$
\mathbb{1}_{B_{n}}\leq \sum_{k=1}^{n}\mathbb{1}_{A_{k}}\equiv R_{n}\nearrow \sum_{k=1}^{\infty}Z_{k}
$$
So $\mathbb{P}(B_{n})\equiv \mathbb{E}(\mathbb{1}_{B_{n}})\leq \mathbb{E}(R_{n})$, which by the monotone convergence theorem is bounded above by
$$
\mathbb{E}\left( \sum_{k=1}^{\infty}Z_{k} \right)=\sum_{k=1}^{\infty}\mathbb{E}(Z_{k})=\sum_{k=1}^{\infty}\mathbb{P}(A_{k})
$$
For all $n\geq 1$
On the other hand, $B_{n}\nearrow \bigcup_{k=1}^{\infty}A_{k}$, equivalently,
$$
0\leq \mathbb{1}_{B_{n}}\nearrow \mathbb{1}_{\bigcup_{k=1}^{\infty}A_{k}}\text{ as }n\to \infty 
$$
So that monotone convergence theorem implies 
$$
\mathbb{P}\left( \bigcup_{k=1}^{\infty}A_{k} \right)\equiv \mathbb{E}\left( \mathbb{1}_{\bigcup_{k=1}^{\infty}A_{k}} \right)\leq \sum_{k=1}^{\infty}\mathbb{P}(A_{k})
$$
Which is Boole's inequality :)
## Corollary
Let random variables $X$ and $(X_{n})_{n\in\mathbb{N}}$ be such that $X_{n}\searrow X$ as $n\to\infty$. If $X_{1}$ is integrable, i.e. $\mathbb{E}(X_{1})<\infty$, then $\mathbb{E}(X_{n})\searrow \mathbb{E}(X)$ as $n\to\infty$
### Proof
Let $Y_{n}:=X_{1}-X_{n}\geq 0$, then $Y_{n}\nearrow X_{1}-X$, and so by monotone convergence theorem we have that
$$
\mathbb{E}(X_{1})-\mathbb{E}(X_{n})=\mathbb{E}(X_{1}-X_{n})=\mathbb{E}(Y_{n})\nearrow \mathbb{E}(X_{1}-X)=\mathbb{E}(X_{1})-\mathbb{E}(X)
$$
As $\mathbb{E}(X_{1})<\infty$, we deduce that $\mathbb{E}(X_{n})\searrow \mathbb{E}(X)$ as $n\to\infty$
### Remark
As in the remark above, the result holds if the assumptions are relaxed to their almost sure versions:
$$
\mathbb{P}(\left\{ \omega \in \Omega :\middle| : X_{n}(\omega)\geq X_{n+1}(\omega)~\forall n\geq 1 \right\})=1
$$
$$
\mathbb{P}(\left\{ \omega \in \Omega :\middle| :X_{n}(\omega)\to X(\omega) \right\})=1
$$
### Example
If we consider $R_{n}$ as above such that $0\leq R_{n}\nearrow R:=\sum_{n=1}^{\infty}Z_{n}$. In terms of $X_{n}:=e^{ -R_{n} }$, the corollary implies that $\mathbb{E}(e^{ -R_{n} })\searrow \mathbb{E}(e^{ -R })$
The distribution of the limit variable $R$ can be bounded along the lines of the general [[Markov's Inequality|Markov inequality]]: for each $k>0$,
$$
e^{ -K }\mathbb{P}(R\leq K)\leq \mathbb{E}(e^{ -R }\mathbb{1}_{R\leq K})\leq \mathbb{E}(e^{ -R })
$$
Implying that $\mathbb{P}(R\leq K)\leq e^{ K }\mathbb{E}(e^{ -R })$
Hence, if $\mathbb{E}(e^{ -R })=0$, by using a suitable monotone approximation, we deduce that $R$ is infinite almost surely
# For Sequences
## Theorem
Let [[Convergence#Sequences of Multiple Indices|$(a_{m,n})_{m,n\in\mathbb{N}}$]]  be a collection of numbers in $\overline{\mathbb{R}}^{+}$, which is increasing in the second index $n$, i.e. for every fixed $m\in\mathbb{N}$, the inequality $a_{m,k}\leq a_{m,n}$ holds provided $k\leq n$. Then
$$
\lim_{ n \to \infty } \sum_{m=1}^{\infty}a_{m,n}=\sum_{m=1}^{\infty}\lim_{ n \to \infty } a_{m,n}
$$
### Proof
Put $s_{m,n}=\sum_{l=1}^{m}a_{l,n}$ and use the Lemma from convergence of sequences of multiple indeces
## Remark
If the functions $f_{n}:\mathbb{N}\to \overline{\mathbb{R}}^{+}$ are defined via $f_{n}(m)=a_{m,n}$, they form a point-wise monotone sequence (i.e. for every fixed $m\in \mathbb{N}$, we have $f_{n}(m)\leq f_{n+1}(m)$ for all $n\geq 1$); the statement above says that the limit of the sum (integral) is equal to the sum (integral) of the limits, which is why this is a version of the monotone convergence theorem
