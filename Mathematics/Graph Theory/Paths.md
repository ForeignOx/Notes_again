A path in [[Graphs|$G=(V,E,\phi)$]] is a [[Trails|trail]] $w_{0}e_{1}w_{1}e_{2}\dots w_{k-1}e_{k}w_{k}$ such that the vertices are $w_{1},w_{1},\dots,w_{k}$ are distinct
## If there is a Walk between Vertices, there is also a Path
Given vertices $u\neq v$ in a graph $G$, if there exists a [[Walks|walk]] from $u$ to $v$ in $G$, then there is a path in $G$ from $u$ to $v$
### Proof
Let $\gamma$ be a walk in $G$ consisting of the vertices $(w_{i})_{0\leq i\leq k}$, $w_{0}=u$, $w_{k}=v$ and edges $(e_{i})_{1\leq i\leq k}$
If $w_{0},\dots,w_{k-1}$ are all distint, then $\gamma$ is a path. If not, let $w_{j}$ be the first occurrence in $\gamma$ of a vertex which appears more than once, and let $w_{j'}$ be the latest occurrence in $\gamma$ of that vertex, e.e. let $j'$ be the greatest index for which $w_{j'}=w_{j}$. Let $\gamma'$ be the walk formed from $\gamma$ by removing the vertices $w_{j+1},\dots,w_{j}$ and the edges $e_{j+1},\dots,e_{j'}$, i.e. if you think about the graph having a loop, remove the entire loop. Then $w_{j}$ appears only once in $\gamma'$ and so the number of repeated vertices in $\gamma'$ is strictly smaller than $\gamma$. Repeat this process with any remaining vertices in $\gamma'$ which appear more than once, until we have a path

#Mathematics #Graphs #Definition #Theorem 