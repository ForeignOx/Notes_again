Let $f_{n}$ be a [[Sequences of Functions|sequence]] of [[Functions|functions]] with [[Continuity|continuous]] [[Differentiation|derivatives]] $f_{n}'(x)$. Assume that $f_{n}\to f$ [[Pointwise Limit|pointwise]] and $f_{n}'\to g$ [[Uniform Convergence|uniformly]] for some function $g(x)$. Then $f(x)$ is differentiable and $f'(x)=g(x)=\lim_{ n \to \infty }f_{n}'(x)$
## Proof
Have 
$$
f_{n}(x)=f_{n}(a)+\int_{a}^{x} f_{n}'(t) \, dt
$$
by the [[Fundamental Theorem of Calculus|FToC]], as $n\to \infty$, $f_{n}(x)\to f(x)$, $f_{n}(a)\to f(a)$, $\int_{a}^{x} f_{n}'(t) \, dt\to\int_{a}^{x} g(t) \, dt$ using [[Convergence of Integrals|convergence of integrals]], so we have our claim;
$$
f(x)=f(a)+\int_{a}^{x} g(x) \, dx 
$$
Hence $f'(x)=g(x)$
Now we don't actually need to be so strict about the convergence of $f_{n}$, we actually only need it to converge at $x=a$
