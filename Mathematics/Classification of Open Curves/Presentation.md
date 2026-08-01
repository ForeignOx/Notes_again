# Title Page:
Multiresolution approach to writhe analysis of open curves and its application to proteins
## Wavelet Dcomposition:
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
For $j\in\left\{ 1,2,\dots,\frac{n}{2} \right\}$, though for our purposes, we 
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
$$Group the edges in pairs $(e_{1},e_{2}),(e_{2},e_{3}),\dots,(e_{n-1},e_{n})$ then for each pair define an average vector and a detail vector:
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



## Writhe



## Proteins



## 