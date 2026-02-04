## Theorem for [[Principle Ideal Domains|Principle Ideal Domains]]
Let [[Rings|$R$]] be a PID, if $a_{1},a_{2},\dots,a_{k}\in R$, are pairwise coprime elements, then the map 
$$
\varphi: R/(a_{1},a_{2},\dots,a_{k})\to R /(a_{1})\times\dots \times R /(a_{k})
$$
$$
 r+(a_{1},\dots, a_{k})\to(r+(a_{1}),\dots,r+(a_{k}))
$$
Is an isomorphism

### Proof omitteed :(

## Examples
This is a generalisation of the [[Isomorphisms|isomorphism]] $\mathbb{Z} /6\cong \mathbb{Z}/2\times \mathbb{Z} /3$ using the [[Homomorphisms|homomorphism]] 
$$
\varphi :\mathbb{Z} /6 \to \mathbb{Z} /2\times \mathbb{Z} /3
$$
$$
 n\mapsto (\overline{n},\overline{n})
$$
$\text{ker}(\varphi)=6\mathbb{Z} = (6)$, so by the [[First Isomorphism Theorem|first isomorphism theorem]], $\mathbb{Z} /6 \cong \mathbb{Z} /2 \times \mathbb{Z} /3$ as injectivity implies surjectivity since $\left| \mathbb{Z} /6 \right| = 6 = \left| \mathbb{Z} /2\times \mathbb{Z} /3 \right|$
___
Similarly for polynomials $f(x)\in \mathbb{F}[x]$, $f(x)=g(x)h(x)$ coprime factors
So the CRT for polynomials says that
$$
\mathbb{F}[x] /(f(x))\rightarrow \mathbb{F}[x]/(g(x))\times \mathbb{F}[x] /(h(x))
$$
$$
 p(x)+(f(x))\mapsto (p(x)+(g(x)),p(x)+(h+x))
$$
is an isomorphism
___
$\mathbb{Q}[x] /(x^{2}-x)\cong \mathbb{Q}[x] /(x) \times \mathbb{Q}[x]  /(x-1)$, but $Q[x] /(x)\cong \mathbb{Q}$ (by taking the evaluation map at 0), and similarly $\mathbb{Q}[x ] /(x-1)\cong \mathbb{Q}$ (by taking the evaluation map at 1), thus
$$
\mathbb{Q}[x] /(x^{2}-x)\cong \mathbb{Q}^{2}
$$
