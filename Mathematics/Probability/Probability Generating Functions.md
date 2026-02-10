2## Definition
If $X$ is a [[Discrete Random Variables|discrete]] [[Random Variables|random variable]], with values in $\mathbb{N}_{0}$, then it's [[Probabilities|probability]] [[Generating Functions|generating function]] is
$$
G(s)\equiv G_{X}(s):= \mathbb{E}(s ^{X})=\sum_{k=0}^{\infty}s ^{k}\mathbb{P}(X=k)
$$
For the pmf $\left\{ p_{k} \right\}\equiv \left\{ \mathbb{P}(X=k) \right\}$ of $X$
## Remark
For $\left| s \right|\leq 1$, the generating function $G_{X}(s)$ is bounded, as
$$
\left| G_{X}(s) \right| \leq \sum_{k=0}^{\infty}\mathbb{P}(X=k)\leq 1
$$
Consequently, each probability generating function:
- Can be [[Differentiation|differentiated]]  or [[Integration|integrated]]  term-wise any number of times at each $s$ such that $\left|  s \right|<1$
- possesses the uniqueness property of generating functions
- satisfies Abel's theorem, namely, if the sequence $(a_{n})_{n\in\mathbb{N}}$ is non-negative, and its generating function $G_{a}(s)$ is finite for $\left| s \right|< 1$, then $\lim_{ s \nearrow 1 }G_{a}(s)=\sum_{n=0}^{\infty}a_{n}$ whether the sum is finite or infinite. This standard result is useful if the [[Cauchy-Hadamard Theorem|radius of convergence]] is $\hspace{0pt}1$ as then one has no reason to expect that the limit exists as $s\nearrow 1$ 
## Example
It is straightforward to derive probability generating functions of many distributions, such as
If $\mathbb{P}(X=c)=1$ for some $c\in\mathbb{R}$, then $G(s)-\mathbb{E}(x^{X})=s ^{c}$
If [[Bernoulli Distribution|$X\sim \mathrm{Ber}(p)$]], then $G(s)=\mathbb{E}(s^{X})=(1-p)^{0}+ps=1-p+ps$
If [[Binomial Distribution|$X\sim B(n,p)$]], then $G(s)=\mathbb{E}(s ^{X})=\sum_{k=0}^{n}{n \choose k }p^{k}(1-p)^{n-k}s ^{k}$
If [[Poisson Distribution|$X\sim Po(\lambda)$]] then $G(s)=\mathbb{E}(s^{X})=\sum_{k=0}^{\infty} \frac{\lambda^{k}}{k!}e^{ -\lambda  }s ^{k}=e^{ \lambda(s-1) }$
## Theorem
If $X$ and $Y$ are [[Independence|independent]] random variables with values in $\mathbb{N}_{0}$, and $Z:=X+Y$, then their generating functions satisfy
$$
G_{Z}(s)=G_{X+Y}(s)=G_{X}(s)G_{Y}(s)
$$
### Proof
Recall that if $X$ and $Y$ are discrete random variables and $f,g:\mathbb{N}_{0}\to \mathbb{R}$ are arbitrary functions, then $f(X)$ and $g(Y)$ are independent random variables and 
$$
\mathbb{E}(f(X) g(Y))=\mathbb{E}(f(X))\mathbb{E}(g(Y))
$$
Taking $f(X)=s^{X}$ and $g(Y)=s^{Y}$, we are done
### Example
Let $X\sim Po(\lambda)$ and $Y\sim Po(\mu)$ be independent. Then $Z=X+Y$ is $Po(\lambda+\mu)$
By the example above for the Poisson distribution and the theorem above, we get
$$
G_{Z}(s)=G_{X}(s)G_{Y}(s)=e^{ \lambda(s-1) }e^{ \mu(s-1) }=e^{ (\lambda+\mu)(s-1) }
$$
The result follows by uniqueness
___
If $(X_{k})_{k=1}^{n}$ are [[Independent and Identically Distributed|independent and identically distributed]] with values in $\mathbb{N}_{0}$, and $S_{n}=X_{1}+X_{2}+\dots+X_{n}$, then 
$$
G_{S_{n}}(s)=G_{X_{1}}(s)\dots G_{X_{n}}(s)=(G_{X}(s))^{n}
$$
Which follows from our theorem by induction
## Convolution Theorem
If sequences $(a_{k})_{k\in\mathbb{N}},(b_{m})_{m\in\mathbb{N}}$ and $(c_{n})_{n\in\mathbb{N}}$ are such that [[Convolution|$c=a\star b$]], then their respective generating functions $G_{c}(s),G_{a}(s),G_{b}(s)$ satisfy
$$
G_{c}(s)=G_{a}(s)G_{b}(s)
$$
# Applications of Generating Functions
## Example
Let $(X_{k})_{k\in\mathbb{N}}$ be independent and identically distributed variables with values in $\mathbb{N}_{0}$, and let $N\geq 0$ be an integer valued random variable independent of $\left\{ X_{k} \right\}_{k\in\mathbb{N}}$. Then $S_{N}=\sum_{k=1}^{N}X_{k}$ has generating function
$$
G_{S_{N}}(s)=G_{N}(G_{X}(s))
$$
This is a straightforward application of the partition theorem for expectations. Alternatively, the result follows from the standard properties of conditional expectations:
$$
\mathbb{E}(z^{S_{N}})=\mathbb{E}(\mathbb{E}(z^{S_{N}}|N))=\mathbb{E}((G_{X}(z))^{N})=G_{N}(G_{X}(z))
$$
___
### Recurrence Relations
Generating functions are very useful in solving [[Recurrence Relations|recurrence relations]] using the fact that
$$
\frac{b}{a-x}=\frac{b}{a}\sum_{k=0}^{\infty}\left( \frac{x}{a} \right)^{k}=\sum_{k=0}^{\infty} \frac{b}{a^{k+1}}x^{k}
$$
Generating functions of sums of random variables can be written as power series, that can then be converted using [[Partial Fractions|partial fractions]]
### Example
Imagine a diligent janitor who replaces a light bulb the same day as it burns out. Suppose the first bulb is put in on day $\hspace{0pt}0$ and let $X_{i}$ be the lifetime of the $i$th light bulb. Let the individual lifetimes $X_{i}$ be independent and identically distributed random variables with values in $\mathbb{N}$ and have common distribution with generating function $G_{f}(s)$
Define 
$$
r_{n}=\mathbb{P}(\text{a bulb was replaced on day }n)
$$
$$
f_{k}:=\mathbb{P}(\text{the first bulb was replaced on day }k)
$$
Then
$$
r_{0}=1,f_{0}=0\text{ and }r_{n}=\sum_{k=1}^{n}f_{k}r_{n-k},~n\geq 1
$$
A standard computation implies that
$$
G_{r}(s)-1=\sum_{n=1}^{\infty}r_{n}s ^{n}=\sum_{n=0}^{\infty}\sum_{ k=1} ^{ n}f_{k}r_{n-k}s^{n}=\sum_{k=1}^{\infty}f_{k}s^{k}\sum_{n=k}^{\infty} r_{n-k}s^{n-k}=\sum_{k=1}^{\infty}f_{k}s^{k}G_{r}(s)
$$
$$
= G_{f}(s)G_{r}(s)
$$
For all $\left| s \right|<1$ so that $G_{r}(s)=\frac{1}{1-G_{f}(s)}$
___
Let $a_{n}$ be the probability that $n$ independent Bernoulli trials with success probability $p$ result in an even number of successes. Find the generating function of $a_{n}$
The event undewr consideration occurs if the initial failure at the fiest trial is followed by an even number of successes where $q=1-p$. Multiplying these equalities by $s^{n}$ and adding them, we get
$$
G_{a}(s)-1=qsG_{a}(s)+p\sum_{n=1}^{\infty}s^{n}-psG_{a}(s)=(q-p)sG_{a}(s)+ \frac{ps}{1-s}
$$
And after rearranging,
$$
G_{a}(s)=\frac{\left( 1+\frac{ps}{1-s} \right)}{1-(q-p)s}=\frac{1}{2}\left( \frac{1}{1-s}+\frac{1}{1-(q-p)s} \right)=\frac{1}{2}\sum_{n=0}^{\infty}(q-p)^{n}s^{n}
$$
As a result $a_{n}=\frac{1+(q-p)^{n}}{2}$
___
A biased coin is tossed repeatedly; on each toss, it shows heads with probability $p$. Let $r_{n}$ be the probability that a sequence of $n$ tosses never has two heads in a row. Show that $r_{0}=1,r_{1}=1$ and for all $n>1$, $r_{n}=qr_{n-1}+pqr_{n-2}$ where $q=1-p$. Deduce the generating function of the sequence $(r_{n})_{n\in\mathbb{N}}$
Every sequence of $n\geq 2$ tosses starts either with $T$ or $HT$; hence the relation
Multiplying these equalities by $s^{n}$ and summing, we get
$$
G_{r}(s)=\sum_{n=0}^{\infty}r_{n}s^{n}=1+s+qs\sum_{n=2}^{\infty}r_{n-1}s^{n-1}+qps^{2}\sum_{n=2}^{\infty}r_{n-2}s^{n-2}
$$
So that
$$
G_{r}(s)-(qs+pqs ^{2})G_{r}(s)+1+ps= \frac{1+ps}{1-qs-pqs^{2}}
$$
## Continuity Theorem
For every fixed $n\geq 0$, let the sequence $(a_{k,n})_{k\geq 0}$ be a probability distribution, i.e. $a_{k,n}\geq 0$ and $\sum_{k=0}^{\infty}a_{k,n}=1$. Denote $G_{n}(s)$ to be the corresponding generating function,
$$
G_{n}(s)=\sum_{k=0}^{\infty} a_{k,n}s^{k}
$$
In order that for every fixed $k$,
$$
\lim_{ n \to \infty } a_{k,n}=a_{k}
$$
I.e. it converges [[Convergence in Distribution|in distribution]]
It is necessarry and sufficient that for every $s\in[0,1)$ we have
$$
\lim_{ n \to \infty } G_{n}(s)=G(s)
$$
Where $G(s)=\sum_{k=0}^{\infty}a_{k}s ^{k}$ is the generating function of the limiting sequence
### Example
If $X_{n}\sim B(n,p)$ with $p=p_{n}$ satisfying $np_{n}\to \lambda$ as $n\to \infty$, then
$$
G_{X_{n}}\equiv(1+p_{n}(s-1))^{n}\to \exp(\lambda(s-1))
$$
So that the distribution of $X_{n}$ converges so that of $X\sim Po(\lambda)$