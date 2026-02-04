Let $(a_{k})_{k\in\mathbb{N}}$ be a [[Sequences|sequence]] with the following properties, $a_{k}\neq 0$ for all $k\in\mathbb{N}$, except finitely many
- If $\lim_{ k \to \infty }\left| \frac{a_{k+1}}{a_{k}} \right|<1$, then the [[Series|Series]] $\sum_{k=1}^{\infty} a_{k}$ is [[Absolute Convergence|absolutely convergent]]
- If $\lim_{ k \to \infty } \left| \frac{a_{k+1}}{a_{k}} \right|>1$, then the series $\sum_{k=1}^{\infty} a_{k}$ is divergent
## Remark
The limit $\lim_{ k \to \infty }\left| \frac{a_{k+1}}{a_{k}} \right|$ need not exist, but we can still make a conclusion, provided:
- If $\lim\sup_{ k \to \infty } \left| \frac{a_{k+1}}{a_{k}} \right|<1$, that is $\left|  \frac{a_{k+1}}{a_{k}}\right|\leq q<1$ for all but finiteely many $k$, then series is absolutely convergent
- If $\left| \frac{a_{k+1}}{a_{k}} \right|\geq 1$ for all but finitely many $k$, then $\sum_{k=1}^{\infty} a_{k}$ diverges
## Proof
Assume $\limsup_{ k \to \infty } \left| \frac{a_{k+1}}{a_{k}} \right|<1$, then there exists $n_{0}$ with  $\left| \frac{a_{k+1}}{a_{k}} \right|\leq q$ for all $k\geq n_{0}$, 
$$
\implies \left| a_{k+1} \right|\leq \left| a_{k} \right|q
$$
$$
\implies \left| a_{n_{0}+j} \right| \leq \left| a_{n_{0}+j-1} \right| q\leq \left| a_{n_{0}+j-2} \right| q^{2}\leq\dots \leq \left| a_{n_{0}} \right| q^{j}
$$
Which can be thought of as a sort of a comparison series, since $0\leq q<1$, so
$$
\sum_{j=0}^{\infty} |a_{n_{0}}|q^{j}=\frac{\left| a_{n_{0}} \right|  }{1-q}
$$
So $\sum_{j=0}^{\infty} \left| a_{n_{0}+j} \right|$ is convergent by comparison test and is equal to $\sum_{k=n_{0}}^{\infty} \left| a_{k} \right|$ so is absolutely convergent. Hence $\sum_{k=1}^{\infty} \left| a_{k} \right|$ is also absolutely convergent
Note: if $\lim_{ k \to \infty } \frac{\left| a_{k+1} \right|}{\left| a_{k} \right|}=q>1$, then look at $\varepsilon=q-1>0$, then we have $n_{0}\in\mathbb{N}$ with 
$$
\left| \left| \frac{a_{k+1}}{a_{k}} \right| -q \right| <\varepsilon \forall k\geq n_{0}
$$
$$
\implies -\varepsilon< \left| \frac{a_{k+1}}{a_{k}} \right| -q<\varepsilon=q-1
$$
So
$$
\left| \frac{a_{k+1}}{a_{k}} \right| >1
$$
Proof of the second part: there is $n_{0}\in\mathbb{N}$ with $\left| \frac{a_{k+1}}{a_{k}} \right|\geq 1$ for all $k\geq n_{0}$, which implies $\left| a_{k+1} \right|\geq \left| a_{k} \right|>0$
In particular, $(a_{k})_{k\in\mathbb{N}}$ does not converge to $0$, the series is therefore divergent
## Examples
Look at $\sum_{n=1}^{\infty} \frac{1}{n}$, $\sum_{n=1}^{\infty} \frac{1}{n^{2}}$
Look at
$$
\frac{\frac{1}{n+1}}{\frac{1}{n}}=\frac{n}{n+1}\to1
$$
So we can't say anything :(
Look at
$$
\frac{\frac{1}{(n+1)^{2}}}{\frac{1}{n^{2}}}=\frac{n^{2}}{(n+1)^{2}}\to 1
$$
So also fails
Key takeaway; ratio test will fail to give an answer when $a_{n}=\frac{f(n)}{g(n)}$, with $f$ and $g$ polynomials
___
It works well for factorials and exponentials, for example:
$$
a_{k}=\frac{c^{k}}{k!}
$$
With $c\in\mathbb{R}\setminus \{ 0 \}$
$$
\left| \frac{a_{k+1}}{a_{k}} \right| =\frac{\left| c \right| ^{k+1}}{(k+1)!}\times \frac{k!}{\left| c \right|^{k} }=\frac{|c|}{k+1}\to0<1
$$
So $\sum_{k=1}^{\infty} a_{k} \frac{c^{k}}{k!}$ converges absolutely
___
Another!
$$
b_{k}=k!c^{k}
$$
Using the ratio test gives:
$$
\left| \frac{(k+1)!\left| c \right| ^{k+1}}{k!\left| c \right| ^{k}} \right| =(k+1)\left| c \right|\to \infty
$$
Which diverges
___
$$
c_{k}=kc^{k}
$$
The test gives:
$$
\frac{(k+1)\left| c \right| ^{k+1}}{k\left| c \right| ^{k}}=\frac{k+1}{k}\left| c \right| \to \left| c \right| 
$$
We get absolute convergence for $|c|<1$ and divergence for $\left| c \right|>1$
___
$$
d_{k}=\frac{(c+3)^{k}}{k^{3}\times 5^{k}}
$$
The ratio test gives:
$$
\frac{|c+3|^{k+1}}{(k+1)^{3}\times 5^{k+1}}\times \frac{k^{3}\times 5^{k}}{\left| c+3 \right| ^{k}}=\frac{\left| c+3 \right| }{5}\times \frac{k^{3}}{(k+1)^{3}}\to \frac{\left| c+3 \right|}{5}
$$
So we get absolute convergence for $\frac{\left| c+3 \right|}{5}<1\iff c\in(-8,2)$, and divergence for $c\in(-\infty,-8)\cup(2,\infty)$
If $c=2$, then $d_{k}=\frac{5^{k}}{k^{3}\times 5^{k}}=\frac{1}{k^{3}}$ and we get absolute convergence
If $c=-8$, then $d_{k}=\frac{(-5)^{k}}{k^{3}\times 5^{k}}=\frac{(-1)^{k}}{k^{3}}$ which is also absolutely convergent
___
$$
e_{k}=(2+(-1)^{k})c^{k}
$$
$$
\left| \frac{e_{k+1}}{e_{k}} \right| =\frac{(2+(-1)^{k+1})|c|^{k+1}}{(2+(-1)^{k})|c|^{k}}=\frac{2\pm 1}{2 \mp 1}|c|
$$
Which does not converge, but we could look at the $\limsup_{ k \to \infty }\left| \frac{e_{k+1}}{e_{k}} \right|=3|c|$, and so for $|c|<\frac{1}{3}$, we get aboslute convergence, and using a similar argument with liminf, we get if $|c|>3$ we have divergence

#Mathematics #Analysis #Theorem