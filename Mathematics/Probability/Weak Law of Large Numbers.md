Idea: if we consider a sample of size $n$, $X_{1},X_{2},\dots,X_{n}$, then the sample mean:
$$
\overline{X}_{n}=\frac{1}{n}\sum_{ i=1} ^{ n}X_{i}
$$
Then $\overline{X}_{n}$ converges to the [[Expectation|expectation]]
## Theorem for Convergence in Probability
Let $X_{1},X_{2},\dots$ be an [[Independence|independent]] sequence of [[Random \mathbb{V}\mathrm{ar}(iables|random variables]], with [[Expectation|$\mathbb{E}(X_{i})=\mu$]] and [[\mathbb{V}\mathrm{ar}(iance|$\mathbb{V}\mathrm{ar}((X_{i})=\sigma^{2}$]] for all $i\geq 1$, 
Let $\overline{X}_{n}=\frac{1}{n}\sum_{i=1}^{n}X_{i}$, then for any $\epsilon>0$, the sequence will [[Convergence in Probability|converge in probability]], i.e.
$$
\lim_{ n \to \infty } \mathbb{P}(| \overline{X}_{n}-\mu|>\epsilon)=0
$$
In the most general case, we need not know $\sigma^{2}$, here in our case, we wanted to use Chebyshev's inequality and hence we needed it, this is known as the advances Kolmogorov Law of Large Numbers
### Proof
$$
\mathbb{E}(\overline{X}_{n})=\frac{1}{n}\sum_{ i=1} ^{ n}\mathbb{E}(X_{i})=\frac{1}{n}\times n \mu=\mu
$$
$$
\mathbb{V}\mathrm{ar}(( \overline{X}_{n})=\frac{1}{n^{2}}\left( \sum_{ i=1} ^{ n}  \mathbb{V}\mathrm{ar}((X_{i})+2\underbrace{ \sum_{ i<j} ^{ n} \mathbb{C}\mathrm{ov}(X_{i},X_{j}) }_{ =0\text{ (independent)} }  \right)
$$
$$
= \frac{1}{n^{2}}\sum_{ i=1} ^{ n}  \mathbb{V}\mathrm{ar}((X_{i})=\frac{1}{n^{2}}\times n\sigma^{2}=\frac{\sigma^{2}}{n}
$$
Now apply Chebyshev's inequality to get $\forall\epsilon>0$,
$$
\mathbb{P}(| \overline{X}_{n}-\mathbb{E}(\overline{X}_{n})|>0)=\mathbb{P}(\left| \overline{X}_{n}-\mu \right|>\epsilon )\leq \frac{1}{\epsilon^{2}}\mathbb{V}\mathrm{ar}((\overline{X}_{n})=\frac{\sigma^{2}}{\epsilon^{2}n}
$$
Equivalently
$$
\lim_{ n \to \infty } \mathbb{P}(\left| \overline{X}_{n}-\mu \right| \leq\epsilon)=1
$$
$$
\implies \mathbb{P}(\left| X_{n}-\mu \right|>\epsilon )=1-\mathbb{P}(\left| \overline{X}_{n}-u \right|\leq\epsilon)
$$
## Example
Let $X$ denote the number of heads in $n$ tosses of coin with probability of success $p$
$$
X\sim Bin(n,p)
$$
$$
 \mathbb{E}(X)=np,\mathbb{V}\mathrm{ar}((X)=np(1-p)
$$
Define $B_{n}=\frac{1}{n}X$, 
$$
\mathbb{E}(B_{n})=\mathbb{E}\left( \frac{1}{n}X \right)=\frac{1}{n}\mathbb{E}(X)
$$
$$
\mathbb{V}\mathrm{ar}((B_{n})=\frac{1}{n^{2}}\mathbb{V}\mathrm{ar}((X)
$$
Now we can apply Chebyshev's inequality, for any $\epsilon>0$, 
$$
\mathbb{P}(|B_{n}-\mathbb{E}(B_{n})|>\epsilon)=\mathbb{P}(|B_{n}-p|>\epsilon)\leq \frac{1}{\epsilon^{2}}\mathbb{V}\mathrm{ar}((B_{n})=\frac{p(1-p)}{\epsilon^{2}n}\to 0
$$
As $n\to \infty$
So $B_{n}$ will be very cose to $p$ with a very high probablity
___
Let us collect a sample of size $n$ of heights of individuals, let $H_{i}$ denote the height of the $i$th individual
Suppose we know that $\mathbb{E}(H_{i})=\mu$ 
Suppose we know that $\mathbb{E}(H_{i})=\mu$ and $\mathbb{V}\mathrm{ar}((H_{i})=\sigma^{2}$. Then if $\overline{X}_{n}=\frac{1}{n}\sum_{ i=1} ^{ n} H_{i}$, then $\forall\epsilon>0$, $\mathbb{P}(\left| \overline{X}_{n}-\mu \right|>\epsilon)\to 0$ as $n\to \infty$, that is, with high probability that $\overline{X}_{n}$ is very close to $\mu$
___
## Theorem for Convergence in [[Lr Space|$L^{2}$]]
Let $(X_{n})_{n\in\mathbb{N}}$ be uncorrelated random variables with $\mathbb{E}(X_{n})=\mu$ and $\mathbb{V}\mathrm{ar}(X_{n})\leq C<\infty$. Denote
$$
S_{n}=X_{1}+X_{2}+\dots+X_{n}=\sum_{k=1}^{n}X_{k}
$$
Then 
$$
\frac{1}{n} S_{n}\overset{L^{2 }}\to \mu \text{ as }n\to \infty
$$
i.e. they [[Convergence in Lr|converge in $L^{2}$]]
### Proof
As variables $X_{k}$ are uncorrelated, we have
$$
\mathbb{V}\mathrm{ar}(S_{n})=\sum_{k=1}^{n}\mathbb{V}\mathrm{ar}(X_{k})
$$
$$
\implies \mathbb{V}\mathrm{ar}(S_{n})\leq C n
$$
$$
\implies \mathbb{E}\left(  \left( \frac{1}{n}S_{n}-\mu \right)^{2} \right)=\mathbb{E}\left(  \frac{(S_{n}-n\mu)^{2}}{n^{2}} \right)=\frac{\mathbb{V}\mathrm{ar}(S_{n})}{n^{2}}\leq \frac{C}{n}\to 0\text{ as }n\to \infty
$$
$W^{5}$
### Remark
Let $Z\sim N(0,\sigma^{2})$, so that $\mathbb{E}(Z)=\mathbb{E}(Z^{3})=0$, $\mathbb{E}(Z^{2})=\sigma^{2}$ and $\mathbb{E}(Z^{4})=3\sigma^{4}$ 
Define
$$
Y_{n}:= \frac{1}{n}\sum_{k=1}^{n} X_{k}
$$
Where $X_{k}:=(Z_{k})^{2}$ with independent $Z_{k}\sim N(0,t)$. Then $\mathbb{E}(Y_{n})=t$, 
$$
\mathbb{E}((Y_{n}-t)^{2})=\frac{1}{n}\mathbb{V}\mathrm{ar}(X_{k})=\frac{2t^{2}}{n}
$$
  And so $Y_{n}\to t$ in $L^{2}$ as $n\to \infty$ 
  This simple observation is at the heart of the construction of the stochastic integral with respect to the brownian motion. The resuting area of stochastic analysis has a wide range of applicability, including in financial mathematics
  ___
  Note also that since $X_{n}\overset{L^{2 }}\to X\implies X_{n}\overset{p}\to X$, this is another form of proving the above theorem for convergence in probability  
## Example
This exaple shows that a high dimensional cube is essentially a sphere
Let random variables $(X_{k})_{k\in\mathbb{N}}$ be [[Independent and Identically Distributed|i.i.d.]] with $X_{k}\sim U(-1,1)$ and define $Y_{k}=(X_{k})^{2}$
Then $\mathbb{E}(Y_{k})=\frac{1}{3}$ and 
$$
\mathbb{V}\mathrm{ar}(Y_{k})\leq \mathbb{E}((Y_{k})^{2})=\mathbb{E}((X_{k})^{4})\leq 1
$$
Fix $\varepsilon \in\left( 0,\frac{1}{3} \right)$ and consider the set
$$
A_{n,\varepsilon}:=\left\{ x\in \mathbb{R}^{n}:\middle|:(1-3\varepsilon) \frac{n}{3}<\left| x \right| ^{2}<(1+3\varepsilon) \frac{n}{3} \right\}
$$
Where $\left| x \right|$ is the usual Euclidean [[Norms|norm]] in $\mathbb{R}^{n}$, $\left| x \right|^{2}=\sum_{k=1}^{n}(x_{k})^{2}$
By the weak law of large numbers,
$$
\frac{1}{n}\sum_{k=1}^{n}(X_{k})^{2}\overset{p}\to  \frac{1}{3}
$$
In other words, for every fixed $\varepsilon \in\left( 0,\frac{1}{3} \right)$ a point $\underline{X}=(X_{1},\dots,X_{n})$ chosen uniformly in $(-1,1)$ satisfies:
$$
\mathbb{P}\left( \left|  \frac{1}{n}\sum_{k=1}^{n}(X_{k})^{2}-\frac{1}{3} \right| \geq \varepsilon \right)=\mathbb{P}(\underline{X}\not\in  A_{n,\varepsilon})\to 0\text{ as }n\to \infty
$$
I.e. for large $n$, with probability approaching $\hspace{0pt}1$, a random point $\underline{X}\in(0,1)^{n}$ is near the $n$ dimensional sphere of radius $\sqrt{ \frac{n}{3} }$ centred at the origin
## Lemma
Let random variables $(S_{n})_{n\in\mathbb{N}}$ have two finite [[Moment (in Probability)|moments]], $\mu_{n}\equiv \mathbb{E}(S_{n}),\sigma^{2}_{n}\equiv \mathbb{V}\mathrm{ar}(S_{n})<\infty$
Further, let $(b_{n})_{n\in\mathbb{N}}$ satisfy $\frac{\sigma_{n}}{b_{n}}\to 0$ as $n\to \infty$, then
$$
\frac{S_{n}-\mu_{n}}{b_{n}}\to 0\text{ as }n\to \infty
$$
Both in $L^{2}$ and in probability
### Proof
We find this similarly to the weak law of large numbers, the result follows from the observation
$$
\mathbb{E}\left(  \frac{(S_{n}-\mu_{n})^{2}}{b_{n}^{2}} \right)=\frac{\mathbb{V}\mathrm{ar}(S_{n})}{b_{n}^{2}}\to 0\text{ as }n\to \infty
$$


#Mathematics #Probability #Theorem 