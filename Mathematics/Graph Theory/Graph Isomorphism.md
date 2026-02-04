Two [[Simple Graphs|simple]] [[Graphs|graphs]] $G_{1}=(V_{1},E_{1}),G_{2}=(V_{2},E_{2})$ are [[Isomorphisms|isomorphic]], written $G_{1}\simeq G_{2}$ if there exists $\varphi :V_{1}\to V_{2}$ which is a [[Bijective Functions|bijection]] and preserves adjacency, i.e. $uv\in E_{1}\iff \varphi(u)\varphi(v)\in E_{2}$
In particular, we must certainly have $\left| V_{1} \right|=\left| V_{2} \right|$ and $\left| E_{1} \right|=\left| E_{2} \right|$; but we must also be able to relabel the vertices of $V_{1}$ to have the same labels as $V_{2}$ in such a way that the relabelled $E_{1}$ matchs $E_{2}$
___
The reason this is useful, is because when we draw graphs, it can help us identify whether two drawings of graphs are in fact the same graph
## Example
![[Graph Isomorphism 2025-01-26 23.28.39.excalidraw]]
It is fairly clear what we need our function $\varphi$ to do; we must have $\varphi(d)=x$ and $\varphi(c)=v$. We can then set $\varphi(a)=u$ and $\varphi(b)=w$. We must check this preserves adjacency. We see
$$
ab\mapsto \varphi(a)\varphi(b)=uw
$$
$$
 ac\mapsto \varphi(a)\varphi(c)=uv
$$
$$
 bc\mapsto \varphi(b)\varphi(c)=wv
$$
$$
 cd \mapsto \varphi(c)\varphi(d)=vx
$$
And so we have an edge in $G_{1}$ iff $\varphi$ produces a corresponding edge in $G_{2}$, and $G_{1}\simeq G_{2}$ as required

#Mathematics #Graphs #Definition 