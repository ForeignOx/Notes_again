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
Now consider the edge of the curve obtained by keeping every other vertex; $x_{0},x_{2},\dots,x_{n}$, then the $j$th edge of this curve i
$$
E_{j}^{(1)}=x_{2j}-x_{2j-2}=2a_{j}^{(1)}
$$
We can then repeat this by
$$
\begin{pmatrix}
a_{j}^{(n)} \\
d_{j}^{(n)} 
\end{pmatrix}=\frac{1}{2}\begin{pmatrix}
1 & 1  \\
1 & -1 
\end{pmatrix}\begin{pmatrix}
a_{j}^{(n-1)} \\
d_{j}^{(n-1)}
\end{pmatrix}=\frac{1}{2^{n}}\begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix}^{n}\begin{pmatrix}
e_{2j-1} \\
e_{2j}
\end{pmatrix}
$$

A level detail coefficient compares neighbouring edges, so if the two edges point in nearly the same direction, $d_{j}^{(1)}$ is mall. If the curve bends sharply between them, $d_{j}^{(1)}$ is large. A level$-2$ detail coefficient compares two neighbouring two-edge average, so it measures whether the firt half of a four-edge block points differently from the second half
In general, $d_{j}^{(k)}$ compares the first and second halves of a block of $2^{k}$ edges. The support is local, but the locality is scale dependent
___
If $n=2^{m}$ then the edge sequence can be reconstructed exactly from one final average and all detail coefficients. Schematically,
$$
e_{i}=a_{1}^{(m)}+\sum_{k=1}^{m}\sum_{j}\sigma_{i,j}^{(k)}d_{j}^{(k)}
$$
Where $\sigma_{i,j}^{(k)}$ is a sign function that is nonzero only when edge $e_{i}$ lies inside the support of the $j$th level $k$ mode, so within that jth block:
$$
\sigma_{i,j}^{(k)}=\begin{cases}
1 & \text{if }e_{i}\text{ is in the firt half of the block} \\
-1 & \text{if }e_{i}\text{ is in the second half of the block}
\end{cases}
$$
Coordinates are recovered by cumulative summation:
$$
x_{p}=x_{0}+\sum_{i=1}^{p}e_{i}
$$
## Time Dependent Curve
Suppoe we have a sequence of curves $C(t_{1}),C(t_{2}),\dots,C(t_{T})$, with vertices at time $t_{\ell}$
$$
x_{0}(t_{\ell}),x_{1}(t_{\ell}),\dots,x_{n}(t_{\ell})
$$
$$
 e_{i}(t_{\ell})=x_{i}(t_{\ell})-x_{i-1}(t_{\ell})
$$Applying the Haar tranform to each frame give time-dependent coefficients:
$$
d_{j}^{(k)}(t_{\ell})
$$
These coefficients contain both the static hape of the molecule and its motion
The changes relative to a reference state are given by
$$
\Delta d_{j}^{(k)}(t)=d_{j}^{(k)}(t)-d_{j}^{(k)}(t_{0})
$$
Which measures the accumulated deformation relative to the starting frame,
Alternatively, for instantaneous motion, we can use coefficient velocities:
$$
\dot{d}_{j}^{(k)}(t_{\ell})\approx \frac{d_{j}^{(k)}(t_{\ell+1})-d_{j}^{(k)}(t_{\ell})}{t_{\ell+1}-t_{\ell}}
$$
Which measure how the multiscale shape is changing at each time
Befor we analyse any curves we must remove global translation an rotation which give the rigid-body motion
## Energy
Define the energy at scale $k$ by
$$
E_{k}(t)=\sum_{j}\lvert \lvert \Delta_{j}^{(k)}(t) \rvert \rvert ^{2}
$$
Which measures how much defomation is present at scale $k$. Small $k$ correspond to short-wavelength local rearrangements. Large $k$ corresponds to collective bending
A ueful normalised version is:
$$
\tilde{E}_{k}(t)= \frac{E_{k}(t)}{\sum_{\ell=1}^{m}E_{\ell}(t)}
$$
Which asks what fraction of the total deformation is present at each scale
Another compact summary i the scale centroid
$$
\tilde{k}(t)=\frac{\sum_{k}kE_{k}(t)}{\sum_{k}E_{k}(t)}
$$
If $\tilde{k}(t)$ grows, then we see that the deformation i moving from fine to coarse scales
## Directional Coherence
Energy alone is not enough as a high value of $E_{k}(t)$ could come from many unrelated local motions. These can be thermally noisy and may cancel each other out, so we also define a coherence score:
$$
A_{k}(t)=\frac{\left\lvert  \left\lvert  \sum_{j}\Delta_{j}^{(k)}(t)  \right\rvert  \right\rvert }{\sum_{j}\lvert \lvert \Delta d_{j}^{(k)}(t) \rvert \rvert }
$$
Which satisfies $0\leq A_{k}(t)\leq 1$
If the detail vectors point in unrelated directions, then then numerator will be small as the vectors cancel, but if they point in a common direction, then the numerator is close to the denominator, so $A_{k}$ will grow close to 1
___
A global coherence score may miss a local event. A protein may have one region beginning to organise while the rest of the chain remains noisy. Let $B_{r}^{(q)}$ enote a block at a coarser scale $q$. We can then perform the above calculation for $A_{k}(t)$ but just within that block
## Detecting Transfer across Scales
We want to test our hypothesis that coherent small-scale rearrangements may appear before the corresponding large-scale conformational motion is obvious in the raw trajectory
A simple way to test this is to compare activity at a fine scale $p$ with later activity at coarser scale $q$, we can define the lagged cross-scale correlation:
$$
R_{p,q}=\mathrm{corr}(E_{p}(t),E_{q}(t+\tau))
$$
If $R_{p,q}(\tau)$ peak for positive $\tau$, then fine-scale activity tends to precede coarse-scale growth, i.e.
$$
T_{p\to q}=\max_{\tau \in [\tau_{min},\tau_{max}]}R_{p,q}(\tau)
$$
With the maximum lag at
$$
\tau ^{*}_{p\to q}=\underset{ \tau \in [\tau_{min},\tau_{max}] }{ \mathrm{argmax} }(R_{p,q}(\tau))
$$
It may be informative to correlate fine-scale coherence with later coarse-scale energy:
$$
R_{p,q}^{A,E}(\tau)=\mathrm{corr}(A_{p}(t),E_{q}(t+\tau))
$$
