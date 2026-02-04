This is the [[Functions|function]]
$$
f(x)=\sum_{k=0}^{\infty} \frac{1}{2^{k}}\cos(15^{k}\pi x) 
$$
```desmos-graph
y=\sum_{n=0}^{30}\frac{1}{2^{n}}\cos\left(15^{n}\pi x\right)
```
And we claim this is [[Continuity|continuous]] on $\mathbb{R}$, since it is [[Uniform Convergence|uniformly convergent]] on $\mathbb{R}$, but [[Differentiation|differentiable]] nowhere
We need to estimate the sums to use the [[Weierstrass M-test|Weierstrass M-test]]:
$$
\left| \frac{1}{2^{k}}\cos(15^{k}\pi x) \right| \leq \frac{1}{2^{k}}=M_{k}
$$
And
$$
\sum_{k=0}^{\infty} \frac{1}{2^{k}}=\frac{1}{1-\frac{1}{2}}=2 
$$
So the $M_{k}$'s converge, so we have continuity :)