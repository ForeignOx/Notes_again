If $f(x)$ is a [[Continuity|continuous]] [[Functions|function]] on a closed [[Intervals|interval]] $[a,b]$, then it is [[Boundedness|bounded]] on that interval, and has upper and lower bounds:
$$
\exists U,L\in [a,b]:f(L)\leq f(x)\leq f(U)\forall x\in [a,b]
$$
Note this does not work for open intervals, take for a counterexample $\frac{1}{x}$ in $(0,1)$, there is no max
Together wth the [[Intermediate Value Theorem|Intermediate Value Theorem]], we get that the [[Image|image]] of a continuous function on a compact interval is again a compact interval
## Proof
We'll only do max, as minimum is the same... (pls do min tooooo :sob:)
### Step 1
$f$ is bounded above on $[a,b]$ if wasn't bounded, then given $n\in\mathbb{N}$, there would exist a [[Sequences|sequence]] $x_{n}\in[a,b]:f(x_{n})\geq n$,  by [[Bolzano-Weierstrass Theorem|Bolzano-Weierstrass]], there exists a [[Convergence|converging]] [[Subsequences|subsequence]] $x_{n_{i}}$ with limit $c\in[a,b]$ (note this is closed interval)
Then $f(\underbrace{ n_{i} }_{ \geq n_{i} })\to f(c)\in\mathbb{R}$, but at some point $n_{i}>c$. Hence, $\text{sup}(f([a,b]))$ exists in $\mathbb{R}=:M$
Same goes for minimum
### Step 2
There exists a sequence $y_{n}\in f([a,b])$ such that $\lim_{ n \to \infty }y_{n}=M$, and $y_{n}=f(x_{n})$ with $x_{n}\in[a,b]$, by continuity, we want to show $\lim_{ n \to \infty }f(x_{n})=M$, these $x_{n}$ might not actually converge but by Bolzano-Weierstrass, $x_{n}$ will ahve a converging subsequence in $[a,b]$, so $\lim_{ n \to \infty }f(x_{n_{i}})=\lim_{ n \to \infty }y_{n_{i}}=M$, so the 
## Complex Version
Let $K$ be a [[Sequential Compactness|sequenctially compact]] subset of $\mathbb{C}$ and let $f:K\to \mathbb{R}$ be continuous. Then $f$ attains its minimum and maximum on $K$
$f$ maps to $\mathbb{R}$
### Proof
Just like real analysis
## Corollary
- If $K$ is a closed and bounded set in $\mathbb{C}$, then $\left| z \right|,\mathfrak{R}(z),\mathfrak{I}(z)$ attain their minimum and maximum on $K$
- If $K$ is a closed and bounded set in $\mathbb{C}$ and $f:K\to \mathbb{C}$ or $\mathbb{R}$ is continuous, then $\left| f(z) \right|$ attains its minimum and maximum on $\mathbb{R}$
To simplify notation, we often refer to sequentially compact sets as compact sets. Theree is a more general ntion of compacness, but oh well

#Mathematics #Analysis #Theorem 