Reliability theory concerns mathematical models of systems that may be functional depending on whether certain components function. If a component fails randomly, reliability theory helps find the [[Probabilities|probablity]] the network works, this will depend on the structure of the system
A reliability network is a diagram of arcs and nodes
Assumption: current flows/system works if we can draw arrows from one to the other
Let $W_{i}$, the [[Events|event]] that the $i$th component is working
We say that the system is working if we can go from left to right using working components only, then denote this event $S$
Let $p_{i}$ be the probability the $i$th component is working, that is, $\mathbb{P}(W_{i})=p_{i}$
Assumption: the components work [[Independence|independently]] of one another
## Series
![[Reliability Network 2024-10-28 15.48.38.excalidraw]]
System is functional if both components $\hspace{0pt}1$ and $\hspace{0pt}2$ are working:
$$
S=W_{1}\cap W_{2}
$$
Since they are independent, we also know:
$$
\mathbb{P}(S)=\mathbb{P}(W_{1})\mathbb{P}(W_{2})=p_{1}p_{2}
$$
## Parallel
![[Reliability Network 2024-10-28 15.50.57.excalidraw]]
System is functional if either or both $\hspace{0pt}1$ and $\hspace{0pt}2$ are working:
$$
S=W_{1}\cup W_{2}
$$
$$
\mathbb{P}(S)=\mathbb{P}(W_{1}\cup W_{2})=\mathbb{P}(W_{1})+\mathbb{P}(W_{2})-\mathbb{P}(W_{1}\cap W_{2})=\mathbb{P}(W_{1})+\mathbb{P}(W_{2})-\mathbb{P}(W_{1})\mathbb{P}(W_{2})=p_{1}+p_{2}-p_{1}p_{2}
$$

#Mathematics #Probability #Definition 