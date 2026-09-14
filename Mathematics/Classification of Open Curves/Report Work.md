# Abstract
An investigation into the hypothesis that a telescoping Haar wavelet decomposition of the writhe would be a useful tool to see how and to what extent local movement of amino acids in a protein lead to large scale changes in the protein geometry.
# Methodology
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
$$
A^{(k)}(t)=\frac{\left\lvert  \left\lvert  \sum_{j}f( \mathbf{d}_{j}^{(k)})  \right\rvert  \right\rvert }{\sum_{j}\lvert \lvert f(\mathbf{d}_{j}^{(k)}) \rvert \rvert }
$$
With $f$ defined as with energy. If the detail vectors point in unrelated directions, then the numerator will be small as the vectors cancel, but if they point in a common direction, then $A^{(k)}\to1$.
To test whether local energy transfers to global energy, a correlation between the energy at fine scale $p$ at time $t$ compared to the energy at coarser scale $q$ at a lagged time $t+\tau$ was investigated.
$$
R_{p,q}=\mathrm{corr}(E^{(p)}(t),E^{(q)}(t+\tau))
$$
Some curves that were tested for these included a line that folded into a circle with parametrisation:
$$
x=\frac{1}{s}\sin(ts),~y=\frac{1}{s}\cos(ts)
$$
A loop that twisted into a helix with parametrisation
$$
x = \tanh(s)\cos(\omega(1-t)s),~y=\sin(\omega(1-t)s),~z=H-as ^{2}
$$
And a relatively straight line that formed a twist halfway through:
$$
r=\frac{2}{1+t^{2}} \mathrm{sech}(s), ~\phi=ts-\frac{\pi}{2},~z=s-\frac{2}{1+t^{2}}\tanh(s) 
$$
## Protein-Like Curves
To test the properties of the metrics developed, more realistic curves are needed than the toy models above. To begin, some noise functions were developed.

The most basic was to add vectors to the position vectors whose components were $a*\varepsilon*d_\text{min}$, where $a$ is sampled from a $U[-1,1]$ distribution, $d_\text{min}$ is the smallest distance between two points on the curve and $\varepsilon$ is the scale of noise that could be varied.

A more nuanced approach that preserved distances between points was to start at one end of the curve and consider the direction edge vector to the next point on a unit sphere and sampling a new vector from the capping surface of the cone around the vector with angle $\varepsilon$:
(diagram pls)
From this sampled vector, rotate the rest of the curve to make it unchanged with respect to this vector, then continue to the second edge vector and repeat.
(perhaps also diagram)
Since one useful application of these tools was thought to be protein evolution analysis, an approach borrowed from (cite) was used whereby one can sample from a database of standard curvature and torsion coefficients of proteins as they follow a strict distribution. Using these (cite again perhaps) developed an algorithm to form what they called a "protein-like random walk" that also had the feature of resampling if the walk self-intersected, allowing for more realistic outputs. A refinement to this process was made by examining that in nature, proteins form 3 main forms of secondary structure, $\alpha$-helices, $\beta$-pleated sheets and the umbrella term "linkers" for the sections that connect helices or sheets of which there are many varieties. One can classify the pairs of curvature-torsion coefficients as belonging to one of these 3 groups, so by sampling from these 3 distributions one could form more customised random walks such as 50 points of helix followed by 10 of linker followed by another 50 points of helix.


A key project goal was to examine properties of protein evolution, so a custom 



## Writhe
Writhe of open curves has been found to be a useful tool(cite) that encodes both local and global geometry of a curve, so can be used to analyse and classify differences between curves.
This project uses a common form of the discretised open writhe as in (paper to cite)
A goal of the project was to examine an approach that combines signal processing tools from wavelets and writhe, but since writhe is nonlinear, the amounts of writhe of each of the simplified curves cannot simply combine to obtain the writhe of the whole curve.
Thus a telescoping decomposition was considered using the method described below.

Consider a set of open spacecurves given by the levels of Haar decomposition
$$
\gamma^{(0)},\gamma^{(1)},\dots,\gamma^{(\ell)}
$$
Where $\gamma^{(0)}$ is our original curve and $\gamma^{(\ell)}$ is the final decomposition, which has only one edge connecting the two endpoints
If we consider this coarsest approximation $\gamma^{(\ell)}$ is a single edge, so possesses no writhe.
Adding the first detail coefficient produces 2 edges which lie on a plane, so also possesses no writhe as there is no torsion, only curvature. 
At the next level up, $\gamma^{(\ell-2)}$, the curve has 4 edges, so we can possess writhe. 
Define
$$
\mathcal{W}^{(k)}=\mathcal{W}(\gamma^{(k)})
$$
Then the contribution associated with adding level $m$ detail is
$$
\Delta \mathcal{W}^{(k)}=\mathcal{W}^{(k)}-\mathcal{W}^{(k+1)}
$$
One can calculate this writhe increase for each relevant wavelet mode, and their sum is simply the total writhe of the original curve:
$$
\mathcal{W} = \mathcal{W}^{(0)}= \sum_{k=0}^{\ell}\Delta \mathcal{W}^{(k)} 
$$
This is not claiming that a wavelet mode has an intrinsic writhe by itself, instead, it says $\Delta \mathcal{W}^{(k)}$ is the change in exact polygonal writhe when the level $k$ geometric detail is added to the already reconstructed coarser curve.
The level contribution can be made more local by examining the segment-pair terms. At level $k$, let $\mathbf{a}_{0}^{(k)},\mathbf{a}_{1}^{(k)},\dots,\mathbf{a}^{(k)}_{m}$ be the edges or approximation coefficients of $\gamma^{(k)}$. Define
$$
K_{ab}^{(k)}=\frac{1}{2\pi}I_{ab}^{(k)}
$$
Where $I_{ab}^{(k)}$ is the signed spherical area contribution between edges $\mathbf{a}_{a}^{(k)}$ and $\mathbf{a}_{b}^{(k)}$ as defined in the discrete writhe calculation; the amount of area on a sphere where observing the edges from that point on that sphere, it appears that they intersect. Then
$$
\mathcal{W}^{(k)}=\sum_{a<b}K_{ab}^{(k)}
$$
Now suppose a coarse edge $A$ at level $k+1$ is split into two children at level $k$, i.e. $A\to a_{0},a_{1}$, and similarly $B\to b_{0},b_{1}$ for some coarse edge $B$.
Define the refinement contribution associated with the coarse pair $(A,B)$ is:
$$
\Delta K_{AB}^{(k)}=\sum_{p=0}^{1}\sum_{q=0}^{1}K_{a_{p}b_{q}}^{(k)}-K_{AB}^{(k+1)}
$$
Which records how the writhe interaction between two coarse regions changes when both regions are refined
The writhe increments can be rewritten in terms of the refinement contributions like so:
$$
\Delta \mathcal{W}^{(k)}=\sum_{A\leq B}\Delta K^{(k)}_{AB}
$$
$\Delta K^{(k)}_{AB}$ depends on the already reconstructed coarser geometry $\gamma^{(k-1)}$, the detial coefficients defining regions $A$ and $B$, and the nonlinear KL geometry of the resulting child edge-pair directions
Therefore it is resonable to say that $\Delta K_{AB}^{(m)}$ tracks the effect of the combination of details in regions $A$ and $B$. However, one cannot say it is a bilinear coefficient, the mapping between the wavelet details and the writhe is non-linear as the curve positions and edge directions change when details are added.







___
This method answers the question:
    At what scales and between which regions of the curve does the writhe appear as the curve is progressively reconstructed?
It does not answer: 
    How much writhe belongs to one Haar coefficient?
The distinction is important. Writhe is a global geometric quantity. A local detail coefficient may only create writhe by changing how one region of the curve sees another region. Therefore the natural quantities are interactions between refined regions, not isolated detail energies







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
Several different methods were employed to analyse the large amount of data provided by the multiresolution decomposition, and some form of correlation between the data of local geometry and global geometry at a later timestep was sought but not found during the timespan of the project.
Inspred by (josh's) projects relating to protein writhe, initially this metric referred to as writhe gain defined:
$$
T^{(k)}( t)=\sum_{a<b}\left| \Delta K_{ab}^{(k)}(t_{0}+t)-\Delta K_{ab}^{(k)}(t_{0}) \right| 
$$
Which measures the accumulation of writhe from the protein's initial state at a given level of decomposition. This was also investigated without the absolute value in case that was removing useful information, but this didn't seem to be the case.
The correlation was calculated using the formula:
$$
 C_{mn}(\tau) = \frac{\sum_{t}(T_{m}(t)-\bar{T}_{m})(T_{n}(t+\tau)-\bar{T}_{n})}{\sigma_{m}\sigma_{n}}
$$
Where to test the hypothesis, $m$ was chosen to be a fine scale (with many vertices) and $n$ a coarser scale to see whether there was a correlation between the writhe gain at fine scale with writhe gain at coarser scale at some lagged time.
These were the sorts of graphs obtained for different amounts of lag, nothing conclusive was found...

As this seemed insufficient, a more specific approach was taken, giving more thought to the geometry of the protein. For this the data given by the matrix generated by the values of $\Delta K_{ab}^{(k)}$, representing the interaction between edge $a$ and $b$ at decomposition level $k$ denoted the pair writhe matrix. For any given edge $\alpha$, one could sum all the edge interactions it would have $\sum_{b} \Delta K_{\alpha b}^{(k)}$ which represents the total contribution of that edge with all other edges. 
Calculating this for every edge gave a distribution denoted a writhe profile.
The earth mover's distance metric was then employed to compare these writhe profile distributions similarly to above, measuring correlation between fine scale and coarse scale at a lagged time.
This was a graph produced for different levels of lag $\tau$:

Then it was considered that the local interactions between an edge and its relatively close neighbours on the fine scale provided much unwanted random noise that may have been obfuscating useful data. This local noise would appear on the pair writhe matrix on the diagonal.
(show diagram)
To account for this a form of the above metrics was developed but ignoring activity on the diagonal on the fine scale a depth of $d$
(show diagram)
The comparison between these correlations and the other counterparts seemed like a promising direction, but again, nothing conclusive was found.
(show graphs)
