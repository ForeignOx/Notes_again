A graph is a set of vertices joined by edges
Given a finite [[Sets|set]] $V$, let $\mathbb{V}=\{ \{ a,b \},a,b\in V,a \}$ be the set of subsets of $V$
## Finite Undirected Graph
A finite undirected graph $G$ is an ordered triple $(V,E,\Phi)$, where $V,E$ are finite sets and 
$$
\Phi:E\to \mathbb{V}
$$
Where $V$ is the vertex set, $E$ is the edge set and $\Phi$ is the incidence function, so if $\phi(e)=\{ a,b \}$, then $e$ is incident to $a$, $e$ is incident to $b$; $a,b$ are the endpoints of $e$
## Example
![[Graph 2025-01-16 15.12.38.excalidraw]]
The above graph has vertex set:
$$
V=\{ a,b,c,d,e,f \}
$$
And edge set:
$$
E=\{ ab,ac,bc,cd,de \}
$$
Here $\phi(a,b)=\{ a,b \}$, this is not always the case
___
![[Graph 2025-01-16 15.22.29.excalidraw]]
The above picture is a drawing of an undirected graph with vertex set $V=\{ a,b,c \}$, edge set $E=\{ e_{1},e_{2},e_{3},e_{4} \}$ and incidence function given by $\phi(e_{1})=\phi(e_{2})=\{ a,b \},\phi(e_{3})=\{ c,d \},\phi(e_{4})=\{ a,c \}$
## Incidence Matrix
One may represent the graph $G=(V,E,\phi)$ with $V=\{ v_{1},\dots,v_{n} \}$ and $E=\{ e_{1},\dots,e_{m} \}$ using the incidence [[Matrices|matrix]] $(B(i,j),i\neq \ln,j\leq m)$ defined by
$$
B(i,j):=\begin{cases}
1&\text{if }v_{i}\in \phi(e_{j})\\0&\text{otherwise}
\end{cases}
$$
Or using the [[Indicator Function|indicator function]]:
$$
B(i,j):=\mathbb{1}_{\{ v\in \phi(e) \}}
$$
### Example
For the graph:
![[Pasted image 20250126215437.png]]
The incidence matrix will be
![[Pasted image 20250126215558.png]]
## Alternate Representations
It is possible to extend from the graphs considered here to graphs that also allow loops, i.e, edges whose two endpoints are the same vertex. We can also consier graphs whose edges are directed, that is, with a defined start-point and end-point. To account for these features requires us to modify our formal definitions a little, but is not difficult

#Mathematics #Graphs #Definition 