Suppose we have a discrete [[Spacecurves|spacecurve]] with vertices
$$
x_{0},x_{1},\dots,x_{n}\in  \mathbb{R}^{3}
$$
and edge vectors
$$
e_{i}=x_{i}~~i=1,\dots,n
$$
If a curve is sampled at approximately fixed aclength, the edge vectors encode the local tangent direction, or the [[Tantrix Curves|tantrix]], we want to detect how motion is distributed across length scales
Instead of applying a wavelet transform directly to the coordinates $x_{i}$, we aply it to the edge sequence $(e_{1},\dots,e_{n})$ removing sensitivity to
