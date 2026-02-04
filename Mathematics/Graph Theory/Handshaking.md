For any [[Graphs|graph]] $G=(V,E,\Phi)$, we have $\sum_{v\in V}d(v)=2\left| E \right|$
## Proof
Each edge contributes $\hspace{0pt}2$ to the sum of [[Degree of Vertices|degrees]] - one to each vertex it is incident to. More formally, note that any edge $e\in E$ is incident to  exactly two vertices, i.e. $\sum_{v\in V}\mathbb{1}_{\{ v\in\phi(e) \}}=2$, so we have
$$
\sum_{v\in  V}d(v)=\sum_{v\in V}\sum_{e\in E}\mathbb{1}_{\{ v\in \phi(e) \}}=\sum_{e\in E}\sum_{v\in V}\mathbb{1}_{\{ v\in \phi(e) \}}=2\left| E \right| 
$$
## Corollary
In any graph, the number of odd-degree vertices is even
### Proof
Let $\left| V \right|=n$ and $\left| E \right|=m$, and let the number of vertices of odd degree by $k$. We have that the sum of degreees $\sum_{v\in V}d(v)=2m$ is even, and furthermore, the sum of the degrees of the $n-k$ vertices of even degree is a sum of even numbers, and thus is even. There muct be an even umber of terms for the sum (of odd numbers) to be even, and hence there must be an even number of vertices of odd degree
#
___
The name handshaking comes from the two ways you could count the hand-shakes at an event; the RHS is like counting each hand-shake as it happens, the LHS is like asking each person, at the end of the conference, how many times they shook hands

#Mathematics #Graphs #Theorem 