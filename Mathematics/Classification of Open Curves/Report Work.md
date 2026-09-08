# Abstract
An investigation into the hypothesis that a telescoping Haar wavelet decomposition of the writhe would be a useful tool to see how and to what extent local movement of amino acids in a protein lead to large scale changes in the protein geometry.
# Mathematical Background
## Haar Wavelet Transform
The main focus of this project was on time-dependent discrete open spacecurves in 3 dimensions:
$$
\gamma: \left\{ 0,1,\dots,n \right\}\times \mathbb{R}^{+}\to \mathbb{R}^{3}
$$
$$
\gamma(s,t) \mapsto \mathbf{x}_{i}(t)
$$
As this was a good way of representing the time evolution of the $C_{\alpha}$ protein backbone (cite paper which uses this?) which was the main real-life application of the project. It was also useful for the computational aspect of the calculations and could be used on other open curves such as magnetic field lines. (maybe provide other e.g.)
It has been found (cite) that writhe is a useful tool to measure the tangling of these protein backbones as it takes careful consideration of local and global geometry.
Proteins are naturally given to multiresolution analysis due to their natural structural ordering, the primary structure of the amino acids themselves, the secondary structure of helices and pleated sheets, and even in some cases tertiary structure such as beta barrels. The Haar wavelet transform on the edges was considered to be a good way to systematically break down a curve into modes that represent these levels of structure.
Defining edge vectors at time $t$:
$$
\mathbf{e}_{i}(t)=\mathbf{x}_{i}(t)-\mathbf{x}_{i-1}(t)
$$
For $i\in\left\{ 1,\dots ,n \right\}$
Group the edges into pairs $(\mathbf{e}_{1},\mathbf{e}_{2}),(\mathbf{e}_{2},\mathbf{e}_{3}),\dots,(\mathbf{e}_{n-1},\mathbf{e}_{n})$ if there are an even number, or pairs and a final triplet $(\mathbf{e}_{n-2},\mathbf{e}_{n-1},\mathbf{e}_{n})$ and for each pair define an average and detail vector:
$$
\mathbf{a}_{j}^{(1)}(t)=\mathbf{e}_{2j-1}(t)+\mathbf{e}_{2j}(t)
$$
$$
 \mathbf{d}_{j}^{(1)}(t)=\mathbf{e}_{2j-1}(t)-\mathbf{e}_{2j}(t)
$$
And for the triplet define the average and two detail vectors:

$$
\mathbf{a}^{(1)}_{j}(t)=\mathbf{e}_{2j-2}(t)+\mathbf{e}_{2j-1}(t)+\mathbf{e}_{2j}(t)
$$
$$
\mathbf{c}_{j}^{(1)}(t)=\mathbf{e}_{2j-2}(t)-\mathbf{e}_{2j-1}(t)
$$
$$
 \mathbf{d}_{j}^{(1)}(t)=\frac{1}{2}(\mathbf{e}_{2j-2}(t)+\mathbf{e}_{2j-1}(t))-\mathbf{e}_{2j}(t)
$$
Note that unlike a standard Haar transform with normalisation constant $\frac{1}{2}$, this has been modified to simply be 1 as to avoid reducing the scale at each level of decomposition.
The average vectors form a simplified spacecurve, and the detail vectors represent how much this curve has been simplified compared to the original.
(diagram here)
This process is then repeated by using the approximation coefficients of one level to find approximation and detail coefficients of the next in the same way:
$$
\mathbf{a}_{j}^{(k+1)}(t)=\mathbf{a}^{(k)}_{2j-1}(t)+\mathbf{a}^{(k)}_{2j}(t)
$$
$$
 \mathbf{d}_{j}^{(k+1)}(t)=\mathbf{a}^{(k)}_{2j-1}(t)-\mathbf{a}^{(k)}_{2j}(t)
$$
Note that using the approximation and detail coefficients, one can reconstruct the more detailed curve by a simple rearrangement.
## Haar Transform Analysis
With this information alone, much like Fourier analysis, one can glean useful information about the geometry of a curve by examining how the coefficients of the Haar transform evolve over time. Since the approximation coefficients simply represent the several simplified curves, the detail coefficients are points of interest.
We define relative detail coefficients as changes in detail coefficient with respect to a reference time $t_{0}$:
$$
\Delta \mathbf{d}_{j}^{(k)}(t)=\mathbf{d}_{j}^{(k)}(t)-\mathbf{d}_{j}^{(k)}(t_{0})
$$
Which shows the 
We also define detail velocity coefficients as instantaneous changes in detail coefficient
$$
\dot{\mathbf{d}}_{j}^{(k)}(t)=\frac{d\mathbf{d}_{j}^{(k)}}{dt} \approx \frac{\mathbf{d}_{j}^{(k)}(t)-\mathbf{d}_{j}^{(k)}(t-\delta t)}{\delta t}
$$
Where we use the approximation in computations as we discretise the timesteps.
We define the energy at scale $k$ and time $t$ as
$$
E^{(k)}(t)=\sum_{j}\lvert \lvert f(\mathbf{d}_{j}^{(k)}) \rvert \rvert ^{2}
$$
Where $f$ can be the identity, or represent the relative detail or detail velocity coefficients.
This is a metric of how much deformation there is in each scale across time.
A useful metric derived from this is a scale centroid:
$$
\tilde{k}(t)=\frac{E^{(k)}(t)}{\sum_{k}E^{(k)}(t)}
$$
Which represents which scales the energy resides. If this increases, then the energy of the detail coefficients is moving from small to large scale which would be indicative of a significant change in the geometry.
Another metric is the directional coherence which rules out whether a high value of $E^{(k)}(t)$ comes from many unrelated motions 


## Writhe
Next writhe time

### Directional Coherence
Energy alone is not enough as a high value of $E_{k}(t)$ could come from many unrelated local motions. These can be thermally noisy and may cancel each other out, so we also define a coherence score:
$$
A_{k}(t)=\frac{\left\lvert  \left\lvert  \sum_{j}\Delta d_{j}^{(k)}(t)  \right\rvert  \right\rvert }{\sum_{j}\lvert \lvert \Delta d_{j}^{(k)}(t) \rvert \rvert }
$$
Which satisfies $0\leq A_{k}(t)\leq 1$
If the detail vectors point in unrelated directions, then then numerator will be small as the vectors cancel, but if they point in a common direction, then the numerator is close to the denominator, so $A_{k}$ will grow close to 1
___
A global coherence score may miss a local event. A protein may have one region beginning to organise while the rest of the chain remains noisy. Let $B_{r}^{(q)}$ denote a block at a coarser scale $q$. We can then perform the above calculation for $A_{k}(t)$ but just within that block
### Detecting Transfer across Scales
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
## Writhe
### Writhe Decomposition
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
The outputs one might analyse are $\Delta \mathcal{W}^{(m)}$, $\Delta K_{AB}^{(m)}$, and$\sum_{m\leq M}\Delta \mathcal{W}^{(m)}$ which is the writhe accumulate up to resolution $M$
Positive and negative contributions can cancel, which shows whether small scale refinement create coherent writhe at any larger scales
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





### Correlation at a Scale
If we have the accumulation of lag from the start, denoted by writhe gain:
$$
T_{m}( t)=\sum_{a<b}\left| K_{ab}^{(m)}(t_{0}+t)-K_{ab}^{(m)}(t_{0}) \right| 
$$
(for correlation we might want to remove the absolute value)
We can also have the accumulation of lag between time steps, denoted by writhe activity:
$$
\Delta T_{m}( t)=\sum_{a<b}\left| K_{ab}^{(m)}(t+\delta t)-K_{ab}^{(m)}(t) \right| 
$$
Then we can find the correlation using:
$$
 C_{mn}(\tau) = \frac{\sum_{t}(T_{m}(t)-\bar{T}_{m})(T_{n}(t+\tau)-\bar{T}_{n})}{\sigma_{m}\sigma_{n}}
$$
Where m is fine scale, $n$ is coarse scale.
$$
M_{mn}= \max_{\tau>0}C_{mn}(\tau)
$$
Produces an $L\times L$ matrix (where $L$ is number of levels), with which we can produce a heatmap to see direction of information flow
### Earthmover's Distance
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

# Analysis
