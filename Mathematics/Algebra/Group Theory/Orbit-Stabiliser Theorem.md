## Theorem
Let $G$ be a [[Groups|group]] [[Group Action|acting]] on the [[Sets|set]] $X$, let $x\in X$, then there exists a [[Bijective Functions|bijection]] $\beta$ which maps [[Orbits and Stabilisers|$\text{orb}(x)$]] to the [[Cosets|left cosets]] of $\text{stab}(x)$ in $G$ given by
$$
\beta(g x)=g\text{stab}(x)
$$
In particular, if $G$ is finite then
$$
\left| \text{orb}(x) \right| =\frac{\left| G \right|}{\left| \text{stab}(x) \right| }
$$
### Proof
$\beta$ is well defined as if $g x=hx$, then $h^{-1} g x=x$, so $h^{-1}g\in\text{stab}(x)$, so
$$
\beta( g x)=g \text{stab}( x)= h\text{stab}(x)=\beta(hx)
$$
To see $\beta$ is a bijection, we first check whether it is [[Surjective Functions|surjective]], and it is a for any $g\text{stab}(x)$, we have $\beta(g x)=g\text{stab}(x)$
$\beta$ is also [[Injective Functions|injective]] as if $\beta( gx)=\beta(hx)$ then $h^{-1}g\in \text{stab}(x)$, so $h^{-1}gx=x$, i.e. $g x=h x$
If $\left| G \right|<\infty$, then bijection means that 
$$
\left| \text{orb}(x) \right|=\left| \text{left cosets of }\text{stab}(x) \right|=\frac{\left| G \right|}{\left| \text{stab}(x) \right|}
$$
## Examples
Reviit the conjugacy classes of $D_{5}$, we know $\text{orb}(r)=\left\{ r,r^{4} \right\}$, $\text{stab}(r)=\left< r \right>$, so 

$$
\left| \text{stab}(r) \right| =5,\left| \text{orb}(r) \right| =2,\left| D_{5} \right| =10
$$
And $2=\frac{10}{5}$ as expected
We know $\left| \text{orb}(s) \right|=5$, so we expect $\left| \text{stab}(s) \right|=2$, which we can check:
$$
\text{stab}(s)=\left\{ r ^{i}\mid| r^{i}s r^{-i} \right\}\cup \left\{r^{i}s\mid (r^{i}s)s(r^{i}s)^{-1}=s \right\}
$$
$$
= \left\{ r^{i}\mid r^{2i}=e \right\}\cup \left\{ r^{i}s\mid r^{2i}=e \right\}=\left\{ e,s \right\}
$$

