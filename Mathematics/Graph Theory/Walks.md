Given a [[Graphs|graph]] $G=(V,E,\phi)$, a walk in $G$ is a sequence of vertices $w_{0},w_{1},\dots,w_{k}$ from $V$ together with edges $e_{1},e_{2},\dots,e_{k}$ in $E$ such that $\phi(e_{i})=\{ w_{i-1},w_{i} \}$ for all $1\leq i\leq k$
We sometimes write such a walk as
$$
\gamma=w_{0}e_{1}w_{1}e_{2}\dots w_{k-1}e_{k}w_{k}
$$
Note there being one more vertex than edge
We say that $\gamma$ is a walk in $G$ from $u$ to $v$ when $\gamma=w_{0}e_{1}w_{1}e_{2}\dots w_{k-1}e_{k}w_{k}$ is a walk in $G$ such that $w_{0}=u$ and $w_{k}=v$
## Length
The length of a walk is the number of edges it contains, i.e. it is $k$
## Closed Walks
If $w_{0}=w_{k}$, we say that the walk is closed
## Simple Graphs
For a [[Simple Graphs|simple graph]], we don't need to be specific which edge we travel down, so you can simply specify the vertices taken; e.g.
$$
\gamma=(w_{0}w_{1}\dots w_{k})
$$

#Mathematics #Graphs #Definition 