Suppose we have a discrete [[Spacecurves|spacecurve]] with vertices
$$
x_{0},x_{1},\dots,x_{n}\in  \mathbb{R}^{3}
$$
and edge vectors
$$
e_{i}=x_{i}~~i=1,\dots,n
$$
If a curve is sampled at approximately fixed aclength, the edge vectors encode the local tangent direction, or the [[Tantrix Curves|tantrix]], we want to detect how motion is distributed across length scales
Instead of applying a wavelet transform directly to the coordinates $x_{i}$, we aply it to the edge sequence $(e_{1},\dots,e_{n})$ removing sensitivity to global tranlation and means that each Haar aeraging step replaces neighbouring edges with courser edges
___
Assume that $n=2^{m}$
Group the edges in pairs $(e_{1},e_{2}),(e_{2},e_{3}),\dots,(e_{n-1},e_{n})$ then for each pair define an average vector and a detail vector:
$$
a_{j}^{(1)}=\frac{1}{2}(e_{2j-1}+e_{2j})
$$
$$
 d_{j}^{(1)}=\frac{1}{2}(e_{2j-1}-e_{2j})
$$
For $j\in\left\{ 1,2,\dots,\frac{n}{2} \right\}$
Equivalently, 
$$
\begin{pmatrix}
a_{j}^{(1)} \\
d_{j}^{(1)} 
\end{pmatrix}=\frac{1}{2}\begin{pmatrix}
1 & 1  \\
1 & -1 
\end{pmatrix}\begin{pmatrix}
e_{2j-1} \\
e_{2j}
\end{pmatrix}
$$
And then the inverse is just
$$
e_{2j-1}=a_{j}^{(1)}+d_{j}^{(1)}
$$
$$
 e_{2j}=a_{j}^{(1)}-d_{j}^{(1)}
$$
So $a_{j}^{(1)}$ records the mean direction of the two edges, while $d_{j}^{(1)}$ records the direction that the average has deviated
We can then repeat this
