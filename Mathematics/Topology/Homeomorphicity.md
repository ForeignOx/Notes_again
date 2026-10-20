## Definition
Let $X,Y$ be [[Topology|topological]] spaces. A [[Functions|map]] $f:X\to Y$ is called a homeomorphism if $f$ is a [[Bijective Functions|bijection]], and $f^{-1}:Y\to X$ is [[Continuity|continuous]]
If a homeomorphism between $X$ and $Y$ exists, we say that $X$ and $Y$ are homeomorphic, and write $X\approx Y$
## Example
The interval $(0,1)$ is homeomorphic to $\mathbb{R}$, we can do this in two steps, $h(x)=\frac{1}{x}$ gives us a homeomorphism from $(0,1)\to(1,\infty)$, then $k(x)=\log(x-1)$ gets a homeomorphism from $(1,\infty)\to \mathbb{R}$
___
The interval $[0,1)$ is not homeomorphic to $\mathbb{R}$, since we wouldn't know where to map 0. We will prove this later...
___
Consider $\mathbb{R}^{n}$ with the various [[Metric Spaces|metric]] topologies. We have already seen that $d_{1},d_{2}$ and $d_{\infty}$ all produce the same topologies
For the discrete metric $d$, we get 
$$
\mathbb{1}:(\mathbb{R}^{n},\mathcal{T}_{d})\to(\mathbb{R}^{n},\mathcal{T}_{d_{2}})
$$
is continuous, while
$$
\mathbb{1}:(\mathbb{R}^{n},\mathcal{T}_{d_{2}})\to(\mathbb{R}^{n},\mathcal{T}_{d})
$$
Is not; there are sets $U\subseteq \mathbb{R}^{n}$ open with the discrete topology (indeed every subset is open) that are not open in the standard topology
## Lemma
Let $X,Y,Z$ be topological spaces, and $f:X\to Y$, $g:Y\to Z$ be maps, then $g\circ f:X\to Z$ is a map
### Proof
Let $U\subseteq Z$ be open. Then $(g\circ f)^{-1}(U)=f^{-1}(g^{-1}(U))$, which is an open set, as $f$ and $g$ are continuous
___
We can also check continuity using closed sets
## Lemma
Let $X,Y$ be topological spaces and $f:X\to Y$ a function. Then $f$ is continuous iff $f^{-1}(A)$ is closed in $X$ for every closed $A\subseteq Y$
### Proof
This simply follows from the equality:
$$
f^{-1}(Y\setminus U)=X\setminus f^{-1}(U)
$$
Which holds for any subset $U\subseteq Y$
Many intereting sets can be written as pre-images via continuous maps