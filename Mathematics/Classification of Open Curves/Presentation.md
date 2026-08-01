# Title Page:
Multiresolution approach to writhe analysis of open curves and its application to proteins
## Wavelet Decomposition:
```
So let's break this project down into sections, firstly the multiresolution approach. I am using a modified Haar wavelet transform. Wavelet transforms are a bit like Fourier transforms that we all know and love, but instead of breaking a signal into its component frequencies, we get a little more information. A nice animation to get the idea across is this:
*show animation of sending a Haar wavelet across a curve and showing its modes*
I am using this in a slightly different way however, essentially the Haar transform is to give us a formal way of simplifying a curve into underlying structures, which we can then use alongside the information that the transform gives us to perform a sort of "frequency analysis" on these proteins. Let's get into the maths:
```

Suppose we have a discrete [[Spacecurves|spacecurve]] with vertices
$$
x_{0},x_{1},\dots,x_{n}\in  \mathbb{R}^{3}
$$
and edge vectors
$$
e_{i}=x_{i+1}-x_{i}~~i=1,\dots,n-1
$$
Group the edges in pairs $(e_{1},e_{2}),(e_{2},e_{3}),\dots,(e_{n-1},e_{n})$ then for each pair define an average vector and a detail vector:
$$
a_{j}^{(1)}=\frac{1}{2}(e_{2j-1}+e_{2j})
$$
$$
 d_{j}^{(1)}=\frac{1}{2}(e_{2j-1}-e_{2j})
$$
For $j\in\left\{ 1,2,\dots,\frac{n}{2} \right\}$. So $a_{j}^{(1)}$ records the mean direction of the two edges, while $d_{j}^{(1)}$ records the direction that the average has deviated.
```
*show geogebra diagram or something*

For our purposes, we actually want to remove the halves as we want our approximation coefficient to resemble the curve, whereas the half would shrink the curve, and since the half is only really there for normalisation, we just remove it from both approximation and detail coefficients.
```
Equivalently we can write this in matrix form, 
$$
\begin{pmatrix}
a_{j}^{(1)} \\
d_{j}^{(1)} 
\end{pmatrix}=\begin{pmatrix}
1 & 1  \\
1 & -1 
\end{pmatrix}\begin{pmatrix}
e_{2j-1} \\
e_{2j}
\end{pmatrix}
$$
We can then repeat this process for our new edge set to get a second level of decomposition, and so on.
```
(*go animation weeee, I'm thinking it will be of unwinding helix at time t_0 *)
The values we care about for analysis, is the detail coefficients as they are a meaure of how much information is lost from each simplification
```
### Time Dependent Curve
```
Now we actually care about a curve that is evolving in time, so to add another layer of informational depth, we want to add some more measures to keep track of. Since this is a largely computational project, we discretise the timesteps:
```
Suppose we have a sequence of curves $C(t_{1}),C(t_{2}),\dots,C(t_{T})$, with vertices at time $t_{\ell}$
$$
x_{0}(t_{\ell}),x_{1}(t_{\ell}),\dots,x_{n}(t_{\ell})
$$
$$
 e_{i}(t_{\ell})=x_{i}(t_{\ell})-x_{i-1}(t_{\ell})
$$Applying the Haar tranform to each frame give time-dependent detail coefficients coefficients:
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
```
So here is an example of the kind of results I got from running this on some toy models
Show animation of unwinding helix with all the bells and whistles
```
## Writhe
```
Now we turn to the writhe, which is a knot theoretic property which people such as Chris have found to be useful in the analysis of curves such as proteins (which I am mainly focusing on), but also magnetic field lines, which perhaps is more exciting for people here
In essence, writhe is a measure of how much a curve self-tangles, which is related to a perhaps more well-known number the linking number that is a measure of how tangled two knots are with each other.
The way we calculate it for closed curves, is we take a knot, and consider how it looks when projected onto a plane from a certain angle, and count how many crossings we see. A right-handed cross will contribute +1, and a left-handed will contriute -1 (czech this!)
*also animate this process :)*
This gives us a crossing number for this projection, $C(nhat)$, then the writhing number is defined as the average crossing number over all projections
We can write this as a nasty looking Gaussian integral:
```

$$
\mathcal{W}=\frac{1}{4\pi}\oint_{\underline{x}}\oint_{\underline{x}} \frac{\underline{\hat{T}}_{\underline{x}}(s)\times \underline{\hat{T}}_{\underline{x}}(s')\cdot(\underline{x}(s)-\underline{x}(s'))}{\left| \underline{x}(s)-\underline{x}(s') \right|^{3} }dsds'
$$
```
This is a rather nice property in that it is invariant under small continuous deformations, which isn't quite as good as being topologically invariant, but that's ok for our purposes. The main glaring issue, is that unless we are working with the very few specific proteins that do have closed representations then we are in trouble.
Thankfully this same integral form still mostly works for open curves, though it no longer is invariant under continuous deformation (you can picture just threading the end of the curve through the knotted bits)
Another issue that we have is that for proteins and computation in general, to match it up with the wavelet decomposition we want to be working on discrete spacecurves... so we actually have to modify our formula further,thankfully it's not too hard to do 
```
show the maths of that bit
```
Next we want to combine our two main tools, essentially we want to decompose our curves down to find which simplifications are the biggest contributors to writhe, similar to how one finds the critical modes with Fourier decomposition. Our main issue is this
distance cubed term which is makes our decomposition nonlinear which causes many issues, as we can't simply calculate the writhe of each layer, they are all tangled together. To sort this issue out, we use a slightly different way of decomposing the writhe
```
Suppose we have our set of open spacecurves given by the levels of Haar decomposition
$$
\gamma^{(0)},\gamma^{(1)},\dots,\gamma^{(\ell)}
$$
Where $\gamma^{(0)}$ is our original curve and $\gamma^{(\ell)}$ is the final decomposition, which has only one edge connecting the two endpoints
```
*show images of each level of decomposition*
```
If we consider this coarsest approximation $\gamma^{(\ell)}$ is a single edge, so it has no writhe 
``` 
a line never tangles with itself (in euclidean space at least)
```
Adding the first detail coefficient produces 2 edges which lie on a plane, so there is no writhe as there is no torsion, only curvature. At the next level up, the curve has 4 edges, so we can have some writhe. 
```
If we keep considering the amount of writhe we gain from adding the next layer of detail, we get a notion of how much writhe i

```


Define
$$
\mathcal{W}^{(m)}=\mathcal{W}(\gamma^{(m)})
$$
The contribution associated with adding level $m$ detail is
$$
\Delta \mathcal{W}^{(m)}=\mathcal{W}^{(m)}-\mathcal{W}^{(m-1)}
$$
This is not claiming that a wavelet mode has an intrinsic writhe by itself, instead, it says $\Delta \mathcal{W}^{(m)}$ is the change in exact polygonal writhe when the level $m$ geometric detail is added to the already reconstructed coarser curve
The main advantage is that the decomposition telescopes:
$$
\mathcal{W}^{(J)}= \mathcal{W}^{(0)}+\sum_{m=1}^{J}\Delta \mathcal{W}^{(m)} 
$$
$$
\implies \mathcal{W}(\gamma)=\sum_{m=1}^{J}\Delta \mathcal{W}^{(m)}
$$
___
The level contribution can be made more local by examining the segment-pair terms. At level $m$, let $e_{0}^{(m)},e_{1}^{(m)},\dots,e^{(m)}_{2^{m}-1}$ be the edges of $\gamma^{(m)}$. Define
$$
K_{ab}^{(m)}=\frac{1}{2\pi}I_{ab}^{(m)}
$$
Where $I_{ab}^{(m)}$ is the signed spherical area contribution between edges $e_{a}^{(m)}$ and $e_{b}^{(m)}$. Then
$$
\mathcal{W}^{(m)}=\sum_{a<b}K_{ab}^{(m)}
$$
Now suppose a coarse edge $A$ at level $m-1$ is split into two children at level $m$, i.e. $A\to a_{0},a_{1}$, and similarly $B\to b_{0},b_{1}$ for some coarse edge $B$
The refinement contribution associated with the coarse pair $(A,B)$ is:
$$
\Delta K_{AB}^{(m)}=\sum_{p=0}^{1}\sum_{q=0}^{1}K_{a_{p}b_{q}}^{(m)}-K_{AB}^{(m-1)}
$$
Which records how the writhe interacttion between two coarse regions changes when both regions are refined
A fully general version also inclues the case $A=B$:
$$
\Delta K^{(m)}_{AA}=\sum_{a<b}K^{(m)}_{ab}
$$
Where $a,b$ are children of $A$
For a binary split into two adjacent children, this is usually zero because adjacent polygonal edges have no KL contribution. However including this case does make the formulae nicer
Then the level increment can be written as
$$
\Delta \mathcal{W}^{(m)}=\sum_{A\leq B}\Delta K^{(m)}_{AB}
$$
___
Each refinement step is controlled by the wavelet detail coefficients. Schematically, a parent edge or parent curve segment is tranformed as:
$$
\text{parent geometry}+\text{detail coefficient}\to \text{two child edges}
$$
So $\Delta K^{(m)}_{AB}$ depends on the already reconstructed coarser geometry $\gamma^{(m-1)}$, the detial coefficients defining regions $A$ and $B$, and the nonlinear KL geometry of the resulting child edge-pair directions
Therefore it is resonable to say that $\Delta K_{AB}^{(m)}$ tracks the effect of the combination of details in regions $A$ and $B$. However, one should not ssay it is a bilinear coefficient, the mapping between the wavelet details and the writhe is non-linear as the curve positions and edge directions change when details are added
___
This method answers the question:
    At what scales and between which regions of the curve does the writhe appear as the curve is progressively reconstructed?
It does not answer: 
    How much writhe belongs to one Haar coefficient?
The distinction is important. Writhe is a global geometric quantity. A local detail coefficient may only create writhe by changing how one region of the curve sees another region. Therefore the natural quantities are interactions between refined regions, not isolated detail energies



## Proteins



## 