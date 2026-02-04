A [[Graphs|graph]] $G$ is connected if, given any two vertices $u,v$ of $G$, there is a [[Paths|path]] in $G$ from $u$ to $v$
## Connected Components
A connected component of $G=(V,E)$ is a [[Subgraphs|subgraph]] $G_{1}=(V_{1},E_{1})$ such that
1. $G_{1}$ is connected
2. for every edge $e=uv\in E$, where $u,v\in V_{1}$, then $e\in E_{1}$ and
3. for any $u\in V_{1}$ and $w\in V\setminus V_{1}$ there is no path in $G$ from $u$ to $w$
A connected component of $G$ is a connected subgraph of $G$ that is not part of any larger connected subgraph of $G$, in other words, it is a maximally connected subgraph of $G$
Then, two vertices of $G$ lie in the same connected component iff there is a path in $G$ between them. If $G$ is not connected, then it has two or more connected components

#Mathematics #Graphs #Definition 