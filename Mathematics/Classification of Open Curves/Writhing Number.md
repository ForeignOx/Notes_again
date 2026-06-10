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
