If a [[Graphs|graph]] has $\phi: E\to \mathbb{V}$ is [[Injective Functions|injective]], we say our graph is simple. A simple graph does not allow for multiple edges between the same pair of vertices
Simple graphs can be represented in a simpler form, using only the pair $(V,E)$, with $E\subset \mathbb{V}$ and the incidence function can be replaced with the adjacency relation:
## Adjacency
Two vertices $u,v\in V$ are said to be adjacent in the graph $G=(V,E)$ if $\{ u,v \}\in E$. For convenience, we write an edge such as $\{ a,b \}$ as $ab$ (or $ba$)
If a vertex is adjacent to no other vertex, it is isolated
## Adjacency Matrix
Similarly to how graphs can be represented by [[Graphs#Incidence Matrix|incidence matrices]], simple graphs $G=(V,E)$, with $V=\{ v_{1},\dots,v_{n} \}$ and $E=\{ e_{1},\dots,e_{m} \}$ can be represented using the more compact adjacency [[Matrices|matrix]] $(A(i,j),i,j\leq n)$ defined by
$$
A(i,j):=\begin{cases}
1&\text{if }v_{i}v_{j}\in E\\0&\text{otherwise}
\end{cases}
$$
Or using the [[Indicator Function|indicator function]]:
$$
A(i,j):=\mathbb{1}_{\{ v_{i}v_{j}\in E \}}
$$


#Mathematics #Graphs #Definition 
