If we have a [[Functions|function]] $f:X\to \mathbb{R}$ on an [[Intervals|interval]] $X$ if uniformly [[Continuity|continuous]] if
$$
\forall\varepsilon>0\exists\delta>0:\forall c,x\in X\text{ with }\left| x-c \right| <\delta\implies \left| f(x)-f(c) \right| <\varepsilon
$$
This is different as now $\delta$ has to be the same for all values of $c\in X$, so $\delta$ no longer depends on the individual point $c$ (but still of $f$ and $\varepsilon$). In particular, uniform continuity is no longer a local concept, but a global one, so is a more powerful result
## Not Uniformly Continuous
The contrapositive, a function is not uniformly continuous if:
$$
\exists\varepsilon>0:\forall\delta>0\exists c,x\in X\text{ with }\left| x-c \right| <\delta\implies \left| f(x)-f(c) \right| \geq\varepsilon
$$

## Remarks
The proof is non-constructive and gives no indication for finding $\delta$. In general this is very difficult
This is what leads to integration later on…
A particularly nice class of functions are Lipschitz-continuous
- The function $e^{ x }$ is not uniformly continuous on $\mathbb{R}$. However, $\ln x$ is uniformly continuous on $[1,\infty)$ even though both functions diverge as $x\to \infty$

#Mathematics #Analysis #Definition