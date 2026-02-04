## Definition
We define a regular polygon to be an object satisfying these three properties:
- Its [[Symmetry Groups|symmetry group]] we denote $Sym(T)$ acts [[Transitive Actions|transitively]] on vertices of $T$
- For any vertex $v$, the [[Subgroups|subgroup]] [[Orbits and Stabilisers|$H=\text{stab}(v)$]] act transitively on edges containing $v$
- Moreover, the subgroup $H'$ of $H$ stabilising one particular edge $vv'$ acts transitively on the [[Sets|set]] of two faces containing $vv'$
## Example
If $T$ is a regular tetrahedrom, then $Sym(T)$ is its symmetry group. Given a vertex $v$ can be mapped to $\hspace{0pt}4$ vertices, then in $\text{stab}(v)$, there are $\hspace{0pt}3$ possiblities to choose where to send $v'$ and two possibilities to choose adjacent face $vv'v''$, hence
$$
\left| Sym(T) \right| =4\times 3\times 2=24
$$
$$
\text{orb}(v)=4
$$
So by the [[Orbit-Stabiliser Theorem|orbit-stabiliser]] theorem,  $\text{stab}(v)=\text{stab}(\triangle)=D_{3}$, so $\left| \text{stab}(v) \right|=6$ which is as expected
Moreover $Sym(T)$ acts by permutation on the vertices of $T$ (or on faces of $T$)
We can in fact conclude that [[Symmetric Groups|$Sym(T)\cong S_{4}$]]
Interestingly, rotation symmetries (without reflections) is the subgroup [[Alternating Group|$A_{4}$]] of even permutations 
___
Consider a cube $C$. 
$$
\left| Sym(C) \right| =8\cdot3\cdot 2=48
$$
Which is made up of considering the number of vertices, number of edges per vertex, and the number of faces next to an edge
For an octahedron:
$$
Sym(O)=6\cdot 4\cdot 2=48
$$
And in fact $Sym(O)=Sym(C)$, which we can see:
![[Regular Polyhedra 2025-12-03 11.49.19.excalidraw]]
We find that $S_{4}\subseteq Sym(C)$ as $S_{4}$ acts on the $\hspace{0pt}4$ principle diagonals by permutations (by subgroup of rotational symmetres), we can also see this by looking at even vertices, which form a tetrahedron:
![[Regular Polyhedra 2025-12-03 11.51.54.excalidraw]]
And since there are $\hspace{0pt}2$ choices of the tetrahera, we need a reflection, so $Sym(C)\cong S_{4}\times \mathbb{Z}/2$ 
___
The icosaheron $I$, we find that
$$
\left| Sym(I) \right| =12\cdot 5\cdot 2=120
$$
$$
 \left| Sym(D) \right| =12\cdot 3\cdot  2=72
$$
$A_{5}\subseteq Sym(I)$ acting on $\hspace{0pt}5$ octahedra