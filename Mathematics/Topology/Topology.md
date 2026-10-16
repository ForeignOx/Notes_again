## Definition
Let $X$ be a [[Sets|set]], a topology on $X$ is a [[Subsets|subset]] $\mathcal{T}$ of the [[Power Sets|power set]] $2^{X}=\left\{ A\subseteq X \right\}$ which satisfy the following:
- $\emptyset$ and $X$ are in $\mathcal{T}$
- Arbitrary unions of elements in $\mathcal{T}$ is in $\mathcal{T}$; if $U_{i}\in \mathcal{T}$ for all $i\in I$, then $\bigcup_{i\in I}U_{i}\in\mathcal{T}$ 
- Finite intersections of elements in $\mathcal{T}$ is in $\mathcal{T}$; if $U_{1},U_{2}\in \mathcal{T}$, then $U_{1}\cap U_{2}\in\mathcal{T}$
The pair $(X,\mathcal{T})$ is called a topological space, and the elements of $\mathcal{T}$ are called the open subsets of $X$
A subset $A\subseteq X$ is called closed if $X\setminus A\in\mathcal{T}$ is open
## Example
If $M$ is a [[Metric Spaces|metric space]], the collection $\mathcal{T}_{d}$ of open sets in $M$ forms a topology; we defined a subset $U\subseteq M$ to be open if for every $x\in U$, there is $\varepsilon>0$ such that $B(x;\varepsilon)\subseteq U$
For $\mathbb{R}^{n}$ the metrics $d_{1},d_{2},d_{\infty}$ all have the same open sets and give the standard topology on $\mathbb{R}^{n}$
## Definition
We call a topological space $(X,\mathcal{T})$ metrisable if there is a metric $d$ on $X$ such that $\mathcal{T}=\mathcal{T}_{d}$
## Lemma
Let $X$ be a topological space, then
- $X$ and $\emptyset$ are closed
- A finite union of closed sets is closed
- An arbitrary intersection of closed sets is closed
We tend to simply call $X$ a topological space
## Example
If $X$ is a set and $\mathcal{T}=2^{X}$, then $(X,\mathcal{T})$ is a topological space. In this case, $\mathcal{T}$ is called the discrete topology. This is metrizable via the discrete metric
For a topology that is not metrizable, we can go to the other extreme, the minimal topology that can be put on a set:
Let $X$ be a set and let $\mathcal{T}=\left\{ \emptyset,X \right\}$, this topology is called the indiscrete topology and if $X$ has more than 1 element, then $X$ with the indiscrete topology is not metrizable
