## Definition
If $X_{n}$ is a [[Sequences|sequence]] of [[Random Variables|random variables]], then $X_{n}\to X$ in [[Probabilities|probability]] iff for every $\varepsilon>0$
$$
\mathbb{P}(\left| X_{n}-X \right| >\varepsilon)\to 0
$$
As $n\to \infty$
## Example
Suppose $X_{n}$ are random variables such that $\mathbb{P}(X_{n}=0)=p_{n}$ and $\mathbb{P}(X_{n}=1)=1-p_{n}$, so
$X_{n}\to X$ in probability if $p_{n}\to 1$
Fixing $\varepsilon>0$,
$$
\mathbb{P}(\left| X_{n} \right| >\varepsilon)=\mathbb{P}(X_{n}=1)=1-p_{n}
$$
So if $p_{n}-1$ as $n\to \infty$, then
$$
\lim_{ n \to \infty } \mathbb{P}(\left| X_{n} \right| >\varepsilon)=0
$$
As required
## Proposition
If $X_{n}\to X$ in probability and $f:\mathbb{R}\to \mathbb{R}$ is a [[Continuity|continuous]] [[Functions|function]], then
$$
f(X_{n})\overset{p}\to f(X) 
$$
### Proof
We know $\mathbb{P}(\left| X_{n}-X \right|>\varepsilon)\to 0$ as $n\to \infty$, we want $\mathbb{P}(\left| f(X_{n})-f(X) \right| >\varepsilon)\to 0$ also
Since $f$ is continuous, for any $x,\varepsilon>0$, there is a $\delta>0$ such that 
$$
\left| x-y \right| <\delta\implies \left| f(x)-f(y) \right| <\varepsilon
$$
Applying this to $x=X$, given $\varepsilon>0$, thwere is a $\delta>0$ such that 
$$
\left| X-y \right|<\delta\implies \left| f(X)-f(y) \right| <\varepsilon
$$
Hence
$$
\left| f(X)-f(y) \right| \geq\varepsilon\implies \left| X-y \right| \geq \delta
$$
This means that the probability
$$
\mathbb{P}(\left| f(X)-f(y) \right| \geq\varepsilon)\leq \mathbb{P}(\left| X-y \right| \geq \delta)
$$
Substituting $y=X_{n}$,
$$
\mathbb{P}(\left| f(X)-f(X_{n}) \right| \geq \varepsilon)\leq \mathbb{P}(\left| X-X_{n} \right| \geq \delta)
$$
Letting $\delta=\frac{\varepsilon}{2}$,
$$
\mathbb{P}(\left| f(X_{n})-f(X) \right| >\varepsilon)\leq \mathbb{P}\left( \left| f(X_{n}-f(X)) \right| \geq \frac{\varepsilon}{2} \right) \leq \mathbb{P}(\left| X_{n}-X \right| \geq\delta')
$$
By squeeze theorem, this implies
