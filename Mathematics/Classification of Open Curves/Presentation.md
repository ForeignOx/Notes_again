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
This is a rather nice property
```

## Proteins



## 