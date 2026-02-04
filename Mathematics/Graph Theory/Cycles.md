A cycle is a [[Walks#Closed Walks|closed]] [[Paths|path]], i.e. $w_{0}=w_{k}$ with $k\geq 1$
## Lemma
If every vertex in a (finite) graph $G=(V,E,\phi)$ has a degree strictly larger than $1$, then $G$ contains a cycle
### Proof
Let $\left| V \right|=n$. Starting from any vertex $u$ in $G$, then as [[Degree of Vertices|$d(u)>1$]], there is some edge $e$ such that $u\in\phi(e)=\{ u,v \}$. Letting $u=w_{0}$, $v=w_{1}$,a dn $e_{1}=\{ w_{0},w_{1} \}$, we construct a cycle in $G$ as follows. At $w_{1}$ (in general at a 'new' vertex $w_{i}$) we have $d(w_{1})>1$, then there must be some edge $e_{2}=(w_{1},w_{2})\neq e_{1}$ (in general some edge $e_{i+1}=(w_{i},w_{i+1})\neq e_{i}$) and there are two possibilities
1. The vertex $w_{i+1}$ has already been visited, i.e. $w_{i+1}\in\{ w_{0},\dots,w_{i} \}$; or
2. The vertex $w_{i+1}$ is an unvisited "new" vertex, i.e. $w_{i+1}\not\in\{ w_{0},\dots,w_{i} \}$
Since we cannot find more than $n$ "new" vertices, at some point $i\leq n-1$, we must have $w_{i+1}=w_{k}\in\{ w_{0},\dots,w_{i} \}$ with $0\leq k<i$. Then the path
$$
\gamma=w_{k}e_{k+1}w_{k+1}\dots w_{i}e_{i+1}w_{i+1}
$$
Is a cycle in $G$ as required

#Mathematics #Graphs #Definition #Theorem