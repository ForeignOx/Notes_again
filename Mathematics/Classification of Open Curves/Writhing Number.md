# Planar Writhing Number
Applying an orientation to a [[Knots|knot]] will induce an orientation to the projection in the [[Knot Diagrams|knot diagram]], the two types of projection crossings which occur are assigned values of $\hspace{0pt}1$ or $-1$ as demonstrated here
![[Pasted image 20260608095750.png|541]]
## Definition
Consider a knot diagram $\mathcal{K}$ which has $n$ self-crossings labelled $\mathcal{C}_{i}$. If we induce an orientation on $\mathcal{K}$ we can label the crossings with a sign $\mathcal{S}(\mathcal{C}_{i})$ as shown above. The planar writhing number of $\mathcal{K}$ represents the sum of the signed self crosings:
$$
w(\mathcal{K})=\sum_{ i=1} ^{ n}\mathcal{S}(\mathcal{C}_{i})
$$
Often this is simply called the [[writhe|writhe]] (without planar prefix), but there is a three dimensional version which is not equivalent.The three dimensional writhe averages $w$ over all projection angles
# 3D Writhing Number
The following definition is for closed spacecurves. The writhe $\mathcal{W}$ unlike the [[Linking Number|linking]] $\mathcal{L}$ cannot be defined by a single planar projection, so it is distinct from the above $w$
By replaxing $\underline{y}(s)$ with $\underline{x}(s')$ in the formula for the linking number, we get an expression representing the self-linking of $\underline{x}$ in $\mathbb{R}^{3}$:
$$
\mathcal{W}=\frac{1}{4\pi}\oint_{\underline{x}}\oint_{\underline{x}} \frac{\underline{\hat{T}}_{\underline{x}}(s)\times \underline{\hat{T}}_{\underline{x}}(s')\cdot(\underline{x}(s)-\underline{x}(s'))}{\left| \underline{x}(s)-\underline{x}(s') \right|^{3} }dsds'
$$
Analogous to the linking number, this measures the average crossing sum of $\underline{x}(s)$ with itelf over all planar projections. 
If an exact copy of $\underline{x}$ is translated along a fixed direction $\sigma$ by a small amount $\varepsilon$, then $\mathcal{W}(\underline{x},\sigma)=\mathcal{L}(\underline{x},\underline{x}+\varepsilon\sigma)$
Applying a set of [[Ambient Isotopy|ambient isotopies]] to a closed curve does not leave $\mathcal{W}$ unchanged, so $\mathcal{W}$ is not a [[Topological Invariants|topological invariant]]. However, a set of continuous transformations can be defined, representing a subset of the ambient isotopies, which leave $\mathcal{W}$ unchanged, these are the [[Constant Conformal Invariance|constant conformal invariants]]
## Properties
- $\mathcal{W}$ is not generally of integer value
- $\mathcal{W}$ is a contant conformal invariant, but not a topological one
- $\mathcal{W}$ changes continually under deformations of the spacecurve, except when the spacecurve crosses itself, in which case it jumps by $\pm 2$
- The double integral form has a singularity at $s=s'$, but the integral does not diverge
- $\mathcal{W}$ of a [[Ribbons|ribbon]] or [[Tubes|tube]] $R(\underline{x},\underline{v})$ depends only on the shape of $\underline{x}$, thus $\mathcal{W}$ is independent of the choice of framing
- The writhe of a planar spacecurve is zero
As with $\mathcal{L}$, our equation for writhe is independent of the choice of parametrisation and can be applied to non smooth curves. 
## Discrete Writhe
jfjfjf
## Writhe Decomposition
For a polygonal curve, we represent it using straight edge vectors. It is tempting to decompose the tangent sequence into Haar wavelet modes and then try to decompose the writhe integral into wavelet-wavelet interactions, but this won't work because writhe is not only a function of tangent vectors, it also depends on the positions of the curve through:
$$
\frac{\underline{x}(s)-\underline{x}(s')}{\left| \underline{x}(s)-\underline{x}(s') \right| ^{3}}
$$
So if the curve is reconstructed from wavelet coefficients, then the positions $\underline{x}(s)$ also change when a detail coefficient is added. Therefore writhe is nonlinear in the wavelet coefficients
The better idea is to decompose the reconstructed curve itself across scaless and measure how the polygonal writhe changes as each scale of detail is added
___
Suppose our curve is represented at $J$ levels of dyadic resolution. For simplicity assume the fiest curve has $2^{J}$ edges. A wavelet decompoition gives a hierarchy of reconstructed curves:
$$
\gamma^{(0)},\gamma^{(1)},\dots,\gamma^{(J)}
$$
Where $\gamma^{(0)}$ is the coarsest approximation, $\gamma^{(1)}$ is obtaine by adding the coarsest detail and so on and $\gamma^{(J)}$ is the original full-resolution polygonal curve
In the simplest picture $\gamma^{(0)}$ might be a single edge, so it has no writhe. Adding the first detail produce two edges, which lie in a plane, so again there is no writhe, only curvature. At the next level, the curve has four edges and genuinely non-planar edge-pair contributions can appear.
For a closed curve, one may need a slightly different coarsest object, because a one-edged closed polygon doesn't exist, so we might want to use a triangle instead.
___
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
Which records how the writhe interacttion between two coarse regions changs when both regions are refined
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
The outputs one might analyse are $\Delta \mathcal{W}^{(m)}$, $\Delta K_{AB}^{(m)}$, and$\sum_{m\leq M}\Delta \mathcal{W}^{(m)}$ which is the writhe accumulate up to resolution $M$
Positive and negative contributions can canncel, which shows whether small scale refinement create coherent writhe at any larger scales
### Decompoition Algorithm:
- Start with polygonal curve $\gamma^{(J)}$ with $2^{J}$ edges
- Perform a Haar or wavelet decomposition of the curvve using the edge vectors
- For each level, reconstruct the polygonal curve $\gamma^{(m)}$
- Compute the exact KL pair matrix $K^{(m)}$for $\gamma^{(m)}$
- Compute the total writhe
$$
\mathcal{W}^{(m)}=\sum_{a<b}K_{ab}^{(m)}
$$
- Compute the level increments:
$$
\Delta \mathcal{W}^{(m)}=\mathcal{W}^{(m)}-\mathcal{W}^{(m-1)}
$$
- Compute the parent-pair refinement increments:
$$
\Delta K_{AB}^{(m)}=
$$





## Correlation between scales
If we have the accumulation of lag between time steps:
$$
T_{m}(t)=\sum_{a<b}\left| K_{ab}^{(m)}(t+\delta t)-K_{ab}^{(m)}(t) \right| 
$$
(for correlation we might want to remove the absolute value)
Then we can find the correlation using:
$$
 C_{mn}(\tau) = \frac{\sum_{t}(T_{m}(t)-\bar{T}_{m})(T_{n}(t+\tau)-\bar{T}_{n})}{\sigma_{m}\sigma_{n}}
$$
Where m is fine scale, $n$ is coarse scale.
$$
M_{mn}= \max_{\tau>0}C_{mn}(\tau)
$$
Produces an $L\times L$ matrix (where $L$ is number of levels), with which we can produce a heatmap to see direction of information flow
## Earthmover's Distance
Normalising our T gives us:
$$
p_{m}(t)=\frac{T_{m}(t)}{\sum_{n}T_{n}(t)}
$$
Representing a probability distribution across scales for each time step. We let $p(t)=\left\{ p_{1}(t),p_{2}(t),\dots \right\}$ be the distribution
We can then compute the Earth mover's distance between $p(t)$ and $p(t+\Delta t)$, and $p(t_{0})$ and $p(t)$ using the formula:
$$
EMD(p,q) = \sum_{m}\left| \sum_{n\leq m}p_{n}-q_{n}  \right| 
$$
So we have the 
$$
EMDVel(t)=EMD(p(t),p+\Delta t)
$$
And
$$
EMDRel(t,t_{0})=EMD(p(t_{0}),p(t))
$$
We can also compute the mean scale:
$$
\mu(t)=\sum_{m}mp_{m}(t)
$$
Then we can have the rate of this:
$$
\Delta \mu(t)=\mu(t+\Delta t)-\mu(t)
$$
Which has property, $\Delta \mu>0$: activity migrating to finer scale, $\Delta \mu<0$ activity is migrating to coarser scale
