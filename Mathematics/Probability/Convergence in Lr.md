## Definition
If we have a [[Sequences|sequence]] of [[Random Variables|random variables]] $(X_{n})_{n\geq 1}$, then $X_{n}\to X$ in [[Lr Space|$L^{r}$]] if
- $\mathbb{E}(\left| X_{n} \right|^{r})<\infty$ for every $n$, and
- $\mathbb{E}(\left| X_{n}-X \right|^{r})\to 0$ as $n\to \infty$
## Remark
Such convergence is also known as convergence in the $r$-th mean. Two special cases are of particular importance; when $r=1$ the sequence $X_{n}$ converges to $X$ in mean, $L^{1}$, similarly, when $r=2$, the sequence converges in mean square, $L^{2}$
## Example
Let $U(0,1)$ be a [[Uniform Distribution|uniform]] random variable, and let
$$
X_{n}(\omega)=n\mathbb{1}_{\left\{ U(\omega)\leq \frac{1}{n} \right\}}
$$
Considering the [[Expectation|expectations]]
$$
\mathbb{E}(\left| X_{n} \right| ^{r})=\mathbb{E}\left( n^{r}\mathbb{1}_{\left\{ U\leq \frac{1}{n} \right\}} \right)=n^{r}\mathbb{P}\left( U\leq \frac{1}{n} \right)=\frac{n^{r}}{n}=n^{r-1}<\infty
$$
Does $X_{n}\to 0$ in $L^{r}$?
We need
$$
\mathbb{E}(\left| X_{n}-0 \right|^{r} )=\mathbb{E}(\left| X_{n} \right|^{r} )\to 0
$$
Which is true for $r<1$, so $X_{n}\to 0$ in $L^{r}$ for $0<r<1$
Otherwise $X_{n} \not\to 0$ in $L^{r}$
___
Let $(X_{n})_{n\in\mathbb{N}}$ be a sequence of random variables such that for some real numbers $(a_{n})_{n\in\mathbb{N}}$, we have
$$
\mathbb{P}(X_{n}=a_{n})=p_{n},~\mathbb{P}(X_{n}=0)=1-p_{n}
$$
Then $X_{n}\overset{L^{r }}\to 0$ iff $\mathbb{E}(\left| X \right|^{r})\equiv \left| a_{n} \right|^{r}p_{n}\to 0$
## Proposition
Suppose $X_{n}\to X$ in $L^{r}$ for $r\geq 1$, then $\mathbb{E}(X_{n})\to \mathbb{E}(X)$
### Proof
We know $X_{n}\to X$ in $L^{r}$, we want $\mathbb{E}(X_{n})\to \mathbb{E}(X)$
So we want to show for any $\varepsilon>0$, then
$$
\left| \mathbb{E}(X_{n})-\mathbb{E}(X) \right|<\varepsilon \forall n\geq N_{\varepsilon} 
$$
$$
0\leq \left| \mathbb{E}(X_{n})-\mathbb{E}(X) \right| =\left| \mathbb{E}(X_{n}-X) \right| \leq \mathbb{E}(\left| X_{n}-X \right| )
$$
Let $\varepsilon'>0$,
$$
A=\left\{ \left| X_{n}-X \right| \leq\varepsilon' \right\}\implies A^{c}=\left\{ \left| X_{n}-X \right| >\varepsilon' \right\}
$$
$$
\mathbb{E}(\left| X_{n}-X \right| )=\mathbb{E}(\left| X_{n}-X \right|\mathbb{1}_{A} )+\mathbb{E}(\left| X_{n}-X \right| \mathbb{1}_{A^{c}})
$$
First, 
$$
\mathbb{E}(\left| X_{n}-X \right| \mathbb{1}_{A})\leq \mathbb{E}(\varepsilon' \mathbb{1}_{A})=\varepsilon'\mathbb{P}(A)\leq\varepsilon'
$$
Secondly
$$
\mathbb{E}(\left| X_{n}-X \right| \mathbb{1}_{A^{c}})
$$
On $A^{c}$, 
$$
\left| X_{n}-X \right| >\varepsilon' \iff \frac{\left| X_{n}-X \right| }{\varepsilon'}>1
$$
If $a\geq 1$ and $r\geq 1$, then $a^{r}\geq a$, so
$$
\left( \frac{\left| X_{n}-X \right| }{\varepsilon'} \right)^{r} \geq \frac{\left| X_{n}-X \right| }{\varepsilon'}
$$
On the event $A^{c}$, sooo
$$
\mathbb{E}(\left| X_{n}-X \right| \mathbb{1}_{A^{c}})\leq \mathbb{E}\left( \varepsilon'\left( \frac{\left| X_{n}-X \right| }{\varepsilon'} \right)\mathbb{1}_{A^{c}} \right)=(\varepsilon')^{1-r}\mathbb{E}(\left| X_{n}-X \right| ^{r}\mathbb{1}_{A^{c}}) \leq (\varepsilon')^{1-r}\mathbb{E}(\left| X_{n}-X \right| )
$$
We conclude
$$
\mathbb{E}(\left| X_{n}-X \right| )\leq \varepsilon'+(\varepsilon')^{1-r}\mathbb{E}(\left| X_{n}-X \right|^{r} )
$$
Given $\varepsilon'>0$, since $\mathbb{E}(\left| X_{n}-X \right|^{r})\to 0$, there is an $N_{\varepsilon'}$ such that if $n\geq N_{\varepsilon'}$, then
$$
\mathbb{E}(\left| X_{n}-X \right| ^{r})<(\varepsilon')^{r}
$$
So for $n>N_{\varepsilon'}$,
$$
\mathbb{E}(\left| X_{n}-X \right| )\leq \varepsilon'+(\varepsilon')^{1-r}(\varepsilon')^{r}=2\varepsilon'
$$
So finally choosing $\varepsilon'=\frac{\varepsilon}{ 2}$, then we have what we want:
$$
\left| \mathbb{E}(X_{n}-X) \right|<\varepsilon \text{ for }n>N_{\frac{\varepsilon}{2}} 
$$
## Proposition
For $L^{r}$ convergence, we get various results:
Since $\mathbb{E}(\left| X \right|)^{2}\leq \mathbb{E}(X^{2})$, If we let $X=Y_{n}-Y$, then
$$
\mathbb{E}(\left| Y_{n}-Y \right| )\leq \mathbb{E}((Y_{n}-Y)^{2})^{\frac{1}{2}}
$$
So if $Y_{n}\to Y$ in $L^{2}$, then $Y_{n}\to Y$ in $L^{1}$, and in fact,
If $r\leq s$, then $L^{s}\to L^{r}$ i.e. if $X_{n}\to X$ in $L^{s}$, then $X_{n}\to X$ in $L^{r}$
### Proof
$$
\mathbb{E}(\left| X_{n}-X \right| ^{s})\to 0
$$
We want $\mathbb{E}(\left| X_{n}-X\right|^{r})\to 0$ where $r\leq s$
Given $\varepsilon>0$, there is $N$ such that if $n>N$, then
$$
\mathbb{E}(\left| X_{n}-X \right| ^{s})<\left( \frac{\varepsilon}{2} \right)^{\frac{s}{r}}
$$
Letting $A=\left\{ \left| X_{n}-X \right|\leq \left( \frac{\varepsilon}{2} \right)^{\frac{s}{r}} \right\}$
$A^{c}$ is such that
$$
\frac{\left| X_{n}-X \right| }{\left( \frac{\varepsilon}{2} \right)^{\frac{1}{r}}}>1
$$
$$
\implies \left(  \frac{\left| X_{n}-X \right| }{\left( \frac{\varepsilon}{2} \right)^{\frac{1}{r}}} \right)^{r}\leq \left(  \frac{\left| X_{n}-X \right| }{\left( \frac{\varepsilon}{2} \right)^{\frac{1}{r}}} \right)^{s}
$$
$$
\implies \left| X_{n}-X \right| ^{r}\leq \left( \frac{\varepsilon}{2} \right)^{\frac{s}{r}}\left| X_{n}-X \right| ^{s}
$$
Consider 
$$
\mathbb{E}(\left| X_{n}-X \right| ^{r})=\mathbb{E}(\left| X_{n}-X \right| ^{r}\mathbb{1}_{A})+\mathbb{E}(\left| X_{n}-X \right| ^{r}\mathbb{1}_{A^{c}})
$$
$$
\mathbb{E}(\left| X_{n}-X \right| ^{r}\mathbb{1}_{A})\leq \mathbb{E}\left( \left( \frac{\varepsilon}{2} \right)\mathbb{1}_{A} \right)= \frac{\varepsilon}{2}\mathbb{P}(A)\leq \frac{\varepsilon}{2}
$$
$$
 \mathbb{E}\left( \left| X_{n}-X \right| ^{r}\mathbb{1}_{\left\{ \left| X_{n}-X \right| > \left( \frac{\varepsilon}{2} \right)^{\frac{s}{r}} \right\}} \right)\leq \left( \frac{\varepsilon}{2} \right)^{1-\frac{s}{r}}\mathbb{E}(\left| X_{n}-X \right| ^{s})\leq \left( \frac{\varepsilon}{2} \right)^{1-\frac{s}{r}}
$$
___
