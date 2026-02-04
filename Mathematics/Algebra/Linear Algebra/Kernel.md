If [[Linear Maps|$T:V\to W$]], we define the kernel of $T$:
$$
\text{ker}(T):=\{ \underline{v}\in V\mid T(\underline{v})=\underline{0} \}\subseteq V
$$
Other notation for the kernel involves calling it the nullspace, $T^{-1}(0),N(T),\mathfrak{K}(T)$ 
## Nullity
The nullity of $T$ is the [[Dimension|dimension]] of the kernel of $T$:
$$
\text{null}(T):=\dim(\text{ker}(T)) 
$$
## Example
If [[Matrices|$A\in M_{m\times n}(\mathbb{R})$]], $A:\mathbb{R}^{n}\to \mathbb{R}^{n}$, 
$$
\text{ker}(A)=\text{nullspace}(A)=\{ \underline{v}\in \mathbb{R}^{n}\mid A\underline{v}=\underline{0} \}\subseteq \mathbb{R}^{n}
$$
### Subexample
$$
A=\begin{pmatrix}
3&1\\12&4
\end{pmatrix}:\mathbb{R}^{2}\to \mathbb{R}^{2}
$$
The kernel can be worked out like so:
$$
\begin{pmatrix}
3&1\\12&4
\end{pmatrix}\begin{pmatrix}
x\\y
\end{pmatrix}=\begin{pmatrix}
0\\0
\end{pmatrix}
$$
Which gives (in this case) two identical equations in $x$ and $y$:
$$
3x+y=0
$$
So the general vector that satisfies this is any multiple of
$$
\begin{pmatrix}
1\\-3
\end{pmatrix}
$$
So
$$
 \text{ker}(A)=\left< \begin{pmatrix}
1\\-3
\end{pmatrix} \right> \subseteq \mathbb{R}^{2}
$$
Hence $\text{null}(A)=1$
___
$$
\frac{d }{dx} :\mathbb{R}[x]_{n}\to \mathbb{R}[x]_{n}
$$
$$
\text{ker}\left( \frac{d }{dx}  \right)=\left\{  p \in \mathbb{R}[x]_{n}\mid \frac{d p}{dx} =0  \right\}=\{ p \in \mathbb{R} \}=\mathbb{R}\subseteq \mathbb{R}^{n}
$$
$$
\text{null}\left( \frac{d }{dx}  \right)=1=\dim(\mathbb{R})
$$


#Mathematics #LinAlg #Definition 